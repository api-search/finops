---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: uspto-trademark-search-api-openapi.yml
  format: yaml
  label: USPTO Trademark Search API Endpoints
  slug: uspto-trademark-search-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/uspto-trademark-search-api/refs/heads/main/openapi/uspto-trademark-search-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  - Tax
  - Credit
  - Adjustment
  chargeFrequency: Recurring
  pricingCategory: Usage-Based
description: FinOps framework definition for the USPTO Trademark Search API API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: USPTO Trademark Search API
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: USPTO Trademark Search API
  PublisherName: USPTO Trademark Search API
  ServiceCategory: Developer Tools / API
  ServiceName: USPTO Trademark Search API
layout: finops
meters:
- aggregation: sum
  description: Count of billable API requests
  dimensions:
  - api
  - endpoint
  - tier
  - region
  - consumer
  name: api_requests
  unit: request
- aggregation: sum
  description: Bytes returned over the network in API responses
  dimensions:
  - api
  - region
  - consumer
  name: data_egress
  unit: GB
- aggregation: sum
  description: Server-side compute consumed by the request, where applicable
  dimensions:
  - api
  - endpoint
  - tier
  name: compute_seconds
  unit: second
name: Uspto Trademark Search Api Finops
provider_name: USPTO Trademark Search API
provider_slug: uspto-trademark-search-api
publisher_name: USPTO Trademark Search API
service_category: API
slug: uspto-trademark-search-api-finops
source_filename: uspto-trademark-search-api-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: USPTO Trademark Search API\nproviderId: uspto-trademark-search-api\npublisherName: USPTO Trademark Search API\nserviceCategory: API\ncreated: '2026-05-04'\nmodified: '2026-05-04'\ntags:\n  - Brand\n  - Brand Protection\n  - Business\n  - Data\n  - Government Data\n  - Intellectual Property\n  - Legal\n  - Search\n  - Trademark\n  - USPTO\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the USPTO Trademark Search API API surface. Provides a FOCUS-aligned\n  mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to\
  \ engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload\
  \ Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: USPTO Trademark Search API\n  ServiceCategory: Developer Tools / API\n  ProviderName: USPTO Trademark Search API\n  PublisherName: USPTO Trademark Search API\n  InvoiceIssuerName: USPTO Trademark Search API\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n\
  \      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: USPTO Trademark Search API Endpoints\n    baseURL: https://uspto-trademark.p.rapidapi.com\n    tags:\n      - Brand Protection\n      - Data Retrieval\n      - Legal Research\n      - Trademark Search\n      - USPTO Data\n    serviceName: USPTO Trademark Search API Endpoints\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target:\
  \ TBD\nmaintainers:\n  - FN: MartonKodok\n    email: android482-one@yahoo.com\n    X-twitter: martonkodok\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/uspto-trademark-search-api/refs/heads/main/finops/uspto-trademark-search-api-finops.yml
sources: []
specification: FinOps Framework
tags:
- Brand
- Brand Protection
- Business
- Data
- Government Data
- Intellectual Property
- Legal
- Search
- Trademark
- USPTO
- FinOps
- Cost Management
- FOCUS
---
