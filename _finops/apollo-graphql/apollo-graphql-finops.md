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
description: FinOps framework definition for the Apollo GraphQL API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Apollo GraphQL
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Apollo GraphQL
  PublisherName: Apollo GraphQL
  ServiceCategory: Developer Tools / API
  ServiceName: Apollo GraphQL
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
name: Apollo Graphql Finops
provider_name: Apollo GraphQL
provider_slug: apollo-graphql
publisher_name: Apollo GraphQL
service_category: API
slug: apollo-graphql-finops
source_filename: apollo-graphql-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Apollo GraphQL\nproviderId: apollo-graphql\npublisherName: Apollo GraphQL\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - API Orchestration\n  - Clients\n  - Connectors\n  - Federation\n  - Graph\n  - GraphQL\n  - Router\n  - Schema Registry\n  - Supergraph\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Apollo GraphQL API surface. Provides a FOCUS-aligned\n  mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n\
  \  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and\
  \ SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Apollo GraphQL\n  ServiceCategory: Developer Tools / API\n  ProviderName: Apollo GraphQL\n  PublisherName: Apollo GraphQL\n  InvoiceIssuerName: Apollo GraphQL\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n\
  \    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Apollo GraphQL\n    baseURL: ''\n    tags:\n      - Clients\n      - Connectors\n      - Federation\n      - Graph\n      - GraphQL\n    serviceName: Apollo GraphQL\n    serviceCategory: API\n  - name: Apollo GraphOS Platform API\n    baseURL: ''\n    tags:\n      - API Management\n      - Federation\n      - GraphQL\n      - Platform\n      - Schema Registry\n    serviceName: Apollo GraphOS Platform API\n    serviceCategory: API\n  - name: Apollo Server\n    baseURL: ''\n    tags:\n      - GraphQL\n      - JavaScript\n      - Node.js\n      - Server\n      - TypeScript\n    serviceName: Apollo Server\n\
  \    serviceCategory: API\n  - name: Apollo Client (Web)\n    baseURL: ''\n    tags:\n      - Client\n      - GraphQL\n      - JavaScript\n      - React\n      - State Management\n      - TypeScript\n    serviceName: Apollo Client (Web)\n    serviceCategory: API\n  - name: Apollo Client (iOS)\n    baseURL: ''\n    tags:\n      - Client\n      - GraphQL\n      - iOS\n      - Mobile\n      - Swift\n    serviceName: Apollo Client (iOS)\n    serviceCategory: API\n  - name: Apollo Client (Kotlin)\n    baseURL: ''\n    tags:\n      - Android\n      - Client\n      - GraphQL\n      - JVM\n      - Kotlin\n      - Mobile\n    serviceName: Apollo Client (Kotlin)\n    serviceCategory: API\n  - name: Apollo Router\n    baseURL: ''\n    tags:\n      - Federation\n      - Gateway\n      - GraphQL\n      - Router\n      - Rust\n    serviceName: Apollo Router\n    serviceCategory: API\n  - name: Apollo Connectors\n    baseURL: ''\n    tags:\n      - Connectors\n      - Federation\n      - GraphQL\n  \
  \    - Integration\n      - REST\n    serviceName: Apollo Connectors\n    serviceCategory: API\n  - name: Rover CLI\n    baseURL: ''\n    tags:\n      - CI/CD\n      - CLI\n      - Federation\n      - GraphQL\n      - Schema Management\n    serviceName: Rover CLI\n    serviceCategory: API\n  - name: Apollo Federation\n    baseURL: ''\n    tags:\n      - Distributed\n      - Federation\n      - GraphQL\n      - Microservices\n      - Supergraph\n    serviceName: Apollo Federation\n    serviceCategory: API\n  - name: Apollo MCP Server\n    baseURL: ''\n    tags:\n      - AI\n      - GraphQL\n      - MCP\n      - Model Context Protocol\n    serviceName: Apollo MCP Server\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/apollo-graphql/refs/heads/main/finops/apollo-graphql-finops.yml
sources: []
specification: FinOps Framework
tags:
- API Orchestration
- Clients
- Connectors
- Federation
- Graph
- GraphQL
- Router
- Schema Registry
- Supergraph
- FinOps
- Cost Management
- FOCUS
---
