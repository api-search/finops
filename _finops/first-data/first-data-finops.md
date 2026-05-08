---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD (settlement varies by acquirer/region)
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  - Tax
  - Adjustment
  - Refund
  - Credit
  pricingCategory: Take Rate + Subscription
description: FOCUS-aligned FinOps mapping for First Data / Fiserv merchant APIs — take-rate (merchant discount) plus per-transaction and monthly platform fees billed via the merchant services agreement.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Fiserv, Inc.
  ProviderName: Fiserv, Inc.
  PublisherName: Fiserv, Inc.
  ServiceCategory: Payments
  ServiceName: First Data (Fiserv)
layout: finops
meters:
- aggregation: sum
  description: Card-present and card-not-present transactions processed via Commerce Hub / Carat / legacy First Data gateways
  dimensions:
  - card_brand
  - mcc
  - country
  - channel
  - merchant_id
  name: card_transactions
  unit: transaction
- aggregation: sum
  description: Gross transaction value (used for percentage-based discount-rate calculations)
  dimensions:
  - card_brand
  - country
  - merchant_id
  name: transaction_volume
  unit: USD
- aggregation: sum
  description: Per-authorization, per-batch, and gateway fees
  dimensions:
  - merchant_id
  - product_line
  name: gateway_fees
  unit: transaction
- aggregation: sum
  description: Recurring platform, PCI, statement, and value-add service fees
  dimensions:
  - merchant_id
  - product_line
  name: monthly_platform_fees
  unit: month
- aggregation: sum
  description: Chargebacks, retrieval requests, and refund-related fees
  dimensions:
  - card_brand
  - reason_code
  - merchant_id
  name: chargebacks_refunds
  unit: event
name: First Data Finops
provider_name: First Data (Fiserv)
provider_slug: first-data
publisher_name: Fiserv, Inc.
service_category: Payments
slug: first-data-finops
source_filename: first-data-finops.yml
source_heading: FinOps Profile
source_url: https://developer.fiserv.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: First Data (Fiserv)\nproviderId: first-data\npublisherName: Fiserv, Inc.\nserviceCategory: Payments\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Payments\n  - Merchant Services\n  - Financial Services\n  - Transaction Processing\n  - FinOps\n  - FOCUS\ndescription: FOCUS-aligned FinOps mapping for First Data / Fiserv merchant APIs — take-rate (merchant discount) plus per-transaction and monthly platform fees billed via the merchant services agreement.\nnotes: Fiserv does not publish public pricing or invoice schemas. Meters below model the expected merchant invoice line items (interchange + assessments + processor\
  \ markup, gateway fees, monthly platform fees) but exact fee structure varies per merchant agreement.\nsources:\n  - https://developer.fiserv.com/\n  - https://www.fiserv.com/\nbillingModel:\n  pricingCategory: Take Rate + Subscription\n  billingFrequency: Monthly\n  billingCurrency: USD (settlement varies by acquirer/region)\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Adjustment\n    - Refund\n    - Credit\nfocusColumns:\n  ServiceName: First Data (Fiserv)\n  ServiceCategory: Payments\n  ProviderName: Fiserv, Inc.\n  PublisherName: Fiserv, Inc.\n  InvoiceIssuerName: Fiserv, Inc.\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: card_transactions\n    description: Card-present and card-not-present transactions processed via Commerce Hub / Carat / legacy First Data gateways\n    unit: transaction\n    aggregation: sum\n    dimensions:\n      - card_brand\n      - mcc\n      - country\n      - channel\n      - merchant_id\n  - name: transaction_volume\n\
  \    description: Gross transaction value (used for percentage-based discount-rate calculations)\n    unit: USD\n    aggregation: sum\n    dimensions:\n      - card_brand\n      - country\n      - merchant_id\n  - name: gateway_fees\n    description: Per-authorization, per-batch, and gateway fees\n    unit: transaction\n    aggregation: sum\n    dimensions:\n      - merchant_id\n      - product_line\n  - name: monthly_platform_fees\n    description: Recurring platform, PCI, statement, and value-add service fees\n    unit: month\n    aggregation: sum\n    dimensions:\n      - merchant_id\n      - product_line\n  - name: chargebacks_refunds\n    description: Chargebacks, retrieval requests, and refund-related fees\n    unit: event\n    aggregation: sum\n    dimensions:\n      - card_brand\n      - reason_code\n      - merchant_id\nprinciples:\n  - name: Visibility\n    description: Reconcile Fiserv merchant statements, Clover/Carat reporting exports, and Commerce Hub Reporting APIs against\
  \ your gateway logs to attribute interchange + processor markup to product lines.\n  - name: Allocation\n    description: Use the merchant_id, MCC, and channel dimensions to allocate spend to business units; tag Commerce Hub idempotency Client-Request-Ids with internal cost-center identifiers for downstream attribution.\n  - name: Optimization\n    description: Optimize interchange via Level II/III data and tokenization, route by lowest-cost network where supported, and consolidate MIDs to qualify for volume tiers in your merchant agreement.\n  - name: Accountability\n    description: Assign merchant-services contract ownership to a single finance/treasury owner; review chargeback ratios monthly and renegotiate the merchant agreement on an annual cadence.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/first-data/refs/heads/main/finops/first-data-finops.yml
sources:
- https://developer.fiserv.com/
- https://www.fiserv.com/
specification: FinOps Framework
tags:
- Payments
- Merchant Services
- Financial Services
- Transaction Processing
- FinOps
- FOCUS
---
