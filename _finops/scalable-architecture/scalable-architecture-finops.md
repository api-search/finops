---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: virtual_service.proto
  format: yaml
  label: Istio Service Mesh API
  slug: istio-service-mesh-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/istio/api/master/networking/v1alpha3/virtual_service.proto
- filename: api
  format: yaml
  label: Envoy Proxy Admin API
  slug: envoy-proxy-admin-api
  spec_type: OpenAPI
  url: https://www.envoyproxy.io/docs/envoy/latest/api-v3/api
- filename: openapi.yaml
  format: yaml
  label: Apache Kafka REST Proxy API
  slug: apache-kafka-rest-proxy-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/confluentinc/kafka-rest/master/api/v3/openapi.yaml
- filename: index.json
  format: json
  label: RabbitMQ Management HTTP API
  slug: rabbitmq-management-http-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/rabbitmq/rabbitmq-server/main/deps/rabbitmq_management/priv/www/api/index.json
- filename: swagger.json
  format: json
  label: Kubernetes API
  slug: kubernetes-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/kubernetes/kubernetes/master/api/openapi-spec/swagger.json
- filename: swagger.json
  format: json
  label: Argo Workflows API
  slug: argo-workflows-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/argoproj/argo-workflows/main/api/openapi-spec/swagger.json
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
description: FinOps framework definition for the Scalable Architecture API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Scalable Architecture
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Scalable Architecture
  PublisherName: Scalable Architecture
  ServiceCategory: Developer Tools / API
  ServiceName: Scalable Architecture
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
name: Scalable Architecture Finops
provider_name: Scalable Architecture
provider_slug: scalable-architecture
publisher_name: Scalable Architecture
service_category: API
slug: scalable-architecture-finops
source_filename: scalable-architecture-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Scalable Architecture\nproviderId: scalable-architecture\npublisherName: Scalable Architecture\nserviceCategory: API\ncreated: '2026-05-04'\nmodified: '2026-05-04'\ntags:\n  - Cloud Architecture\n  - Cloud Native\n  - Distributed Systems\n  - High Availability\n  - Infrastructure\n  - Microservices\n  - Performance\n  - Resilience\n  - Scalability\n  - Service Mesh\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Scalable Architecture API surface. Provides a FOCUS-aligned\n  mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption\
  \ costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n\
  \      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Scalable Architecture\n  ServiceCategory: Developer Tools / API\n  ProviderName: Scalable Architecture\n  PublisherName: Scalable Architecture\n  InvoiceIssuerName: Scalable Architecture\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n\
  \      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Istio Service Mesh API\n    baseURL: ''\n    tags:\n      - CNCF\n      - Kubernetes\n      - Microservices\n      - Observability\n      - Security\n      - Service Mesh\n      - Traffic Management\n    serviceName: Istio Service Mesh API\n    serviceCategory: API\n  - name: Linkerd API\n    baseURL: ''\n    tags:\n      - CNCF\n      - Kubernetes\n      - Microservices\n      - mTLS\n      - Observability\n      - Security\n      - Service Mesh\n    serviceName: Linkerd API\n    serviceCategory: API\n\
  \  - name: Envoy Proxy Admin API\n    baseURL: ''\n    tags:\n      - CNCF\n      - Load Balancing\n      - Open Source\n      - Proxy\n      - Service Mesh\n      - Traffic Management\n    serviceName: Envoy Proxy Admin API\n    serviceCategory: API\n  - name: Apache Kafka REST Proxy API\n    baseURL: ''\n    tags:\n      - Apache Kafka\n      - Event Streaming\n      - Event-Driven\n      - Message Broker\n      - Microservices\n      - Pub-Sub\n    serviceName: Apache Kafka REST Proxy API\n    serviceCategory: API\n  - name: Redis REST API (Redis Stack)\n    baseURL: ''\n    tags:\n      - Caching\n      - Data Store\n      - In-Memory\n      - Message Broker\n      - Open Source\n      - Pub-Sub\n      - Redis\n    serviceName: Redis REST API (Redis Stack)\n    serviceCategory: API\n  - name: RabbitMQ Management HTTP API\n    baseURL: ''\n    tags:\n      - AMQP\n      - Event-Driven\n      - Message Broker\n      - Microservices\n      - Open Source\n      - RabbitMQ\n    serviceName:\
  \ RabbitMQ Management HTTP API\n    serviceCategory: API\n  - name: Kubernetes API\n    baseURL: ''\n    tags:\n      - CNCF\n      - Cloud Native\n      - Containers\n      - Kubernetes\n      - Orchestration\n      - Open Source\n    serviceName: Kubernetes API\n    serviceCategory: API\n  - name: Argo Workflows API\n    baseURL: ''\n    tags:\n      - CNCF\n      - CI/CD\n      - Kubernetes\n      - Orchestration\n      - Pipelines\n      - Workflow\n    serviceName: Argo Workflows API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: API Evangelist\n    email: kin@apievangelist.com\n    url: https://apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/scalable-architecture/refs/heads/main/finops/scalable-architecture-finops.yml
sources: []
specification: FinOps Framework
tags:
- Cloud Architecture
- Cloud Native
- Distributed Systems
- High Availability
- Infrastructure
- Microservices
- Performance
- Resilience
- Scalability
- Service Mesh
- FinOps
- Cost Management
- FOCUS
---
