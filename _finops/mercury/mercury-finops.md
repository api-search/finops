---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Purchase
  - Usage
  - Adjustment
  - Tax
  - Credit
  pricingCategory: Subscription + Per-Transaction Fees
description: FOCUS-aligned FinOps for Mercury. Cost is dominated by three streams - a flat monthly product subscription (Mercury free, Plus $35/mo, Pro $350/mo), per-transaction fees on certain invoicing payments (e.g. Plus charges $1 per ACH invoice payment, free on Pro), and outbound wire fees for international wires and certain domestic flows. Treasury yields offset cost as a credit. The API itself is not separately metered; usage limits apply to invoicing-API calls and active-user counts on reimbursements.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Mercury Technologies, Inc.
  ProviderName: Mercury
  PublisherName: Mercury Technologies, Inc.
  ServiceCategory: Banking
  ServiceName: Mercury
layout: finops
meters:
- aggregation: sum
  description: Recurring monthly or annual subscription for the active product tier (Free, Plus, or Pro).
  dimensions:
  - plan_tier
  - billing_cycle
  name: subscription_fee
  unit: month
- aggregation: sum
  description: Per-payment fee on inbound ACH invoice payments for the Plus tier ($1 per payment); waived on Pro.
  dimensions:
  - plan_tier
  name: ach_invoice_payment
  unit: payment
- aggregation: sum
  description: Outbound wire fees for international wires and certain domestic non-included wire types.
  dimensions:
  - wire_type
  - destination_country
  name: outbound_wire
  unit: wire
- aggregation: sum
  description: Cashback/rewards credit applied against corporate card spend (offsets cost on qualifying transactions).
  dimensions:
  - card_id
  - merchant_category
  name: card_interchange_credit
  unit: transaction
- aggregation: sum
  description: Yield credit accrued on Mercury Treasury balances; appears as an account credit and reduces effective cost.
  dimensions:
  - account_id
  - portfolio
  name: treasury_yield
  unit: USD
name: Mercury Finops
provider_name: Mercury
provider_slug: mercury
publisher_name: Mercury Technologies, Inc.
service_category: Banking
slug: mercury-finops
source_filename: mercury-finops.yml
source_heading: FinOps Profile
source_url: https://mercury.com/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Mercury\nproviderId: mercury\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: true\ntags:\n  - Banking\n  - Fintech\n  - Startups\n  - Treasury\n  - Payments\n  - FinOps\n  - FOCUS\ndescription: >-\n  FOCUS-aligned FinOps for Mercury. Cost is dominated by three streams - a flat monthly\n  product subscription (Mercury free, Plus $35/mo, Pro $350/mo), per-transaction fees on\n  certain invoicing payments (e.g. Plus charges $1 per ACH invoice payment, free on Pro),\n  and outbound wire fees for international wires and certain domestic flows. Treasury\n  yields offset cost as a credit. The API itself is not separately metered; usage limits\n  apply to invoicing-API calls and active-user counts on reimbursements.\nsources:\n  - https://mercury.com/pricing\n  - https://docs.mercury.com/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl:\
  \ https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Mercury Technologies, Inc.\nserviceCategory: Banking\nbillingModel:\n  pricingCategory: Subscription + Per-Transaction Fees\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\n    - Adjustment\n    - Tax\n    - Credit\nfocusColumns:\n  ServiceName: Mercury\n  ServiceCategory: Banking\n  ProviderName: Mercury\n  PublisherName: Mercury Technologies, Inc.\n  InvoiceIssuerName: Mercury Technologies, Inc.\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: subscription_fee\n    description: >-\n      Recurring monthly or annual subscription for the active product tier (Free,\n      Plus, or Pro).\n    unit: month\n    aggregation: sum\n    dimensions:\n      - plan_tier\n      - billing_cycle\n  - name: ach_invoice_payment\n    description: >-\n      Per-payment\
  \ fee on inbound ACH invoice payments for the Plus tier\n      ($1 per payment); waived on Pro.\n    unit: payment\n    aggregation: sum\n    dimensions:\n      - plan_tier\n  - name: outbound_wire\n    description: >-\n      Outbound wire fees for international wires and certain domestic non-included\n      wire types.\n    unit: wire\n    aggregation: sum\n    dimensions:\n      - wire_type\n      - destination_country\n  - name: card_interchange_credit\n    description: >-\n      Cashback/rewards credit applied against corporate card spend (offsets cost on\n      qualifying transactions).\n    unit: transaction\n    aggregation: sum\n    dimensions:\n      - card_id\n      - merchant_category\n  - name: treasury_yield\n    description: >-\n      Yield credit accrued on Mercury Treasury balances; appears as an account\n      credit and reduces effective cost.\n    unit: USD\n    aggregation: sum\n    dimensions:\n      - account_id\n      - portfolio\nprinciples:\n  - name: Visibility\n\
  \    description: >-\n      Pull statements via the Statements API and use the Transactions API to\n      categorize fee, wire, and card spend; treasury yield appears as a credit\n      entry on the linked treasury account.\n  - name: Allocation\n    description: >-\n      Tag transactions with the note field on payment creation, and assign cards\n      to spend owners. Use webhooks to land transaction events into a finops or\n      ledger store at near-real-time.\n  - name: Optimization\n    description: >-\n      Choose the lowest tier that satisfies your invoicing-API and reimbursement-user\n      needs. Prefer ACH over wire where speed allows. Park idle cash in Mercury\n      Treasury to convert float to yield.\n  - name: Accountability\n    description: >-\n      Assign a finance owner per Mercury account. Rotate API tokens via Settings and\n      keep the IP allowlist current to prevent unauthorized API spend on outbound\n      payments.\nmaintainers:\n  - FN: Kin Lane\n    email:\
  \ kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/mercury/refs/heads/main/finops/mercury-finops.yml
sources:
- https://mercury.com/pricing
- https://docs.mercury.com/
specification: FinOps Framework
tags:
- Banking
- Fintech
- Startups
- Treasury
- Payments
- FinOps
- FOCUS
---
