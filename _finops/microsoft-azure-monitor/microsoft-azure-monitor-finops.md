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
  - Credit
  - Adjustment
  chargeFrequency: Recurring
  pricingCategory: Usage-Based
description: FinOps framework definition for the Azure Monitor API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Azure Monitor
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Azure Monitor
  PublisherName: Azure Monitor
  ServiceCategory: Developer Tools / API
  ServiceName: Azure Monitor
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
name: Microsoft Azure Monitor Finops
provider_name: Azure Monitor
provider_slug: microsoft-azure-monitor
publisher_name: Azure Monitor
service_category: API
slug: microsoft-azure-monitor-finops
source_filename: microsoft-azure-monitor-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Azure Monitor\nproviderId: microsoft-azure-monitor\npublisherName: Azure Monitor\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Application Insights\n  - Cloud\n  - Logs\n  - Metrics\n  - Monitoring\n  - Observability\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Azure Monitor API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description:\
  \ Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n\
  \    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Azure Monitor\n  ServiceCategory: Developer Tools / API\n  ProviderName: Azure Monitor\n  PublisherName: Azure Monitor\n  InvoiceIssuerName: Azure Monitor\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network\
  \ in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Azure Monitor Metrics API\n    baseURL: https://management.azure.com\n    tags:\n      - Metrics\n      - Performance\n      - Resource Monitoring\n      - Time Series\n    serviceName: Azure Monitor Metrics API\n    serviceCategory: API\n  - name: Azure Monitor Metric Definitions API\n    baseURL: https://management.azure.com\n    tags:\n      - Definitions\n      - Metadata\n      - Metrics\n      - Resource Monitoring\n    serviceName: Azure Monitor Metric Definitions API\n    serviceCategory: API\n  - name: Azure Monitor Metrics Batch API\n    baseURL: https://management.azure.com\n    tags:\n      - Batch\n      - High Volume\n      - Metrics\n\
  \      - Performance\n    serviceName: Azure Monitor Metrics Batch API\n    serviceCategory: API\n  - name: Azure Monitor Logs API\n    baseURL: https://api.loganalytics.io\n    tags:\n      - Analytics\n      - KQL\n      - Logs\n      - Query\n    serviceName: Azure Monitor Logs API\n    serviceCategory: API\n  - name: Azure Monitor Logs Ingestion API\n    baseURL: https://management.azure.com\n    tags:\n      - Custom Logs\n      - Data Collection\n      - Ingestion\n      - Logs\n    serviceName: Azure Monitor Logs Ingestion API\n    serviceCategory: API\n  - name: Azure Monitor Alerts API\n    baseURL: https://management.azure.com\n    tags:\n      - Action Groups\n      - Alerts\n      - Monitoring\n      - Notifications\n    serviceName: Azure Monitor Alerts API\n    serviceCategory: API\n  - name: Azure Monitor Scheduled Query Rules API\n    baseURL: https://management.azure.com\n    tags:\n      - Alerts\n      - Automation\n      - Log Search\n      - Scheduled Query\n    serviceName:\
  \ Azure Monitor Scheduled Query Rules API\n    serviceCategory: API\n  - name: Azure Monitor Action Groups API\n    baseURL: https://management.azure.com\n    tags:\n      - Action Groups\n      - Automation\n      - Notifications\n      - Webhooks\n    serviceName: Azure Monitor Action Groups API\n    serviceCategory: API\n  - name: Azure Monitor Autoscale API\n    baseURL: https://management.azure.com\n    tags:\n      - Autoscale\n      - Capacity Management\n      - Performance\n      - Scaling\n    serviceName: Azure Monitor Autoscale API\n    serviceCategory: API\n  - name: Azure Application Insights API\n    baseURL: https://api.applicationinsights.io\n    tags:\n      - APM\n      - Application Performance\n      - Telemetry\n      - Tracing\n    serviceName: Azure Application Insights API\n    serviceCategory: API\n  - name: Azure Monitor Diagnostic Settings API\n    baseURL: https://management.azure.com\n    tags:\n      - Configuration\n      - Diagnostics\n      - Logs\n  \
  \    - Routing\n    serviceName: Azure Monitor Diagnostic Settings API\n    serviceCategory: API\n  - name: Azure Monitor Activity Log API\n    baseURL: https://management.azure.com\n    tags:\n      - Activity Log\n      - Audit\n      - Compliance\n      - Events\n    serviceName: Azure Monitor Activity Log API\n    serviceCategory: API\n  - name: Azure Monitor Data Collection Rules API\n    baseURL: https://management.azure.com\n    tags:\n      - Configuration\n      - Data Collection\n      - Ingestion\n      - Rules\n    serviceName: Azure Monitor Data Collection Rules API\n    serviceCategory: API\n  - name: Azure Monitor Data Collection Endpoints API\n    baseURL: https://management.azure.com\n    tags:\n      - Configuration\n      - Data Collection\n      - Endpoints\n      - Ingestion\n    serviceName: Azure Monitor Data Collection Endpoints API\n    serviceCategory: API\n  - name: Azure Monitor Private Link Scopes API\n    baseURL: https://management.azure.com\n    tags:\n\
  \      - Configuration\n      - Networking\n      - Private Link\n      - Security\n    serviceName: Azure Monitor Private Link Scopes API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/microsoft-azure-monitor/refs/heads/main/finops/microsoft-azure-monitor-finops.yml
sources: []
specification: FinOps Framework
tags:
- Application Insights
- Cloud
- Logs
- Metrics
- Monitoring
- Observability
- FinOps
- Cost Management
- FOCUS
---
