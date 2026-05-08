---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: openapi.json
  format: json
  label: SimCorp Dimension Data API
  slug: ''
  spec_type: OpenAPI
  url: https://api.simcorp.com/dimension/v1/openapi.json
- filename: openapi.json
  format: json
  label: SimCorp Dimension Integration API
  slug: ''
  spec_type: OpenAPI
  url: https://api.simcorp.com/dimension/integration/v1/openapi.json
- filename: openapi.json
  format: json
  label: SimCorp Dimension Analytics API
  slug: ''
  spec_type: OpenAPI
  url: https://api.simcorp.com/dimension/analytics/v1/openapi.json
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
description: FinOps framework definition for the SimCorp Dimension API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: SimCorp Dimension
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: SimCorp Dimension
  PublisherName: SimCorp Dimension
  ServiceCategory: Developer Tools / API
  ServiceName: SimCorp Dimension
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
name: Simcorp Dimension Finops
provider_name: SimCorp Dimension
provider_slug: simcorp-dimension
publisher_name: SimCorp Dimension
service_category: API
slug: simcorp-dimension-finops
source_filename: simcorp-dimension-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: SimCorp Dimension\nproviderId: simcorp-dimension\npublisherName: SimCorp Dimension\nserviceCategory: API\ncreated: '2026-05-04'\nmodified: '2026-05-04'\ntags:\n  - Accounting\n  - Asset Management\n  - Compliance\n  - Data Distribution\n  - Enterprise Software\n  - Financial Data\n  - Financial Technology\n  - Investment Management\n  - Portfolio Management\n  - Risk Management\n  - SimCorp One\n  - Streaming\n  - Trading\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the SimCorp Dimension API surface. Provides a FOCUS-aligned\n  mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n\
  \  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n\
  \      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: SimCorp Dimension\n  ServiceCategory: Developer Tools / API\n  ProviderName: SimCorp Dimension\n  PublisherName: SimCorp Dimension\n  InvoiceIssuerName: SimCorp Dimension\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit:\
  \ request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: SimCorp Dimension Data API\n    baseURL: https://api.simcorp.com/dimension/v1\n    tags:\n      - Asset Management\n      - Financial Services\n      - Investment Data\n      - Portfolio Management\n    serviceName: SimCorp Dimension Data API\n    serviceCategory: API\n  - name: SimCorp Dimension Integration API\n    baseURL: https://api.simcorp.com/dimension/integration/v1\n    tags:\n      - Data Synchronization\n      - Financial Services\n      -\
  \ Integration\n      - Workflow Automation\n    serviceName: SimCorp Dimension Integration API\n    serviceCategory: API\n  - name: SimCorp Dimension Analytics API\n    baseURL: https://api.simcorp.com/dimension/analytics/v1\n    tags:\n      - Analytics\n      - Performance\n      - Reporting\n      - Risk Management\n    serviceName: SimCorp Dimension Analytics API\n    serviceCategory: API\n  - name: SimCorp Dimension Web API\n    baseURL: https://api.simcorp.com/dimension/web/v1\n    tags:\n      - Investment Management\n      - Real-Time Data\n      - REST\n      - Web API\n    serviceName: SimCorp Dimension Web API\n    serviceCategory: API\n  - name: SimCorp Dimension Data Distribution API\n    baseURL: https://api.simcorp.com/dimension/datadistribution/v1\n    tags:\n      - Data Distribution\n      - Data Sharing\n      - Event Streaming\n      - Integration\n    serviceName: SimCorp Dimension Data Distribution API\n    serviceCategory: API\n  - name: SimCorp Dimension Streaming\
  \ API\n    baseURL: https://api.simcorp.com/dimension/streaming/v1\n    tags:\n      - Event-Driven\n      - Market Data\n      - Real-Time Data\n      - Streaming\n    serviceName: SimCorp Dimension Streaming API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n    url: https://apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/simcorp-dimension/refs/heads/main/finops/simcorp-dimension-finops.yml
sources: []
specification: FinOps Framework
tags:
- Accounting
- Asset Management
- Compliance
- Data Distribution
- Enterprise Software
- Financial Data
- Financial Technology
- Investment Management
- Portfolio Management
- Risk Management
- SimCorp One
- Streaming
- Trading
- FinOps
- Cost Management
- FOCUS
---
