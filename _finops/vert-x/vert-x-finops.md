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
description: FinOps framework definition for the Vert.x API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Vert.x
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Vert.x
  PublisherName: Vert.x
  ServiceCategory: Developer Tools / API
  ServiceName: Vert.x
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
name: Vert X Finops
provider_name: Vert.x
provider_slug: vert-x
publisher_name: Vert.x
service_category: API
slug: vert-x-finops
source_filename: vert-x-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Vert.x\nproviderId: vert-x\npublisherName: Vert.x\nserviceCategory: API\ncreated: '2026-05-04'\nmodified: '2026-05-04'\ntags:\n  - Event-Driven\n  - Frameworks\n  - Java\n  - JVM\n  - Microservices\n  - Polyglot\n  - Reactive\n  - Eclipse Foundation\n  - Open Source\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Vert.x API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n  \
  \  description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the\
  \ FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Vert.x\n  ServiceCategory: Developer Tools / API\n  ProviderName: Vert.x\n  PublisherName: Vert.x\n  InvoiceIssuerName: Vert.x\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n\
  \    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Vert.x Core\n    baseURL: ''\n    tags:\n      - Event-Driven\n      - Event Loop\n      - Verticles\n      - Event Bus\n      - Reactive\n      - JVM\n    serviceName: Vert.x Core\n    serviceCategory: API\n  - name: Vert.x Web\n    baseURL: ''\n    tags:\n      - REST\n      - HTTP\n      - Web Framework\n      - Routing\n      - WebSocket\n    serviceName: Vert.x Web\n    serviceCategory: API\n  - name: Vert.x OpenAPI\n    baseURL: ''\n    tags:\n      - OpenAPI\n      - API Specification\n      - Validation\n      - Contract-Driven\n    serviceName: Vert.x OpenAPI\n    serviceCategory: API\n  - name: Vert.x gRPC\n    baseURL: ''\n    tags:\n      - gRPC\n     \
  \ - Protocol Buffers\n      - HTTP/2\n      - Streaming\n    serviceName: Vert.x gRPC\n    serviceCategory: API\n  - name: Vert.x SQL Client\n    baseURL: ''\n    tags:\n      - SQL\n      - Database\n      - PostgreSQL\n      - MySQL\n      - Reactive\n    serviceName: Vert.x SQL Client\n    serviceCategory: API\n  - name: Vert.x Auth\n    baseURL: ''\n    tags:\n      - Authentication\n      - Authorization\n      - JWT\n      - OAuth2\n      - Security\n    serviceName: Vert.x Auth\n    serviceCategory: API\n  - name: Vert.x Health Check\n    baseURL: ''\n    tags:\n      - Health Check\n      - Kubernetes\n      - Observability\n      - Liveness\n      - Readiness\n    serviceName: Vert.x Health Check\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/vert-x/refs/heads/main/finops/vert-x-finops.yml
sources: []
specification: FinOps Framework
tags:
- Event-Driven
- Frameworks
- Java
- JVM
- Microservices
- Polyglot
- Reactive
- Eclipse Foundation
- Open Source
- FinOps
- Cost Management
- FOCUS
---
