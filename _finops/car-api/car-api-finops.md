---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: car-api-openapi-original.yml
  format: yaml
  label: CarAPI Vehicle API
  slug: vehicle-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/car-api/refs/heads/main/openapi/car-api-openapi-original.yml
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
description: FinOps framework definition for the Car API (carapi.app) API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Car API (carapi.app)
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Car API (carapi.app)
  PublisherName: Car API (carapi.app)
  ServiceCategory: Developer Tools / API
  ServiceName: Car API (carapi.app)
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
name: Car Api Finops
provider_name: Car API (carapi.app)
provider_slug: car-api
publisher_name: Car API (carapi.app)
service_category: API
slug: car-api-finops
source_filename: car-api-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Car API (carapi.app)\nproviderId: car-api\npublisherName: Car API (carapi.app)\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Automobiles\n  - Automotive Data\n  - Cars\n  - License Plate Decoder\n  - OBD-II\n  - Power Sports\n  - Vehicle API\n  - Vehicle Specifications\n  - Vehicles\n  - VIN Decoder\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Car API (carapi.app) API surface. Provides a FOCUS-aligned\n  mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering,\
  \ product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n\
  \      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Car API (carapi.app)\n  ServiceCategory: Developer Tools / API\n  ProviderName: Car API (carapi.app)\n  PublisherName: Car API (carapi.app)\n  InvoiceIssuerName: Car API (carapi.app)\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n\
  \      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: CarAPI Vehicle API\n    baseURL: https://carapi.app/api\n    tags:\n      - Automobiles\n      - Vehicle API\n      - Vehicle Specifications\n      - Vehicles\n    serviceName: CarAPI Vehicle API\n    serviceCategory: API\n  - name: CarAPI VIN Decoder API\n    baseURL: https://carapi.app/api\n    tags:\n      - Automobiles\n      - Vehicles\n      - VIN Decoder\n    serviceName: CarAPI VIN Decoder API\n    serviceCategory: API\n  - name: CarAPI License Plate API\n    baseURL: https://carapi.app/api\n    tags:\n      - Automobiles\n\
  \      - License Plate Decoder\n      - Vehicles\n    serviceName: CarAPI License Plate API\n    serviceCategory: API\n  - name: CarAPI OBD-II Code API\n    baseURL: https://carapi.app/api\n    tags:\n      - Automobiles\n      - Diagnostics\n      - OBD-II\n      - Vehicles\n    serviceName: CarAPI OBD-II Code API\n    serviceCategory: API\n  - name: CarAPI Power Sports API\n    baseURL: https://carapi.app/api\n    tags:\n      - ATV\n      - Motorcycles\n      - Power Sports\n      - UTV\n      - Vehicles\n    serviceName: CarAPI Power Sports API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/car-api/refs/heads/main/finops/car-api-finops.yml
sources: []
specification: FinOps Framework
tags:
- Automobiles
- Automotive Data
- Cars
- License Plate Decoder
- OBD-II
- Power Sports
- Vehicle API
- Vehicle Specifications
- Vehicles
- VIN Decoder
- FinOps
- Cost Management
- FOCUS
---
