---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: OpenAPI_3_0
  format: yaml
  label: Boomi Platform REST API
  slug: platform-rest-api
  spec_type: OpenAPI
  url: https://developer.boomi.com/docs/APIs/PlatformAPI/Introduction/OpenAPI_3_0
- filename: OpenAPI_3_0
  format: yaml
  label: Boomi Platform Partner API
  slug: platform-partner-api
  spec_type: OpenAPI
  url: https://developer.boomi.com/docs/APIs/PlatformAPI/Introduction/OpenAPI_3_0
- filename: boomi-datahub-api-openapi.yml
  format: yaml
  label: Boomi DataHub API
  slug: datahub-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/boomi/refs/heads/main/openapi/boomi-datahub-api-openapi.yml
- filename: boomi-event-streams-openapi.yml
  format: yaml
  label: Boomi Event Streams REST API
  slug: event-streams-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/boomi/refs/heads/main/openapi/boomi-event-streams-openapi.yml
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
description: FinOps framework definition for the Boomi API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Boomi
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Boomi
  PublisherName: Boomi
  ServiceCategory: Developer Tools / API
  ServiceName: Boomi
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
name: Boomi Finops
provider_name: Boomi
provider_slug: boomi
publisher_name: Boomi
service_category: API
slug: boomi-finops
source_filename: boomi-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Boomi\nproviderId: boomi\npublisherName: Boomi\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - AI Agents\n  - Automation\n  - B2B\n  - Data Integration\n  - EDI\n  - Integrations\n  - Management\n  - MFT\n  - Platform\n  - Workflows\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Boomi API surface. Provides a FOCUS-aligned mapping for\n  cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description:\
  \ Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n\
  \    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Boomi\n  ServiceCategory: Developer Tools / API\n  ProviderName: Boomi\n  PublisherName: Boomi\n  InvoiceIssuerName: Boomi\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n\
  \    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Boomi\n    baseURL: ''\n    tags: []\n    serviceName: Boomi\n    serviceCategory: API\n  - name: Boomi Platform REST API\n    baseURL: ''\n    tags:\n      - Integration\n      - Platform\n      - REST\n    serviceName: Boomi Platform REST API\n    serviceCategory: API\n  - name: Boomi Platform Partner API\n    baseURL: ''\n    tags:\n      - Partners\n      - Platform\n      - REST\n    serviceName: Boomi Platform Partner API\n    serviceCategory: API\n  - name: Boomi API Management API\n    baseURL: ''\n    tags:\n      - API Management\n      - GraphQL\n      - REST\n      - SOAP\n    serviceName: Boomi API Management API\n    serviceCategory: API\n  - name: Boomi DataHub API\n\
  \    baseURL: ''\n    tags:\n      - Data Hub\n      - Master Data\n      - REST\n    serviceName: Boomi DataHub API\n    serviceCategory: API\n  - name: Boomi Event Streams REST API\n    baseURL: ''\n    tags:\n      - Events\n      - Messaging\n      - REST\n      - Streaming\n    serviceName: Boomi Event Streams REST API\n    serviceCategory: API\n  - name: Boomi Flow API\n    baseURL: ''\n    tags:\n      - Automation\n      - Low-Code\n      - REST\n      - Workflows\n    serviceName: Boomi Flow API\n    serviceCategory: API\n  - name: Boomi Connector Deployment API\n    baseURL: ''\n    tags:\n      - Connectors\n      - Deployment\n      - REST\n      - SDK\n    serviceName: Boomi Connector Deployment API\n    serviceCategory: API\n  - name: Boomi Platform SOAP API\n    baseURL: ''\n    tags:\n      - Integration\n      - Platform\n      - SOAP\n    serviceName: Boomi Platform SOAP API\n    serviceCategory: API\n  - name: Boomi MFT API\n    baseURL: ''\n    tags:\n      - Managed\
  \ File Transfer\n      - MFT\n      - REST\n      - SOAP\n    serviceName: Boomi MFT API\n    serviceCategory: API\n  - name: Boomi API Gateway GraphQL API\n    baseURL: ''\n    tags:\n      - API Gateway\n      - API Management\n      - GraphQL\n    serviceName: Boomi API Gateway GraphQL API\n    serviceCategory: API\n  - name: Boomi Agent Control Tower GraphQL API\n    baseURL: ''\n    tags:\n      - AI Agents\n      - Governance\n      - GraphQL\n    serviceName: Boomi Agent Control Tower GraphQL API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/boomi/refs/heads/main/finops/boomi-finops.yml
sources: []
specification: FinOps Framework
tags:
- AI Agents
- Automation
- B2B
- Data Integration
- EDI
- Integrations
- Management
- MFT
- Platform
- Workflows
- FinOps
- Cost Management
- FOCUS
---
