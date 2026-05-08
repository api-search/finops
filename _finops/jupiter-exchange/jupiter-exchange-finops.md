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
  pricingCategory: Subscription
description: FinOps view of Jupiter Developer Platform. Free Lite tier and paid Pro subscription per API key. No usage-based billing beyond the rate limit. Solana on-chain trading fees are protocol level and not part of the API subscription bill.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Subscription
  InvoiceIssuerName: Jupiter
  ProviderName: Jupiter
  PublisherName: Jupiter
  ServiceCategory: DeFi Infrastructure
  ServiceName: Jupiter Developer Platform
layout: finops
meters:
- aggregation: sum
  description: Monthly Pro subscription per API key.
  dimensions:
  - api_key
  name: subscription
  unit: month
name: Jupiter Exchange Finops
provider_name: Jupiter
provider_slug: jupiter-exchange
publisher_name: Jupiter Aggregator
service_category: DeFi Infrastructure
slug: jupiter-exchange-finops
source_filename: jupiter-exchange-finops.yml
source_heading: FinOps Profile
source_url: https://portal.jup.ag/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Jupiter\nproviderId: jupiter-exchange\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: true\ntags:\n  - Solana\n  - DEX\n  - FinOps\n  - FOCUS\ndescription: >-\n  FinOps view of Jupiter Developer Platform. Free Lite tier and paid Pro subscription per API\n  key. No usage-based billing beyond the rate limit. Solana on-chain trading fees are protocol\n  level and not part of the API subscription bill.\nsources:\n  - https://portal.jup.ag/pricing\n  - https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Jupiter Aggregator\nserviceCategory: DeFi Infrastructure\nbillingModel:\n  pricingCategory: Subscription\n  billingFrequency:\
  \ Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Subscription\nfocusColumns:\n  ServiceName: Jupiter Developer Platform\n  ServiceCategory: DeFi Infrastructure\n  ProviderName: Jupiter\n  PublisherName: Jupiter\n  InvoiceIssuerName: Jupiter\n  BillingCurrency: USD\n  ChargeCategory: Subscription\nmeters:\n  - name: subscription\n    description: Monthly Pro subscription per API key.\n    unit: month\n    aggregation: sum\n    dimensions:\n      - api_key\nprinciples:\n  - name: Visibility\n    description: Tag each Pro key to a single owning workload.\n  - name: Allocation\n    description: Allocate subscription to consuming product line.\n  - name: Optimization\n    description: Stay on Lite where rps is below cap.\n  - name: Accountability\n    description: Assign a billing owner per Pro API key.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/jupiter-exchange/refs/heads/main/finops/jupiter-exchange-finops.yml
sources:
- https://portal.jup.ag/pricing
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Solana
- DEX
- FinOps
- FOCUS
---
