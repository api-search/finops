---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: openapi.yml
  format: yaml
  label: Temporal API
  slug: temporal
  spec_type: OpenAPI
  url: https://github.com/temporalio/api/blob/master/openapi/openapi.yml
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
description: FinOps framework definition for the Scalable Software and Systems API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Scalable Software and Systems
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Scalable Software and Systems
  PublisherName: Scalable Software and Systems
  ServiceCategory: Developer Tools / API
  ServiceName: Scalable Software and Systems
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
name: Scalable Software And Systems Finops
provider_name: Scalable Software and Systems
provider_slug: scalable-software-and-systems
publisher_name: Scalable Software and Systems
service_category: API
slug: scalable-software-and-systems-finops
source_filename: scalable-software-and-systems-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Scalable Software and Systems\nproviderId: scalable-software-and-systems\npublisherName: Scalable Software and Systems\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - API First\n  - Architecture Patterns\n  - CQRS\n  - Distributed Systems\n  - Enterprise\n  - Event Driven\n  - Microservices\n  - Scalable Architecture\n  - Software Engineering\n  - Systems Design\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Scalable Software and Systems API surface. Provides a\n  FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the\n  provider's APIs.\nprinciples:\n  - name: Visibility\n\
  \    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting\
  \ for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Scalable Software and Systems\n  ServiceCategory: Developer Tools / API\n  ProviderName: Scalable Software and Systems\n  PublisherName: Scalable Software and Systems\n  InvoiceIssuerName: Scalable Software and Systems\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable\
  \ API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Backstage Software Catalog API\n    baseURL: ''\n    tags:\n      - Developer Portal\n      - Internal Developer Platform\n      - Software Catalog\n      - Systems Design\n    serviceName: Backstage Software Catalog API\n    serviceCategory: API\n  - name: CloudEvents API\n    baseURL: ''\n    tags:\n      - CNCF\n      - Event Driven\n      - Events\n      - Integration\n      - Standards\n    serviceName: CloudEvents API\n \
  \   serviceCategory: API\n  - name: Apache Kafka Admin API\n    baseURL: ''\n    tags:\n      - Event Driven\n      - Event Streaming\n      - High Throughput\n      - Messaging\n    serviceName: Apache Kafka Admin API\n    serviceCategory: API\n  - name: NATS Management API\n    baseURL: ''\n    tags:\n      - Cloud Native\n      - Event Driven\n      - High Performance\n      - Messaging\n      - Microservices\n    serviceName: NATS Management API\n    serviceCategory: API\n  - name: Temporal API\n    baseURL: ''\n    tags:\n      - Distributed Systems\n      - Durable Execution\n      - Saga Pattern\n      - Workflow Orchestration\n    serviceName: Temporal API\n    serviceCategory: API\n  - name: Dapr API\n    baseURL: ''\n    tags:\n      - Distributed Systems\n      - Event Driven\n      - Microservices\n      - Scalable Architecture\n    serviceName: Dapr API\n    serviceCategory: API\n  - name: OpenTelemetry API\n    baseURL: ''\n    tags:\n      - Distributed Tracing\n      -\
  \ Logs\n      - Metrics\n      - Observability\n      - Telemetry\n    serviceName: OpenTelemetry API\n    serviceCategory: API\n  - name: Argo CD API\n    baseURL: ''\n    tags:\n      - CD\n      - GitOps\n      - Kubernetes\n      - Platform Engineering\n    serviceName: Argo CD API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n    url: https://apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/scalable-software-and-systems/refs/heads/main/finops/scalable-software-and-systems-finops.yml
sources: []
specification: FinOps Framework
tags:
- API First
- Architecture Patterns
- CQRS
- Distributed Systems
- Enterprise
- Event Driven
- Microservices
- Scalable Architecture
- Software Engineering
- Systems Design
- FinOps
- Cost Management
- FOCUS
---
