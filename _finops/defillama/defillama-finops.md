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
description: 'FinOps view of DefiLlama. Two simple cost lines: zero (Public API) and a flat $300/month Pro subscription. No usage-based billing beyond the included rate cap. Allocation is by API key.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Subscription
  InvoiceIssuerName: DefiLlama
  ProviderName: DefiLlama
  PublisherName: DefiLlama
  ServiceCategory: Crypto Analytics
  ServiceName: DefiLlama Pro API
layout: finops
meters:
- aggregation: sum
  description: Flat monthly Pro subscription per API key.
  dimensions:
  - api_key
  name: pro_subscription
  unit: month
name: Defillama Finops
provider_name: DefiLlama
provider_slug: defillama
publisher_name: DefiLlama
service_category: Crypto Analytics
slug: defillama-finops
source_filename: defillama-finops.yml
source_heading: FinOps Profile
source_url: https://defillama.com/pro-api
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: DefiLlama\nproviderId: defillama\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: true\ntags:\n  - DeFi\n  - Crypto\n  - FinOps\n  - FOCUS\ndescription: >-\n  FinOps view of DefiLlama. Two simple cost lines: zero (Public API) and a flat $300/month Pro\n  subscription. No usage-based billing beyond the included rate cap. Allocation is by API key.\nsources:\n  - https://defillama.com/pro-api\n  - https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: DefiLlama\nserviceCategory: Crypto Analytics\nbillingModel:\n  pricingCategory: Subscription\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Subscription\n\
  focusColumns:\n  ServiceName: DefiLlama Pro API\n  ServiceCategory: Crypto Analytics\n  ProviderName: DefiLlama\n  PublisherName: DefiLlama\n  InvoiceIssuerName: DefiLlama\n  BillingCurrency: USD\n  ChargeCategory: Subscription\nmeters:\n  - name: pro_subscription\n    description: Flat monthly Pro subscription per API key.\n    unit: month\n    aggregation: sum\n    dimensions:\n      - api_key\nprinciples:\n  - name: Visibility\n    description: Tag each Pro key to one owning workload.\n  - name: Allocation\n    description: Allocate $300/month flat to the consuming product.\n  - name: Optimization\n    description: Stay on free Public API unless exclusive endpoints or higher rate limit are required.\n  - name: Accountability\n    description: Assign a billing owner per Pro API key; review monthly.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/defillama/refs/heads/main/finops/defillama-finops.yml
sources:
- https://defillama.com/pro-api
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- DeFi
- Crypto
- FinOps
- FOCUS
---
