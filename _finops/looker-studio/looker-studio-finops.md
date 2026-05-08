---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: looker-studio-api-openapi.yml
  format: yaml
  label: Looker Studio API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/looker-studio/refs/heads/main/openapi/looker-studio-api-openapi.yml
- filename: looker-studio-linking-api-openapi.yml
  format: yaml
  label: Looker Studio Linking API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/looker-studio/refs/heads/main/openapi/looker-studio-linking-api-openapi.yml
- filename: looker-studio-embedding-api-openapi.yml
  format: yaml
  label: Looker Studio Embedding API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/looker-studio/refs/heads/main/openapi/looker-studio-embedding-api-openapi.yml
- filename: looker-studio-community-connector-api-openapi.yml
  format: yaml
  label: Looker Studio Community Connector API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/looker-studio/refs/heads/main/openapi/looker-studio-community-connector-api-openapi.yml
- filename: looker-studio-community-visualization-api-openapi.yml
  format: yaml
  label: Looker Studio Community Visualization API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/looker-studio/refs/heads/main/openapi/looker-studio-community-visualization-api-openapi.yml
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
description: FinOps framework definition for the Looker Studio API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Looker Studio
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Looker Studio
  PublisherName: Looker Studio
  ServiceCategory: Developer Tools / API
  ServiceName: Looker Studio
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
name: Looker Studio Finops
provider_name: Looker Studio
provider_slug: looker-studio
publisher_name: Looker Studio
service_category: API
slug: looker-studio-finops
source_filename: looker-studio-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Looker Studio\nproviderId: looker-studio\npublisherName: Looker Studio\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Analytics\n  - Business Intelligence\n  - Dashboards\n  - Data Visualization\n  - Google\n  - Reports\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Looker Studio API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description:\
  \ Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n\
  \    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Looker Studio\n  ServiceCategory: Developer Tools / API\n  ProviderName: Looker Studio\n  PublisherName: Looker Studio\n  InvoiceIssuerName: Looker Studio\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network\
  \ in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Looker Studio API\n    baseURL: https://datastudio.googleapis.com/v1\n    tags:\n      - Assets\n      - Automation\n      - Data Sources\n      - Permissions\n      - Reports\n    serviceName: Looker Studio API\n    serviceCategory: API\n  - name: Looker Studio Linking API\n    baseURL: https://lookerstudio.google.com\n    tags:\n      - Data Sources\n      - Integration\n      - Linking\n      - Reports\n      - URL Parameters\n    serviceName: Looker Studio Linking API\n    serviceCategory: API\n  - name: Looker Studio Embedding API\n    baseURL: https://lookerstudio.google.com/embed\n    tags:\n      - Embedding\n      - Iframe\n      - Integration\n\
  \      - Reports\n      - Sharing\n    serviceName: Looker Studio Embedding API\n    serviceCategory: API\n  - name: Looker Studio Community Connector API\n    baseURL: https://datastudio.google.com/datasources/create\n    tags:\n      - Apps Script\n      - Connectors\n      - Custom Integration\n      - Data Sources\n      - ETL\n    serviceName: Looker Studio Community Connector API\n    serviceCategory: API\n  - name: Looker Studio Community Visualization API\n    baseURL: https://lookerstudio.google.com/visualization\n    tags:\n      - Components\n      - Custom Charts\n      - Data Visualization\n      - JavaScript\n      - Visualizations\n    serviceName: Looker Studio Community Visualization API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/looker-studio/refs/heads/main/finops/looker-studio-finops.yml
sources: []
specification: FinOps Framework
tags:
- Analytics
- Business Intelligence
- Dashboards
- Data Visualization
- Google
- Reports
- FinOps
- Cost Management
- FOCUS
---
