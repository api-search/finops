---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: valueray-symbol-data-openapi.yml
  format: yaml
  label: ValueRay Symbol Data API
  slug: symbol-data-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/valueray/refs/heads/main/openapi/valueray-symbol-data-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: NotApplicable
  chargeCategories:
  - Usage
  pricingCategory: Free
description: FOCUS-aligned FinOps profile for ValueRay. ValueRay currently exposes only a free public tier of its AI-ready Symbol Data API; no paid plans or invoice-bearing offering have been published. This profile captures the FinOps surface that would apply once paid tiers ship and is marked unreconciled until then.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: ValueRay
  ProviderName: ValueRay
  PublisherName: ValueRay
  ServiceCategory: Market Data
  ServiceName: ValueRay Symbol Data API
layout: finops
meters:
- aggregation: sum
  dimensions:
  - api_token
  - symbol
  name: api_calls
  unit: request
name: Valueray Finops
provider_name: ValueRay
provider_slug: valueray
publisher_name: ValueRay
service_category: Market Data
slug: valueray-finops
source_filename: valueray-finops.yml
source_heading: FinOps Profile
source_url: https://www.valueray.com/api
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: ValueRay\nproviderId: valueray\ncreated: '2026-05-06'\nmodified: '2026-05-06'\nreconciled: false\ntags:\n  - AI/LLM\n  - Financial Data\n  - FinOps\n  - FOCUS\n  - Stocks\ndescription: >-\n  FOCUS-aligned FinOps profile for ValueRay. ValueRay currently exposes\n  only a free public tier of its AI-ready Symbol Data API; no paid plans\n  or invoice-bearing offering have been published. This profile captures\n  the FinOps surface that would apply once paid tiers ship and is marked\n  unreconciled until then.\nsources:\n  - https://www.valueray.com/api\n  - https://www.valueray.com/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: ValueRay\nserviceCategory: Market Data\nbillingModel:\n\
  \  pricingCategory: Free\n  billingFrequency: NotApplicable\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\nfocusColumns:\n  ServiceName: ValueRay Symbol Data API\n  ServiceCategory: Market Data\n  ProviderName: ValueRay\n  PublisherName: ValueRay\n  InvoiceIssuerName: ValueRay\n  BillingCurrency: USD\nmeters:\n  - name: api_calls\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api_token\n      - symbol\nprinciples:\n  - name: Visibility\n    description: Track call volume per consumer to project demand against the published 1 request/minute\n      throttle and to inform any future paid-tier sizing.\n  - name: Allocation\n    description: Tag calls by application or agent so usage is attributable when a paid tier ships.\n  - name: Optimization\n    description: Cache symbol responses locally; the response includes a field_explanations URL that can be\n      fetched once and reused, reducing repeat calls.\n  - name: Accountability\n    description: Designate\
  \ an owner for ValueRay usage tracking; revisit when ValueRay publishes formal\n      pricing and metering policies.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/valueray/refs/heads/main/finops/valueray-finops.yml
sources:
- https://www.valueray.com/api
- https://www.valueray.com/
specification: FinOps Framework
tags:
- AI/LLM
- Financial Data
- FinOps
- FOCUS
- Stocks
---
