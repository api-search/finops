---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: ice-consolidated-feed-api-openapi.yml
  format: yaml
  label: ICE Consolidated Feed API
  slug: consolidated-feed-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/intercontinental-exchange/refs/heads/main/openapi/ice-consolidated-feed-api-openapi.yml
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
description: FinOps framework definition for the Intercontinental Exchange API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Intercontinental Exchange
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Intercontinental Exchange
  PublisherName: Intercontinental Exchange
  ServiceCategory: Developer Tools / API
  ServiceName: Intercontinental Exchange
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
name: Intercontinental Exchange Finops
provider_name: Intercontinental Exchange
provider_slug: intercontinental-exchange
publisher_name: Intercontinental Exchange
service_category: API
slug: intercontinental-exchange-finops
source_filename: intercontinental-exchange-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Intercontinental Exchange\nproviderId: intercontinental-exchange\npublisherName: Intercontinental Exchange\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Commodities\n  - Financial Exchanges\n  - Market Data\n  - NYSE\n  - Trading\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Intercontinental Exchange API surface. Provides a FOCUS-aligned\n  mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name:\
  \ Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  -\
  \ name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Intercontinental Exchange\n  ServiceCategory: Developer Tools / API\n  ProviderName: Intercontinental Exchange\n  PublisherName: Intercontinental Exchange\n  InvoiceIssuerName: Intercontinental Exchange\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      -\
  \ consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: ICE Consolidated Feed API\n    baseURL: https://api.theice.com\n    tags:\n      - Exchanges\n      - Financial Data\n      - Market Data\n      - Real-Time Data\n      - Trading\n    serviceName: ICE Consolidated Feed API\n    serviceCategory: API\n  - name: ICE Data Services API\n    baseURL: https://idsportal.icedataservices.com\n    tags:\n      - Analytics\n      - Financial Services\n      - Market Data\n      - Reference Data\n    serviceName: ICE Data Services API\n    serviceCategory: API\n  - name: ICE Mortgage Technology Developer Portal\n    baseURL: https://api.mortgagetech.ice.com\n\
  \    tags:\n      - Financial Services\n      - Lending\n      - Mortgage\n      - Real Estate\n    serviceName: ICE Mortgage Technology Developer Portal\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: API Evangelist\n    email: info@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/intercontinental-exchange/refs/heads/main/finops/intercontinental-exchange-finops.yml
sources: []
specification: FinOps Framework
tags:
- Commodities
- Financial Exchanges
- Market Data
- NYSE
- Trading
- FinOps
- Cost Management
- FOCUS
---
