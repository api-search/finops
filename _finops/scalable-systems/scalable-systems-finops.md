---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: haproxy_spec.yaml
  format: yaml
  label: HAProxy Data Plane API
  slug: haproxy
  spec_type: OpenAPI
  url: https://github.com/haproxytech/dataplaneapi/blob/master/specification/build/haproxy_spec.yaml
- filename: management-api.json
  format: json
  label: RabbitMQ Management API
  slug: rabbitmq
  spec_type: OpenAPI
  url: https://www.rabbitmq.com/resources/specs/management-api.json
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
description: FinOps framework definition for the Scalable Systems API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Scalable Systems
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Scalable Systems
  PublisherName: Scalable Systems
  ServiceCategory: Developer Tools / API
  ServiceName: Scalable Systems
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
name: Scalable Systems Finops
provider_name: Scalable Systems
provider_slug: scalable-systems
publisher_name: Scalable Systems
service_category: API
slug: scalable-systems-finops
source_filename: scalable-systems-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Scalable Systems\nproviderId: scalable-systems\npublisherName: Scalable Systems\nserviceCategory: API\ncreated: '2026-05-04'\nmodified: '2026-05-04'\ntags:\n  - Auto Scaling\n  - Caching\n  - Cloud Infrastructure\n  - Distributed Systems\n  - High Availability\n  - Infrastructure\n  - Load Balancing\n  - Message Queues\n  - Platform Engineering\n  - Scalable Architecture\n  - Service Discovery\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Scalable Systems API surface. Provides a FOCUS-aligned\n  mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description:\
  \ Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n   \
  \   - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Scalable Systems\n  ServiceCategory: Developer Tools / API\n  ProviderName: Scalable Systems\n  PublisherName: Scalable Systems\n  InvoiceIssuerName: Scalable Systems\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n\
  \      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: AWS Auto Scaling API\n    baseURL: ''\n    tags:\n      - Auto Scaling\n      - AWS\n      - Cloud Infrastructure\n      - Scalable Architecture\n    serviceName: AWS Auto Scaling API\n    serviceCategory: API\n  - name: HAProxy Data Plane API\n    baseURL: ''\n    tags:\n      - High Availability\n      - Load Balancing\n      - Proxy\n      - Traffic Management\n    serviceName: HAProxy Data Plane API\n    serviceCategory: API\n  - name: Redis REST API (Upstash)\n    baseURL: ''\n    tags:\n     \
  \ - Caching\n      - Distributed Systems\n      - In-Memory\n      - Low Latency\n    serviceName: Redis REST API (Upstash)\n    serviceCategory: API\n  - name: RabbitMQ Management API\n    baseURL: ''\n    tags:\n      - Asynchronous\n      - Decoupling\n      - Message Queues\n      - Messaging\n    serviceName: RabbitMQ Management API\n    serviceCategory: API\n  - name: Consul API\n    baseURL: ''\n    tags:\n      - Configuration Management\n      - High Availability\n      - Service Discovery\n      - Service Mesh\n    serviceName: Consul API\n    serviceCategory: API\n  - name: etcd API\n    baseURL: ''\n    tags:\n      - Configuration Management\n      - Distributed Systems\n      - High Availability\n      - Kubernetes\n    serviceName: etcd API\n    serviceCategory: API\n  - name: Celery Flower API\n    baseURL: ''\n    tags:\n      - Asynchronous\n      - Distributed Systems\n      - Message Queues\n      - Task Queue\n    serviceName: Celery Flower API\n    serviceCategory:\
  \ API\n  - name: NGINX Plus API\n    baseURL: ''\n    tags:\n      - HTTP\n      - High Performance\n      - Load Balancing\n      - Traffic Management\n    serviceName: NGINX Plus API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n    url: https://apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/scalable-systems/refs/heads/main/finops/scalable-systems-finops.yml
sources: []
specification: FinOps Framework
tags:
- Auto Scaling
- Caching
- Cloud Infrastructure
- Distributed Systems
- High Availability
- Infrastructure
- Load Balancing
- Message Queues
- Platform Engineering
- Scalable Architecture
- Service Discovery
- FinOps
- Cost Management
- FOCUS
---
