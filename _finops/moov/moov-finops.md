---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: moov-api-openapi.yml
  format: yaml
  label: Moov API
  slug: moov-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/moov/refs/heads/main/openapi/moov-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  pricingCategory: Per-Transaction with $500/mo Minimum
description: FOCUS-aligned FinOps for Moov.
focus_columns:
  BillingCurrency: USD
  ProviderName: Moov
  PublisherName: Moov
  ServiceCategory: Embedded Finance
  ServiceName: Moov
layout: finops
meters:
- aggregation: sum
  dimensions:
  - channel
  - card_present
  name: card_transactions
  unit: transaction
- aggregation: sum
  name: transaction_volume
  unit: USD
- aggregation: sum
  name: ach_transactions
  unit: transaction
- aggregation: sum
  name: instant_payments
  unit: transaction
- aggregation: max
  name: active_wallets
  unit: wallet-month
- aggregation: sum
  name: virtual_cards_issued
  unit: card
name: Moov Finops
provider_name: Moov
provider_slug: moov
publisher_name: Moov
service_category: Embedded Finance
slug: moov-finops
source_filename: moov-finops.yml
source_heading: FinOps Profile
source_url: https://moov.io/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Moov\nproviderId: moov\ncreated: '2026-05-04'\nmodified: '2026-05-04'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Embedded Finance\ndescription: FOCUS-aligned FinOps for Moov.\nsources:\n  - https://moov.io/pricing\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Moov\nserviceCategory: Embedded Finance\nbillingModel:\n  pricingCategory: Per-Transaction with $500/mo Minimum\n  billingFrequency: Monthly\n  billingCurrency: USD\nfocusColumns:\n  ServiceName: Moov\n  ServiceCategory: Embedded Finance\n  ProviderName: Moov\n  PublisherName: Moov\n  BillingCurrency: USD\nmeters:\n  - name: card_transactions\n    unit: transaction\n    aggregation: sum\n    dimensions:\n     \
  \ - channel\n      - card_present\n  - name: transaction_volume\n    unit: USD\n    aggregation: sum\n  - name: ach_transactions\n    unit: transaction\n    aggregation: sum\n  - name: instant_payments\n    unit: transaction\n    aggregation: sum\n  - name: active_wallets\n    unit: wallet-month\n    aggregation: max\n  - name: virtual_cards_issued\n    unit: card\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Track Moov consumption monthly.\n  - name: Allocation\n    description: Tag usage to teams/cost centers.\n  - name: Optimization\n    description: Right-size; reclaim unused entitlements.\n  - name: Accountability\n    description: Set spend alerts; quarterly review.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/moov/refs/heads/main/finops/moov-finops.yml
sources:
- https://moov.io/pricing
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Embedded Finance
---
