---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: cloudevents-http-asyncapi.yml
  format: yaml
  label: CloudEvents Specification
  slug: cloudevents-spec
  spec_type: AsyncAPI
  url: https://raw.githubusercontent.com/api-evangelist/cloudevents/refs/heads/main/asyncapi/cloudevents-http-asyncapi.yml
- filename: cloudevents-subscriptions-openapi.yml
  format: yaml
  label: CloudEvents Subscriptions API
  slug: cloudevents-subscriptions
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/cloudevents/refs/heads/main/openapi/cloudevents-subscriptions-openapi.yml
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
description: FinOps framework definition for the CloudEvents API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: CloudEvents
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: CloudEvents
  PublisherName: CloudEvents
  ServiceCategory: Developer Tools / API
  ServiceName: CloudEvents
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
name: Cloudevents Finops
provider_name: CloudEvents
provider_slug: cloudevents
publisher_name: CloudEvents
service_category: API
slug: cloudevents-finops
source_filename: cloudevents-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: CloudEvents\nproviderId: cloudevents\npublisherName: CloudEvents\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Cloud Native\n  - Events\n  - Graduated\n  - Interoperability\n  - Messaging\n  - Specification\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the CloudEvents API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every\
  \ chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n   \
  \ capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: CloudEvents\n  ServiceCategory: Developer Tools / API\n  ProviderName: CloudEvents\n  PublisherName: CloudEvents\n  InvoiceIssuerName: CloudEvents\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n\
  \    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: CloudEvents Specification\n    baseURL: ''\n    tags:\n      - Events\n      - Specification\n      - Standards\n    serviceName: CloudEvents Specification\n    serviceCategory: API\n  - name: CloudEvents HTTP Protocol Binding\n    baseURL: ''\n    tags:\n      - HTTP\n      - Protocol Binding\n      - REST\n    serviceName: CloudEvents HTTP Protocol Binding\n    serviceCategory: API\n  - name: CloudEvents Kafka Protocol Binding\n    baseURL: ''\n    tags:\n      - Kafka\n      - Messaging\n      - Protocol Binding\n    serviceName: CloudEvents Kafka Protocol Binding\n    serviceCategory: API\n  - name: CloudEvents AMQP Protocol Binding\n    baseURL: ''\n    tags:\n\
  \      - AMQP\n      - Messaging\n      - Protocol Binding\n    serviceName: CloudEvents AMQP Protocol Binding\n    serviceCategory: API\n  - name: CloudEvents MQTT Protocol Binding\n    baseURL: ''\n    tags:\n      - IoT\n      - MQTT\n      - Protocol Binding\n    serviceName: CloudEvents MQTT Protocol Binding\n    serviceCategory: API\n  - name: CloudEvents NATS Protocol Binding\n    baseURL: ''\n    tags:\n      - Messaging\n      - NATS\n      - Protocol Binding\n    serviceName: CloudEvents NATS Protocol Binding\n    serviceCategory: API\n  - name: CloudEvents Subscriptions API\n    baseURL: ''\n    tags:\n      - REST\n      - Specification\n      - Subscriptions\n    serviceName: CloudEvents Subscriptions API\n    serviceCategory: API\n  - name: CloudEvents SQL (CESQL)\n    baseURL: ''\n    tags:\n      - Filtering\n      - Specification\n      - SQL\n    serviceName: CloudEvents SQL (CESQL)\n    serviceCategory: API\n  - name: CloudEvents Go SDK\n    baseURL: ''\n    tags:\n\
  \      - Client Library\n      - Go\n      - SDK\n    serviceName: CloudEvents Go SDK\n    serviceCategory: API\n  - name: CloudEvents JavaScript SDK\n    baseURL: ''\n    tags:\n      - Client Library\n      - JavaScript\n      - SDK\n    serviceName: CloudEvents JavaScript SDK\n    serviceCategory: API\n  - name: CloudEvents Java SDK\n    baseURL: ''\n    tags:\n      - Client Library\n      - Java\n      - SDK\n    serviceName: CloudEvents Java SDK\n    serviceCategory: API\n  - name: CloudEvents Python SDK\n    baseURL: ''\n    tags:\n      - Client Library\n      - Python\n      - SDK\n    serviceName: CloudEvents Python SDK\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/cloudevents/refs/heads/main/finops/cloudevents-finops.yml
sources: []
specification: FinOps Framework
tags:
- Cloud Native
- Events
- Graduated
- Interoperability
- Messaging
- Specification
- FinOps
- Cost Management
- FOCUS
---
