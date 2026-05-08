---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: bank-of-america-cashpro-api-openapi.yml
  format: yaml
  label: Bank of America CashPro API
  slug: cashpro-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/bank-of-america/refs/heads/main/openapi/bank-of-america-cashpro-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Tax
  - Adjustment
  - Refund
  - Credit
  chargeFrequency: Recurring
  pricingCategory: Bundled Banking Fees
description: 'FOCUS-aligned FinOps shape for Bank of America CashPro: API access is bundled into a corporate banking / treasury services agreement, so FinOps focuses on per-transaction banking fees (wire, ACH, FX margin) rather than per-API-call charges. Public meter values are not available.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Bank of America, N.A.
  PricingCategory: Bundled Banking Fees
  PricingUnit: transaction
  ProviderName: Bank of America
  PublisherName: Bank of America Corporation
  ServiceCategory: Corporate Banking / Treasury Services
  ServiceName: Bank of America CashPro
layout: finops
meters:
- aggregation: sum
  description: Count of payment instructions submitted (wires, ACH, check, RTP, etc.)
  dimensions:
  - payment_type
  - originating_account
  - business_unit
  name: payment_transactions
  unit: transaction
- aggregation: sum
  description: Settled payment value (separate from per-transaction fees)
  dimensions:
  - payment_type
  - currency
  - originating_account
  name: payment_volume
  unit: USD
- aggregation: sum
  description: FX-converted volume; pricing is via spread/margin, not per-API-call fee
  dimensions:
  - currency_pair
  - originating_account
  name: fx_volume
  unit: USD
- aggregation: sum
  description: Balance and statement API calls; included with the CashPro relationship
  dimensions:
  - account
  - api
  name: balance_inquiries
  unit: request
name: Bank Of America Finops
provider_name: Bank of America
provider_slug: bank-of-america
publisher_name: Bank of America Corporation
service_category: Corporate Banking / Treasury Services
slug: bank-of-america-finops
source_filename: bank-of-america-finops.yml
source_heading: FinOps Profile
source_url: https://developer.bankofamerica.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Bank of America\nproviderId: bank-of-america\npublisherName: Bank of America Corporation\nserviceCategory: Corporate Banking / Treasury Services\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Banking\n  - Corporate Banking\n  - Treasury\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps shape for Bank of America CashPro: API access is bundled into a corporate\n  banking / treasury services agreement, so FinOps focuses on per-transaction banking fees (wire, ACH,\n  FX margin) rather than per-API-call charges. Public meter values are not available.'\nnotes: No public rate card. Replace meter prices with the customer's negotiated CashPro fee schedule\n\
  \  once available.\nsources:\n  - https://developer.bankofamerica.com/\n  - https://business.bofa.com/en-us/content/cashpro.html\nprinciples:\n  - name: Visibility\n    description: Pull statements and transaction details via the CashPro APIs to attribute banking fees\n      back to the originating business unit.\n  - name: Allocation\n    description: Allocate wire, ACH, lockbox, and FX fees by originating account, business unit, and payment\n      type using the structured payment metadata returned by the API.\n  - name: Optimization\n    description: Optimize payment-rail mix (ACH vs wire vs same-day ACH vs RTP) based on cost vs settlement-time\n      requirements; consolidate FX across business units to negotiate tighter spreads.\n  - name: Accountability\n    description: Assign a corporate treasury owner who reviews monthly account-analysis statements and\n      reconciles fee categories to internal cost centers.\nbillingModel:\n  pricingCategory: Bundled Banking Fees\n  billingFrequency:\
  \ Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Tax\n    - Adjustment\n    - Refund\n    - Credit\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Bank of America CashPro\n  ServiceCategory: Corporate Banking / Treasury Services\n  ProviderName: Bank of America\n  PublisherName: Bank of America Corporation\n  InvoiceIssuerName: Bank of America, N.A.\n  PricingCategory: Bundled Banking Fees\n  PricingUnit: transaction\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: payment_transactions\n    description: Count of payment instructions submitted (wires, ACH, check, RTP, etc.)\n    unit: transaction\n    aggregation: sum\n    dimensions:\n      - payment_type\n      - originating_account\n      - business_unit\n  - name: payment_volume\n    description: Settled payment value (separate from per-transaction fees)\n    unit: USD\n    aggregation: sum\n    dimensions:\n      - payment_type\n      - currency\n      - originating_account\n\
  \  - name: fx_volume\n    description: FX-converted volume; pricing is via spread/margin, not per-API-call fee\n    unit: USD\n    aggregation: sum\n    dimensions:\n      - currency_pair\n      - originating_account\n  - name: balance_inquiries\n    description: Balance and statement API calls; included with the CashPro relationship\n    unit: request\n    aggregation: sum\n    dimensions:\n      - account\n      - api\napis:\n  - name: Bank of America CashPro API\n    baseURL: https://api.bankofamerica.com/cashpro/v1\n    tags:\n      - Accounts\n      - Balances\n      - Banking\n      - Corporate Banking\n      - Payments\n      - Statements\n      - Treasury\n    serviceName: Bank of America CashPro API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per Payment Transaction\n    metric: total_payment_fees / payment_transactions\n    target: minimize via rail-mix optimization\n  - name: FX Margin Rate\n    metric: fx_margin_revenue / fx_volume\n    target: negotiate downward\
  \ at relationship review\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/bank-of-america/refs/heads/main/finops/bank-of-america-finops.yml
sources:
- https://developer.bankofamerica.com/
- https://business.bofa.com/en-us/content/cashpro.html
specification: FinOps Framework
tags:
- Banking
- Corporate Banking
- Treasury
- FinOps
- FOCUS
---
