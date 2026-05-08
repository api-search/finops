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
description: FinOps framework definition for the Confluent | the Data Streaming Platform API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Confluent | the Data Streaming Platform
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Confluent | the Data Streaming Platform
  PublisherName: Confluent | the Data Streaming Platform
  ServiceCategory: Developer Tools / API
  ServiceName: Confluent | the Data Streaming Platform
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
name: Confluent The Data Streaming Platform Finops
provider_name: Confluent | the Data Streaming Platform
provider_slug: confluent-the-data-streaming-platform
publisher_name: Confluent | the Data Streaming Platform
service_category: API
slug: confluent-the-data-streaming-platform-finops
source_filename: confluent-the-data-streaming-platform-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Confluent | the Data Streaming Platform\nproviderId: confluent-the-data-streaming-platform\npublisherName: Confluent | the Data Streaming Platform\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Apache Flink\n  - Apache Kafka\n  - Confluent Cloud\n  - Connectors\n  - Data Streaming\n  - Event Streaming\n  - Kafka Connect\n  - ksqlDB\n  - Real-Time Data\n  - REST\n  - Schema Registry\n  - Stream Processing\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Confluent | the Data Streaming Platform API surface.\n  Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting\n \
  \ across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name:\
  \ Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Confluent | the Data Streaming Platform\n  ServiceCategory: Developer Tools / API\n  ProviderName: Confluent | the Data Streaming Platform\n  PublisherName: Confluent | the Data Streaming Platform\n  InvoiceIssuerName: Confluent | the Data Streaming Platform\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency:\
  \ USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Confluent Cloud REST API\n    baseURL: https://api.confluent.cloud\n    tags:\n      - Confluent Cloud\n      - Management\n      - REST\n    serviceName: Confluent Cloud REST API\n    serviceCategory: API\n  - name: Confluent Kafka REST API\n    baseURL: https://pkc-XXXXX.region.aws.confluent.cloud\n    tags:\n      - Apache Kafka\n\
  \      - Producer\n      - Consumer\n      - REST\n    serviceName: Confluent Kafka REST API\n    serviceCategory: API\n  - name: Confluent Schema Registry REST API\n    baseURL: https://psrc-XXXXX.region.aws.confluent.cloud\n    tags:\n      - Avro\n      - JSON Schema\n      - Protobuf\n      - Schema Registry\n    serviceName: Confluent Schema Registry REST API\n    serviceCategory: API\n  - name: Kafka Connect REST API\n    baseURL: https://localhost:8083\n    tags:\n      - Connectors\n      - Kafka Connect\n      - REST\n    serviceName: Kafka Connect REST API\n    serviceCategory: API\n  - name: ksqlDB REST API\n    baseURL: https://localhost:8088\n    tags:\n      - ksqlDB\n      - REST\n      - Streaming SQL\n    serviceName: ksqlDB REST API\n    serviceCategory: API\n  - name: Confluent Cloud for Apache Flink REST API\n    baseURL: https://flink.region.aws.confluent.cloud\n    tags:\n      - Apache Flink\n      - Stream Processing\n    serviceName: Confluent Cloud for Apache\
  \ Flink REST API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/confluent-the-data-streaming-platform/refs/heads/main/finops/confluent-the-data-streaming-platform-finops.yml
sources: []
specification: FinOps Framework
tags:
- Apache Flink
- Apache Kafka
- Confluent Cloud
- Connectors
- Data Streaming
- Event Streaming
- Kafka Connect
- ksqlDB
- Real-Time Data
- REST
- Schema Registry
- Stream Processing
- FinOps
- Cost Management
- FOCUS
---
