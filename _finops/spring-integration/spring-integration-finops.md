---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: spring-integration-http-openapi.yml
  format: yaml
  label: Spring Integration HTTP Adapter API
  slug: spring-integration-http
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/spring-integration/refs/heads/main/openapi/spring-integration-http-openapi.yml
- filename: spring-integration-management-openapi.yml
  format: yaml
  label: Spring Integration Management API
  slug: spring-integration-management
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/spring-integration/refs/heads/main/openapi/spring-integration-management-openapi.yml
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
description: FinOps framework definition for the Spring Integration API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Spring Integration
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Spring Integration
  PublisherName: Spring Integration
  ServiceCategory: Developer Tools / API
  ServiceName: Spring Integration
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
name: Spring Integration Finops
provider_name: Spring Integration
provider_slug: spring-integration
publisher_name: Spring Integration
service_category: API
slug: spring-integration-finops
source_filename: spring-integration-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Spring Integration\nproviderId: spring-integration\npublisherName: Spring Integration\nserviceCategory: API\ncreated: '2026-05-04'\nmodified: '2026-05-04'\ntags:\n  - AMQP\n  - Enterprise Integration\n  - Event-Driven\n  - Integration Patterns\n  - Java\n  - Messaging\n  - Spring\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Spring Integration API surface. Provides a FOCUS-aligned\n  mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n\
  \  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and\
  \ SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Spring Integration\n  ServiceCategory: Developer Tools / API\n  ProviderName: Spring Integration\n  PublisherName: Spring Integration\n  InvoiceIssuerName: Spring Integration\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name:\
  \ data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Spring Integration HTTP Adapter API\n    baseURL: http://localhost:8080\n    tags:\n      - HTTP\n      - Inbound\n      - Messaging\n      - Outbound\n      - REST\n    serviceName: Spring Integration HTTP Adapter API\n    serviceCategory: API\n  - name: Spring Integration Management API\n    baseURL: http://localhost:8080/api\n    tags:\n      - Management\n      - Messaging\n      - Metrics\n      - Monitoring\n    serviceName: Spring Integration Management API\n    serviceCategory: API\n  - name: Spring Integration AMQP Adapter\n    baseURL: ''\n    tags:\n      - AMQP\n      - Messaging\n\
  \      - RabbitMQ\n    serviceName: Spring Integration AMQP Adapter\n    serviceCategory: API\n  - name: Spring Integration Kafka Adapter\n    baseURL: ''\n    tags:\n      - Event Streaming\n      - Kafka\n      - Messaging\n    serviceName: Spring Integration Kafka Adapter\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Spring Team\n    email: spring-projects@vmware.com\n    url: https://spring.io/team\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/spring-integration/refs/heads/main/finops/spring-integration-finops.yml
sources: []
specification: FinOps Framework
tags:
- AMQP
- Enterprise Integration
- Event-Driven
- Integration Patterns
- Java
- Messaging
- Spring
- FinOps
- Cost Management
- FOCUS
---
