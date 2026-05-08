---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: salesforce-rest-api-openapi.json
  format: json
  label: Salesforce REST API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/salesforce-automation/refs/heads/main/openapi/salesforce-rest-api-openapi.json
- filename: salesforce-bulk-api-openapi.json
  format: json
  label: Salesforce Bulk API 2.0
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/salesforce-automation/refs/heads/main/openapi/salesforce-bulk-api-openapi.json
- filename: salesforce-streaming-api-openapi.json
  format: json
  label: Salesforce Streaming API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/salesforce-automation/refs/heads/main/openapi/salesforce-streaming-api-openapi.json
- filename: salesforce-platform-events-api-openapi.json
  format: json
  label: Salesforce Platform Events API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/salesforce-automation/refs/heads/main/openapi/salesforce-platform-events-api-openapi.json
- filename: salesforce-analytics-api-openapi.json
  format: json
  label: Salesforce Analytics API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/salesforce-automation/refs/heads/main/openapi/salesforce-analytics-api-openapi.json
- filename: salesforce-tooling-api-openapi.json
  format: json
  label: Salesforce Tooling API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/salesforce-automation/refs/heads/main/openapi/salesforce-tooling-api-openapi.json
- filename: salesforce-connect-rest-api-openapi.json
  format: json
  label: Salesforce Connect REST API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/salesforce-automation/refs/heads/main/openapi/salesforce-connect-rest-api-openapi.json
- filename: salesforce-change-data-capture-api-openapi.json
  format: json
  label: Salesforce Change Data Capture API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/salesforce-automation/refs/heads/main/openapi/salesforce-change-data-capture-api-openapi.json
- filename: salesforce-invocable-actions-api-openapi.json
  format: json
  label: Salesforce Invocable Actions API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/salesforce-automation/refs/heads/main/openapi/salesforce-invocable-actions-api-openapi.json
- filename: salesforce-composite-api-openapi.json
  format: json
  label: Salesforce Composite API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/salesforce-automation/refs/heads/main/openapi/salesforce-composite-api-openapi.json
- filename: salesforce-apex-rest-api-openapi.json
  format: json
  label: Salesforce Apex REST API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/salesforce-automation/refs/heads/main/openapi/salesforce-apex-rest-api-openapi.json
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
description: FinOps framework definition for the Salesforce Automation API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Salesforce Automation
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Salesforce Automation
  PublisherName: Salesforce Automation
  ServiceCategory: Developer Tools / API
  ServiceName: Salesforce Automation
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
name: Salesforce Automation Finops
provider_name: Salesforce Automation
provider_slug: salesforce-automation
publisher_name: Salesforce Automation
service_category: API
slug: salesforce-automation-finops
source_filename: salesforce-automation-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Salesforce Automation\nproviderId: salesforce-automation\npublisherName: Salesforce Automation\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Automation\n  - Cloud\n  - CRM\n  - Enterprise\n  - Sales\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Salesforce Automation API surface. Provides a FOCUS-aligned\n  mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag\
  \ every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n\
  \    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Salesforce Automation\n  ServiceCategory: Developer Tools / API\n  ProviderName: Salesforce Automation\n  PublisherName: Salesforce Automation\n  InvoiceIssuerName: Salesforce Automation\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description:\
  \ Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Salesforce REST API\n    baseURL: https://yourInstance.salesforce.com/services/data\n    tags:\n      - CRUD\n      - Data\n      - REST\n    serviceName: Salesforce REST API\n    serviceCategory: API\n  - name: Salesforce SOAP API\n    baseURL: https://yourInstance.salesforce.com/services/Soap/c\n    tags:\n      - Enterprise\n      - Integration\n      - SOAP\n    serviceName: Salesforce SOAP API\n    serviceCategory: API\n  - name: Salesforce Bulk API 2.0\n    baseURL: https://yourInstance.salesforce.com/services/data/v63.0/jobs\n    tags:\n      - Async\n      - Bulk\n      - ETL\n    serviceName: Salesforce Bulk\
  \ API 2.0\n    serviceCategory: API\n  - name: Salesforce Metadata API\n    baseURL: https://yourInstance.salesforce.com/services/Soap/m\n    tags:\n      - Deployment\n      - DevOps\n      - Metadata\n    serviceName: Salesforce Metadata API\n    serviceCategory: API\n  - name: Salesforce Streaming API\n    baseURL: https://yourInstance.salesforce.com/cometd\n    tags:\n      - Events\n      - Push\n      - Real-Time\n      - Streaming\n    serviceName: Salesforce Streaming API\n    serviceCategory: API\n  - name: Salesforce Platform Events API\n    baseURL: https://yourInstance.salesforce.com/services/data/v63.0/sobjects\n    tags:\n      - Events\n      - Integration\n      - Pub/Sub\n    serviceName: Salesforce Platform Events API\n    serviceCategory: API\n  - name: Salesforce Analytics API\n    baseURL: https://yourInstance.salesforce.com/services/data/v63.0/wave\n    tags:\n      - Analytics\n      - Dashboards\n      - Reports\n    serviceName: Salesforce Analytics API\n    serviceCategory:\
  \ API\n  - name: Salesforce Tooling API\n    baseURL: https://yourInstance.salesforce.com/services/data/v63.0/tooling\n    tags:\n      - Debugging\n      - Development\n      - Tooling\n    serviceName: Salesforce Tooling API\n    serviceCategory: API\n  - name: Salesforce Connect REST API\n    baseURL: https://yourInstance.salesforce.com/services/data/v63.0/connect\n    tags:\n      - Chatter\n      - Collaboration\n      - Connect\n      - Social\n    serviceName: Salesforce Connect REST API\n    serviceCategory: API\n  - name: Salesforce Pub/Sub API\n    baseURL: https://api.pubsub.salesforce.com:7443\n    tags:\n      - Events\n      - gRPC\n      - Pub/Sub\n      - Real-Time\n      - Streaming\n    serviceName: Salesforce Pub/Sub API\n    serviceCategory: API\n  - name: Salesforce GraphQL API\n    baseURL: https://yourInstance.salesforce.com/services/data/v63.0/graphql\n    tags:\n      - Data\n      - GraphQL\n      - Query\n    serviceName: Salesforce GraphQL API\n    serviceCategory:\
  \ API\n  - name: Salesforce Change Data Capture API\n    baseURL: https://yourInstance.salesforce.com/services/data/v63.0/sobjects\n    tags:\n      - CDC\n      - Change Data Capture\n      - Events\n      - Real-Time\n      - Synchronization\n    serviceName: Salesforce Change Data Capture API\n    serviceCategory: API\n  - name: Salesforce Invocable Actions API\n    baseURL: https://yourInstance.salesforce.com/services/data/v63.0/actions\n    tags:\n      - Actions\n      - Automation\n      - Flows\n      - Invocable\n    serviceName: Salesforce Invocable Actions API\n    serviceCategory: API\n  - name: Salesforce Composite API\n    baseURL: https://yourInstance.salesforce.com/services/data/v63.0/composite\n    tags:\n      - Batch\n      - Composite\n      - Performance\n      - REST\n    serviceName: Salesforce Composite API\n    serviceCategory: API\n  - name: Salesforce Apex REST API\n    baseURL: https://yourInstance.salesforce.com/services/apexrest\n    tags:\n      - Apex\n\
  \      - Custom Endpoints\n      - Development\n      - REST\n    serviceName: Salesforce Apex REST API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n    url: https://apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/salesforce-automation/refs/heads/main/finops/salesforce-automation-finops.yml
sources: []
specification: FinOps Framework
tags:
- Automation
- Cloud
- CRM
- Enterprise
- Sales
- FinOps
- Cost Management
- FOCUS
---
