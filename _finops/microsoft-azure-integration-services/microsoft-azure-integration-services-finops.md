---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: microsoft-azure-integration-services-openapi.yml
  format: yaml
  label: Azure API Management
  slug: azure-api-management
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-azure-integration-services/refs/heads/main/openapi/microsoft-azure-integration-services-openapi.yml
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
description: FinOps framework definition for the Microsoft Azure Integration Services API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Microsoft Azure Integration Services
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Microsoft Azure Integration Services
  PublisherName: Microsoft Azure Integration Services
  ServiceCategory: Developer Tools / API
  ServiceName: Microsoft Azure Integration Services
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
name: Microsoft Azure Integration Services Finops
provider_name: Microsoft Azure Integration Services
provider_slug: microsoft-azure-integration-services
publisher_name: Microsoft Azure Integration Services
service_category: API
slug: microsoft-azure-integration-services-finops
source_filename: microsoft-azure-integration-services-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Microsoft Azure Integration Services\nproviderId: microsoft-azure-integration-services\npublisherName: Microsoft Azure Integration Services\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - API Management\n  - Enterprise\n  - Event-Driven\n  - Integration\n  - Messaging\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Microsoft Azure Integration Services API surface. Provides\n  a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across\n  the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and\
  \ finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud\
  \ Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Microsoft Azure Integration Services\n  ServiceCategory: Developer Tools / API\n  ProviderName: Microsoft Azure Integration Services\n  PublisherName: Microsoft Azure Integration Services\n  InvoiceIssuerName: Microsoft Azure Integration Services\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation:\
  \ sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Azure API Management\n    baseURL: https://management.azure.com/\n    tags:\n      - API Gateway\n      - API Management\n      - Azure\n      - Developer Portal\n    serviceName: Azure API Management\n    serviceCategory: API\n  - name: Azure Logic Apps\n    baseURL: https://management.azure.com/\n    tags:\n      - Azure\n      - Integration\n      - Low-Code\n      - Workflow Automation\n    serviceName: Azure Logic Apps\n    serviceCategory: API\n  - name: Azure Service Bus\n\
  \    baseURL: https://management.azure.com/\n    tags:\n      - Azure\n      - Message Queue\n      - Messaging\n      - Publish-Subscribe\n    serviceName: Azure Service Bus\n    serviceCategory: API\n  - name: Azure Event Grid\n    baseURL: https://management.azure.com/\n    tags:\n      - Azure\n      - Event-Driven\n      - Eventing\n      - Pub-Sub\n    serviceName: Azure Event Grid\n    serviceCategory: API\n  - name: Azure Event Hubs\n    baseURL: https://management.azure.com/\n    tags:\n      - Azure\n      - Big Data\n      - Event Streaming\n      - Kafka\n    serviceName: Azure Event Hubs\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/microsoft-azure-integration-services/refs/heads/main/finops/microsoft-azure-integration-services-finops.yml
sources: []
specification: FinOps Framework
tags:
- API Management
- Enterprise
- Event-Driven
- Integration
- Messaging
- FinOps
- Cost Management
- FOCUS
---
