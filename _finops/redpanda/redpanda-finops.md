---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: redpanda-admin-cluster-openapi.json
  format: json
  label: Redpanda Admin API
  slug: redpanda-admin-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/redpanda/refs/heads/main/openapi/redpanda-admin-cluster-openapi.json
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
description: FinOps framework definition for the Redpanda API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Redpanda
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Redpanda
  PublisherName: Redpanda
  ServiceCategory: Developer Tools / API
  ServiceName: Redpanda
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
name: Redpanda Finops
provider_name: Redpanda
provider_slug: redpanda
publisher_name: Redpanda
service_category: API
slug: redpanda-finops
source_filename: redpanda-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Redpanda\nproviderId: redpanda\npublisherName: Redpanda\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Streaming\n  - Kafka\n  - Event Streaming\n  - Real-Time\n  - Data Platform\n  - Open Source\n  - C++\n  - Stream Processing\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Redpanda API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description:\
  \ Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n\
  \    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Redpanda\n  ServiceCategory: Developer Tools / API\n  ProviderName: Redpanda\n  PublisherName: Redpanda\n  InvoiceIssuerName: Redpanda\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n \
  \   unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Redpanda Kafka API\n    baseURL: ''\n    tags:\n      - Kafka\n      - Wire Protocol\n      - Producers\n      - Consumers\n    serviceName: Redpanda Kafka API\n    serviceCategory: API\n  - name: Redpanda Admin API\n    baseURL: ''\n    tags:\n      - Admin\n      - Cluster\n      - Brokers\n      - Configuration\n      - Operations\n    serviceName: Redpanda Admin API\n    serviceCategory: API\n  - name: Redpanda Schema Registry API\n    baseURL: ''\n    tags:\n      - Schema Registry\n      - Avro\n      - JSON Schema\n      - Protobuf\n    serviceName: Redpanda Schema Registry API\n    serviceCategory: API\n  - name: Redpanda HTTP Proxy (Pandaproxy) API\n    baseURL:\
  \ ''\n    tags:\n      - HTTP Proxy\n      - REST\n      - Producers\n      - Consumers\n    serviceName: Redpanda HTTP Proxy (Pandaproxy) API\n    serviceCategory: API\n  - name: Redpanda Cloud Control Plane API\n    baseURL: ''\n    tags:\n      - Cloud\n      - Control Plane\n      - Clusters\n      - Networks\n      - Organizations\n      - Resource Groups\n    serviceName: Redpanda Cloud Control Plane API\n    serviceCategory: API\n  - name: Redpanda Cloud Data Plane API\n    baseURL: ''\n    tags:\n      - Cloud\n      - Data Plane\n      - Topics\n      - ACLs\n      - Users\n    serviceName: Redpanda Cloud Data Plane API\n    serviceCategory: API\n  - name: Redpanda Console API\n    baseURL: ''\n    tags:\n      - Console\n      - UI\n      - Backend API\n    serviceName: Redpanda Console API\n    serviceCategory: API\n  - name: Redpanda Connect (Benthos) API\n    baseURL: ''\n    tags:\n      - Stream Processing\n      - Connectors\n      - Benthos\n      - ETL\n    serviceName:\
  \ Redpanda Connect (Benthos) API\n    serviceCategory: API\n  - name: Redpanda rpk CLI Surface\n    baseURL: ''\n    tags:\n      - CLI\n      - rpk\n      - Operations\n    serviceName: Redpanda rpk CLI Surface\n    serviceCategory: API\n  - name: Redpanda Iceberg Topic API\n    baseURL: ''\n    tags:\n      - Iceberg\n      - Lakehouse\n      - Tiered Storage\n    serviceName: Redpanda Iceberg Topic API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/redpanda/refs/heads/main/finops/redpanda-finops.yml
sources: []
specification: FinOps Framework
tags:
- Streaming
- Kafka
- Event Streaming
- Real-Time
- Data Platform
- Open Source
- C++
- Stream Processing
- FinOps
- Cost Management
- FOCUS
---
