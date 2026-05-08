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
  - Usage
  - Purchase
  - Tax
  - Credit
  - Adjustment
  chargeFrequency: Recurring
  pricingCategory: Usage-Based
description: FinOps framework definition for the Mercedes-Benz API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Mercedes-Benz
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Mercedes-Benz
  PublisherName: Mercedes-Benz
  ServiceCategory: Developer Tools / API
  ServiceName: Mercedes-Benz
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
name: Mercedes Benz Finops
provider_name: Mercedes-Benz
provider_slug: mercedes-benz
publisher_name: Mercedes-Benz
service_category: API
slug: mercedes-benz-finops
source_filename: mercedes-benz-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Mercedes-Benz\nproviderId: mercedes-benz\npublisherName: Mercedes-Benz\nserviceCategory: API\ncreated: '2026-05-04'\nmodified: '2026-05-04'\ntags:\n  - Automobiles\n  - Cars\n  - Vehicles\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Mercedes-Benz API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment,\
  \ application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      -\
  \ FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Mercedes-Benz\n  ServiceCategory: Developer Tools / API\n  ProviderName: Mercedes-Benz\n  PublisherName: Mercedes-Benz\n  InvoiceIssuerName: Mercedes-Benz\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n\
  \      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Mercedes-Benz Car Configurator API\n    baseURL: ''\n    tags: []\n    serviceName: Mercedes-Benz Car Configurator API\n    serviceCategory: API\n  - name: Mercedes-Benz Connect Your Business API\n    baseURL: ''\n    tags: []\n    serviceName: Mercedes-Benz Connect Your Business API\n    serviceCategory: API\n  - name: Mercedes-Benz Connect Your Fleet API\n    baseURL: ''\n    tags: []\n    serviceName: Mercedes-Benz Connect Your Fleet API\n    serviceCategory: API\n  - name: Mercedes-Benz Electric Vehicle Status 2.0 API\n    baseURL: ''\n    tags: []\n    serviceName: Mercedes-Benz Electric Vehicle Status 2.0 API\n    serviceCategory: API\n  - name: Mercedes-Benz Electric Vehicle Status 3.0 API\n    baseURL: ''\n \
  \   tags: []\n    serviceName: Mercedes-Benz Electric Vehicle Status 3.0 API\n    serviceCategory: API\n  - name: Mercedes-Benz Hazard Warnings API\n    baseURL: ''\n    tags: []\n    serviceName: Mercedes-Benz Hazard Warnings API\n    serviceCategory: API\n  - name: Mercedes-Benz Micro Weather API\n    baseURL: ''\n    tags: []\n    serviceName: Mercedes-Benz Micro Weather API\n    serviceCategory: API\n  - name: Mercedes-Benz Parking Analytics API\n    baseURL: ''\n    tags: []\n    serviceName: Mercedes-Benz Parking Analytics API\n    serviceCategory: API\n  - name: Mercedes-Benz Parking Monitoring API\n    baseURL: ''\n    tags: []\n    serviceName: Mercedes-Benz Parking Monitoring API\n    serviceCategory: API\n  - name: Mercedes-Benz Pay as You Drive 2.0 API\n    baseURL: ''\n    tags: []\n    serviceName: Mercedes-Benz Pay as You Drive 2.0 API\n    serviceCategory: API\n  - name: Mercedes-Benz Road Safety Hotspots API\n    baseURL: ''\n    tags: []\n    serviceName: Mercedes-Benz\
  \ Road Safety Hotspots API\n    serviceCategory: API\n  - name: Mercedes-Benz Surface Events API\n    baseURL: ''\n    tags: []\n    serviceName: Mercedes-Benz Surface Events API\n    serviceCategory: API\n  - name: Mercedes-Benz Traffic Signs API\n    baseURL: ''\n    tags: []\n    serviceName: Mercedes-Benz Traffic Signs API\n    serviceCategory: API\n  - name: Mercedes-Benz Vehicle Images API\n    baseURL: ''\n    tags: []\n    serviceName: Mercedes-Benz Vehicle Images API\n    serviceCategory: API\n  - name: Mercedes-Benz Vehicle Specification API\n    baseURL: ''\n    tags: []\n    serviceName: Mercedes-Benz Vehicle Specification API\n    serviceCategory: API\n  - name: Mercedes-Benz Vehicle Specification Fleet API\n    baseURL: ''\n    tags: []\n    serviceName: Mercedes-Benz Vehicle Specification Fleet API\n    serviceCategory: API\n  - name: Mercedes-Benz Vehicle Status 1.5 API\n    baseURL: ''\n    tags: []\n    serviceName: Mercedes-Benz Vehicle Status 1.5 API\n    serviceCategory:\
  \ API\n  - name: Mercedes-Benz Waviness API\n    baseURL: ''\n    tags: []\n    serviceName: Mercedes-Benz Waviness API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: info@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/mercedes-benz/refs/heads/main/finops/mercedes-benz-finops.yml
sources: []
specification: FinOps Framework
tags:
- Automobiles
- Cars
- Vehicles
- FinOps
- Cost Management
- FOCUS
---
