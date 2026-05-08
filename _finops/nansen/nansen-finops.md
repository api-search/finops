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
  - Subscription
  - Adjustment
  pricingCategory: Subscription / Custom Contract
description: FinOps view of Nansen. Subscription-based with separate API and Studio plan ladders. API access is sales-led, with Standard and Enterprise contracts. No usage-based billing beyond the per-second / per-minute rate limit.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Subscription
  InvoiceIssuerName: Nansen
  ProviderName: Nansen
  PublisherName: Nansen
  ServiceCategory: Crypto Analytics
  ServiceName: Nansen API
layout: finops
meters:
- aggregation: sum
  description: Monthly API subscription per key.
  dimensions:
  - api_key
  name: subscription
  unit: month
name: Nansen Finops
provider_name: Nansen
provider_slug: nansen
publisher_name: Nansen
service_category: Crypto Analytics
slug: nansen-finops
source_filename: nansen-finops.yml
source_heading: FinOps Profile
source_url: https://www.nansen.ai/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Nansen\nproviderId: nansen\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: true\ntags:\n  - Crypto\n  - On-Chain\n  - FinOps\n  - FOCUS\ndescription: >-\n  FinOps view of Nansen. Subscription-based with separate API and Studio plan ladders. API\n  access is sales-led, with Standard and Enterprise contracts. No usage-based billing beyond\n  the per-second / per-minute rate limit.\nsources:\n  - https://www.nansen.ai/pricing\n  - https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Nansen\nserviceCategory: Crypto Analytics\nbillingModel:\n  pricingCategory: Subscription / Custom Contract\n  billingFrequency: Monthly\n  billingCurrency:\
  \ USD\n  chargeCategories:\n    - Subscription\n    - Adjustment\nfocusColumns:\n  ServiceName: Nansen API\n  ServiceCategory: Crypto Analytics\n  ProviderName: Nansen\n  PublisherName: Nansen\n  InvoiceIssuerName: Nansen\n  BillingCurrency: USD\n  ChargeCategory: Subscription\nmeters:\n  - name: subscription\n    description: Monthly API subscription per key.\n    unit: month\n    aggregation: sum\n    dimensions:\n      - api_key\nprinciples:\n  - name: Visibility\n    description: Tag each API key to a single owning workload.\n  - name: Allocation\n    description: Allocate subscription across consuming product lines.\n  - name: Optimization\n    description: Drop redundant Studio seats if API consumers can serve the same dashboard need.\n  - name: Accountability\n    description: Assign a billing owner; review quarterly.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/nansen/refs/heads/main/finops/nansen-finops.yml
sources:
- https://www.nansen.ai/pricing
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Crypto
- On-Chain
- FinOps
- FOCUS
---
