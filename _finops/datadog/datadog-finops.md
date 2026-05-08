---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: datadog-api-openapi.yml
  format: yaml
  label: Datadog API
  slug: datadog-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/datadog/refs/heads/main/openapi/datadog-api-openapi.yml
- filename: datadog-metrics-openapi.yml
  format: yaml
  label: Datadog Metrics API
  slug: datadog-metrics-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/datadog/refs/heads/main/openapi/datadog-metrics-openapi.yml
- filename: datadog-logs-openapi.yml
  format: yaml
  label: Datadog Logs API
  slug: datadog-logs-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/datadog/refs/heads/main/openapi/datadog-logs-openapi.yml
- filename: datadog-events-openapi.yml
  format: yaml
  label: Datadog Events API
  slug: datadog-events-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/datadog/refs/heads/main/openapi/datadog-events-openapi.yml
- filename: datadog-monitors-openapi.yml
  format: yaml
  label: Datadog Monitors API
  slug: datadog-monitors-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/datadog/refs/heads/main/openapi/datadog-monitors-openapi.yml
- filename: datadog-incidents-openapi.yml
  format: yaml
  label: Datadog Incidents API
  slug: datadog-incidents-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/datadog/refs/heads/main/openapi/datadog-incidents-openapi.yml
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
description: FinOps framework definition for the Datadog API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Datadog
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Datadog
  PublisherName: Datadog
  ServiceCategory: Developer Tools / API
  ServiceName: Datadog
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
name: Datadog Finops
provider_name: Datadog
provider_slug: datadog
publisher_name: Datadog
service_category: API
slug: datadog-finops
source_filename: datadog-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Datadog\nproviderId: datadog\npublisherName: Datadog\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Analytics\n  - Dashboards\n  - Monitoring\n  - Platform\n  - T1\n  - Visualizations\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Datadog API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with\
  \ the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps\
  \ Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Datadog\n  ServiceCategory: Developer Tools / API\n  ProviderName: Datadog\n  PublisherName: Datadog\n  InvoiceIssuerName: Datadog\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n  \
  \  dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Datadog API\n    baseURL: https://api.datadoghq.com\n    tags:\n      - Monitoring\n      - Observability\n    serviceName: Datadog API\n    serviceCategory: API\n  - name: Datadog Metrics API\n    baseURL: https://api.datadoghq.com\n    tags:\n      - Metrics\n      - Monitoring\n      - Timeseries\n    serviceName: Datadog Metrics API\n    serviceCategory: API\n  - name: Datadog Logs API\n    baseURL: https://api.datadoghq.com\n    tags:\n      - Log Management\n      - Logs\n      - Search\n    serviceName: Datadog Logs API\n    serviceCategory: API\n  - name: Datadog Events API\n    baseURL: https://api.datadoghq.com\n    tags:\n      - Event Management\n      - Events\n    serviceName: Datadog Events\
  \ API\n    serviceCategory: API\n  - name: Datadog Monitors API\n    baseURL: https://api.datadoghq.com\n    tags:\n      - Alerting\n      - Monitors\n      - Notifications\n    serviceName: Datadog Monitors API\n    serviceCategory: API\n  - name: Datadog Dashboards API\n    baseURL: https://api.datadoghq.com\n    tags:\n      - Dashboards\n      - Visualizations\n    serviceName: Datadog Dashboards API\n    serviceCategory: API\n  - name: Datadog Incidents API\n    baseURL: https://api.datadoghq.com\n    tags:\n      - Incident Management\n      - Incidents\n    serviceName: Datadog Incidents API\n    serviceCategory: API\n  - name: Datadog Synthetics API\n    baseURL: https://api.datadoghq.com\n    tags:\n      - Synthetics\n      - Testing\n      - Uptime\n    serviceName: Datadog Synthetics API\n    serviceCategory: API\n  - name: Datadog Service Level Objectives API\n    baseURL: https://api.datadoghq.com\n    tags:\n      - Reliability\n      - Service Level Objectives\n      -\
  \ SLOs\n    serviceName: Datadog Service Level Objectives API\n    serviceCategory: API\n  - name: Datadog Security Monitoring API\n    baseURL: https://api.datadoghq.com\n    tags:\n      - Security\n      - Security Monitoring\n      - SIEM\n    serviceName: Datadog Security Monitoring API\n    serviceCategory: API\n  - name: Datadog Service Definition API\n    baseURL: https://api.datadoghq.com\n    tags:\n      - Service Catalog\n    serviceName: Datadog Service Definition API\n    serviceCategory: API\n  - name: Datadog Software Catalog API\n    baseURL: https://api.datadoghq.com\n    tags:\n      - Software Catalog\n    serviceName: Datadog Software Catalog API\n    serviceCategory: API\n  - name: Datadog Users API\n    baseURL: https://api.datadoghq.com\n    tags:\n      - Account Management\n      - Users\n    serviceName: Datadog Users API\n    serviceCategory: API\n  - name: Datadog Roles API\n    baseURL: https://api.datadoghq.com\n    tags:\n      - Access Control\n      -\
  \ RBAC\n      - Roles\n    serviceName: Datadog Roles API\n    serviceCategory: API\n  - name: Datadog Key Management API\n    baseURL: https://api.datadoghq.com\n    tags:\n      - API Keys\n      - Application Keys\n      - Authentication\n    serviceName: Datadog Key Management API\n    serviceCategory: API\n  - name: Datadog Organizations API\n    baseURL: https://api.datadoghq.com\n    tags:\n      - Account Management\n      - Organizations\n    serviceName: Datadog Organizations API\n    serviceCategory: API\n  - name: Datadog Downtimes API\n    baseURL: https://api.datadoghq.com\n    tags:\n      - Alerting\n      - Downtimes\n      - Monitors\n    serviceName: Datadog Downtimes API\n    serviceCategory: API\n  - name: Datadog RUM API\n    baseURL: https://api.datadoghq.com\n    tags:\n      - Real User Monitoring\n      - RUM\n      - Session Replay\n    serviceName: Datadog RUM API\n    serviceCategory: API\n  - name: Datadog APM Retention Filters API\n    baseURL: https://api.datadoghq.com\n\
  \    tags:\n      - APM\n      - Retention\n      - Tracing\n    serviceName: Datadog APM Retention Filters API\n    serviceCategory: API\n  - name: Datadog Usage Metering API\n    baseURL: https://api.datadoghq.com\n    tags:\n      - Billing\n      - Metering\n      - Usage\n    serviceName: Datadog Usage Metering API\n    serviceCategory: API\n  - name: Datadog Spans API\n    baseURL: https://api.datadoghq.com\n    tags:\n      - APM\n      - Spans\n      - Tracing\n    serviceName: Datadog Spans API\n    serviceCategory: API\n  - name: Datadog Processes API\n    baseURL: https://api.datadoghq.com\n    tags:\n      - Infrastructure\n      - Processes\n    serviceName: Datadog Processes API\n    serviceCategory: API\n  - name: Datadog Teams API\n    baseURL: https://api.datadoghq.com\n    tags:\n      - Account Management\n      - Teams\n    serviceName: Datadog Teams API\n    serviceCategory: API\n  - name: Datadog Workflow Automation API\n    baseURL: https://api.datadoghq.com\n  \
  \  tags:\n      - Automation\n      - Workflows\n    serviceName: Datadog Workflow Automation API\n    serviceCategory: API\n  - name: Datadog Case Management API\n    baseURL: https://api.datadoghq.com\n    tags:\n      - Case Management\n      - Cases\n    serviceName: Datadog Case Management API\n    serviceCategory: API\n  - name: Datadog Observability Pipelines API\n    baseURL: https://api.datadoghq.com\n    tags:\n      - Logs\n      - Observability Pipelines\n    serviceName: Datadog Observability Pipelines API\n    serviceCategory: API\n  - name: Datadog Sensitive Data Scanner API\n    baseURL: https://api.datadoghq.com\n    tags:\n      - Data Privacy\n      - Security\n      - Sensitive Data\n    serviceName: Datadog Sensitive Data Scanner API\n    serviceCategory: API\n  - name: Datadog AWS Integration API\n    baseURL: https://api.datadoghq.com\n    tags:\n      - AWS\n      - Cloud\n      - Integrations\n    serviceName: Datadog AWS Integration API\n    serviceCategory: API\n\
  \  - name: Datadog GCP Integration API\n    baseURL: https://api.datadoghq.com\n    tags:\n      - Cloud\n      - GCP\n      - Google Cloud\n      - Integrations\n    serviceName: Datadog GCP Integration API\n    serviceCategory: API\n  - name: Datadog CI Visibility Pipelines API\n    baseURL: https://api.datadoghq.com\n    tags:\n      - CI\n      - CI/CD\n      - Pipelines\n    serviceName: Datadog CI Visibility Pipelines API\n    serviceCategory: API\n  - name: Datadog Network Device Monitoring API\n    baseURL: https://api.datadoghq.com\n    tags:\n      - Infrastructure\n      - Network\n      - Network Device Monitoring\n    serviceName: Datadog Network Device Monitoring API\n    serviceCategory: API\n  - name: Datadog On-Call API\n    baseURL: https://api.datadoghq.com\n    tags:\n      - Incident Management\n      - On-Call\n      - Paging\n    serviceName: Datadog On-Call API\n    serviceCategory: API\n  - name: Datadog DORA Metrics API\n    baseURL: https://api.datadoghq.com\n\
  \    tags:\n      - CI/CD\n      - DevOps\n      - DORA Metrics\n    serviceName: Datadog DORA Metrics API\n    serviceCategory: API\n  - name: Datadog Cloud Cost Management API\n    baseURL: https://api.datadoghq.com\n    tags:\n      - Cloud\n      - Cloud Cost Management\n      - FinOps\n    serviceName: Datadog Cloud Cost Management API\n    serviceCategory: API\n  - name: Datadog Hosts API\n    baseURL: https://api.datadoghq.com\n    tags:\n      - Hosts\n      - Infrastructure\n    serviceName: Datadog Hosts API\n    serviceCategory: API\n  - name: Datadog Tags API\n    baseURL: https://api.datadoghq.com\n    tags:\n      - Infrastructure\n    serviceName: Datadog Tags API\n    serviceCategory: API\n  - name: Datadog Containers API\n    baseURL: https://api.datadoghq.com\n    tags:\n      - Containers\n      - Infrastructure\n    serviceName: Datadog Containers API\n    serviceCategory: API\n  - name: Datadog Container Images API\n    baseURL: https://api.datadoghq.com\n    tags:\n\
  \      - Container Images\n      - Containers\n      - Infrastructure\n    serviceName: Datadog Container Images API\n    serviceCategory: API\n  - name: Datadog Notebooks API\n    baseURL: https://api.datadoghq.com\n    tags:\n      - Collaboration\n      - Notebooks\n    serviceName: Datadog Notebooks API\n    serviceCategory: API\n  - name: Datadog Dashboard Lists API\n    baseURL: https://api.datadoghq.com\n    tags:\n      - Dashboard Lists\n      - Dashboards\n    serviceName: Datadog Dashboard Lists API\n    serviceCategory: API\n  - name: Datadog Logs Pipelines API\n    baseURL: https://api.datadoghq.com\n    tags:\n      - Log Processing\n      - Logs\n      - Pipelines\n    serviceName: Datadog Logs Pipelines API\n    serviceCategory: API\n  - name: Datadog Logs Indexes API\n    baseURL: https://api.datadoghq.com\n    tags:\n      - Indexes\n      - Log Management\n      - Logs\n    serviceName: Datadog Logs Indexes API\n    serviceCategory: API\n  - name: Datadog Logs Metrics\
  \ API\n    baseURL: https://api.datadoghq.com\n    tags:\n      - Log-Based Metrics\n      - Logs\n      - Metrics\n    serviceName: Datadog Logs Metrics API\n    serviceCategory: API\n  - name: Datadog Logs Archives API\n    baseURL: https://api.datadoghq.com\n    tags:\n      - Archives\n      - Logs\n      - Storage\n    serviceName: Datadog Logs Archives API\n    serviceCategory: API\n  - name: Datadog Logs Custom Destinations API\n    baseURL: https://api.datadoghq.com\n    tags:\n      - Custom Destinations\n      - Log Forwarding\n      - Logs\n    serviceName: Datadog Logs Custom Destinations API\n    serviceCategory: API\n  - name: Datadog Logs Restriction Queries API\n    baseURL: https://api.datadoghq.com\n    tags:\n      - Access Control\n      - Logs\n      - RBAC\n    serviceName: Datadog Logs Restriction Queries API\n    serviceCategory: API\n  - name: Datadog Spans Metrics API\n    baseURL: https://api.datadoghq.com\n    tags:\n      - APM\n      - Metrics\n      - Spans\n\
  \    serviceName: Datadog Spans Metrics API\n    serviceCategory: API\n  - name: Datadog Service Checks API\n    baseURL: https://api.datadoghq.com\n    tags:\n      - Monitoring\n      - Service Checks\n    serviceName: Datadog Service Checks API\n    serviceCategory: API\n  - name: Datadog Snapshots API\n    baseURL: https://api.datadoghq.com\n    tags:\n      - Graphs\n      - Snapshots\n      - Visualizations\n    serviceName: Datadog Snapshots API\n    serviceCategory: API\n  - name: Datadog IP Ranges API\n    baseURL: https://api.datadoghq.com\n    tags:\n      - Infrastructure\n      - IP Ranges\n      - Network\n    serviceName: Datadog IP Ranges API\n    serviceCategory: API\n  - name: Datadog IP Allowlist API\n    baseURL: https://api.datadoghq.com\n    tags:\n      - Access Control\n      - IP Allowlist\n      - Security\n    serviceName: Datadog IP Allowlist API\n    serviceCategory: API\n  - name: Datadog Audit API\n    baseURL: https://api.datadoghq.com\n    tags:\n     \
  \ - Audit\n      - Audit Logs\n      - Compliance\n    serviceName: Datadog Audit API\n    serviceCategory: API\n  - name: Datadog APM API\n    baseURL: https://api.datadoghq.com\n    tags:\n      - APM\n      - Application Performance\n      - Tracing\n    serviceName: Datadog APM API\n    serviceCategory: API\n  - name: Datadog Webhooks Integration API\n    baseURL: https://api.datadoghq.com\n    tags:\n      - Integrations\n      - Notifications\n      - Webhooks\n    serviceName: Datadog Webhooks Integration API\n    serviceCategory: API\n  - name: Datadog SLO Corrections API\n    baseURL: https://api.datadoghq.com\n    tags:\n      - Reliability\n      - SLO Corrections\n      - SLOs\n    serviceName: Datadog SLO Corrections API\n    serviceCategory: API\n  - name: Datadog AWS Logs Integration API\n    baseURL: https://api.datadoghq.com\n    tags:\n      - AWS\n      - Integrations\n      - Logs\n    serviceName: Datadog AWS Logs Integration API\n    serviceCategory: API\n  - name:\
  \ Datadog Azure Integration API\n    baseURL: https://api.datadoghq.com\n    tags:\n      - Azure\n      - Cloud\n      - Integrations\n    serviceName: Datadog Azure Integration API\n    serviceCategory: API\n  - name: Datadog Slack Integration API\n    baseURL: https://api.datadoghq.com\n    tags:\n      - Integrations\n      - Notifications\n      - Slack\n    serviceName: Datadog Slack Integration API\n    serviceCategory: API\n  - name: Datadog PagerDuty Integration API\n    baseURL: https://api.datadoghq.com\n    tags:\n      - Incident Management\n      - Integrations\n      - PagerDuty\n    serviceName: Datadog PagerDuty Integration API\n    serviceCategory: API\n  - name: Datadog Opsgenie Integration API\n    baseURL: https://api.datadoghq.com\n    tags:\n      - Incident Management\n      - Integrations\n      - Opsgenie\n    serviceName: Datadog Opsgenie Integration API\n    serviceCategory: API\n  - name: Datadog Cloudflare Integration API\n    baseURL: https://api.datadoghq.com\n\
  \    tags:\n      - CDN\n      - Cloudflare\n      - Integrations\n    serviceName: Datadog Cloudflare Integration API\n    serviceCategory: API\n  - name: Datadog Fastly Integration API\n    baseURL: https://api.datadoghq.com\n    tags:\n      - CDN\n      - Fastly\n      - Integrations\n    serviceName: Datadog Fastly Integration API\n    serviceCategory: API\n  - name: Datadog Confluent Cloud API\n    baseURL: https://api.datadoghq.com\n    tags:\n      - Confluent Cloud\n      - Integrations\n      - Kafka\n    serviceName: Datadog Confluent Cloud API\n    serviceCategory: API\n  - name: Datadog Okta Integration API\n    baseURL: https://api.datadoghq.com\n    tags:\n      - Identity\n      - Integrations\n      - Okta\n    serviceName: Datadog Okta Integration API\n    serviceCategory: API\n  - name: Datadog Microsoft Teams Integration API\n    baseURL: https://api.datadoghq.com\n    tags:\n      - Integrations\n      - Microsoft Teams\n      - Notifications\n    serviceName: Datadog\
  \ Microsoft Teams Integration API\n    serviceCategory: API\n  - name: Datadog Jira Integration API\n    baseURL: https://api.datadoghq.com\n    tags:\n      - Integrations\n      - Issue Tracking\n      - Jira\n    serviceName: Datadog Jira Integration API\n    serviceCategory: API\n  - name: Datadog Error Tracking API\n    baseURL: https://api.datadoghq.com\n    tags:\n      - Debugging\n      - Error Tracking\n    serviceName: Datadog Error Tracking API\n    serviceCategory: API\n  - name: Datadog Application Security API\n    baseURL: https://api.datadoghq.com\n    tags:\n      - Application Security\n      - AppSec\n      - Security\n    serviceName: Datadog Application Security API\n    serviceCategory: API\n  - name: Datadog CSM Threats API\n    baseURL: https://api.datadoghq.com\n    tags:\n      - Cloud Security\n      - CSM\n      - Threats\n    serviceName: Datadog CSM Threats API\n    serviceCategory: API\n  - name: Datadog CSM Agents API\n    baseURL: https://api.datadoghq.com\n\
  \    tags:\n      - Agents\n      - Cloud Security\n      - CSM\n    serviceName: Datadog CSM Agents API\n    serviceCategory: API\n  - name: Datadog Service Scorecards API\n    baseURL: https://api.datadoghq.com\n    tags:\n      - Best Practices\n      - Scorecards\n      - Service Catalog\n    serviceName: Datadog Service Scorecards API\n    serviceCategory: API\n  - name: Datadog Service Dependencies API\n    baseURL: https://api.datadoghq.com\n    tags:\n      - APM\n      - Dependencies\n    serviceName: Datadog Service Dependencies API\n    serviceCategory: API\n  - name: Datadog Powerpack API\n    baseURL: https://api.datadoghq.com\n    tags:\n      - Dashboards\n      - Powerpacks\n      - Widgets\n    serviceName: Datadog Powerpack API\n    serviceCategory: API\n  - name: Datadog Embeddable Graphs API\n    baseURL: https://api.datadoghq.com\n    tags:\n      - Embeds\n      - Graphs\n      - Visualizations\n    serviceName: Datadog Embeddable Graphs API\n    serviceCategory:\
  \ API\n  - name: Datadog RUM Metrics API\n    baseURL: https://api.datadoghq.com\n    tags:\n      - Metrics\n      - Real User Monitoring\n      - RUM\n    serviceName: Datadog RUM Metrics API\n    serviceCategory: API\n  - name: Datadog Domain Allowlist API\n    baseURL: https://api.datadoghq.com\n    tags:\n      - Access Control\n      - Domain Allowlist\n      - Security\n    serviceName: Datadog Domain Allowlist API\n    serviceCategory: API\n  - name: Datadog Restriction Policies API\n    baseURL: https://api.datadoghq.com\n    tags:\n      - Access Control\n      - RBAC\n      - Restriction Policies\n    serviceName: Datadog Restriction Policies API\n    serviceCategory: API\n  - name: Datadog AuthN Mappings API\n    baseURL: https://api.datadoghq.com\n    tags:\n      - Authentication\n      - Identity\n      - Mappings\n    serviceName: Datadog AuthN Mappings API\n    serviceCategory: API\n  - name: Datadog Integrations API\n    baseURL: https://api.datadoghq.com\n    tags:\n\
  \      - Integrations\n    serviceName: Datadog Integrations API\n    serviceCategory: API\n  - name: Datadog CI Visibility Tests API\n    baseURL: https://api.datadoghq.com\n    tags:\n      - CI\n      - CI/CD\n      - Tests\n    serviceName: Datadog CI Visibility Tests API\n    serviceCategory: API\n  - name: Datadog Agentless Scanning API\n    baseURL: https://api.datadoghq.com\n    tags:\n      - Agentless Scanning\n      - Cloud Security\n      - Vulnerabilities\n    serviceName: Datadog Agentless Scanning API\n    serviceCategory: API\n  - name: Datadog Static Analysis API\n    baseURL: https://api.datadoghq.com\n    tags:\n      - Code Quality\n      - Security\n      - Static Analysis\n    serviceName: Datadog Static Analysis API\n    serviceCategory: API\n  - name: Datadog Entity Risk Scores API\n    baseURL: https://api.datadoghq.com\n    tags:\n      - Cloud Security\n      - Risk Scores\n      - Security\n    serviceName: Datadog Entity Risk Scores API\n    serviceCategory:\
  \ API\n  - name: Datadog API Management API\n    baseURL: https://api.datadoghq.com\n    tags:\n      - API Catalog\n      - API Management\n    serviceName: Datadog API Management API\n    serviceCategory: API\n  - name: Datadog Cloud Workload Security API\n    baseURL: https://api.datadoghq.com\n    tags:\n      - Cloud Workload Security\n      - Runtime Protection\n      - Security\n    serviceName: Datadog Cloud Workload Security API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    url: http://apievangelist.com\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/datadog/refs/heads/main/finops/datadog-finops.yml
sources: []
specification: FinOps Framework
tags:
- Analytics
- Dashboards
- Monitoring
- Platform
- T1
- Visualizations
- FinOps
- Cost Management
- FOCUS
---
