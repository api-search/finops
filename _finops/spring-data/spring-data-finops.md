---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: spring-data-rest-openapi.yml
  format: yaml
  label: Spring Data REST
  slug: spring-data-rest
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/spring-data/refs/heads/main/openapi/spring-data-rest-openapi.yml
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
description: FinOps framework definition for the Spring Data API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Spring Data
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Spring Data
  PublisherName: Spring Data
  ServiceCategory: Developer Tools / API
  ServiceName: Spring Data
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
name: Spring Data Finops
provider_name: Spring Data
provider_slug: spring-data
publisher_name: Spring Data
service_category: API
slug: spring-data-finops
source_filename: spring-data-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Spring Data\nproviderId: spring-data\npublisherName: Spring Data\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Data Access\n  - Database\n  - Framework\n  - Java\n  - JPA\n  - MongoDB\n  - ORM\n  - Redis\n  - REST\n  - Spring\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Spring Data API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n   \
  \ description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the\
  \ FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Spring Data\n  ServiceCategory: Developer Tools / API\n  ProviderName: Spring Data\n  PublisherName: Spring Data\n  InvoiceIssuerName: Spring Data\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the\
  \ network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Spring Data REST\n    baseURL: http://localhost:8080\n    tags:\n      - HATEOAS\n      - HAL\n      - Hypermedia\n      - Repository\n      - REST\n    serviceName: Spring Data REST\n    serviceCategory: API\n  - name: Spring Data JPA\n    baseURL: http://localhost:8080\n    tags:\n      - Database\n      - Hibernate\n      - JPA\n      - Persistence\n      - Repository\n    serviceName: Spring Data JPA\n    serviceCategory: API\n  - name: Spring Data MongoDB\n    baseURL: http://localhost:8080\n    tags:\n      - Document Database\n      - MongoDB\n      - NoSQL\n    serviceName: Spring Data MongoDB\n    serviceCategory: API\n  - name:\
  \ Spring Data Redis\n    baseURL: http://localhost:8080\n    tags:\n      - Cache\n      - Key-Value Store\n      - Pub/Sub\n      - Redis\n    serviceName: Spring Data Redis\n    serviceCategory: API\n  - name: Spring Data Cassandra\n    baseURL: http://localhost:8080\n    tags:\n      - Cassandra\n      - Distributed Database\n      - NoSQL\n    serviceName: Spring Data Cassandra\n    serviceCategory: API\n  - name: Spring Data Neo4j\n    baseURL: http://localhost:8080\n    tags:\n      - Graph Database\n      - Neo4j\n      - NoSQL\n    serviceName: Spring Data Neo4j\n    serviceCategory: API\n  - name: Spring Data Elasticsearch\n    baseURL: http://localhost:8080\n    tags:\n      - Elasticsearch\n      - Full-Text Search\n      - Search Engine\n    serviceName: Spring Data Elasticsearch\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost\
  \ / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Spring Team\n    email: spring-data@pivotal.io\n    X-twitter: springcentral\n    X-github: spring-projects\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/spring-data/refs/heads/main/finops/spring-data-finops.yml
sources: []
specification: FinOps Framework
tags:
- Data Access
- Database
- Framework
- Java
- JPA
- MongoDB
- ORM
- Redis
- REST
- Spring
- FinOps
- Cost Management
- FOCUS
---
