---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: verisk-insurance-analytics-openapi.yml
  format: yaml
  label: Verisk Insurance Analytics API
  slug: insurance-analytics
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/verisk/refs/heads/main/openapi/verisk-insurance-analytics-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  pricingCategory: Subscription
description: 'FOCUS-aligned FinOps stub for Verisk: contractual data / analytics license sold to insurance carriers and brokers. No public pricing or usage/billing API.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Verisk Analytics, Inc.
  ProviderName: Verisk
  PublisherName: Verisk Analytics, Inc.
  ServiceCategory: Insurance Risk Analytics
  ServiceName: Verisk Data & Analytics
layout: finops
meters:
- aggregation: sum
  description: Annual contractual license for Verisk data sets / APIs; sub-meters not publicly published.
  name: data_api_license
  unit: varies
name: Verisk Finops
provider_name: Verisk
provider_slug: verisk
publisher_name: Verisk Analytics, Inc.
service_category: Insurance Risk Analytics
slug: verisk-finops
source_filename: verisk-finops.yml
source_heading: FinOps Profile
source_url: https://www.verisk.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Verisk\nproviderId: verisk\npublisherName: Verisk Analytics, Inc.\nserviceCategory: Insurance Risk Analytics\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Insurance\n  - Risk Analytics\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps stub for Verisk: contractual data / analytics license sold to insurance\n  carriers and brokers. No public pricing or usage/billing API.'\nsources:\n  - https://www.verisk.com/\nnotes: No public pricing or billing API. Meters are not invented; reconciliation deferred pending customer-portal\n  access.\nbillingModel:\n  pricingCategory: Subscription\n  billingFrequency: Annual\n\
  \  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: Verisk Data & Analytics\n  ServiceCategory: Insurance Risk Analytics\n  ProviderName: Verisk\n  PublisherName: Verisk Analytics, Inc.\n  InvoiceIssuerName: Verisk Analytics, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: data_api_license\n    description: Annual contractual license for Verisk data sets / APIs; sub-meters not publicly published.\n    unit: varies\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Customers consume data via Verisk product portals and APIs; usage telemetry is exposed\n      contractually rather than via a public cost API.\n  - name: Allocation\n    description: Allocation is contract-level (per line of business, geography, data set scope).\n  - name: Optimization\n    description: Optimization is scoping-driven (which data sets, geographies, and query volumes are\n      licensed); renewal is the primary optimization checkpoint.\n  - name:\
  \ Accountability\n    description: Accountability sits with the actuarial / underwriting / claims business owner; finance\n      owns the annual subscription line.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n    url: https://apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/verisk/refs/heads/main/finops/verisk-finops.yml
sources:
- https://www.verisk.com/
specification: FinOps Framework
tags:
- Insurance
- Risk Analytics
- FinOps
- FOCUS
---
