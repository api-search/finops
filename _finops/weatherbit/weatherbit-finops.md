---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: weatherbit-current-weather-openapi-original.yml
  format: yaml
  label: Weatherbit Current Weather API
  slug: weatherbit-current-weather-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/weatherbit/refs/heads/main/openapi/weatherbit-current-weather-openapi-original.yml
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
description: FinOps framework definition for the Weatherbit API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Weatherbit
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Weatherbit
  PublisherName: Weatherbit
  ServiceCategory: Developer Tools / API
  ServiceName: Weatherbit
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
name: Weatherbit Finops
provider_name: Weatherbit
provider_slug: weatherbit
publisher_name: Weatherbit
service_category: API
slug: weatherbit-finops
source_filename: weatherbit-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Weatherbit\nproviderId: weatherbit\npublisherName: Weatherbit\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Weather\n  - Forecasting\n  - Historical Data\n  - Air Quality\n  - Alerts\n  - Agricultural Weather\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Weatherbit API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every\
  \ chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n   \
  \ capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Weatherbit\n  ServiceCategory: Developer Tools / API\n  ProviderName: Weatherbit\n  PublisherName: Weatherbit\n  InvoiceIssuerName: Weatherbit\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n\
  \    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Weatherbit Current Weather API\n    baseURL: https://api.weatherbit.io/v2.0\n    tags:\n      - Weather\n      - Current Conditions\n      - Observations\n    serviceName: Weatherbit Current Weather API\n    serviceCategory: API\n  - name: Weatherbit Severe Weather Alerts API\n    baseURL: https://api.weatherbit.io/v2.0\n    tags:\n      - Weather\n      - Alerts\n      - Emergency\n    serviceName: Weatherbit Severe Weather Alerts API\n    serviceCategory: API\n  - name: Weatherbit Weather Forecast API\n    baseURL: https://api.weatherbit.io/v2.0\n    tags:\n      - Weather\n      - Forecasting\n      - Daily\n      - Hourly\n    serviceName: Weatherbit Weather Forecast\
  \ API\n    serviceCategory: API\n  - name: Weatherbit Historical Weather API\n    baseURL: https://api.weatherbit.io/v2.0\n    tags:\n      - Weather\n      - Historical\n      - Climate\n    serviceName: Weatherbit Historical Weather API\n    serviceCategory: API\n  - name: Weatherbit Ag-Weather API\n    baseURL: https://api.weatherbit.io/v2.0\n    tags:\n      - Weather\n      - Agriculture\n      - Evapotranspiration\n    serviceName: Weatherbit Ag-Weather API\n    serviceCategory: API\n  - name: Weatherbit Air Quality API\n    baseURL: https://api.weatherbit.io/v2.0\n    tags:\n      - Air Quality\n      - AQI\n      - Environment\n    serviceName: Weatherbit Air Quality API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/weatherbit/refs/heads/main/finops/weatherbit-finops.yml
sources: []
specification: FinOps Framework
tags:
- Weather
- Forecasting
- Historical Data
- Air Quality
- Alerts
- Agricultural Weather
- FinOps
- Cost Management
- FOCUS
---
