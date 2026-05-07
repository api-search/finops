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
description: FinOps framework definition for the Data Commons API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Data Commons
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Data Commons
  PublisherName: Data Commons
  ServiceCategory: Developer Tools / API
  ServiceName: Data Commons
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
name: Data Commons Finops
provider_name: Data Commons
provider_slug: data-commons
publisher_name: Data Commons
service_category: API
slug: data-commons-finops
source_filename: data-commons-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Data Commons\nproviderId: data-commons\npublisherName: Data Commons\nserviceCategory: API\ncreated: '2026-05-04'\nmodified: '2026-05-04'\ntags:\n  - Data Commons\n  - Knowledge Graph\n  - Open Data\n  - Public Data\n  - Statistics\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Data Commons API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable\
  \ API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n\
  \      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Data Commons\n  ServiceCategory: Developer Tools / API\n  ProviderName: Data Commons\n  PublisherName: Data Commons\n  InvoiceIssuerName: Data Commons\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit:\
  \ GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Data Commons REST API V2\n    baseURL: ''\n    tags:\n      - Knowledge Graph\n      - REST\n      - Statistics\n    serviceName: Data Commons REST API V2\n    serviceCategory: API\n  - name: Data Commons Python Client\n    baseURL: ''\n    tags:\n      - Pandas\n      - Python\n      - SDK\n    serviceName: Data Commons Python Client\n    serviceCategory: API\n  - name: Data Commons Google Sheets\n    baseURL: ''\n    tags:\n      - Google Sheets\n      - Spreadsheets\n    serviceName: Data Commons Google Sheets\n    serviceCategory: API\n  - name: Data Commons Web Components\n    baseURL: ''\n    tags:\n      - JavaScript\n      - Visualization\n      - Web Components\n \
  \   serviceName: Data Commons Web Components\n    serviceCategory: API\n  - name: Data Commons BigQuery\n    baseURL: ''\n    tags:\n      - BigQuery\n      - SQL\n    serviceName: Data Commons BigQuery\n    serviceCategory: API\n  - name: Data Commons MCP Server\n    baseURL: ''\n    tags:\n      - AI Agents\n      - MCP\n      - Natural Language\n    serviceName: Data Commons MCP Server\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/data-commons/refs/heads/main/finops/data-commons-finops.yml
sources: []
specification: FinOps Framework
tags:
- Data Commons
- Knowledge Graph
- Open Data
- Public Data
- Statistics
- FinOps
- Cost Management
- FOCUS
---
