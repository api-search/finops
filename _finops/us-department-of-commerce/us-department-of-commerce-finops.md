---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: commerce-gov-api-openapi.yml
  format: yaml
  label: Commerce.gov API
  slug: commercegov-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/us-department-of-commerce/refs/heads/main/openapi/commerce-gov-api-openapi.yml
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
description: FinOps framework definition for the US Department of Commerce API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: US Department of Commerce
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: US Department of Commerce
  PublisherName: US Department of Commerce
  ServiceCategory: Developer Tools / API
  ServiceName: US Department of Commerce
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
name: Us Department Of Commerce Finops
provider_name: US Department of Commerce
provider_slug: us-department-of-commerce
publisher_name: US Department of Commerce
service_category: API
slug: us-department-of-commerce-finops
source_filename: us-department-of-commerce-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: US Department of Commerce\nproviderId: us-department-of-commerce\npublisherName: US Department of Commerce\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Commerce\n  - Federal Government\n  - Open Data\n  - Trade\n  - Economic Data\n  - Climate\n  - Standards\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the US Department of Commerce API surface. Provides a FOCUS-aligned\n  mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n\
  \      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n   \
  \   - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: US Department of Commerce\n  ServiceCategory: Developer Tools / API\n  ProviderName: US Department of Commerce\n  PublisherName: US Department of Commerce\n  InvoiceIssuerName: US Department of Commerce\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n\
  \      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Commerce.gov API\n    baseURL: ''\n    tags:\n      - Commerce\n      - News\n      - Blogs\n      - Federal Government\n    serviceName: Commerce.gov API\n    serviceCategory: API\n  - name: US Census Bureau Data API\n    baseURL: ''\n    tags:\n      - Census\n      - Demographics\n      - Economic Data\n      - Federal Government\n    serviceName: US Census Bureau Data API\n    serviceCategory: API\n  - name: Bureau of Economic Analysis API\n    baseURL: ''\n    tags:\n      - Economic Data\n      - GDP\n      - National Accounts\n      - Federal\
  \ Government\n    serviceName: Bureau of Economic Analysis API\n    serviceCategory: API\n  - name: International Trade Administration Trade Data API\n    baseURL: ''\n    tags:\n      - International Trade\n      - Exports\n      - Trade Leads\n      - Federal Government\n    serviceName: International Trade Administration Trade Data API\n    serviceCategory: API\n  - name: NOAA Climate and Weather API\n    baseURL: ''\n    tags:\n      - Weather\n      - Climate\n      - Environment\n      - Federal Government\n    serviceName: NOAA Climate and Weather API\n    serviceCategory: API\n  - name: NIST Data Discovery API\n    baseURL: ''\n    tags:\n      - Research Data\n      - Standards\n      - Materials Science\n      - Federal Government\n    serviceName: NIST Data Discovery API\n    serviceCategory: API\n  - name: Commerce Data Hub Open Data Portal API\n    baseURL: ''\n    tags:\n      - Open Data\n      - Commerce\n      - Federal Government\n    serviceName: Commerce Data Hub Open\
  \ Data Portal API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/us-department-of-commerce/refs/heads/main/finops/us-department-of-commerce-finops.yml
sources: []
specification: FinOps Framework
tags:
- Commerce
- Federal Government
- Open Data
- Trade
- Economic Data
- Climate
- Standards
- FinOps
- Cost Management
- FOCUS
---
