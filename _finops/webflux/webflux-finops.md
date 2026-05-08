---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: webflux-websocket-asyncapi.yml
  format: yaml
  label: Spring WebFlux WebSocket
  slug: ''
  spec_type: AsyncAPI
  url: https://raw.githubusercontent.com/api-evangelist/webflux/refs/heads/main/asyncapi/webflux-websocket-asyncapi.yml
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
description: FinOps framework definition for the Spring WebFlux API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Spring WebFlux
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Spring WebFlux
  PublisherName: Spring WebFlux
  ServiceCategory: Developer Tools / API
  ServiceName: Spring WebFlux
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
name: Webflux Finops
provider_name: Spring WebFlux
provider_slug: webflux
publisher_name: Spring WebFlux
service_category: API
slug: webflux-finops
source_filename: webflux-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Spring WebFlux\nproviderId: webflux\npublisherName: Spring WebFlux\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Java\n  - Microservices\n  - Non-Blocking IO\n  - Reactive Programming\n  - REST API\n  - Spring Boot\n  - Spring Framework\n  - WebFlux\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Spring WebFlux API surface. Provides a FOCUS-aligned\n  mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n\
  \  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and\
  \ SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Spring WebFlux\n  ServiceCategory: Developer Tools / API\n  ProviderName: Spring WebFlux\n  PublisherName: Spring WebFlux\n  InvoiceIssuerName: Spring WebFlux\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n\
  \    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Spring WebFlux Core\n    baseURL: ''\n    tags:\n      - Annotated Controllers\n      - Dispatcher Handler\n      - Functional Endpoints\n      - Non-Blocking\n      - Reactive\n      - Spring Framework\n      - WebFlux\n    serviceName: Spring WebFlux Core\n    serviceCategory: API\n  - name: Spring WebFlux WebClient\n    baseURL: ''\n    tags:\n      - HTTP Client\n      - Non-Blocking\n      - Reactive\n      - REST\n      - WebClient\n    serviceName: Spring WebFlux WebClient\n    serviceCategory: API\n  - name: Spring WebFlux Router Functions\n    baseURL: ''\n    tags:\n      - Functional Programming\n\
  \      - Handler Functions\n      - Reactive\n      - Router Functions\n      - Routing\n    serviceName: Spring WebFlux Router Functions\n    serviceCategory: API\n  - name: Spring WebFlux WebSocket\n    baseURL: ''\n    tags:\n      - Bidirectional\n      - Full Duplex\n      - Messaging\n      - Real-Time\n      - WebSocket\n    serviceName: Spring WebFlux WebSocket\n    serviceCategory: API\n  - name: Spring WebFlux RSocket\n    baseURL: ''\n    tags:\n      - Binary Protocol\n      - Microservices\n      - Reactive\n      - RSocket\n      - Streaming\n    serviceName: Spring WebFlux RSocket\n    serviceCategory: API\n  - name: Reactor Core\n    baseURL: ''\n    tags:\n      - Flux\n      - Mono\n      - Project Reactor\n      - Reactive Streams\n      - Reactor\n    serviceName: Reactor Core\n    serviceCategory: API\n  - name: Spring WebFlux HTTP Service Client\n    baseURL: ''\n    tags:\n      - Declarative\n      - HTTP Client\n      - HTTP Interface\n      - Reactive\n      -\
  \ REST\n    serviceName: Spring WebFlux HTTP Service Client\n    serviceCategory: API\n  - name: Spring WebFlux Testing\n    baseURL: ''\n    tags:\n      - Integration Testing\n      - Reactive Testing\n      - Spring Boot Test\n      - Testing\n      - WebTestClient\n    serviceName: Spring WebFlux Testing\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/webflux/refs/heads/main/finops/webflux-finops.yml
sources: []
specification: FinOps Framework
tags:
- Java
- Microservices
- Non-Blocking IO
- Reactive Programming
- REST API
- Spring Boot
- Spring Framework
- WebFlux
- FinOps
- Cost Management
- FOCUS
---
