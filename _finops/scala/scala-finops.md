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
description: FinOps framework definition for the Scala API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Scala
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Scala
  PublisherName: Scala
  ServiceCategory: Developer Tools / API
  ServiceName: Scala
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
name: Scala Finops
provider_name: Scala
provider_slug: scala
publisher_name: Scala
service_category: API
slug: scala-finops
source_filename: scala-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Scala\nproviderId: scala\npublisherName: Scala\nserviceCategory: API\ncreated: '2026-05-04'\nmodified: '2026-05-04'\ntags:\n  - Big Data\n  - Distributed Systems\n  - Functional Programming\n  - JVM\n  - Programming Language\n  - Scala\n  - Scala 3\n  - Type Safety\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Scala API surface. Provides a FOCUS-aligned mapping for\n  cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description:\
  \ Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n\
  \    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Scala\n  ServiceCategory: Developer Tools / API\n  ProviderName: Scala\n  PublisherName: Scala\n  InvoiceIssuerName: Scala\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n\
  \    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Scala Standard Library API\n    baseURL: ''\n    tags:\n      - Core\n      - JVM\n      - Programming Language\n      - Scala\n      - Standard Library\n    serviceName: Scala Standard Library API\n    serviceCategory: API\n  - name: Akka API\n    baseURL: ''\n    tags:\n      - Actors\n      - Concurrent\n      - Distributed Systems\n      - HTTP\n      - Reactive\n      - Scala\n    serviceName: Akka API\n    serviceCategory: API\n  - name: Akka HTTP API\n    baseURL: ''\n    tags:\n      - Akka\n      - Client\n      - HTTP\n      - Reactive\n      - Scala\n      - Server\n    serviceName: Akka HTTP API\n    serviceCategory: API\n  - name: Play Framework API\n    baseURL: ''\n\
  \    tags:\n      - MVC\n      - Reactive\n      - REST\n      - Scala\n      - Web Framework\n    serviceName: Play Framework API\n    serviceCategory: API\n  - name: ZIO API\n    baseURL: ''\n    tags:\n      - Async\n      - Concurrent\n      - Effect System\n      - Functional Programming\n      - Scala\n      - Type Safe\n    serviceName: ZIO API\n    serviceCategory: API\n  - name: Cats API\n    baseURL: ''\n    tags:\n      - Category Theory\n      - Functional Programming\n      - Scala\n      - Type Classes\n    serviceName: Cats API\n    serviceCategory: API\n  - name: http4s API\n    baseURL: ''\n    tags:\n      - Cats Effect\n      - Functional Programming\n      - HTTP\n      - Scala\n      - Streaming\n    serviceName: http4s API\n    serviceCategory: API\n  - name: Slick API\n    baseURL: ''\n    tags:\n      - Database\n      - Functional\n      - ORM\n      - Scala\n      - SQL\n    serviceName: Slick API\n    serviceCategory: API\n  - name: Circe API\n    baseURL: ''\n\
  \    tags:\n      - Cats\n      - Functional Programming\n      - JSON\n      - Parsing\n      - Scala\n      - Serialization\n    serviceName: Circe API\n    serviceCategory: API\n  - name: Apache Spark API\n    baseURL: ''\n    tags:\n      - Big Data\n      - Data Engineering\n      - Distributed Systems\n      - Machine Learning\n      - Scala\n      - Spark\n    serviceName: Apache Spark API\n    serviceCategory: API\n  - name: sbt Build Tool\n    baseURL: ''\n    tags:\n      - Build Tool\n      - Developer Tools\n      - Scala\n    serviceName: sbt Build Tool\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n    url: https://apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/scala/refs/heads/main/finops/scala-finops.yml
sources: []
specification: FinOps Framework
tags:
- Big Data
- Distributed Systems
- Functional Programming
- JVM
- Programming Language
- Scala
- Scala 3
- Type Safety
- FinOps
- Cost Management
- FOCUS
---
