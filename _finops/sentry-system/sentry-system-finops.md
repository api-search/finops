---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: openapi-derefed.json
  format: json
  label: Sentry API
  slug: ''
  spec_type: OpenAPI
  url: https://github.com/getsentry/sentry-api-schema/blob/main/openapi-derefed.json
- filename: openapi-derefed.json
  format: json
  label: Sentry Events and Issues API
  slug: ''
  spec_type: OpenAPI
  url: https://github.com/getsentry/sentry-api-schema/blob/main/openapi-derefed.json
- filename: openapi-derefed.json
  format: json
  label: Sentry Organizations API
  slug: ''
  spec_type: OpenAPI
  url: https://github.com/getsentry/sentry-api-schema/blob/main/openapi-derefed.json
- filename: openapi-derefed.json
  format: json
  label: Sentry Projects API
  slug: ''
  spec_type: OpenAPI
  url: https://github.com/getsentry/sentry-api-schema/blob/main/openapi-derefed.json
- filename: openapi-derefed.json
  format: json
  label: Sentry Teams API
  slug: ''
  spec_type: OpenAPI
  url: https://github.com/getsentry/sentry-api-schema/blob/main/openapi-derefed.json
- filename: openapi-derefed.json
  format: json
  label: Sentry Releases API
  slug: ''
  spec_type: OpenAPI
  url: https://github.com/getsentry/sentry-api-schema/blob/main/openapi-derefed.json
- filename: openapi-derefed.json
  format: json
  label: Sentry Alerts API
  slug: ''
  spec_type: OpenAPI
  url: https://github.com/getsentry/sentry-api-schema/blob/main/openapi-derefed.json
- filename: openapi-derefed.json
  format: json
  label: Sentry Crons API
  slug: ''
  spec_type: OpenAPI
  url: https://github.com/getsentry/sentry-api-schema/blob/main/openapi-derefed.json
- filename: openapi-derefed.json
  format: json
  label: Sentry Dashboards API
  slug: ''
  spec_type: OpenAPI
  url: https://github.com/getsentry/sentry-api-schema/blob/main/openapi-derefed.json
- filename: openapi-derefed.json
  format: json
  label: Sentry Discover API
  slug: ''
  spec_type: OpenAPI
  url: https://github.com/getsentry/sentry-api-schema/blob/main/openapi-derefed.json
- filename: openapi-derefed.json
  format: json
  label: Sentry Environments API
  slug: ''
  spec_type: OpenAPI
  url: https://github.com/getsentry/sentry-api-schema/blob/main/openapi-derefed.json
- filename: openapi-derefed.json
  format: json
  label: Sentry Explore API
  slug: ''
  spec_type: OpenAPI
  url: https://github.com/getsentry/sentry-api-schema/blob/main/openapi-derefed.json
- filename: openapi-derefed.json
  format: json
  label: Sentry Integration Platform API
  slug: ''
  spec_type: OpenAPI
  url: https://github.com/getsentry/sentry-api-schema/blob/main/openapi-derefed.json
- filename: openapi-derefed.json
  format: json
  label: Sentry Integrations API
  slug: ''
  spec_type: OpenAPI
  url: https://github.com/getsentry/sentry-api-schema/blob/main/openapi-derefed.json
- filename: openapi-derefed.json
  format: json
  label: Sentry Mobile Builds API
  slug: ''
  spec_type: OpenAPI
  url: https://github.com/getsentry/sentry-api-schema/blob/main/openapi-derefed.json
- filename: openapi-derefed.json
  format: json
  label: Sentry Monitors API
  slug: ''
  spec_type: OpenAPI
  url: https://github.com/getsentry/sentry-api-schema/blob/main/openapi-derefed.json
- filename: openapi-derefed.json
  format: json
  label: Sentry Prevent API
  slug: ''
  spec_type: OpenAPI
  url: https://github.com/getsentry/sentry-api-schema/blob/main/openapi-derefed.json
- filename: openapi-derefed.json
  format: json
  label: Sentry Replays API
  slug: ''
  spec_type: OpenAPI
  url: https://github.com/getsentry/sentry-api-schema/blob/main/openapi-derefed.json
- filename: openapi-derefed.json
  format: json
  label: Sentry SCIM API
  slug: ''
  spec_type: OpenAPI
  url: https://github.com/getsentry/sentry-api-schema/blob/main/openapi-derefed.json
- filename: openapi-derefed.json
  format: json
  label: Sentry Seer API
  slug: ''
  spec_type: OpenAPI
  url: https://github.com/getsentry/sentry-api-schema/blob/main/openapi-derefed.json
- filename: openapi-derefed.json
  format: json
  label: Sentry Users API
  slug: ''
  spec_type: OpenAPI
  url: https://github.com/getsentry/sentry-api-schema/blob/main/openapi-derefed.json
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
description: FinOps framework definition for the Sentry API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Sentry
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Sentry
  PublisherName: Sentry
  ServiceCategory: Developer Tools / API
  ServiceName: Sentry
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
name: Sentry System Finops
provider_name: Sentry
provider_slug: sentry-system
publisher_name: Sentry
service_category: API
slug: sentry-system-finops
source_filename: sentry-system-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Sentry\nproviderId: sentry-system\npublisherName: Sentry\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - APM\n  - Application Monitoring\n  - Bug Tracking\n  - Developer Tools\n  - Error Tracking\n  - Observability\n  - Performance Monitoring\n  - Real-Time Monitoring\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Sentry API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n\
  \  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and\
  \ SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Sentry\n  ServiceCategory: Developer Tools / API\n  ProviderName: Sentry\n  PublisherName: Sentry\n  InvoiceIssuerName: Sentry\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned\
  \ over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Sentry API\n    baseURL: https://sentry.io/api/0\n    tags:\n      - Error Tracking\n      - Monitoring\n      - Observability\n      - Performance\n    serviceName: Sentry API\n    serviceCategory: API\n  - name: Sentry Events and Issues API\n    baseURL: https://sentry.io/api/0\n    tags:\n      - Debugging\n      - Error Tracking\n      - Events\n      - Issues\n    serviceName: Sentry Events and Issues API\n    serviceCategory: API\n  - name: Sentry Organizations API\n    baseURL: https://sentry.io/api/0\n    tags:\n      - Administration\n      - Members\n      - Organizations\n    serviceName: Sentry Organizations API\n   \
  \ serviceCategory: API\n  - name: Sentry Projects API\n    baseURL: https://sentry.io/api/0\n    tags:\n      - Configuration\n      - Management\n      - Projects\n    serviceName: Sentry Projects API\n    serviceCategory: API\n  - name: Sentry Teams API\n    baseURL: https://sentry.io/api/0\n    tags:\n      - Collaboration\n      - Members\n      - Teams\n    serviceName: Sentry Teams API\n    serviceCategory: API\n  - name: Sentry Releases API\n    baseURL: https://sentry.io/api/0\n    tags:\n      - Deployments\n      - Releases\n      - Version Management\n    serviceName: Sentry Releases API\n    serviceCategory: API\n  - name: Sentry Alerts API\n    baseURL: https://sentry.io/api/0\n    tags:\n      - Alerts\n      - Monitoring\n      - Notifications\n    serviceName: Sentry Alerts API\n    serviceCategory: API\n  - name: Sentry Crons API\n    baseURL: https://sentry.io/api/0\n    tags:\n      - Crons\n      - Monitoring\n      - Scheduled Tasks\n    serviceName: Sentry Crons API\n\
  \    serviceCategory: API\n  - name: Sentry Dashboards API\n    baseURL: https://sentry.io/api/0\n    tags:\n      - Analytics\n      - Dashboards\n      - Visualization\n    serviceName: Sentry Dashboards API\n    serviceCategory: API\n  - name: Sentry Discover API\n    baseURL: https://sentry.io/api/0\n    tags:\n      - Analytics\n      - Discover\n      - Performance\n      - Queries\n    serviceName: Sentry Discover API\n    serviceCategory: API\n  - name: Sentry Environments API\n    baseURL: https://sentry.io/api/0\n    tags:\n      - Configuration\n      - Environments\n      - Management\n    serviceName: Sentry Environments API\n    serviceCategory: API\n  - name: Sentry Explore API\n    baseURL: https://sentry.io/api/0\n    tags:\n      - Analytics\n      - Events\n      - Explore\n    serviceName: Sentry Explore API\n    serviceCategory: API\n  - name: Sentry Integration Platform API\n    baseURL: https://sentry.io/api/0\n    tags:\n      - Integrations\n      - Platform\n\
  \      - Webhooks\n    serviceName: Sentry Integration Platform API\n    serviceCategory: API\n  - name: Sentry Integrations API\n    baseURL: https://sentry.io/api/0\n    tags:\n      - Configuration\n      - Data Forwarding\n      - Integrations\n    serviceName: Sentry Integrations API\n    serviceCategory: API\n  - name: Sentry Mobile Builds API\n    baseURL: https://sentry.io/api/0\n    tags:\n      - Artifacts\n      - Builds\n      - Mobile\n    serviceName: Sentry Mobile Builds API\n    serviceCategory: API\n  - name: Sentry Monitors API\n    baseURL: https://sentry.io/api/0\n    tags:\n      - Alerts\n      - Monitors\n      - Uptime\n    serviceName: Sentry Monitors API\n    serviceCategory: API\n  - name: Sentry Prevent API\n    baseURL: https://sentry.io/api/0\n    tags:\n      - Quality Assurance\n      - Repositories\n      - Testing\n    serviceName: Sentry Prevent API\n    serviceCategory: API\n  - name: Sentry Replays API\n    baseURL: https://sentry.io/api/0\n    tags:\n\
  \      - Replays\n      - Session Recording\n      - User Experience\n    serviceName: Sentry Replays API\n    serviceCategory: API\n  - name: Sentry SCIM API\n    baseURL: https://sentry.io/api/0\n    tags:\n      - Enterprise\n      - Identity Management\n      - Provisioning\n      - SCIM\n    serviceName: Sentry SCIM API\n    serviceCategory: API\n  - name: Sentry Seer API\n    baseURL: https://sentry.io/api/0\n    tags:\n      - AI\n      - Automation\n      - Issue Analysis\n    serviceName: Sentry Seer API\n    serviceCategory: API\n  - name: Sentry Users API\n    baseURL: https://sentry.io/api/0\n    tags:\n      - Accounts\n      - Authentication\n      - Users\n    serviceName: Sentry Users API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - name: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/sentry-system/refs/heads/main/finops/sentry-system-finops.yml
sources: []
specification: FinOps Framework
tags:
- APM
- Application Monitoring
- Bug Tracking
- Developer Tools
- Error Tracking
- Observability
- Performance Monitoring
- Real-Time Monitoring
- FinOps
- Cost Management
- FOCUS
---
