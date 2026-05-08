---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: bloomberg-data-license-api.yml
  format: yaml
  label: Bloomberg Data License API
  slug: bloomberg-data-license-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/bloomberg-aim/refs/heads/main/openapi/bloomberg-data-license-api.yml
- filename: bloomberg-emsx-api.yml
  format: yaml
  label: Bloomberg EMSX API
  slug: bloomberg-emsx-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/bloomberg-aim/refs/heads/main/openapi/bloomberg-emsx-api.yml
- filename: bloomberg-http-api.yml
  format: yaml
  label: Bloomberg HTTP API
  slug: bloomberg-http-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/bloomberg-aim/refs/heads/main/openapi/bloomberg-http-api.yml
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
description: FinOps framework definition for the Bloomberg AIM API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Bloomberg AIM
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Bloomberg AIM
  PublisherName: Bloomberg AIM
  ServiceCategory: Developer Tools / API
  ServiceName: Bloomberg AIM
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
name: Bloomberg Aim Finops
provider_name: Bloomberg AIM
provider_slug: bloomberg-aim
publisher_name: Bloomberg AIM
service_category: API
slug: bloomberg-aim-finops
source_filename: bloomberg-aim-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Bloomberg AIM\nproviderId: bloomberg-aim\npublisherName: Bloomberg AIM\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Financial Data\n  - Market Data\n  - Order Management\n  - Portfolio Management\n  - Trading\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Bloomberg AIM API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag\
  \ every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n\
  \    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Bloomberg AIM\n  ServiceCategory: Developer Tools / API\n  ProviderName: Bloomberg AIM\n  PublisherName: Bloomberg AIM\n  InvoiceIssuerName: Bloomberg AIM\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network\
  \ in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Bloomberg Data License API\n    baseURL: https://api.bloomberg.com/eap\n    tags:\n      - Financial Data\n      - Market Data\n      - Pricing Data\n      - Reference Data\n    serviceName: Bloomberg Data License API\n    serviceCategory: API\n  - name: Bloomberg Server API (SAPI)\n    baseURL: ''\n    tags:\n      - Financial Analytics\n      - Market Data\n      - Real-Time Data\n      - Server API\n    serviceName: Bloomberg Server API (SAPI)\n    serviceCategory: API\n  - name: Bloomberg EMSX API\n    baseURL: https://localhost:3000\n    tags:\n      - Equities\n      - Execution Management\n      - Order Management\n      - Trading\n    serviceName:\
  \ Bloomberg EMSX API\n    serviceCategory: API\n  - name: Bloomberg HTTP API\n    baseURL: https://localhost:3000\n    tags:\n      - Historical Data\n      - HTTP API\n      - Market Data\n      - Reference Data\n      - Streaming\n    serviceName: Bloomberg HTTP API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/bloomberg-aim/refs/heads/main/finops/bloomberg-aim-finops.yml
sources: []
specification: FinOps Framework
tags:
- Financial Data
- Market Data
- Order Management
- Portfolio Management
- Trading
- FinOps
- Cost Management
- FOCUS
---
