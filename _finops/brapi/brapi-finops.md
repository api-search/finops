---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: brapi-openapi.yml
  format: yaml
  label: brapi Quotes API
  slug: quotes-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/brapi/refs/heads/main/openapi/brapi-openapi.yml
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
description: FinOps framework definition for the brapi API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: brapi
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: brapi
  PublisherName: brapi
  ServiceCategory: Developer Tools / API
  ServiceName: brapi
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
name: Brapi Finops
provider_name: brapi
provider_slug: brapi
publisher_name: brapi
service_category: API
slug: brapi-finops
source_filename: brapi-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: brapi\nproviderId: brapi\npublisherName: brapi\nserviceCategory: API\ncreated: '2026-05-04'\nmodified: '2026-05-04'\ntags:\n  - Finance\n  - Brazilian Financial Data\n  - Stock Market\n  - Investments\n  - Economic Indicators\n  - Cryptocurrency\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the brapi API surface. Provides a FOCUS-aligned mapping for\n  cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every\
  \ chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n   \
  \ capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: brapi\n  ServiceCategory: Developer Tools / API\n  ProviderName: brapi\n  PublisherName: brapi\n  InvoiceIssuerName: brapi\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n  \
  \  aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: brapi Quotes API\n    baseURL: ''\n    tags:\n      - Stock Quotes\n      - B3\n      - Real-Time Data\n      - Historical Data\n    serviceName: brapi Quotes API\n    serviceCategory: API\n  - name: brapi Fundamentals API\n    baseURL: ''\n    tags:\n      - Fundamentals\n      - Balance Sheet\n      - Income Statement\n      - Financial Statements\n    serviceName: brapi Fundamentals API\n    serviceCategory: API\n  - name: brapi Dividends API\n    baseURL: ''\n    tags:\n      - Dividends\n      - Distributions\n      - Corporate Actions\n    serviceName: brapi Dividends API\n    serviceCategory: API\n  - name: brapi Cryptocurrency API\n    baseURL: ''\n    tags:\n      - Cryptocurrency\n\
  \      - BRL\n      - Digital Assets\n    serviceName: brapi Cryptocurrency API\n    serviceCategory: API\n  - name: brapi Exchange Rates API\n    baseURL: ''\n    tags:\n      - Foreign Exchange\n      - Currency\n      - BRL\n    serviceName: brapi Exchange Rates API\n    serviceCategory: API\n  - name: brapi Economic Indicators API\n    baseURL: ''\n    tags:\n      - Inflation\n      - Interest Rates\n      - Economic Data\n      - SELIC\n    serviceName: brapi Economic Indicators API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: info@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/brapi/refs/heads/main/finops/brapi-finops.yml
sources: []
specification: FinOps Framework
tags:
- Finance
- Brazilian Financial Data
- Stock Market
- Investments
- Economic Indicators
- Cryptocurrency
- FinOps
- Cost Management
- FOCUS
---
