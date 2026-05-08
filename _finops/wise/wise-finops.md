---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: wise-platform-openapi.yml
  format: yaml
  label: Wise Profiles API
  slug: profiles
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/wise/refs/heads/main/openapi/wise-platform-openapi.yml
- filename: wise-platform-openapi.yml
  format: yaml
  label: Wise Recipients API
  slug: recipients
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/wise/refs/heads/main/openapi/wise-platform-openapi.yml
- filename: wise-platform-openapi.yml
  format: yaml
  label: Wise Quotes API
  slug: quotes
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/wise/refs/heads/main/openapi/wise-platform-openapi.yml
- filename: wise-platform-openapi.yml
  format: yaml
  label: Wise Transfers API
  slug: transfers
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/wise/refs/heads/main/openapi/wise-platform-openapi.yml
- filename: wise-platform-openapi.yml
  format: yaml
  label: Wise Balances API
  slug: balances
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/wise/refs/heads/main/openapi/wise-platform-openapi.yml
- filename: wise-platform-openapi.yml
  format: yaml
  label: Wise Multi-Currency Account API
  slug: multi-currency-account
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/wise/refs/heads/main/openapi/wise-platform-openapi.yml
- filename: wise-platform-openapi.yml
  format: yaml
  label: Wise Statements API
  slug: statements
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/wise/refs/heads/main/openapi/wise-platform-openapi.yml
- filename: wise-platform-openapi.yml
  format: yaml
  label: Wise Cards API
  slug: cards
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/wise/refs/heads/main/openapi/wise-platform-openapi.yml
- filename: wise-platform-openapi.yml
  format: yaml
  label: Wise Webhooks API
  slug: webhooks
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/wise/refs/heads/main/openapi/wise-platform-openapi.yml
- filename: wise-platform-openapi.yml
  format: yaml
  label: Wise Simulation API
  slug: simulation
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/wise/refs/heads/main/openapi/wise-platform-openapi.yml
billing_model:
  billingCurrency: Multi-Currency
  billingFrequency: Per Transaction (statement monthly)
  chargeCategories:
  - Usage
  - Purchase
  - Adjustment
  - Tax
  - Credit
  pricingCategory: Pay-As-You-Go (Transaction Fees + FX Markup)
description: FOCUS-aligned FinOps for Wise. The Wise Platform API itself is free; cost is incurred per transaction in two components - a route-specific transfer fee (a fixed amount plus a percentage of the converted amount) and a small markup applied on top of the mid-market FX rate when a conversion occurs. Wise Business adds a one-time account-opening fee in most regions and per-card issuance fees. Wise Platform (embedded partner) tenants negotiate consolidated pricing with monthly settlement.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Wise Payments Limited
  ProviderName: Wise
  PublisherName: Wise Payments Limited
  ServiceCategory: Payments
  ServiceName: Wise Platform
layout: finops
meters:
- aggregation: sum
  description: Per-transfer fee composed of a route-specific fixed component plus a percentage of the converted amount. Visible on the quote response before the transfer is created.
  dimensions:
  - source_currency
  - target_currency
  - pay_in_method
  - profile_type
  name: transfer_fee
  unit: transfer
- aggregation: sum
  description: Margin applied to the mid-market exchange rate on currency conversions. Captured implicitly in the rate returned by the Quotes API.
  dimensions:
  - source_currency
  - target_currency
  name: fx_markup
  unit: fx_conversion
- aggregation: sum
  description: One-time fee charged on Wise Business account creation in most regions (e.g. ~$31 US / GBP 45 UK).
  dimensions:
  - region
  name: account_opening_fee
  unit: account
- aggregation: sum
  description: Wise debit card issuance and replacement fees (issuance ~$9 in the US, GBP 7 UK).
  dimensions:
  - region
  - card_type
  name: card_fee
  unit: card
- aggregation: sum
  description: Embedded Wise Platform partner per-transaction or settlement fee, negotiated contractually for banks and fintechs that resell Wise capabilities.
  dimensions:
  - partner_id
  - transaction_type
  name: platform_partner_fee
  unit: transaction
name: Wise Finops
provider_name: Wise
provider_slug: wise
publisher_name: Wise Payments Limited
service_category: Payments
slug: wise-finops
source_filename: wise-finops.yml
source_heading: FinOps Profile
source_url: https://wise.com/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Wise\nproviderId: wise\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: true\ntags:\n  - Payments\n  - FX\n  - Cross-Border\n  - Banking\n  - Multi-Currency\n  - FinOps\n  - FOCUS\ndescription: >-\n  FOCUS-aligned FinOps for Wise. The Wise Platform API itself is free; cost is incurred\n  per transaction in two components - a route-specific transfer fee (a fixed amount plus\n  a percentage of the converted amount) and a small markup applied on top of the\n  mid-market FX rate when a conversion occurs. Wise Business adds a one-time\n  account-opening fee in most regions and per-card issuance fees. Wise Platform\n  (embedded partner) tenants negotiate consolidated pricing with monthly settlement.\nsources:\n  - https://wise.com/pricing\n  - https://wise.com/help/articles/2932150\n  - https://docs.wise.com/\nalignedWith:\n  framework: FinOps Foundation Framework\n\
  \  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Wise Payments Limited\nserviceCategory: Payments\nbillingModel:\n  pricingCategory: Pay-As-You-Go (Transaction Fees + FX Markup)\n  billingFrequency: Per Transaction (statement monthly)\n  billingCurrency: Multi-Currency\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Adjustment\n    - Tax\n    - Credit\nfocusColumns:\n  ServiceName: Wise Platform\n  ServiceCategory: Payments\n  ProviderName: Wise\n  PublisherName: Wise Payments Limited\n  InvoiceIssuerName: Wise Payments Limited\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: transfer_fee\n    description: >-\n      Per-transfer fee composed of a route-specific fixed component plus a percentage of\n      the converted amount. Visible on the quote response before the transfer is created.\n    unit: transfer\n    aggregation: sum\n\
  \    dimensions:\n      - source_currency\n      - target_currency\n      - pay_in_method\n      - profile_type\n  - name: fx_markup\n    description: >-\n      Margin applied to the mid-market exchange rate on currency conversions. Captured\n      implicitly in the rate returned by the Quotes API.\n    unit: fx_conversion\n    aggregation: sum\n    dimensions:\n      - source_currency\n      - target_currency\n  - name: account_opening_fee\n    description: >-\n      One-time fee charged on Wise Business account creation in most regions\n      (e.g. ~$31 US / GBP 45 UK).\n    unit: account\n    aggregation: sum\n    dimensions:\n      - region\n  - name: card_fee\n    description: >-\n      Wise debit card issuance and replacement fees (issuance ~$9 in the US, GBP 7 UK).\n    unit: card\n    aggregation: sum\n    dimensions:\n      - region\n      - card_type\n  - name: platform_partner_fee\n    description: >-\n      Embedded Wise Platform partner per-transaction or settlement fee, negotiated\n\
  \      contractually for banks and fintechs that resell Wise capabilities.\n    unit: transaction\n    aggregation: sum\n    dimensions:\n      - partner_id\n      - transaction_type\nprinciples:\n  - name: Visibility\n    description: >-\n      Every transfer carries an explicit fee breakdown on the quote and the resulting\n      transfer object. Use the Statements API (JSON/CSV/MT940) to reconcile fees and FX\n      markup against the converted amount line by line.\n  - name: Allocation\n    description: >-\n      Tag transfers with customerTransactionId on creation to attribute spend to a\n      cost center or end-customer. Wise Business multi-user RBAC and Wise Platform\n      partner accounts allow per-team or per-tenant attribution.\n  - name: Optimization\n    description: >-\n      Pre-fund transfers from a same-currency Wise balance to skip the FX markup. Batch\n      payouts (up to 1,000 per file) reduce per-transfer overhead. Choose lower-fee\n      pay-in methods (bank debit\
  \ / ACH) over card funding where speed permits.\n  - name: Accountability\n    description: >-\n      Assign a treasury owner per Wise profile. Wire pay-in/pay-out paths and FX corridors\n      to internal cost categories so the FX markup is treated as a controllable spend\n      lever, not a hidden cost.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/wise/refs/heads/main/finops/wise-finops.yml
sources:
- https://wise.com/pricing
- https://wise.com/help/articles/2932150
- https://docs.wise.com/
specification: FinOps Framework
tags:
- Payments
- FX
- Cross-Border
- Banking
- Multi-Currency
- FinOps
- FOCUS
---
