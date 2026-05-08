---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: opsgenie-alert-openapi.yml
  format: yaml
  label: OpsGenie Alert API
  slug: opsgenie-alert
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/opsgenie/refs/heads/main/openapi/opsgenie-alert-openapi.yml
- filename: opsgenie-incident-openapi.yml
  format: yaml
  label: OpsGenie Incident API
  slug: opsgenie-incident
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/opsgenie/refs/heads/main/openapi/opsgenie-incident-openapi.yml
- filename: opsgenie-user-openapi.yml
  format: yaml
  label: OpsGenie User API
  slug: opsgenie-user
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/opsgenie/refs/heads/main/openapi/opsgenie-user-openapi.yml
- filename: opsgenie-team-openapi.yml
  format: yaml
  label: OpsGenie Team API
  slug: opsgenie-team
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/opsgenie/refs/heads/main/openapi/opsgenie-team-openapi.yml
- filename: opsgenie-schedule-openapi.yml
  format: yaml
  label: OpsGenie Schedule API
  slug: opsgenie-schedule
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/opsgenie/refs/heads/main/openapi/opsgenie-schedule-openapi.yml
- filename: opsgenie-escalation-openapi.yml
  format: yaml
  label: OpsGenie Escalation API
  slug: opsgenie-escalation
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/opsgenie/refs/heads/main/openapi/opsgenie-escalation-openapi.yml
- filename: opsgenie-integration-openapi.yml
  format: yaml
  label: OpsGenie Integration API
  slug: opsgenie-integration
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/opsgenie/refs/heads/main/openapi/opsgenie-integration-openapi.yml
- filename: opsgenie-heartbeat-openapi.yml
  format: yaml
  label: OpsGenie Heartbeat API
  slug: opsgenie-heartbeat
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/opsgenie/refs/heads/main/openapi/opsgenie-heartbeat-openapi.yml
- filename: opsgenie-service-openapi.yml
  format: yaml
  label: OpsGenie Service API
  slug: opsgenie-service
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/opsgenie/refs/heads/main/openapi/opsgenie-service-openapi.yml
- filename: opsgenie-notification-rule-openapi.yml
  format: yaml
  label: OpsGenie Notification Rule API
  slug: opsgenie-notification-rule
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/opsgenie/refs/heads/main/openapi/opsgenie-notification-rule-openapi.yml
- filename: opsgenie-account-openapi.yml
  format: yaml
  label: OpsGenie Account API
  slug: opsgenie-account
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/opsgenie/refs/heads/main/openapi/opsgenie-account-openapi.yml
- filename: opsgenie-maintenance-openapi.yml
  format: yaml
  label: OpsGenie Maintenance API
  slug: opsgenie-maintenance
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/opsgenie/refs/heads/main/openapi/opsgenie-maintenance-openapi.yml
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
description: FinOps framework definition for the OpsGenie API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: OpsGenie
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: OpsGenie
  PublisherName: OpsGenie
  ServiceCategory: Developer Tools / API
  ServiceName: OpsGenie
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
name: Opsgenie Finops
provider_name: OpsGenie
provider_slug: opsgenie
publisher_name: OpsGenie
service_category: API
slug: opsgenie-finops
source_filename: opsgenie-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: OpsGenie\nproviderId: opsgenie\npublisherName: OpsGenie\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Alerts\n  - Incident Management\n  - Monitoring\n  - On-Call\n  - Operations\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the OpsGenie API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the\
  \ consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps\
  \ Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: OpsGenie\n  ServiceCategory: Developer Tools / API\n  ProviderName: OpsGenie\n  PublisherName: OpsGenie\n  InvoiceIssuerName: OpsGenie\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n\
  \    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: OpsGenie Alert API\n    baseURL: https://api.opsgenie.com\n    tags:\n      - Alerts\n      - Incident Management\n      - Monitoring\n      - Notifications\n    serviceName: OpsGenie Alert API\n    serviceCategory: API\n  - name: OpsGenie Incident API\n    baseURL: https://api.opsgenie.com\n    tags:\n      - Incidents\n      - Incident Management\n      - Operations\n      - Response\n    serviceName: OpsGenie Incident API\n    serviceCategory: API\n  - name: OpsGenie User API\n    baseURL: https://api.opsgenie.com\n    tags:\n      - Users\n      - Accounts\n      - Identity\n      - Management\n    serviceName: OpsGenie User API\n    serviceCategory: API\n  - name: OpsGenie Team API\n    baseURL:\
  \ https://api.opsgenie.com\n    tags:\n      - Teams\n      - Groups\n      - Collaboration\n      - Management\n    serviceName: OpsGenie Team API\n    serviceCategory: API\n  - name: OpsGenie Schedule API\n    baseURL: https://api.opsgenie.com\n    tags:\n      - Schedules\n      - On-Call\n      - Rotations\n      - Planning\n    serviceName: OpsGenie Schedule API\n    serviceCategory: API\n  - name: OpsGenie Escalation API\n    baseURL: https://api.opsgenie.com\n    tags:\n      - Escalations\n      - Routing\n      - Alerts\n      - Workflows\n    serviceName: OpsGenie Escalation API\n    serviceCategory: API\n  - name: OpsGenie Integration API\n    baseURL: https://api.opsgenie.com\n    tags:\n      - Integrations\n      - Connections\n      - Third Party\n      - Automation\n    serviceName: OpsGenie Integration API\n    serviceCategory: API\n  - name: OpsGenie Heartbeat API\n    baseURL: https://api.opsgenie.com\n    tags:\n      - Heartbeat\n      - Health Checks\n      - Monitoring\n\
  \      - Uptime\n    serviceName: OpsGenie Heartbeat API\n    serviceCategory: API\n  - name: OpsGenie Service API\n    baseURL: https://api.opsgenie.com\n    tags:\n      - Services\n      - Service Catalog\n      - Operations\n      - Management\n    serviceName: OpsGenie Service API\n    serviceCategory: API\n  - name: OpsGenie Notification Rule API\n    baseURL: https://api.opsgenie.com\n    tags:\n      - Notifications\n      - Rules\n      - Alerts\n      - Configuration\n    serviceName: OpsGenie Notification Rule API\n    serviceCategory: API\n  - name: OpsGenie Account API\n    baseURL: https://api.opsgenie.com\n    tags:\n      - Accounts\n      - Administration\n      - Settings\n      - Configuration\n    serviceName: OpsGenie Account API\n    serviceCategory: API\n  - name: OpsGenie Maintenance API\n    baseURL: https://api.opsgenie.com\n    tags:\n      - Maintenance\n      - Windows\n      - Scheduling\n      - Operations\n    serviceName: OpsGenie Maintenance API\n    serviceCategory:\
  \ API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: API Evangelist\n    email: info@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/opsgenie/refs/heads/main/finops/opsgenie-finops.yml
sources: []
specification: FinOps Framework
tags:
- Alerts
- Incident Management
- Monitoring
- On-Call
- Operations
- FinOps
- Cost Management
- FOCUS
---
