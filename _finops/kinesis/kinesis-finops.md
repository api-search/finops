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
  - Tax
  - Adjustment
  - Credit
  pricingCategory: Pay-As-You-Go
description: 'FOCUS-aligned FinOps for AWS Kinesis: pure pay-as-you-go billed via the AWS consolidated invoice, with three Data Streams capacity modes (On-Demand Standard, On-Demand Advantage, Provisioned) and per-GB Firehose delivery. Reservations / Savings Plans do not apply.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Amazon Web Services, Inc.
  ProviderName: AWS
  PublisherName: Amazon Web Services, Inc.
  RegionId: aws-region
  ServiceCategory: Analytics
  ServiceName: Amazon Kinesis
  ServiceSubcategory: Streaming Data
layout: finops
meters:
- aggregation: sum
  dimensions:
  - region
  - stream
  - capacity_mode
  name: kds_shard_hours
  unit: shard-hour
- aggregation: sum
  dimensions:
  - region
  - stream
  - capacity_mode
  name: kds_stream_hours
  unit: stream-hour
- aggregation: sum
  dimensions:
  - region
  - stream
  name: kds_put_payload_units
  unit: payload-unit
- aggregation: sum
  dimensions:
  - region
  - stream
  name: kds_data_in_gb
  unit: GB
- aggregation: sum
  dimensions:
  - region
  - stream
  name: kds_data_out_gb
  unit: GB
- aggregation: sum
  dimensions:
  - region
  - stream
  - consumer
  name: kds_efo_consumer_shard_hours
  unit: consumer-shard-hour
- aggregation: sum
  dimensions:
  - region
  - stream
  name: kds_extended_retention_shard_hours
  unit: shard-hour
- aggregation: sum
  dimensions:
  - region
  - stream
  name: kds_long_term_storage_gb_month
  unit: GB-month
- aggregation: sum
  dimensions:
  - region
  - delivery_stream
  - source_type
  name: firehose_ingested_gb
  unit: GB
- aggregation: sum
  dimensions:
  - region
  - delivery_stream
  name: firehose_format_conversion_gb
  unit: GB
- aggregation: sum
  dimensions:
  - region
  - delivery_stream
  name: firehose_dynamic_partitioning_gb
  unit: GB
name: Kinesis Finops
provider_name: AWS Kinesis
provider_slug: kinesis
publisher_name: Amazon Web Services, Inc.
service_category: Streaming Data
slug: kinesis-finops
source_filename: kinesis-finops.yml
source_heading: FinOps Profile
source_url: https://aws.amazon.com/kinesis/data-streams/pricing/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: AWS Kinesis\nproviderId: kinesis\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Streaming\n  - AWS\n  - Real-Time\ndescription: 'FOCUS-aligned FinOps for AWS Kinesis: pure pay-as-you-go billed via the AWS consolidated\n  invoice, with three Data Streams capacity modes (On-Demand Standard, On-Demand Advantage, Provisioned)\n  and per-GB Firehose delivery. Reservations / Savings Plans do not apply.'\nsources:\n  - https://aws.amazon.com/kinesis/data-streams/pricing/\n  - https://aws.amazon.com/kinesis/data-firehose/pricing/\n  - https://docs.aws.amazon.com/streams/latest/dev/service-sizes-and-limits.html\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\n\
  publisherName: Amazon Web Services, Inc.\nserviceCategory: Streaming Data\nbillingModel:\n  pricingCategory: Pay-As-You-Go\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Tax\n    - Adjustment\n    - Credit\nfocusColumns:\n  ServiceName: Amazon Kinesis\n  ServiceCategory: Analytics\n  ServiceSubcategory: Streaming Data\n  ProviderName: AWS\n  PublisherName: Amazon Web Services, Inc.\n  InvoiceIssuerName: Amazon Web Services, Inc.\n  BillingCurrency: USD\n  RegionId: aws-region\nmeters:\n  - name: kds_shard_hours\n    unit: shard-hour\n    aggregation: sum\n    dimensions:\n      - region\n      - stream\n      - capacity_mode\n  - name: kds_stream_hours\n    unit: stream-hour\n    aggregation: sum\n    dimensions:\n      - region\n      - stream\n      - capacity_mode\n  - name: kds_put_payload_units\n    unit: payload-unit\n    aggregation: sum\n    dimensions:\n      - region\n      - stream\n  - name: kds_data_in_gb\n    unit: GB\n    aggregation:\
  \ sum\n    dimensions:\n      - region\n      - stream\n  - name: kds_data_out_gb\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - region\n      - stream\n  - name: kds_efo_consumer_shard_hours\n    unit: consumer-shard-hour\n    aggregation: sum\n    dimensions:\n      - region\n      - stream\n      - consumer\n  - name: kds_extended_retention_shard_hours\n    unit: shard-hour\n    aggregation: sum\n    dimensions:\n      - region\n      - stream\n  - name: kds_long_term_storage_gb_month\n    unit: GB-month\n    aggregation: sum\n    dimensions:\n      - region\n      - stream\n  - name: firehose_ingested_gb\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - region\n      - delivery_stream\n      - source_type\n  - name: firehose_format_conversion_gb\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - region\n      - delivery_stream\n  - name: firehose_dynamic_partitioning_gb\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - region\n    \
  \  - delivery_stream\nprinciples:\n  - name: Visibility\n    description: Use AWS Cost Explorer with usage-type filters (Kinesis-PUT-units, Kinesis-shardHourUsage,\n      Firehose-DataIngested) and CloudWatch Kinesis metrics (IncomingBytes, IncomingRecords, GetRecords.IteratorAgeMilliseconds)\n      to tie cost to throughput.\n  - name: Allocation\n    description: Apply cost-allocation tags (Owner, Team, Environment) to every stream and Firehose delivery\n      stream; activate them in Cost Allocation Tags so CUR/FOCUS exports can split spend per consuming\n      team.\n  - name: Optimization\n    description: Switch low-volume streams to On-Demand to avoid over-provisioned shards; for steady high\n      throughput, use Provisioned with Application Auto Scaling on shard count, or move to On-Demand Advantage\n      to bundle Enhanced Fan-Out without per-stream-hour fees.\n  - name: Accountability\n    description: Stream owners review monthly Cost & Usage Report Kinesis line items, alert\
  \ on shard-hour\n      spikes via CloudWatch billing alarms, and rebalance shards or capacity mode at the next change window\n      (max two switches per 24h per stream).\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/kinesis/refs/heads/main/finops/kinesis-finops.yml
sources:
- https://aws.amazon.com/kinesis/data-streams/pricing/
- https://aws.amazon.com/kinesis/data-firehose/pricing/
- https://docs.aws.amazon.com/streams/latest/dev/service-sizes-and-limits.html
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Streaming
- Real-Time
---
