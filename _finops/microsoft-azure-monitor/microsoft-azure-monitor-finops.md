---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: metrics_API.json
  format: json
  label: Azure Monitor Metrics API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/Azure/azure-rest-api-specs/main/specification/monitor/resource-manager/Microsoft.Insights/stable/2023-10-01/metrics_API.json
- filename: metricDefinitions_API.json
  format: json
  label: Azure Monitor Metric Definitions API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/Azure/azure-rest-api-specs/main/specification/monitor/resource-manager/Microsoft.Insights/stable/2023-10-01/metricDefinitions_API.json
- filename: azure-monitor-metrics-batch-openapi.yml
  format: yaml
  label: Azure Monitor Metrics Batch API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-azure-monitor/refs/heads/main/openapi/azure-monitor-metrics-batch-openapi.yml
- filename: OperationalInsights.json
  format: json
  label: Azure Monitor Logs API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/Azure/azure-rest-api-specs/main/specification/operationalinsights/data-plane/Microsoft.OperationalInsights/stable/2022-10-27/OperationalInsights.json
- filename: azure-monitor-logs-ingestion-openapi.yml
  format: yaml
  label: Azure Monitor Logs Ingestion API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-azure-monitor/refs/heads/main/openapi/azure-monitor-logs-ingestion-openapi.yml
- filename: alertRules_API.json
  format: json
  label: Azure Monitor Alerts API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/Azure/azure-rest-api-specs/main/specification/monitor/resource-manager/Microsoft.Insights/stable/2016-03-01/alertRules_API.json
- filename: scheduledQueryRule_API.json
  format: json
  label: Azure Monitor Scheduled Query Rules API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/Azure/azure-rest-api-specs/main/specification/monitor/resource-manager/Microsoft.Insights/stable/2021-08-01/scheduledQueryRule_API.json
- filename: actionGroups_API.json
  format: json
  label: Azure Monitor Action Groups API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/Azure/azure-rest-api-specs/main/specification/monitor/resource-manager/Microsoft.Insights/stable/2022-06-01/actionGroups_API.json
- filename: autoscale_API.json
  format: json
  label: Azure Monitor Autoscale API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/Azure/azure-rest-api-specs/main/specification/monitor/resource-manager/Microsoft.Insights/stable/2022-10-01/autoscale_API.json
- filename: AppInsights.json
  format: json
  label: Azure Application Insights API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/Azure/azure-rest-api-specs/main/specification/applicationinsights/data-plane/Microsoft.Insights/stable/v1/AppInsights.json
- filename: diagnosticsSettings_API.json
  format: json
  label: Azure Monitor Diagnostic Settings API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/Azure/azure-rest-api-specs/main/specification/monitor/resource-manager/Microsoft.Insights/stable/2021-05-01-preview/diagnosticsSettings_API.json
- filename: activityLogs_API.json
  format: json
  label: Azure Monitor Activity Log API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/Azure/azure-rest-api-specs/main/specification/monitor/resource-manager/Microsoft.Insights/stable/2015-04-01/activityLogs_API.json
- filename: dataCollectionRules_API.json
  format: json
  label: Azure Monitor Data Collection Rules API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/Azure/azure-rest-api-specs/main/specification/monitor/resource-manager/Microsoft.Insights/stable/2023-03-11/dataCollectionRules_API.json
- filename: dataCollectionEndpoints_API.json
  format: json
  label: Azure Monitor Data Collection Endpoints API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/Azure/azure-rest-api-specs/main/specification/monitor/resource-manager/Microsoft.Insights/stable/2023-03-11/dataCollectionEndpoints_API.json
- filename: azure-monitor-private-link-scopes-openapi.yml
  format: yaml
  label: Azure Monitor Private Link Scopes API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-azure-monitor/refs/heads/main/openapi/azure-monitor-private-link-scopes-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  - Tax
  - Adjustment
  - Credit
  pricingCategory: Pay-As-You-Go + Committed Use
description: 'FOCUS-aligned FinOps for Azure Monitor: per-GB ingestion + per-GB-month retention on Log Analytics (Analytics PAYG, Basic, Archive) with optional daily Commitment Tiers, plus per-million-sample custom metrics and per-rule alert pricing.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Microsoft Corporation
  ProviderName: Microsoft
  PublisherName: Microsoft Corporation
  ServiceCategory: Observability
  ServiceName: Azure Monitor
layout: finops
meters:
- aggregation: sum
  dimensions:
  - workspace
  - region
  - table
  - source
  name: analytics_logs_ingestion_gb
  unit: GB
- aggregation: sum
  dimensions:
  - workspace
  - table
  name: basic_logs_ingestion_gb
  unit: GB
- aggregation: avg
  dimensions:
  - workspace
  - tier
  name: log_retention_gb_month
  unit: GB-month
- aggregation: avg
  dimensions:
  - workspace
  name: log_archive_gb_month
  unit: GB-month
- aggregation: sum
  dimensions:
  - workspace
  name: basic_logs_search_gb
  unit: GB
- aggregation: sum
  dimensions:
  - resource
  - region
  name: custom_metrics_samples
  unit: sample
- aggregation: max
  dimensions:
  - rule_type
  - severity
  name: alert_rules
  unit: rule-month
- aggregation: sum
  dimensions:
  - channel
  name: notification_messages
  unit: message
name: Microsoft Azure Monitor Finops
provider_name: Azure Monitor
provider_slug: microsoft-azure-monitor
publisher_name: Microsoft Corporation
service_category: Observability / Monitoring
slug: microsoft-azure-monitor-finops
source_filename: microsoft-azure-monitor-finops.yml
source_heading: FinOps Profile
source_url: https://azure.microsoft.com/en-us/pricing/details/monitor/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Azure Monitor\nproviderId: microsoft-azure-monitor\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Observability\n  - Microsoft Azure\ndescription: 'FOCUS-aligned FinOps for Azure Monitor: per-GB ingestion + per-GB-month retention on\n  Log Analytics (Analytics PAYG, Basic, Archive) with optional daily Commitment Tiers, plus per-million-sample\n  custom metrics and per-rule alert pricing.'\nsources:\n  - https://azure.microsoft.com/en-us/pricing/details/monitor/\n  - https://learn.microsoft.com/en-us/azure/azure-monitor/logs/cost-logs\n  - https://learn.microsoft.com/en-us/azure/azure-monitor/fundamentals/cost-usage\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\n\
  publisherName: Microsoft Corporation\nserviceCategory: Observability / Monitoring\nbillingModel:\n  pricingCategory: Pay-As-You-Go + Committed Use\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Adjustment\n    - Credit\nfocusColumns:\n  ServiceName: Azure Monitor\n  ServiceCategory: Observability\n  ProviderName: Microsoft\n  PublisherName: Microsoft Corporation\n  InvoiceIssuerName: Microsoft Corporation\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: analytics_logs_ingestion_gb\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - workspace\n      - region\n      - table\n      - source\n  - name: basic_logs_ingestion_gb\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - workspace\n      - table\n  - name: log_retention_gb_month\n    unit: GB-month\n    aggregation: avg\n    dimensions:\n      - workspace\n      - tier\n  - name: log_archive_gb_month\n    unit: GB-month\n\
  \    aggregation: avg\n    dimensions:\n      - workspace\n  - name: basic_logs_search_gb\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - workspace\n  - name: custom_metrics_samples\n    unit: sample\n    aggregation: sum\n    dimensions:\n      - resource\n      - region\n  - name: alert_rules\n    unit: rule-month\n    aggregation: max\n    dimensions:\n      - rule_type\n      - severity\n  - name: notification_messages\n    unit: message\n    aggregation: sum\n    dimensions:\n      - channel\nprinciples:\n  - name: Visibility\n    description: Use Azure Monitor's Usage and Estimated Costs pane and Cost Management to break\n      down spend by workspace, table, and resource type; the Usage table inside the workspace gives\n      per-table GB ingested.\n  - name: Allocation\n    description: Use multi-workspace, multi-resource-group designs aligned to teams; tag workspaces\n      with cost-center; route per-application telemetry to per-team workspaces; use cluster-level\n\
  \      commit pooling across workspaces.\n  - name: Optimization\n    description: Switch verbose tables to Basic Logs; archive cold data; tune Application Insights\n      sampling; use Data Collection Rule transformations to drop noisy columns; right-size Commitment\n      Tier; set daily caps; pre-aggregate custom metrics.\n  - name: Accountability\n    description: Assign workspace owners as cost owners; alert on daily ingestion drift; review\n      Commitment Tier vs PAYG break-even quarterly; review unused alert rules and stale data sources\n      monthly.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/microsoft-azure-monitor/refs/heads/main/finops/microsoft-azure-monitor-finops.yml
sources:
- https://azure.microsoft.com/en-us/pricing/details/monitor/
- https://learn.microsoft.com/en-us/azure/azure-monitor/logs/cost-logs
- https://learn.microsoft.com/en-us/azure/azure-monitor/fundamentals/cost-usage
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Observability
- Microsoft Azure
---
