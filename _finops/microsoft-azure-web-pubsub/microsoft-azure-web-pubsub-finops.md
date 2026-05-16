---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: webpubsub.json
  format: json
  label: Azure Web PubSub Service REST API
  slug: azure-web-pubsub-service-rest-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/Azure/azure-rest-api-specs/main/specification/webpubsub/data-plane/WebPubSub/stable/2024-01-01/webpubsub.json
- filename: webpubsub.json
  format: json
  label: Azure Web PubSub Management REST API
  slug: azure-web-pubsub-management-rest-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/Azure/azure-rest-api-specs/main/specification/webpubsub/resource-manager/Microsoft.SignalRService/stable/2024-03-01/webpubsub.json
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
description: FinOps framework definition for the Azure Web PubSub API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Azure Web PubSub
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Azure Web PubSub
  PublisherName: Azure Web PubSub
  ServiceCategory: Developer Tools / API
  ServiceName: Azure Web PubSub
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
name: Microsoft Azure Web Pubsub Finops
provider_name: Azure Web PubSub
provider_slug: microsoft-azure-web-pubsub
publisher_name: Azure Web PubSub
service_category: API
slug: microsoft-azure-web-pubsub-finops
source_filename: microsoft-azure-web-pubsub-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Azure Web PubSub\nproviderId: microsoft-azure-web-pubsub\npublisherName: Azure Web PubSub\nserviceCategory: API\ncreated: '2026-05-04'\nmodified: '2026-05-04'\ntags:\n  - Messaging\n  - Pub-Sub\n  - Real-Time\n  - Serverless\n  - WebSockets\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Azure Web PubSub API surface. Provides a FOCUS-aligned\n  mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag\
  \ every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n\
  \    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Azure Web PubSub\n  ServiceCategory: Developer Tools / API\n  ProviderName: Azure Web PubSub\n  PublisherName: Azure Web PubSub\n  InvoiceIssuerName: Azure Web PubSub\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over\
  \ the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Azure Web PubSub Service REST API\n    baseURL: https://{instance}.webpubsub.azure.com\n    tags:\n      - Data Plane\n      - Messaging\n      - Web PubSub\n    serviceName: Azure Web PubSub Service REST API\n    serviceCategory: API\n  - name: Azure Web PubSub Management REST API\n    baseURL: https://management.azure.com\n    tags:\n      - Control Plane\n      - Resource Manager\n      - Web PubSub\n    serviceName: Azure Web PubSub Management REST API\n    serviceCategory: API\n  - name: Azure Web PubSub Hubs REST API\n    baseURL: https://management.azure.com\n    tags:\n      - Hubs\n      - Resource Manager\n      - Web PubSub\n\
  \    serviceName: Azure Web PubSub Hubs REST API\n    serviceCategory: API\n  - name: Azure Web PubSub for Socket.IO REST API\n    baseURL: https://management.azure.com\n    tags:\n      - Resource Manager\n      - Socket.IO\n      - Web PubSub\n    serviceName: Azure Web PubSub for Socket.IO REST API\n    serviceCategory: API\n  - name: Azure Web PubSub Private Endpoint Connections REST API\n    baseURL: https://management.azure.com\n    tags:\n      - Networking\n      - Private Endpoints\n      - Resource Manager\n    serviceName: Azure Web PubSub Private Endpoint Connections REST API\n    serviceCategory: API\n  - name: Azure Web PubSub Shared Private Link Resources REST API\n    baseURL: https://management.azure.com\n    tags:\n      - Networking\n      - Private Link\n      - Resource Manager\n    serviceName: Azure Web PubSub Shared Private Link Resources REST API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests /\
  \ 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/microsoft-azure-web-pubsub/refs/heads/main/finops/microsoft-azure-web-pubsub-finops.yml
sources: []
specification: FinOps Framework
tags:
- Messaging
- Pub-Sub
- Real-Time
- Serverless
- WebSockets
- FinOps
- Cost Management
- FOCUS
---
