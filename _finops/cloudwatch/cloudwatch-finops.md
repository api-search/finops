---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: openapi.yaml
  format: yaml
  label: Amazon CloudWatch API
  slug: amazon-cloudwatch-api
  spec_type: OpenAPI
  url: https://api.apis.guru/v2/specs/amazonaws.com/monitoring/2010-08-01/openapi.yaml
- filename: openapi.yaml
  format: yaml
  label: Amazon CloudWatch Logs API
  slug: amazon-cloudwatch-logs-api
  spec_type: OpenAPI
  url: https://api.apis.guru/v2/specs/amazonaws.com/logs/2014-03-28/openapi.yaml
- filename: openapi.yaml
  format: yaml
  label: Amazon CloudWatch Events API
  slug: amazon-cloudwatch-events-api
  spec_type: OpenAPI
  url: https://api.apis.guru/v2/specs/amazonaws.com/events/2015-10-07/openapi.yaml
- filename: openapi.yaml
  format: yaml
  label: Amazon CloudWatch Application Insights API
  slug: amazon-cloudwatch-application-insights-api
  spec_type: OpenAPI
  url: https://api.apis.guru/v2/specs/amazonaws.com/application-insights/2018-11-25/openapi.yaml
- filename: openapi.yaml
  format: yaml
  label: Amazon CloudWatch Synthetics API
  slug: amazon-cloudwatch-synthetics-api
  spec_type: OpenAPI
  url: https://api.apis.guru/v2/specs/amazonaws.com/synthetics/2017-10-11/openapi.yaml
- filename: openapi.yaml
  format: yaml
  label: Amazon CloudWatch Internet Monitor API
  slug: amazon-cloudwatch-internet-monitor-api
  spec_type: OpenAPI
  url: https://api.apis.guru/v2/specs/amazonaws.com/internetmonitor/2021-06-03/openapi.yaml
- filename: openapi.yaml
  format: yaml
  label: Amazon CloudWatch RUM API
  slug: amazon-cloudwatch-rum-api
  spec_type: OpenAPI
  url: https://api.apis.guru/v2/specs/amazonaws.com/rum/2018-05-10/openapi.yaml
- filename: openapi.yaml
  format: yaml
  label: Amazon CloudWatch Observability Access Manager API
  slug: amazon-cloudwatch-observability-access-manager-api
  spec_type: OpenAPI
  url: https://api.apis.guru/v2/specs/amazonaws.com/oam/2022-06-10/openapi.yaml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Tax
  - Adjustment
  - Refund
  - Credit
  pricingCategory: Pay-As-You-Go + Committed Use
description: 'FOCUS-aligned FinOps for Amazon CloudWatch: pure pay-as-you-go metering across metrics, API requests, alarms, logs (ingest / storage / query / Live Tail), dashboards, Contributor Insights, Synthetics, RUM, Application Signals, Internet Monitor and Network Flow Monitor. Costs land in AWS Cost and Usage Reports (CUR / CUR 2.0) under service code `AmazonCloudWatch` with usage-type granularity, and CloudWatch itself emits service-quota usage metrics that can be alarmed.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Amazon Web Services, Inc.
  PricingCategory: Usage-Based
  ProviderName: Amazon Web Services
  PublisherName: Amazon Web Services, Inc.
  ServiceCategory: Observability
  ServiceName: AmazonCloudWatch
layout: finops
meters:
- aggregation: max
  description: Custom and detailed-monitoring metrics, billed monthly with volume-tiered pricing.
  dimensions:
  - region
  - namespace
  - resolution
  name: custom_metrics
  unit: metric-month
- aggregation: sum
  description: CloudWatch API requests (PutMetricData, GetMetricData, GetMetricStatistics, ListMetrics, etc.).
  dimensions:
  - region
  - api_action
  name: api_requests
  unit: request
- aggregation: max
  description: Standard- and high-resolution alarm metrics.
  dimensions:
  - region
  - resolution
  name: alarm_metrics
  unit: alarm-month
- aggregation: sum
  description: Volume of log data ingested into CloudWatch Logs.
  dimensions:
  - region
  - log_group
  - log_class
  name: logs_ingested
  unit: GB
- aggregation: avg
  description: Archived log data retained beyond ingest.
  dimensions:
  - region
  - log_group
  - log_class
  name: logs_storage
  unit: GB-month
- aggregation: sum
  description: Bytes scanned by Logs Insights queries.
  dimensions:
  - region
  - log_group
  name: logs_insights_scanned
  unit: GB
- aggregation: sum
  description: Live Tail streaming session minutes.
  dimensions:
  - region
  name: live_tail_minutes
  unit: minute
- aggregation: max
  description: Contributor Insights rules and matched events.
  dimensions:
  - region
  name: contributor_insights_rules
  unit: rule-month
- aggregation: sum
  description: Synthetics canary runs.
  dimensions:
  - region
  - canary
  name: synthetics_canary_runs
  unit: run
- aggregation: sum
  description: CloudWatch RUM events recorded from end-user browsers.
  dimensions:
  - region
  - app_monitor
  name: rum_events
  unit: event
- aggregation: sum
  description: Application Signals telemetry ingestion volume.
  dimensions:
  - region
  name: application_signals_data
  unit: GB
name: Cloudwatch Finops
provider_name: AWS CloudWatch
provider_slug: cloudwatch
publisher_name: Amazon Web Services, Inc.
service_category: Observability
slug: cloudwatch-finops
source_filename: cloudwatch-finops.yml
source_heading: FinOps Profile
source_url: https://aws.amazon.com/cloudwatch/pricing/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: AWS CloudWatch\nproviderId: cloudwatch\npublisherName: Amazon Web Services, Inc.\nserviceCategory: Observability\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Aws\n  - Observability\n  - Cost Management\ndescription: 'FOCUS-aligned FinOps for Amazon CloudWatch: pure pay-as-you-go metering across metrics, API\n  requests, alarms, logs (ingest / storage / query / Live Tail), dashboards, Contributor Insights, Synthetics,\n  RUM, Application Signals, Internet Monitor and Network Flow Monitor. Costs land in AWS Cost and Usage\n  Reports (CUR / CUR 2.0) under service code `AmazonCloudWatch` with usage-type\
  \ granularity, and CloudWatch\n  itself emits service-quota usage metrics that can be alarmed.'\nsources:\n  - https://aws.amazon.com/cloudwatch/pricing/\n  - https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/cloudwatch_billing.html\n  - https://docs.aws.amazon.com/cur/latest/userguide/what-is-cur.html\nbillingModel:\n  pricingCategory: Pay-As-You-Go + Committed Use\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Tax\n    - Adjustment\n    - Refund\n    - Credit\nfocusColumns:\n  ServiceName: AmazonCloudWatch\n  ServiceCategory: Observability\n  ProviderName: Amazon Web Services\n  PublisherName: Amazon Web Services, Inc.\n  InvoiceIssuerName: Amazon Web Services, Inc.\n  PricingCategory: Usage-Based\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: custom_metrics\n    description: Custom and detailed-monitoring metrics, billed monthly with volume-tiered pricing.\n    unit: metric-month\n    aggregation: max\n\
  \    dimensions:\n      - region\n      - namespace\n      - resolution\n  - name: api_requests\n    description: CloudWatch API requests (PutMetricData, GetMetricData, GetMetricStatistics, ListMetrics,\n      etc.).\n    unit: request\n    aggregation: sum\n    dimensions:\n      - region\n      - api_action\n  - name: alarm_metrics\n    description: Standard- and high-resolution alarm metrics.\n    unit: alarm-month\n    aggregation: max\n    dimensions:\n      - region\n      - resolution\n  - name: logs_ingested\n    description: Volume of log data ingested into CloudWatch Logs.\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - region\n      - log_group\n      - log_class\n  - name: logs_storage\n    description: Archived log data retained beyond ingest.\n    unit: GB-month\n    aggregation: avg\n    dimensions:\n      - region\n      - log_group\n      - log_class\n  - name: logs_insights_scanned\n    description: Bytes scanned by Logs Insights queries.\n    unit: GB\n\
  \    aggregation: sum\n    dimensions:\n      - region\n      - log_group\n  - name: live_tail_minutes\n    description: Live Tail streaming session minutes.\n    unit: minute\n    aggregation: sum\n    dimensions:\n      - region\n  - name: contributor_insights_rules\n    description: Contributor Insights rules and matched events.\n    unit: rule-month\n    aggregation: max\n    dimensions:\n      - region\n  - name: synthetics_canary_runs\n    description: Synthetics canary runs.\n    unit: run\n    aggregation: sum\n    dimensions:\n      - region\n      - canary\n  - name: rum_events\n    description: CloudWatch RUM events recorded from end-user browsers.\n    unit: event\n    aggregation: sum\n    dimensions:\n      - region\n      - app_monitor\n  - name: application_signals_data\n    description: Application Signals telemetry ingestion volume.\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - region\nprinciples:\n  - name: Visibility\n    description: Use AWS Cost Explorer\
  \ and the Cost and Usage Report (CUR / CUR 2.0) filtered to service\n      `AmazonCloudWatch` for line-item visibility. CloudWatch also exposes its own usage metrics under the\n      `AWS/Usage` namespace so engineers can alarm on quota burn-down.\n  - name: Allocation\n    description: Tag log groups, alarms, dashboards and synthetics canaries; AWS-generated and user-defined\n      tags flow through to CUR for chargeback. Use Account/OU and Region as natural allocation dimensions.\n  - name: Optimization\n    description: Drop noisy log groups, set retention policies on archived logs, batch PutMetricData (up\n      to 1,000 data points per call), favor metric math over additional custom metrics, use CloudWatch Logs\n      Infrequent Access log class for cold logs, and consolidate alarms via composite alarms.\n  - name: Accountability\n    description: Assign per-team budget alerts in AWS Budgets keyed on the CloudWatch service filter; review\n      the top usage-types (DataProcessing-Bytes,\
  \ Requests, AlarmMonitorUsage, MetricMonitorUsage) monthly.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/cloudwatch/refs/heads/main/finops/cloudwatch-finops.yml
sources:
- https://aws.amazon.com/cloudwatch/pricing/
- https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/cloudwatch_billing.html
- https://docs.aws.amazon.com/cur/latest/userguide/what-is-cur.html
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Aws
- Observability
- Cost Management
---
