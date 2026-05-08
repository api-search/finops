---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: cal-com-openapi.json
  format: json
  label: Cal.com Bookings API
  slug: cal-com-bookings-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/cal-com/refs/heads/main/openapi/cal-com-openapi.json
- filename: cal-com-openapi.json
  format: json
  label: Cal.com Event Types API
  slug: cal-com-event-types-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/cal-com/refs/heads/main/openapi/cal-com-openapi.json
- filename: cal-com-openapi.json
  format: json
  label: Cal.com Schedules API
  slug: cal-com-schedules-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/cal-com/refs/heads/main/openapi/cal-com-openapi.json
- filename: cal-com-openapi.json
  format: json
  label: Cal.com Availability API
  slug: cal-com-availability-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/cal-com/refs/heads/main/openapi/cal-com-openapi.json
- filename: cal-com-openapi.json
  format: json
  label: Cal.com Slots API
  slug: cal-com-slots-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/cal-com/refs/heads/main/openapi/cal-com-openapi.json
- filename: cal-com-openapi.json
  format: json
  label: Cal.com Webhooks API
  slug: cal-com-webhooks-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/cal-com/refs/heads/main/openapi/cal-com-openapi.json
- filename: cal-com-openapi.json
  format: json
  label: Cal.com OAuth & Auth API
  slug: cal-com-oauth-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/cal-com/refs/heads/main/openapi/cal-com-openapi.json
- filename: cal-com-openapi.json
  format: json
  label: Cal.com Teams API
  slug: cal-com-teams-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/cal-com/refs/heads/main/openapi/cal-com-openapi.json
- filename: cal-com-openapi.json
  format: json
  label: Cal.com Organizations API
  slug: cal-com-organizations-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/cal-com/refs/heads/main/openapi/cal-com-openapi.json
- filename: cal-com-openapi.json
  format: json
  label: Cal.com Out-of-Office API
  slug: cal-com-ooo-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/cal-com/refs/heads/main/openapi/cal-com-openapi.json
- filename: cal-com-openapi.json
  format: json
  label: Cal.com Conferencing API
  slug: cal-com-conferencing-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/cal-com/refs/heads/main/openapi/cal-com-openapi.json
- filename: cal-com-openapi.json
  format: json
  label: Cal.com Destination Calendars API
  slug: cal-com-destination-calendars-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/cal-com/refs/heads/main/openapi/cal-com-openapi.json
- filename: cal-com-openapi.json
  format: json
  label: Cal.com Atoms (Platform)
  slug: cal-com-atoms-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/cal-com/refs/heads/main/openapi/cal-com-openapi.json
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
description: FinOps framework definition for the Cal.com API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Cal.com
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Cal.com
  PublisherName: Cal.com
  ServiceCategory: Developer Tools / API
  ServiceName: Cal.com
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
name: Cal Com Finops
provider_name: Cal.com
provider_slug: cal-com
publisher_name: Cal.com
service_category: API
slug: cal-com-finops
source_filename: cal-com-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Cal.com\nproviderId: cal-com\npublisherName: Cal.com\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Productivity\n  - Scheduling\n  - Calendar\n  - Open Source\n  - Booking\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Cal.com API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming\
  \ team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice\
  \ Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Cal.com\n  ServiceCategory: Developer Tools / API\n  ProviderName: Cal.com\n  PublisherName: Cal.com\n  InvoiceIssuerName: Cal.com\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n\
  \      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Cal.com Bookings API\n    baseURL: https://api.cal.com/v2\n    tags:\n      - Bookings\n      - CRUD\n    serviceName: Cal.com Bookings API\n    serviceCategory: API\n  - name: Cal.com Event Types API\n    baseURL: https://api.cal.com/v2\n    tags:\n      - Event Types\n      - Configuration\n    serviceName: Cal.com Event Types API\n    serviceCategory: API\n  - name: Cal.com Schedules API\n    baseURL: https://api.cal.com/v2\n    tags:\n      - Schedules\n      - Working Hours\n    serviceName: Cal.com Schedules API\n    serviceCategory: API\n  - name: Cal.com Availability API\n    baseURL: https://api.cal.com/v2\n    tags:\n      - Availability\n      - Calendar\n    serviceName: Cal.com Availability API\n    serviceCategory:\
  \ API\n  - name: Cal.com Slots API\n    baseURL: https://api.cal.com/v2\n    tags:\n      - Slots\n      - Time\n    serviceName: Cal.com Slots API\n    serviceCategory: API\n  - name: Cal.com Webhooks API\n    baseURL: https://api.cal.com/v2\n    tags:\n      - Webhooks\n      - Events\n    serviceName: Cal.com Webhooks API\n    serviceCategory: API\n  - name: Cal.com OAuth & Auth API\n    baseURL: https://api.cal.com/v2\n    tags:\n      - OAuth\n      - Authentication\n    serviceName: Cal.com OAuth & Auth API\n    serviceCategory: API\n  - name: Cal.com Teams API\n    baseURL: https://api.cal.com/v2\n    tags:\n      - Teams\n      - Membership\n    serviceName: Cal.com Teams API\n    serviceCategory: API\n  - name: Cal.com Organizations API\n    baseURL: https://api.cal.com/v2\n    tags:\n      - Organizations\n      - Enterprise\n    serviceName: Cal.com Organizations API\n    serviceCategory: API\n  - name: Cal.com Out-of-Office API\n    baseURL: https://api.cal.com/v2\n    tags:\n\
  \      - OOO\n      - Availability\n    serviceName: Cal.com Out-of-Office API\n    serviceCategory: API\n  - name: Cal.com Conferencing API\n    baseURL: https://api.cal.com/v2\n    tags:\n      - Conferencing\n      - Video\n    serviceName: Cal.com Conferencing API\n    serviceCategory: API\n  - name: Cal.com Destination Calendars API\n    baseURL: https://api.cal.com/v2\n    tags:\n      - Calendars\n      - Integration\n    serviceName: Cal.com Destination Calendars API\n    serviceCategory: API\n  - name: Cal.com Atoms (Platform)\n    baseURL: https://api.cal.com/v2\n    tags:\n      - Atoms\n      - SDK\n      - Embed\n    serviceName: Cal.com Atoms (Platform)\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/cal-com/refs/heads/main/finops/cal-com-finops.yml
sources: []
specification: FinOps Framework
tags:
- Productivity
- Scheduling
- Calendar
- Open Source
- Booking
- FinOps
- Cost Management
- FOCUS
---
