---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: amazon-kinesis-data-streams-openapi-original.yml
  format: yaml
  label: Amazon Kinesis Data Streams API
  slug: data-streams-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/kinesis/refs/heads/main/openapi/amazon-kinesis-data-streams-openapi-original.yml
- filename: amazon-data-firehose-openapi-original.yml
  format: yaml
  label: Amazon Data Firehose API
  slug: data-firehose-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/kinesis/refs/heads/main/openapi/amazon-data-firehose-openapi-original.yml
- filename: amazon-kinesis-data-analytics-openapi-original.yml
  format: yaml
  label: Amazon Kinesis Data Analytics API
  slug: data-analytics-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/kinesis/refs/heads/main/openapi/amazon-kinesis-data-analytics-openapi-original.yml
- filename: amazon-kinesis-video-streams-openapi-original.yml
  format: yaml
  label: Amazon Kinesis Video Streams API
  slug: video-streams-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/kinesis/refs/heads/main/openapi/amazon-kinesis-video-streams-openapi-original.yml
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
description: FinOps framework definition for the AWS Kinesis API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: AWS Kinesis
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: AWS Kinesis
  PublisherName: AWS Kinesis
  ServiceCategory: Developer Tools / API
  ServiceName: AWS Kinesis
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
name: Kinesis Finops
provider_name: AWS Kinesis
provider_slug: kinesis
publisher_name: AWS Kinesis
service_category: API
slug: kinesis-finops
source_filename: kinesis-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: AWS Kinesis\nproviderId: kinesis\npublisherName: AWS Kinesis\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Analytics\n  - Apache Flink\n  - AWS\n  - Big Data\n  - Data Processing\n  - Real-Time\n  - Streaming\n  - Video\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the AWS Kinesis API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description:\
  \ Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n\
  \    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: AWS Kinesis\n  ServiceCategory: Developer Tools / API\n  ProviderName: AWS Kinesis\n  PublisherName: AWS Kinesis\n  InvoiceIssuerName: AWS Kinesis\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n\
  \    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Amazon Kinesis Data Streams API\n    baseURL: https://kinesis.{region}.amazonaws.com\n    tags:\n      - Data Streams\n      - Ingestion\n      - Real-Time\n      - Streaming\n    serviceName: Amazon Kinesis Data Streams API\n    serviceCategory: API\n  - name: Amazon Data Firehose API\n    baseURL: https://firehose.{region}.amazonaws.com\n    tags:\n      - Data Delivery\n      - ETL\n      - Streaming\n    serviceName: Amazon Data Firehose API\n    serviceCategory: API\n  - name: Amazon Kinesis Data Analytics API\n    baseURL: https://kinesisanalytics.{region}.amazonaws.com\n    tags:\n      - Analytics\n      - Apache Flink\n      - SQL\n      - Streaming\n    serviceName:\
  \ Amazon Kinesis Data Analytics API\n    serviceCategory: API\n  - name: Amazon Managed Service for Apache Flink API\n    baseURL: https://kinesisanalytics.{region}.amazonaws.com\n    tags:\n      - Analytics\n      - Apache Flink\n      - Real-Time\n      - Streaming\n    serviceName: Amazon Managed Service for Apache Flink API\n    serviceCategory: API\n  - name: Amazon Kinesis Video Streams API\n    baseURL: https://kinesisvideo.{region}.amazonaws.com\n    tags:\n      - IoT\n      - Machine Learning\n      - Streaming\n      - Video\n      - WebRTC\n    serviceName: Amazon Kinesis Video Streams API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/kinesis/refs/heads/main/finops/kinesis-finops.yml
sources: []
specification: FinOps Framework
tags:
- Analytics
- Apache Flink
- Big Data
- Data Processing
- Real-Time
- Streaming
- Video
- FinOps
- Cost Management
- FOCUS
---
