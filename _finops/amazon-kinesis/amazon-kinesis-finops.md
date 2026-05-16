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
  slug: amazon-kinesis-data-streams
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/amazon-kinesis/refs/heads/main/openapi/amazon-kinesis-data-streams-openapi.yml
- filename: openapi.yaml
  format: yaml
  label: Amazon Data Firehose
  slug: amazon-data-firehose
  spec_type: OpenAPI
  url: https://api.apis.guru/v2/specs/amazonaws.com/firehose/2015-08-04/openapi.yaml
- filename: openapi.yaml
  format: yaml
  label: Amazon Managed Service for Apache Flink
  slug: amazon-managed-service-for-apache-flink
  spec_type: OpenAPI
  url: https://api.apis.guru/v2/specs/amazonaws.com/kinesisanalyticsv2/2018-05-23/openapi.yaml
- filename: openapi.yaml
  format: yaml
  label: Amazon Kinesis Video Streams
  slug: amazon-kinesis-video-streams
  spec_type: OpenAPI
  url: https://api.apis.guru/v2/specs/amazonaws.com/kinesisvideo/2017-09-30/openapi.yaml
- filename: openapi.yaml
  format: yaml
  label: Amazon Kinesis Video Streams Media
  slug: amazon-kinesis-video-streams-media
  spec_type: OpenAPI
  url: https://api.apis.guru/v2/specs/amazonaws.com/kinesis-video-media/2017-09-30/openapi.yaml
- filename: openapi.yaml
  format: yaml
  label: Amazon Kinesis Video Streams Archived Media
  slug: amazon-kinesis-video-streams-archived-media
  spec_type: OpenAPI
  url: https://api.apis.guru/v2/specs/amazonaws.com/kinesis-video-archived-media/2017-09-30/openapi.yaml
- filename: openapi.yaml
  format: yaml
  label: Amazon Kinesis Video Signaling Channels
  slug: amazon-kinesis-video-signaling-channels
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
  pricingCategory: Pay-As-You-Go
description: 'FOCUS-aligned FinOps for Amazon Kinesis Data Streams: per-GB ingest/retrieval and per-shard-hour charges across On-Demand and Provisioned modes, with separately metered Enhanced Fan-Out, extended retention, and long-term storage.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Amazon Web Services, Inc.
  ProviderName: AWS
  PublisherName: Amazon Web Services, Inc.
  ServiceCategory: Analytics
  ServiceName: Amazon Kinesis Data Streams
  ServiceSubcategory: Streaming
layout: finops
meters:
- aggregation: sum
  dimensions:
  - region
  - stream_name
  - capacity_mode
  name: data_ingested_gb
  unit: GB
- aggregation: sum
  dimensions:
  - region
  - stream_name
  - consumer_type
  name: data_retrieved_gb
  unit: GB
- aggregation: sum
  dimensions:
  - region
  - stream_name
  name: shard_hours
  unit: shard-hour
- aggregation: sum
  dimensions:
  - region
  - stream_name
  - capacity_mode
  name: stream_hours
  unit: stream-hour
- aggregation: sum
  dimensions:
  - region
  - stream_name
  name: put_payload_units
  unit: PUT-payload-unit
- aggregation: sum
  dimensions:
  - region
  - stream_name
  - consumer_arn
  name: efo_consumer_shard_hours
  unit: consumer-shard-hour
- aggregation: sum
  dimensions:
  - region
  - stream_name
  name: long_term_storage_gb_month
  unit: GB-month
name: Amazon Kinesis Finops
provider_name: Amazon Kinesis
provider_slug: amazon-kinesis
publisher_name: Amazon Web Services, Inc.
service_category: Analytics / Streaming
slug: amazon-kinesis-finops
source_filename: amazon-kinesis-finops.yml
source_heading: FinOps Profile
source_url: https://aws.amazon.com/kinesis/data-streams/pricing/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Amazon Kinesis\nproviderId: amazon-kinesis\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - AWS\n  - Streaming\n  - Kinesis\n  - Cost Management\ndescription: 'FOCUS-aligned FinOps for Amazon Kinesis Data Streams: per-GB ingest/retrieval and per-shard-hour\n  charges across On-Demand and Provisioned modes, with separately metered Enhanced Fan-Out, extended\n  retention, and long-term storage.'\nsources:\n  - https://aws.amazon.com/kinesis/data-streams/pricing/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Amazon Web Services, Inc.\nserviceCategory: Analytics / Streaming\nbillingModel:\n  pricingCategory: Pay-As-You-Go\n  billingFrequency:\
  \ Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\nfocusColumns:\n  ServiceName: Amazon Kinesis Data Streams\n  ServiceCategory: Analytics\n  ServiceSubcategory: Streaming\n  ProviderName: AWS\n  PublisherName: Amazon Web Services, Inc.\n  InvoiceIssuerName: Amazon Web Services, Inc.\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: data_ingested_gb\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - region\n      - stream_name\n      - capacity_mode\n  - name: data_retrieved_gb\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - region\n      - stream_name\n      - consumer_type\n  - name: shard_hours\n    unit: shard-hour\n    aggregation: sum\n    dimensions:\n      - region\n      - stream_name\n  - name: stream_hours\n    unit: stream-hour\n    aggregation: sum\n    dimensions:\n      - region\n      - stream_name\n      - capacity_mode\n  - name: put_payload_units\n\
  \    unit: PUT-payload-unit\n    aggregation: sum\n    dimensions:\n      - region\n      - stream_name\n  - name: efo_consumer_shard_hours\n    unit: consumer-shard-hour\n    aggregation: sum\n    dimensions:\n      - region\n      - stream_name\n      - consumer_arn\n  - name: long_term_storage_gb_month\n    unit: GB-month\n    aggregation: sum\n    dimensions:\n      - region\n      - stream_name\nprinciples:\n  - name: Visibility\n    description: Use CloudWatch Kinesis metrics (IncomingBytes, IncomingRecords, GetRecords.IteratorAgeMilliseconds)\n      and the AWS CUR / FOCUS export for per-stream cost.\n  - name: Allocation\n    description: Tag streams with Environment, Team, Pipeline; enable cost allocation tags in Billing.\n  - name: Optimization\n    description: Choose On-Demand for spiky workloads, Provisioned for steady throughput; aggregate small\n      records via KPL to reduce PUT payload units; size retention to match consumer SLA; consider On-Demand\n      Advantage at\
  \ over 25 MB/s baseline.\n  - name: Accountability\n    description: Set AWS Budgets per stream tag, alert on iterator-age (consumer lag), and review monthly\n      shard utilization for right-sizing.\nmaintainers:\n  - name: Kin Lane\n    email: kin@apievangelist.com\n    url: https://apievangelist.com\n  - name: Amazon Web Services\n    email: support@aws.amazon.com\n    url: https://aws.amazon.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/amazon-kinesis/refs/heads/main/finops/amazon-kinesis-finops.yml
sources:
- https://aws.amazon.com/kinesis/data-streams/pricing/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Streaming
- Kinesis
- Cost Management
---
