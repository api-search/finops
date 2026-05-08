---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: eodhd-eod-historical-data-openapi.yml
  format: yaml
  label: EODHD End-Of-Day Historical Data API
  slug: eod-historical-data-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/eodhd/refs/heads/main/openapi/eodhd-eod-historical-data-openapi.yml
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
description: FinOps framework definition for the EODHD API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: EODHD
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: EODHD
  PublisherName: EODHD
  ServiceCategory: Developer Tools / API
  ServiceName: EODHD
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
name: Eodhd Finops
provider_name: EODHD
provider_slug: eodhd
publisher_name: EODHD
service_category: API
slug: eodhd-finops
source_filename: eodhd-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: EODHD\nproviderId: eodhd\npublisherName: EODHD\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Financial\n  - Market Data\n  - Stock Options\n  - Stocks\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the EODHD API surface. Provides a FOCUS-aligned mapping for\n  cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment,\
  \ application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      -\
  \ FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: EODHD\n  ServiceCategory: Developer Tools / API\n  ProviderName: EODHD\n  PublisherName: EODHD\n  InvoiceIssuerName: EODHD\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n\
  \      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: EODHD End-Of-Day Historical Data API\n    baseURL: ''\n    tags:\n      - End Of Day\n      - Financial\n      - Historical Data\n      - Stocks\n    serviceName: EODHD End-Of-Day Historical Data API\n    serviceCategory: API\n  - name: EODHD Intraday Historical Data API\n    baseURL: ''\n    tags:\n      - Financial\n      - Historical Data\n      - Intraday\n      - Stocks\n    serviceName: EODHD Intraday Historical Data API\n    serviceCategory: API\n  - name: EODHD Live (Delayed) Stock Prices API\n    baseURL: ''\n    tags:\n      - Financial\n      - Live Data\n      - Real Time\n      - Stocks\n    serviceName: EODHD Live (Delayed) Stock Prices API\n    serviceCategory: API\n  - name: EODHD WebSockets Real-Time API\n    baseURL: ''\n    tags:\n\
  \      - Financial\n      - Real Time\n      - Streaming\n      - WebSockets\n    serviceName: EODHD WebSockets Real-Time API\n    serviceCategory: API\n  - name: EODHD Fundamental Data API\n    baseURL: ''\n    tags:\n      - Financial\n      - Fundamentals\n      - Stocks\n    serviceName: EODHD Fundamental Data API\n    serviceCategory: API\n  - name: EODHD Stock Options API\n    baseURL: ''\n    tags:\n      - Derivatives\n      - Financial\n      - Options\n    serviceName: EODHD Stock Options API\n    serviceCategory: API\n  - name: EODHD Technical Indicators API\n    baseURL: ''\n    tags:\n      - Analytics\n      - Financial\n      - Technical Indicators\n    serviceName: EODHD Technical Indicators API\n    serviceCategory: API\n  - name: EODHD Economic Events Calendar API\n    baseURL: ''\n    tags:\n      - Calendar\n      - Economic Data\n      - Financial\n    serviceName: EODHD Economic Events Calendar API\n    serviceCategory: API\n  - name: EODHD Financial News and Sentiment\
  \ API\n    baseURL: ''\n    tags:\n      - Financial\n      - News\n      - Sentiment\n    serviceName: EODHD Financial News and Sentiment API\n    serviceCategory: API\n  - name: EODHD Exchanges and Symbols API\n    baseURL: ''\n    tags:\n      - Exchanges\n      - Financial\n      - Reference Data\n      - Symbols\n    serviceName: EODHD Exchanges and Symbols API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/eodhd/refs/heads/main/finops/eodhd-finops.yml
sources: []
specification: FinOps Framework
tags:
- Financial
- Market Data
- Stock Options
- Stocks
- FinOps
- Cost Management
- FOCUS
---
