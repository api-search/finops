---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: air-quality-programmatic-apis-openapi.yml
  format: yaml
  label: AQICN Real-Time Air Quality API
  slug: air-quality-programmatic-apis
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/air-quality-programmatic-apis/refs/heads/main/openapi/air-quality-programmatic-apis-openapi.yml
- filename: aqicn-json-api-openapi.yaml
  format: yaml
  label: AQICN JSON Air Quality API
  slug: aqicn-json-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/air-quality-programmatic-apis/refs/heads/main/openapi/aqicn-json-api-openapi.yaml
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
description: FinOps framework definition for the Air Quality Programmatic APIs API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Air Quality Programmatic APIs
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Air Quality Programmatic APIs
  PublisherName: Air Quality Programmatic APIs
  ServiceCategory: Developer Tools / API
  ServiceName: Air Quality Programmatic APIs
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
name: Air Quality Programmatic Apis Finops
provider_name: Air Quality Programmatic APIs
provider_slug: air-quality-programmatic-apis
publisher_name: Air Quality Programmatic APIs
service_category: API
slug: air-quality-programmatic-apis-finops
source_filename: air-quality-programmatic-apis-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Air Quality Programmatic APIs\nproviderId: air-quality-programmatic-apis\npublisherName: Air Quality Programmatic APIs\nserviceCategory: API\ncreated: '2026-05-04'\nmodified: '2026-05-04'\ntags:\n  - Air Quality\n  - Environment\n  - EPA\n  - Open Data\n  - Public Health\n  - IoT\n  - Government Data\n  - Real-Time Data\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Air Quality Programmatic APIs API surface. Provides a\n  FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the\n  provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering,\
  \ product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n\
  \      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Air Quality Programmatic APIs\n  ServiceCategory: Developer Tools / API\n  ProviderName: Air Quality Programmatic APIs\n  PublisherName: Air Quality Programmatic APIs\n  InvoiceIssuerName: Air Quality Programmatic APIs\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n\
  \      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: AQICN Real-Time Air Quality API\n    baseURL: ''\n    tags:\n      - Air Quality\n      - AQI\n      - PM2.5\n      - EPA\n      - Environment\n      - Public Health\n      - Real-Time\n      - Open Data\n    serviceName: AQICN Real-Time Air Quality API\n    serviceCategory: API\n  - name: AQICN JSON Air Quality API\n    baseURL: ''\n    tags:\n      - Air Quality\n      - AQI\n      - PM2.5\n      - JSON\n      - Real-Time\n      - Forecast\n    serviceName: AQICN JSON Air Quality API\n    serviceCategory:\
  \ API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/air-quality-programmatic-apis/refs/heads/main/finops/air-quality-programmatic-apis-finops.yml
sources: []
specification: FinOps Framework
tags:
- Air Quality
- Environment
- EPA
- Open Data
- Public Health
- IoT
- Government Data
- Real-Time Data
- FinOps
- Cost Management
- FOCUS
---
