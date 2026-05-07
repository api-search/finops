---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: nomba-authentication-openapi.yml
  format: yaml
  label: Nomba Authentication API
  slug: authentication
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/nomba/refs/heads/main/openapi/nomba-authentication-openapi.yml
- filename: nomba-accounts-openapi.yml
  format: yaml
  label: Nomba Accounts API
  slug: accounts
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/nomba/refs/heads/main/openapi/nomba-accounts-openapi.yml
- filename: nomba-virtual-accounts-openapi.yml
  format: yaml
  label: Nomba Virtual Accounts API
  slug: virtual-accounts
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/nomba/refs/heads/main/openapi/nomba-virtual-accounts-openapi.yml
- filename: nomba-transfers-openapi.yml
  format: yaml
  label: Nomba Transfers API
  slug: transfers
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/nomba/refs/heads/main/openapi/nomba-transfers-openapi.yml
- filename: nomba-online-checkout-openapi.yml
  format: yaml
  label: Nomba Online Checkout API
  slug: online-checkout
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/nomba/refs/heads/main/openapi/nomba-online-checkout-openapi.yml
- filename: nomba-charge-openapi.yml
  format: yaml
  label: Nomba Charge API
  slug: charge
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/nomba/refs/heads/main/openapi/nomba-charge-openapi.yml
- filename: nomba-transactions-openapi.yml
  format: yaml
  label: Nomba Transactions API
  slug: transactions
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/nomba/refs/heads/main/openapi/nomba-transactions-openapi.yml
- filename: nomba-global-payout-openapi.yml
  format: yaml
  label: Nomba Global Payout API
  slug: global-payout
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/nomba/refs/heads/main/openapi/nomba-global-payout-openapi.yml
billing_model:
  billingCurrency: NGN (settlement varies)
  billingFrequency: Continuous Settlement
  chargeCategories:
  - Usage
  - Purchase
  - Tax
  - Adjustment
  - Refund
  pricingCategory: Take Rate + Hardware
description: 'FOCUS-aligned FinOps for Nomba: per-transaction fees on cards, bank transfers, USSD/QR, and cross-border payouts, plus POS terminal hardware sales. Settlement currency is NGN with USD/EUR for cross-border lines.'
focus_columns:
  BillingCurrency: NGN
  InvoiceIssuerName: Nomba
  PricingCategory: Take Rate
  ProviderName: Nomba
  PublisherName: Nomba
  RegionId: NG
  ServiceCategory: Payments
  ServiceName: Nomba
  ServiceSubcategory: Card / Bank Transfer / POS
layout: finops
meters:
- aggregation: sum
  description: Card payments processed via Nomba.
  dimensions:
  - card_brand
  - currency
  - merchant
  name: card_transactions
  unit: transaction
- aggregation: sum
  description: Bank transfer transactions.
  dimensions:
  - direction
  - currency
  - merchant
  name: bank_transfers
  unit: transaction
- aggregation: sum
  description: USSD and QR-code payment transactions.
  dimensions:
  - channel
  - merchant
  name: ussd_qr_transactions
  unit: transaction
- aggregation: sum
  description: Inflows received on Nomba virtual accounts.
  dimensions:
  - merchant
  name: virtual_account_inflows
  unit: transaction
- aggregation: sum
  description: Cross-border payout volume.
  dimensions:
  - corridor
  - currency
  - merchant
  name: cross_border_payouts
  unit: transaction
- aggregation: avg
  description: POS terminals deployed.
  dimensions:
  - merchant
  - region
  name: pos_terminal_units
  unit: terminal-month
name: Nomba Finops
provider_name: Nomba
provider_slug: nomba
publisher_name: Nomba
service_category: Payments
slug: nomba-finops
source_filename: nomba-finops.yml
source_heading: FinOps Profile
source_url: https://nomba.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Nomba\nproviderId: nomba\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Payments\n  - Fintech\n  - Nigeria\nnotes: Nomba does not publicly post per-transaction take rates or terminal pricing. FinOps shape captured\n  here describes the typical Nigerian payment-processor billing pattern (per-transaction fees on cards\n  / transfers / USSD / QR, plus POS terminal hardware sales). Reconcile against the merchant onboarding\n  agreement.\ndescription: 'FOCUS-aligned FinOps for Nomba: per-transaction fees on cards, bank transfers, USSD/QR,\n  and cross-border payouts, plus POS terminal hardware sales. Settlement currency is NGN with USD/EUR\n  for cross-border lines.'\nsources:\n  - https://nomba.com/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec:\
  \ FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Nomba\nserviceCategory: Payments\nbillingModel:\n  pricingCategory: Take Rate + Hardware\n  billingFrequency: Continuous Settlement\n  billingCurrency: NGN (settlement varies)\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Adjustment\n    - Refund\nfocusColumns:\n  ServiceName: Nomba\n  ServiceCategory: Payments\n  ServiceSubcategory: Card / Bank Transfer / POS\n  ProviderName: Nomba\n  PublisherName: Nomba\n  InvoiceIssuerName: Nomba\n  BillingCurrency: NGN\n  RegionId: NG\n  PricingCategory: Take Rate\nmeters:\n  - name: card_transactions\n    description: Card payments processed via Nomba.\n    unit: transaction\n    aggregation: sum\n    dimensions:\n      - card_brand\n      - currency\n      - merchant\n  - name: bank_transfers\n    description: Bank transfer transactions.\n    unit: transaction\n    aggregation: sum\n    dimensions:\n      - direction\n\
  \      - currency\n      - merchant\n  - name: ussd_qr_transactions\n    description: USSD and QR-code payment transactions.\n    unit: transaction\n    aggregation: sum\n    dimensions:\n      - channel\n      - merchant\n  - name: virtual_account_inflows\n    description: Inflows received on Nomba virtual accounts.\n    unit: transaction\n    aggregation: sum\n    dimensions:\n      - merchant\n  - name: cross_border_payouts\n    description: Cross-border payout volume.\n    unit: transaction\n    aggregation: sum\n    dimensions:\n      - corridor\n      - currency\n      - merchant\n  - name: pos_terminal_units\n    description: POS terminals deployed.\n    unit: terminal-month\n    aggregation: avg\n    dimensions:\n      - merchant\n      - region\nprinciples:\n  - name: Visibility\n    description: Use Nomba merchant dashboard and the Transactions / Settlements API to attribute revenue\n      and fees per channel and per merchant.\n  - name: Allocation\n    description: Tag transactions\
  \ with merchant_id and channel; map sub-merchants under platform accounts\n      for chargeback / showback.\n  - name: Optimization\n    description: Route low-value payments via USSD / QR (typically lower fees than card); consolidate\n      payouts to reduce per-transaction overhead; right-size POS terminal fleet per location footprint.\n  - name: Accountability\n    description: Reconcile Nomba settlements daily against the merchant ledger; investigate take-rate\n      and FX variances on cross-border payouts; review terminal utilization against fixed-cost recovery.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/nomba/refs/heads/main/finops/nomba-finops.yml
sources:
- https://nomba.com/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Payments
- Fintech
- Nigeria
---
