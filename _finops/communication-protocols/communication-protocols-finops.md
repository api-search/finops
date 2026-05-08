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
description: FinOps framework definition for the Communication Protocols API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Communication Protocols
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Communication Protocols
  PublisherName: Communication Protocols
  ServiceCategory: Developer Tools / API
  ServiceName: Communication Protocols
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
name: Communication Protocols Finops
provider_name: Communication Protocols
provider_slug: communication-protocols
publisher_name: Communication Protocols
service_category: API
slug: communication-protocols-finops
source_filename: communication-protocols-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Communication Protocols\nproviderId: communication-protocols\npublisherName: Communication Protocols\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - APIs\n  - Application Protocols\n  - Communication Protocols\n  - Internet\n  - IETF\n  - Networking\n  - Real-Time\n  - Standards\n  - Transport\n  - Web\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Communication Protocols API surface. Provides a FOCUS-aligned\n  mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering,\
  \ product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n\
  \      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Communication Protocols\n  ServiceCategory: Developer Tools / API\n  ProviderName: Communication Protocols\n  PublisherName: Communication Protocols\n  InvoiceIssuerName: Communication Protocols\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n \
  \     - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Hypertext Transfer Protocol (HTTP)\n    baseURL: https://httpwg.org\n    tags:\n      - Application Protocol\n      - HTTP\n      - IETF\n      - REST\n      - Web\n    serviceName: Hypertext Transfer Protocol (HTTP)\n    serviceCategory: API\n  - name: gRPC\n    baseURL: https://grpc.io\n    tags:\n      - CNCF\n      - HTTP/2\n      - Protocol Buffers\n      - RPC\n      - Streaming\n    serviceName: gRPC\n    serviceCategory: API\n  - name: GraphQL\n    baseURL: https://graphql.org\n    tags:\n      - API\n  \
  \    - GraphQL\n      - HTTP\n      - Schema\n      - Subscriptions\n    serviceName: GraphQL\n    serviceCategory: API\n  - name: WebSocket\n    baseURL: https://www.rfc-editor.org\n    tags:\n      - Bidirectional\n      - IETF\n      - Real-Time\n      - Web\n      - WebSocket\n    serviceName: WebSocket\n    serviceCategory: API\n  - name: MQTT\n    baseURL: https://mqtt.org\n    tags:\n      - IoT\n      - Lightweight\n      - OASIS\n      - Pub/Sub\n    serviceName: MQTT\n    serviceCategory: API\n  - name: AMQP\n    baseURL: https://www.amqp.org\n    tags:\n      - Brokered\n      - Enterprise Messaging\n      - OASIS\n      - Queuing\n    serviceName: AMQP\n    serviceCategory: API\n  - name: Webhooks\n    baseURL: https://webhooks.fyi\n    tags:\n      - Async\n      - Events\n      - HTTP\n      - Push\n    serviceName: Webhooks\n    serviceCategory: API\n  - name: Server-Sent Events (SSE)\n    baseURL: https://html.spec.whatwg.org\n    tags:\n      - HTML\n      - HTTP\n   \
  \   - Real-Time\n      - Streaming\n    serviceName: Server-Sent Events (SSE)\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/communication-protocols/refs/heads/main/finops/communication-protocols-finops.yml
sources: []
specification: FinOps Framework
tags:
- APIs
- Application Protocols
- Communication Protocols
- Internet
- IETF
- Networking
- Real-Time
- Standards
- Transport
- Web
- FinOps
- Cost Management
- FOCUS
---
