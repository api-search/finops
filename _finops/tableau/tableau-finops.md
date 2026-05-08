---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: tableau-rest-api-openapi.yml
  format: yaml
  label: Tableau REST API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/tableau/refs/heads/main/openapi/tableau-rest-api-openapi.yml
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
description: FinOps framework definition for the Tableau API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Tableau
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Tableau
  PublisherName: Tableau
  ServiceCategory: Developer Tools / API
  ServiceName: Tableau
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
name: Tableau Finops
provider_name: Tableau
provider_slug: tableau
publisher_name: Tableau
service_category: API
slug: tableau-finops
source_filename: tableau-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Tableau\nproviderId: tableau\npublisherName: Tableau\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Analytics\n  - Business Intelligence\n  - Dashboards\n  - Data Visualization\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Tableau API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming\
  \ team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice\
  \ Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Tableau\n  ServiceCategory: Developer Tools / API\n  ProviderName: Tableau\n  PublisherName: Tableau\n  InvoiceIssuerName: Tableau\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n\
  \      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Tableau REST API\n    baseURL: https://[server]/api/[api-version]\n    tags:\n      - Data Sources\n      - REST\n      - Server Management\n      - Sites\n      - Workbooks\n    serviceName: Tableau REST API\n    serviceCategory: API\n  - name: Tableau Metadata API\n    baseURL: https://[server]/api/metadata/graphql\n    tags:\n      - Data Catalog\n      - GraphQL\n      - Lineage\n      - Metadata\n    serviceName: Tableau Metadata API\n    serviceCategory: API\n  - name: Tableau Hyper API\n    baseURL: https://github.com/tableau/hyper-api-samples\n    tags:\n      - Data Files\n      - ETL\n      - Extracts\n      - Hyper\n    serviceName: Tableau Hyper API\n    serviceCategory: API\n  - name: Tableau Embedding API\n\
  \    baseURL: https://[server]\n    tags:\n      - Embedding\n      - JavaScript\n      - Visualization\n      - Web Components\n    serviceName: Tableau Embedding API\n    serviceCategory: API\n  - name: Tableau Document API\n    baseURL: https://github.com/tableau/document-api-python\n    tags:\n      - Automation\n      - Data Sources\n      - Python\n      - Workbooks\n    serviceName: Tableau Document API\n    serviceCategory: API\n  - name: Tableau Server Client (Python)\n    baseURL: https://github.com/tableau/server-client-python\n    tags:\n      - Python\n      - REST\n      - SDK\n      - Wrapper\n    serviceName: Tableau Server Client (Python)\n    serviceCategory: API\n  - name: Tableau Extensions API\n    baseURL: https://[server]\n    tags:\n      - Dashboard Extensions\n      - Extensibility\n      - JavaScript\n      - Viz Extensions\n      - Web Components\n    serviceName: Tableau Extensions API\n    serviceCategory: API\n  - name: Tableau Web Data Connector\n    baseURL:\
  \ https://[server]\n    tags:\n      - Connectors\n      - Data Integration\n      - HTTP\n      - JavaScript\n    serviceName: Tableau Web Data Connector\n    serviceCategory: API\n  - name: Tableau Connector SDK\n    baseURL: https://github.com/tableau/connector-plugin-sdk\n    tags:\n      - Connectors\n      - Custom Connectors\n      - JDBC\n      - ODBC\n      - SDK\n    serviceName: Tableau Connector SDK\n    serviceCategory: API\n  - name: Tableau Analytics Extensions API\n    baseURL: https://[server]\n    tags:\n      - Analytics\n      - Data Science\n      - Machine Learning\n      - Python\n      - R\n    serviceName: Tableau Analytics Extensions API\n    serviceCategory: API\n  - name: Tableau Webhooks\n    baseURL: https://[server]/api/[api-version]\n    tags:\n      - Automation\n      - Events\n      - Notifications\n      - Webhooks\n    serviceName: Tableau Webhooks\n    serviceCategory: API\n  - name: Tableau VizQL Data Service\n    baseURL: https://[server]/api/v1\n\
  \    tags:\n      - Data Access\n      - Headless\n      - Query\n      - REST\n    serviceName: Tableau VizQL Data Service\n    serviceCategory: API\n  - name: Tableau Pulse API\n    baseURL: https://[server]/api/[api-version]\n    tags:\n      - Analytics\n      - Insights\n      - Metrics\n      - Pulse\n    serviceName: Tableau Pulse API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - name: Tableau\n    email: developers@tableau.com\n    url: https://www.tableau.com\n  - name: Kin Lane\n    email: kin@apievangelist.com\n    url: https://apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/tableau/refs/heads/main/finops/tableau-finops.yml
sources: []
specification: FinOps Framework
tags:
- Analytics
- Business Intelligence
- Dashboards
- Data Visualization
- FinOps
- Cost Management
- FOCUS
---
