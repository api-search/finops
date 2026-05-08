---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: national-renewable-energy-laboratory-openapi.yml
  format: yaml
  label: NREL Developer Network
  slug: nrel-developer-network
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/national-renewable-energy-laboratory/refs/heads/main/openapi/national-renewable-energy-laboratory-openapi.yml
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
description: FinOps framework definition for the National Renewable Energy Laboratory API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: National Renewable Energy Laboratory
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: National Renewable Energy Laboratory
  PublisherName: National Renewable Energy Laboratory
  ServiceCategory: Developer Tools / API
  ServiceName: National Renewable Energy Laboratory
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
name: National Renewable Energy Laboratory Finops
provider_name: National Renewable Energy Laboratory
provider_slug: national-renewable-energy-laboratory
publisher_name: National Renewable Energy Laboratory
service_category: API
slug: national-renewable-energy-laboratory-finops
source_filename: national-renewable-energy-laboratory-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: National Renewable Energy Laboratory\nproviderId: national-renewable-energy-laboratory\npublisherName: National Renewable Energy Laboratory\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Energy\n  - Renewable Energy\n  - Federal Government\n  - Climate\n  - Research\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the National Renewable Energy Laboratory API surface. Provides\n  a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across\n  the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and\
  \ finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud\
  \ Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: National Renewable Energy Laboratory\n  ServiceCategory: Developer Tools / API\n  ProviderName: National Renewable Energy Laboratory\n  PublisherName: National Renewable Energy Laboratory\n  InvoiceIssuerName: National Renewable Energy Laboratory\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation:\
  \ sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: NREL Developer Network\n    baseURL: https://developer.nrel.gov/api/\n    tags:\n      - Energy\n      - Renewable Energy\n    serviceName: NREL Developer Network\n    serviceCategory: API\n  - name: Alternative Fuel Stations\n    baseURL: https://developer.nrel.gov/api/alt-fuel-stations/v1/\n    tags:\n      - Transportation\n      - Alternative Fuel\n    serviceName: Alternative Fuel Stations\n    serviceCategory: API\n  - name: PVWatts\n    baseURL: https://developer.nrel.gov/api/pvwatts/v8/\n\
  \    tags:\n      - Solar\n      - Modeling\n    serviceName: PVWatts\n    serviceCategory: API\n  - name: Utility Rates\n    baseURL: https://developer.nrel.gov/api/utility_rates/v3/\n    tags:\n      - Electricity\n      - Rates\n    serviceName: Utility Rates\n    serviceCategory: API\n  - name: Solar Resource Data\n    baseURL: https://developer.nrel.gov/api/solar/solar_resource/v1/\n    tags:\n      - Solar\n      - Climate\n    serviceName: Solar Resource Data\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/national-renewable-energy-laboratory/refs/heads/main/finops/national-renewable-energy-laboratory-finops.yml
sources: []
specification: FinOps Framework
tags:
- Energy
- Renewable Energy
- Federal Government
- Climate
- Research
- FinOps
- Cost Management
- FOCUS
---
