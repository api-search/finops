---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: new-relic-openapi.yml
  format: yaml
  label: New Relic REST API v2
  slug: new-relic-rest-api-v2
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/new-relic/refs/heads/main/openapi/new-relic-openapi.yml
- filename: new-relic-metric-api-openapi.yml
  format: yaml
  label: New Relic Metric API
  slug: new-relic-metric-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/new-relic/refs/heads/main/openapi/new-relic-metric-api-openapi.yml
- filename: new-relic-event-api-openapi.yml
  format: yaml
  label: New Relic Event API
  slug: new-relic-event-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/new-relic/refs/heads/main/openapi/new-relic-event-api-openapi.yml
- filename: new-relic-log-api-openapi.yml
  format: yaml
  label: New Relic Log API
  slug: new-relic-log-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/new-relic/refs/heads/main/openapi/new-relic-log-api-openapi.yml
- filename: new-relic-trace-api-openapi.yml
  format: yaml
  label: New Relic Trace API
  slug: new-relic-trace-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/new-relic/refs/heads/main/openapi/new-relic-trace-api-openapi.yml
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
description: FinOps framework definition for the New Relic API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: New Relic
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: New Relic
  PublisherName: New Relic
  ServiceCategory: Developer Tools / API
  ServiceName: New Relic
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
name: New Relic Finops
provider_name: New Relic
provider_slug: new-relic
publisher_name: New Relic
service_category: API
slug: new-relic-finops
source_filename: new-relic-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: New Relic\nproviderId: new-relic\npublisherName: New Relic\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Analysis\n  - Analytics\n  - APM\n  - DevOps\n  - Infrastructure\n  - Monitoring\n  - Observability\n  - Performance\n  - Platform\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the New Relic API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n\
  \    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage\
  \ the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: New Relic\n  ServiceCategory: Developer Tools / API\n  ProviderName: New Relic\n  PublisherName: New Relic\n  InvoiceIssuerName: New Relic\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network\
  \ in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: New Relic REST API v2\n    baseURL: https://api.newrelic.com/v2/\n    tags:\n      - APM\n      - Applications\n      - Monitoring\n      - REST\n    serviceName: New Relic REST API v2\n    serviceCategory: API\n  - name: New Relic NerdGraph API\n    baseURL: https://api.newrelic.com/graphql\n    tags:\n      - GraphQL\n      - Monitoring\n      - Observability\n      - Platform\n    serviceName: New Relic NerdGraph API\n    serviceCategory: API\n  - name: New Relic Metric API\n    baseURL: https://metric-api.newrelic.com/metric/v1\n    tags:\n      - Ingest\n      - Metrics\n      - Monitoring\n      - Telemetry\n    serviceName: New Relic Metric\
  \ API\n    serviceCategory: API\n  - name: New Relic Event API\n    baseURL: https://insights-collector.newrelic.com/v1/accounts\n    tags:\n      - Custom Data\n      - Events\n      - Ingest\n      - Telemetry\n    serviceName: New Relic Event API\n    serviceCategory: API\n  - name: New Relic Log API\n    baseURL: https://log-api.newrelic.com/log/v1\n    tags:\n      - Ingest\n      - Log Management\n      - Logs\n      - Telemetry\n    serviceName: New Relic Log API\n    serviceCategory: API\n  - name: New Relic Trace API\n    baseURL: https://trace-api.newrelic.com/trace/v1\n    tags:\n      - Distributed Tracing\n      - Ingest\n      - Telemetry\n      - Traces\n    serviceName: New Relic Trace API\n    serviceCategory: API\n  - name: New Relic Alerts API\n    baseURL: https://api.newrelic.com/v2/\n    tags:\n      - Alerts\n      - Monitoring\n      - Notifications\n      - REST\n    serviceName: New Relic Alerts API\n    serviceCategory: API\n  - name: New Relic Synthetics API\n\
  \    baseURL: https://api.newrelic.com/graphql\n    tags:\n      - Monitoring\n      - Synthetics\n      - Testing\n      - Uptime Monitoring\n    serviceName: New Relic Synthetics API\n    serviceCategory: API\n  - name: New Relic Infrastructure Alerts API\n    baseURL: https://infra-api.newrelic.com/v2/\n    tags:\n      - Alerts\n      - Infrastructure\n      - Monitoring\n      - REST\n    serviceName: New Relic Infrastructure Alerts API\n    serviceCategory: API\n  - name: New Relic Browser API\n    baseURL: https://bam.nr-data.net\n    tags:\n      - Browser\n      - JavaScript\n      - Monitoring\n      - Real User Monitoring\n    serviceName: New Relic Browser API\n    serviceCategory: API\n  - name: New Relic Partnership API\n    baseURL: https://rpm.newrelic.com/api/v2/partners/\n    tags:\n      - Account Management\n      - Partners\n      - Platform\n    serviceName: New Relic Partnership API\n    serviceCategory: API\n  - name: New Relic Telemetry SDKs\n    baseURL: https://metric-api.newrelic.com\n\
  \    tags:\n      - Client Libraries\n      - Open Source\n      - SDKs\n      - Telemetry\n    serviceName: New Relic Telemetry SDKs\n    serviceCategory: API\n  - name: New Relic OpenTelemetry OTLP Endpoint\n    baseURL: https://otlp.nr-data.net\n    tags:\n      - Ingest\n      - OpenTelemetry\n      - OTLP\n      - Telemetry\n    serviceName: New Relic OpenTelemetry OTLP Endpoint\n    serviceCategory: API\n  - name: New Relic Control\n    baseURL: https://api.newrelic.com\n    tags:\n      - Agent Management\n      - Automation\n      - Fleet Control\n      - Observability\n      - Platform\n    serviceName: New Relic Control\n    serviceCategory: API\n  - name: New Relic NRQL Lookups API\n    baseURL: https://nrql-lookup.service.newrelic.com\n    tags:\n      - Data Enrichment\n      - Lookups\n      - NRQL\n      - REST\n    serviceName: New Relic NRQL Lookups API\n    serviceCategory: API\n  - name: New Relic Security Data API\n    baseURL: https://security-api.newrelic.com/security/v1\n\
  \    tags:\n      - Compliance\n      - Ingest\n      - Security\n      - Vulnerabilities\n    serviceName: New Relic Security Data API\n    serviceCategory: API\n  - name: New Relic Mobile SDK\n    baseURL: https://mobile-collector.newrelic.com\n    tags:\n      - Android\n      - iOS\n      - Mobile\n      - Monitoring\n      - SDK\n    serviceName: New Relic Mobile SDK\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/new-relic/refs/heads/main/finops/new-relic-finops.yml
sources: []
specification: FinOps Framework
tags:
- Analysis
- Analytics
- APM
- DevOps
- Infrastructure
- Monitoring
- Observability
- Performance
- Platform
- FinOps
- Cost Management
- FOCUS
---
