---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: salesforce-sales-cloud-rest-api-openapi.yml
  format: yaml
  label: Salesforce REST API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/salesforce-sales-cloud/refs/heads/main/openapi/salesforce-sales-cloud-rest-api-openapi.yml
- filename: salesforce-sales-cloud-bulk-api-openapi.yml
  format: yaml
  label: Bulk API 2.0
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/salesforce-sales-cloud/refs/heads/main/openapi/salesforce-sales-cloud-bulk-api-openapi.yml
- filename: salesforce-sales-cloud-platform-events-api-openapi.yml
  format: yaml
  label: Platform Events API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/salesforce-sales-cloud/refs/heads/main/openapi/salesforce-sales-cloud-platform-events-api-openapi.yml
- filename: salesforce-sales-cloud-analytics-api-openapi.yml
  format: yaml
  label: Analytics REST API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/salesforce-sales-cloud/refs/heads/main/openapi/salesforce-sales-cloud-analytics-api-openapi.yml
- filename: salesforce-sales-cloud-composite-api-openapi.yml
  format: yaml
  label: Salesforce Composite API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/salesforce-sales-cloud/refs/heads/main/openapi/salesforce-sales-cloud-composite-api-openapi.yml
- filename: salesforce-sales-cloud-graphql-api-openapi.yml
  format: yaml
  label: Salesforce GraphQL API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/salesforce-sales-cloud/refs/heads/main/openapi/salesforce-sales-cloud-graphql-api-openapi.yml
- filename: salesforce-sales-cloud-tooling-api-openapi.yml
  format: yaml
  label: Salesforce Tooling API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/salesforce-sales-cloud/refs/heads/main/openapi/salesforce-sales-cloud-tooling-api-openapi.yml
- filename: salesforce-sales-cloud-change-data-capture-api-openapi.yml
  format: yaml
  label: Salesforce Change Data Capture API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/salesforce-sales-cloud/refs/heads/main/openapi/salesforce-sales-cloud-change-data-capture-api-openapi.yml
- filename: salesforce-sales-cloud-connect-api-openapi.yml
  format: yaml
  label: Salesforce Connect REST API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/salesforce-sales-cloud/refs/heads/main/openapi/salesforce-sales-cloud-connect-api-openapi.yml
- filename: salesforce-sales-cloud-ui-api-openapi.yml
  format: yaml
  label: Salesforce User Interface API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/salesforce-sales-cloud/refs/heads/main/openapi/salesforce-sales-cloud-ui-api-openapi.yml
- filename: salesforce-sales-cloud-apex-rest-api-openapi.yml
  format: yaml
  label: Salesforce Apex REST API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/salesforce-sales-cloud/refs/heads/main/openapi/salesforce-sales-cloud-apex-rest-api-openapi.yml
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
description: FinOps framework definition for the Salesforce Sales Cloud API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Salesforce Sales Cloud
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Salesforce Sales Cloud
  PublisherName: Salesforce Sales Cloud
  ServiceCategory: Developer Tools / API
  ServiceName: Salesforce Sales Cloud
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
name: Salesforce Sales Cloud Finops
provider_name: Salesforce Sales Cloud
provider_slug: salesforce-sales-cloud
publisher_name: Salesforce Sales Cloud
service_category: API
slug: salesforce-sales-cloud-finops
source_filename: salesforce-sales-cloud-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Salesforce Sales Cloud\nproviderId: salesforce-sales-cloud\npublisherName: Salesforce Sales Cloud\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Cloud\n  - CRM\n  - Customer Management\n  - Enterprise\n  - Sales\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Salesforce Sales Cloud API surface. Provides a FOCUS-aligned\n  mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description:\
  \ Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n\
  \    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Salesforce Sales Cloud\n  ServiceCategory: Developer Tools / API\n  ProviderName: Salesforce Sales Cloud\n  PublisherName: Salesforce Sales Cloud\n  InvoiceIssuerName: Salesforce Sales Cloud\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description:\
  \ Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Salesforce REST API\n    baseURL: https://yourInstance.salesforce.com/services/data/v59.0\n    tags:\n      - CRUD\n      - Data\n      - Objects\n      - Records\n      - REST\n    serviceName: Salesforce REST API\n    serviceCategory: API\n  - name: Salesforce SOAP API\n    baseURL: https://yourInstance.salesforce.com/services/Soap/u/59.0\n    tags:\n      - Enterprise\n      - Integration\n      - SOAP\n      - XML\n    serviceName: Salesforce SOAP API\n    serviceCategory: API\n  - name: Bulk API 2.0\n    baseURL: https://yourInstance.salesforce.com/services/data/v59.0/jobs/ingest\n    tags:\n      - Async\n  \
  \    - Bulk\n      - Data Loading\n      - ETL\n    serviceName: Bulk API 2.0\n    serviceCategory: API\n  - name: Metadata API\n    baseURL: https://yourInstance.salesforce.com/services/Soap/m/59.0\n    tags:\n      - Configuration\n      - Customization\n      - Deployment\n      - Metadata\n    serviceName: Metadata API\n    serviceCategory: API\n  - name: Streaming API\n    baseURL: https://yourInstance.salesforce.com/cometd/59.0\n    tags:\n      - Events\n      - Push Notifications\n      - Real-Time\n      - Streaming\n    serviceName: Streaming API\n    serviceCategory: API\n  - name: Platform Events API\n    baseURL: https://yourInstance.salesforce.com/services/data/v59.0/sobjects\n    tags:\n      - Events\n      - Integration\n      - Messaging\n      - Pub/Sub\n    serviceName: Platform Events API\n    serviceCategory: API\n  - name: Analytics REST API\n    baseURL: https://yourInstance.salesforce.com/services/data/v59.0/analytics\n    tags:\n      - Analytics\n      - Business\
  \ Intelligence\n      - Dashboards\n      - Reports\n    serviceName: Analytics REST API\n    serviceCategory: API\n  - name: Salesforce Composite API\n    baseURL: https://yourInstance.salesforce.com/services/data/v59.0/composite\n    tags:\n      - Batch\n      - Composite\n      - Integration\n      - Performance\n    serviceName: Salesforce Composite API\n    serviceCategory: API\n  - name: Salesforce GraphQL API\n    baseURL: https://yourInstance.salesforce.com/services/data/v59.0/graphql\n    tags:\n      - Data Access\n      - GraphQL\n      - Query\n      - Schema\n    serviceName: Salesforce GraphQL API\n    serviceCategory: API\n  - name: Salesforce Tooling API\n    baseURL: https://yourInstance.salesforce.com/services/data/v59.0/tooling\n    tags:\n      - Apex\n      - Development\n      - Metadata\n      - Tooling\n    serviceName: Salesforce Tooling API\n    serviceCategory: API\n  - name: Salesforce Pub/Sub API\n    baseURL: https://yourInstance.salesforce.com\n    tags:\n\
  \      - Events\n      - gRPC\n      - Pub/Sub\n      - Real-Time\n    serviceName: Salesforce Pub/Sub API\n    serviceCategory: API\n  - name: Salesforce Change Data Capture API\n    baseURL: https://yourInstance.salesforce.com/services/data/v59.0\n    tags:\n      - Change Data Capture\n      - Events\n      - Real-Time\n      - Synchronization\n    serviceName: Salesforce Change Data Capture API\n    serviceCategory: API\n  - name: Salesforce Connect REST API\n    baseURL: https://yourInstance.salesforce.com/services/data/v59.0/connect\n    tags:\n      - Chatter\n      - Collaboration\n      - Connect\n      - Social\n    serviceName: Salesforce Connect REST API\n    serviceCategory: API\n  - name: Salesforce User Interface API\n    baseURL: https://yourInstance.salesforce.com/services/data/v59.0/ui-api\n    tags:\n      - Layouts\n      - Lightning\n      - Records\n      - User Interface\n    serviceName: Salesforce User Interface API\n    serviceCategory: API\n  - name: Salesforce\
  \ Apex REST API\n    baseURL: https://yourInstance.salesforce.com/services/apexrest\n    tags:\n      - Apex\n      - Custom Endpoints\n      - Development\n      - REST\n    serviceName: Salesforce Apex REST API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers: []\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/salesforce-sales-cloud/refs/heads/main/finops/salesforce-sales-cloud-finops.yml
sources: []
specification: FinOps Framework
tags:
- Cloud
- CRM
- Customer Management
- Enterprise
- Sales
- FinOps
- Cost Management
- FOCUS
---
