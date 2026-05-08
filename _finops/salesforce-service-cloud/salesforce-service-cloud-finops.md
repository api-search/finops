---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: resources_list.htm
  format: yaml
  label: Salesforce Service Cloud REST API
  slug: ''
  spec_type: OpenAPI
  url: https://developer.salesforce.com/docs/atlas.en-us.api_rest.meta/api_rest/resources_list.htm
- filename: salesforce-streaming-api-asyncapi.yml
  format: yaml
  label: Service Cloud Streaming API
  slug: ''
  spec_type: AsyncAPI
  url: https://raw.githubusercontent.com/api-evangelist/salesforce-service-cloud/refs/heads/main/asyncapi/salesforce-streaming-api-asyncapi.yml
- filename: salesforce-live-agent-openapi.yml
  format: yaml
  label: Live Agent REST API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/salesforce-service-cloud/refs/heads/main/openapi/salesforce-live-agent-openapi.yml
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
description: FinOps framework definition for the Salesforce Service Cloud API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Salesforce Service Cloud
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Salesforce Service Cloud
  PublisherName: Salesforce Service Cloud
  ServiceCategory: Developer Tools / API
  ServiceName: Salesforce Service Cloud
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
name: Salesforce Service Cloud Finops
provider_name: Salesforce Service Cloud
provider_slug: salesforce-service-cloud
publisher_name: Salesforce Service Cloud
service_category: API
slug: salesforce-service-cloud-finops
source_filename: salesforce-service-cloud-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Salesforce Service Cloud\nproviderId: salesforce-service-cloud\npublisherName: Salesforce Service Cloud\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Case Management\n  - CRM\n  - Customer Service\n  - Help Desk\n  - Support\n  - Ticketing\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Salesforce Service Cloud API surface. Provides a FOCUS-aligned\n  mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n\
  \  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and\
  \ SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Salesforce Service Cloud\n  ServiceCategory: Developer Tools / API\n  ProviderName: Salesforce Service Cloud\n  PublisherName: Salesforce Service Cloud\n  InvoiceIssuerName: Salesforce Service Cloud\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n\
  \      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Salesforce Service Cloud REST API\n    baseURL: https://yourInstance.salesforce.com/services/data/v59.0/\n    tags:\n      - Accounts\n      - Cases\n      - Contacts\n      - REST\n    serviceName: Salesforce Service Cloud REST API\n    serviceCategory: API\n  - name: Salesforce Service Cloud SOAP API\n    baseURL: https://yourInstance.salesforce.com/services/Soap/c/59.0/\n    tags:\n      - Enterprise\n      - Integration\n      - SOAP\n    serviceName: Salesforce Service Cloud SOAP API\n    serviceCategory: API\n  - name: Service Cloud Streaming API\n    baseURL:\
  \ https://yourInstance.salesforce.com/cometd/59.0/\n    tags:\n      - Events\n      - Push Notifications\n      - Real-Time\n      - Streaming\n    serviceName: Service Cloud Streaming API\n    serviceCategory: API\n  - name: Live Agent REST API\n    baseURL: https://yourInstance.salesforce.com/chat/rest/\n    tags:\n      - Agent\n      - Live Chat\n      - Real-Time Support\n    serviceName: Live Agent REST API\n    serviceCategory: API\n  - name: Knowledge API\n    baseURL: https://yourInstance.salesforce.com/services/data/v59.0/knowledge/\n    tags:\n      - Articles\n      - Content Management\n      - Knowledge Base\n    serviceName: Knowledge API\n    serviceCategory: API\n  - name: Einstein Bot API\n    baseURL: https://yourInstance.salesforce.com/services/data/v59.0/einstein/bots/\n    tags:\n      - AI\n      - Automation\n      - Chatbot\n      - Einstein\n    serviceName: Einstein Bot API\n    serviceCategory: API\n  - name: Omni-Channel API\n    baseURL: https://yourInstance.salesforce.com/services/data/v59.0/\n\
  \    tags:\n      - Agent Presence\n      - Omni-Channel\n      - Routing\n      - Work Distribution\n    serviceName: Omni-Channel API\n    serviceCategory: API\n  - name: Service Cloud Voice Telephony Integration API\n    baseURL: https://yourInstance.salesforce.com/services/data/v59.0/\n    tags:\n      - Call Center\n      - Real-Time\n      - Telephony\n      - Voice\n    serviceName: Service Cloud Voice Telephony Integration API\n    serviceCategory: API\n  - name: Service Cloud Voice for Partner Telephony API\n    baseURL: https://yourInstance.salesforce.com/services/data/v59.0/\n    tags:\n      - Connector\n      - Integration\n      - Partner Telephony\n      - Voice\n    serviceName: Service Cloud Voice for Partner Telephony API\n    serviceCategory: API\n  - name: Agentforce Service Agent API\n    baseURL: https://yourInstance.salesforce.com/services/data/v59.0/\n    tags:\n      - Agentforce\n      - AI\n      - Automation\n      - Service Agent\n    serviceName: Agentforce\
  \ Service Agent API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n    url: https://apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/salesforce-service-cloud/refs/heads/main/finops/salesforce-service-cloud-finops.yml
sources: []
specification: FinOps Framework
tags:
- Case Management
- CRM
- Customer Service
- Help Desk
- Support
- Ticketing
- FinOps
- Cost Management
- FOCUS
---
