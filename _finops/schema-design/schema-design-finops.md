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
description: FinOps framework definition for the Schema Design API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Schema Design
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Schema Design
  PublisherName: Schema Design
  ServiceCategory: Developer Tools / API
  ServiceName: Schema Design
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
name: Schema Design Finops
provider_name: Schema Design
provider_slug: schema-design
publisher_name: Schema Design
service_category: API
slug: schema-design-finops
source_filename: schema-design-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Schema Design\nproviderId: schema-design\npublisherName: Schema Design\nserviceCategory: API\ncreated: '2026-05-04'\nmodified: '2026-05-04'\ntags:\n  - Schema Design\n  - Data Modeling\n  - API Design\n  - JSON Schema\n  - OpenAPI\n  - GraphQL\n  - Data Validation\n  - Type Systems\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Schema Design API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n \
  \ - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n\
  \  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Schema Design\n  ServiceCategory: Developer Tools / API\n  ProviderName: Schema Design\n  PublisherName: Schema Design\n  InvoiceIssuerName: Schema Design\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description:\
  \ Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: JSON Schema Specification\n    baseURL: https://json-schema.org\n    tags:\n      - JSON Schema\n      - Validation\n      - Specification\n    serviceName: JSON Schema Specification\n    serviceCategory: API\n  - name: OpenAPI Schema Objects\n    baseURL: https://spec.openapis.org\n    tags:\n      - OpenAPI\n      - REST\n      - API Design\n      - Schema\n    serviceName: OpenAPI Schema Objects\n    serviceCategory: API\n  - name: GraphQL Type System\n    baseURL: https://graphql.org\n    tags:\n      - GraphQL\n      - Type System\n      - API Design\n      - Schema\n    serviceName: GraphQL Type System\n    serviceCategory:\
  \ API\n  - name: Apache Avro Schema\n    baseURL: https://avro.apache.org\n    tags:\n      - Avro\n      - Event Streaming\n      - Kafka\n      - Serialization\n    serviceName: Apache Avro Schema\n    serviceCategory: API\n  - name: Protocol Buffers (Protobuf) Schema\n    baseURL: https://protobuf.dev\n    tags:\n      - Protobuf\n      - gRPC\n      - Serialization\n      - API Design\n    serviceName: Protocol Buffers (Protobuf) Schema\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: API Evangelist\n    email: info@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/schema-design/refs/heads/main/finops/schema-design-finops.yml
sources: []
specification: FinOps Framework
tags:
- Schema Design
- Data Modeling
- API Design
- JSON Schema
- OpenAPI
- GraphQL
- Data Validation
- Type Systems
- FinOps
- Cost Management
- FOCUS
---
