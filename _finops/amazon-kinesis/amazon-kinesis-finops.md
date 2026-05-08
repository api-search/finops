---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: amazon-kinesis-data-streams-openapi.yml
  format: yaml
  label: Amazon Kinesis Data Streams
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/amazon-kinesis/refs/heads/main/openapi/amazon-kinesis-data-streams-openapi.yml
- filename: openapi.yaml
  format: yaml
  label: Amazon Data Firehose
  slug: ''
  spec_type: OpenAPI
  url: https://api.apis.guru/v2/specs/amazonaws.com/firehose/2015-08-04/openapi.yaml
- filename: openapi.yaml
  format: yaml
  label: Amazon Managed Service for Apache Flink
  slug: ''
  spec_type: OpenAPI
  url: https://api.apis.guru/v2/specs/amazonaws.com/kinesisanalyticsv2/2018-05-23/openapi.yaml
- filename: openapi.yaml
  format: yaml
  label: Amazon Kinesis Video Streams
  slug: ''
  spec_type: OpenAPI
  url: https://api.apis.guru/v2/specs/amazonaws.com/kinesisvideo/2017-09-30/openapi.yaml
- filename: openapi.yaml
  format: yaml
  label: Amazon Kinesis Video Streams Media
  slug: ''
  spec_type: OpenAPI
  url: https://api.apis.guru/v2/specs/amazonaws.com/kinesis-video-media/2017-09-30/openapi.yaml
- filename: openapi.yaml
  format: yaml
  label: Amazon Kinesis Video Streams Archived Media
  slug: ''
  spec_type: OpenAPI
  url: https://api.apis.guru/v2/specs/amazonaws.com/kinesis-video-archived-media/2017-09-30/openapi.yaml
- filename: openapi.yaml
  format: yaml
  label: Amazon Kinesis Video Signaling Channels
  slug: ''
  spec_type: OpenAPI
  url: https://api.apis.guru/v2/specs/amazonaws.com/kinesis-video-signaling/2019-12-04/openapi.yaml
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
description: FinOps framework definition for the Amazon Kinesis API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Amazon Kinesis
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Amazon Kinesis
  PublisherName: Amazon Kinesis
  ServiceCategory: Developer Tools / API
  ServiceName: Amazon Kinesis
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
name: Amazon Kinesis Finops
provider_name: Amazon Kinesis
provider_slug: amazon-kinesis
publisher_name: Amazon Kinesis
service_category: API
slug: amazon-kinesis-finops
source_filename: amazon-kinesis-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Amazon Kinesis\nproviderId: amazon-kinesis\npublisherName: Amazon Kinesis\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Analytics\n  - Big Data\n  - Data Processing\n  - Real-Time\n  - Streaming\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Amazon Kinesis API surface. Provides a FOCUS-aligned\n  mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable\
  \ API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n\
  \      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Amazon Kinesis\n  ServiceCategory: Developer Tools / API\n  ProviderName: Amazon Kinesis\n  PublisherName: Amazon Kinesis\n  InvoiceIssuerName: Amazon Kinesis\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n\
  \    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Amazon Kinesis Data Streams\n    baseURL: https://kinesis.amazonaws.com\n    tags:\n      - Data Ingestion\n      - Real-Time\n      - Streams\n    serviceName: Amazon Kinesis Data Streams\n    serviceCategory: API\n  - name: Amazon Data Firehose\n    baseURL: https://firehose.amazonaws.com\n    tags:\n      - Data Loading\n      - ETL\n      - Streaming\n    serviceName: Amazon Data Firehose\n    serviceCategory: API\n  - name: Amazon Managed Service for Apache Flink\n    baseURL: https://kinesisanalytics.amazonaws.com\n    tags:\n      - Analytics\n      - Apache Flink\n      - SQL\n      - Stream Processing\n    serviceName: Amazon Managed Service for Apache Flink\n\
  \    serviceCategory: API\n  - name: Amazon Kinesis Video Streams\n    baseURL: https://kinesisvideo.amazonaws.com\n    tags:\n      - IoT\n      - Machine Learning\n      - Streaming\n      - Video\n    serviceName: Amazon Kinesis Video Streams\n    serviceCategory: API\n  - name: Amazon Kinesis Video Streams Media\n    baseURL: https://kinesisvideo.amazonaws.com\n    tags:\n      - Media\n      - Real-Time\n      - Streaming\n      - Video\n    serviceName: Amazon Kinesis Video Streams Media\n    serviceCategory: API\n  - name: Amazon Kinesis Video Streams Archived Media\n    baseURL: https://kinesisvideo.amazonaws.com\n    tags:\n      - Archived Media\n      - DASH\n      - HLS\n      - Playback\n      - Video\n    serviceName: Amazon Kinesis Video Streams Archived Media\n    serviceCategory: API\n  - name: Amazon Kinesis Video Signaling Channels\n    baseURL: https://kinesisvideo.amazonaws.com\n    tags:\n      - Real-Time\n      - Signaling\n      - Video\n      - WebRTC\n    serviceName:\
  \ Amazon Kinesis Video Signaling Channels\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    url: http://apievangelist.com\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/amazon-kinesis/refs/heads/main/finops/amazon-kinesis-finops.yml
sources: []
specification: FinOps Framework
tags:
- Analytics
- Big Data
- Data Processing
- Real-Time
- Streaming
- FinOps
- Cost Management
- FOCUS
---
