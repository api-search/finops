---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: cisco-webex-meetings-openapi.yml
  format: yaml
  label: Webex Meetings API
  slug: webex-meetings-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/cisco-webex/refs/heads/main/openapi/cisco-webex-meetings-openapi.yml
- filename: cisco-webex-messaging-openapi.yml
  format: yaml
  label: Webex Messaging API
  slug: webex-messaging-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/cisco-webex/refs/heads/main/openapi/cisco-webex-messaging-openapi.yml
- filename: cisco-webex-people-openapi.yml
  format: yaml
  label: Webex People API
  slug: webex-people-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/cisco-webex/refs/heads/main/openapi/cisco-webex-people-openapi.yml
- filename: cisco-webex-teams-openapi.yml
  format: yaml
  label: Webex Teams API
  slug: webex-teams-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/cisco-webex/refs/heads/main/openapi/cisco-webex-teams-openapi.yml
- filename: cisco-webex-rooms-openapi.yml
  format: yaml
  label: Webex Rooms API
  slug: webex-rooms-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/cisco-webex/refs/heads/main/openapi/cisco-webex-rooms-openapi.yml
- filename: cisco-webex-webhooks-openapi.yml
  format: yaml
  label: Webex Webhooks API
  slug: webex-webhooks-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/cisco-webex/refs/heads/main/openapi/cisco-webex-webhooks-openapi.yml
- filename: cisco-webex-devices-openapi.yml
  format: yaml
  label: Webex Devices API
  slug: webex-devices-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/cisco-webex/refs/heads/main/openapi/cisco-webex-devices-openapi.yml
- filename: cisco-webex-memberships-openapi.yml
  format: yaml
  label: Webex Memberships API
  slug: webex-memberships-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/cisco-webex/refs/heads/main/openapi/cisco-webex-memberships-openapi.yml
- filename: cisco-webex-team-memberships-openapi.yml
  format: yaml
  label: Webex Team Memberships API
  slug: webex-team-memberships-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/cisco-webex/refs/heads/main/openapi/cisco-webex-team-memberships-openapi.yml
- filename: cisco-webex-events-openapi.yml
  format: yaml
  label: Webex Events API
  slug: webex-events-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/cisco-webex/refs/heads/main/openapi/cisco-webex-events-openapi.yml
- filename: cisco-webex-recordings-openapi.yml
  format: yaml
  label: Webex Recordings API
  slug: webex-recordings-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/cisco-webex/refs/heads/main/openapi/cisco-webex-recordings-openapi.yml
- filename: cisco-webex-call-controls-openapi.yml
  format: yaml
  label: Webex Call Controls API
  slug: webex-call-controls-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/cisco-webex/refs/heads/main/openapi/cisco-webex-call-controls-openapi.yml
- filename: cisco-webex-attachment-actions-openapi.yml
  format: yaml
  label: Webex Attachment Actions API
  slug: webex-attachment-actions-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/cisco-webex/refs/heads/main/openapi/cisco-webex-attachment-actions-openapi.yml
- filename: cisco-webex-organizations-openapi.yml
  format: yaml
  label: Webex Organizations API
  slug: webex-organizations-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/cisco-webex/refs/heads/main/openapi/cisco-webex-organizations-openapi.yml
- filename: cisco-webex-licenses-openapi.yml
  format: yaml
  label: Webex Licenses API
  slug: webex-licenses-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/cisco-webex/refs/heads/main/openapi/cisco-webex-licenses-openapi.yml
- filename: cisco-webex-roles-openapi.yml
  format: yaml
  label: Webex Roles API
  slug: webex-roles-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/cisco-webex/refs/heads/main/openapi/cisco-webex-roles-openapi.yml
- filename: cisco-webex-workspaces-openapi.yml
  format: yaml
  label: Webex Workspaces API
  slug: webex-workspaces-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/cisco-webex/refs/heads/main/openapi/cisco-webex-workspaces-openapi.yml
- filename: cisco-webex-admin-audit-events-openapi.yml
  format: yaml
  label: Webex Admin Audit Events API
  slug: webex-admin-audit-events-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/cisco-webex/refs/heads/main/openapi/cisco-webex-admin-audit-events-openapi.yml
- filename: cisco-webex-converged-recordings-openapi.yml
  format: yaml
  label: Webex Converged Recordings API
  slug: webex-converged-recordings-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/cisco-webex/refs/heads/main/openapi/cisco-webex-converged-recordings-openapi.yml
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
description: FinOps framework definition for the Cisco Webex API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Cisco Webex
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Cisco Webex
  PublisherName: Cisco Webex
  ServiceCategory: Developer Tools / API
  ServiceName: Cisco Webex
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
name: Cisco Webex Finops
provider_name: Cisco Webex
provider_slug: cisco-webex
publisher_name: Cisco Webex
service_category: API
slug: cisco-webex-finops
source_filename: cisco-webex-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Cisco Webex\nproviderId: cisco-webex\npublisherName: Cisco Webex\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Collaboration\n  - Communications\n  - Meetings\n  - Messaging\n  - Teams\n  - Video Conferencing\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Cisco Webex API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag\
  \ every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n\
  \    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Cisco Webex\n  ServiceCategory: Developer Tools / API\n  ProviderName: Cisco Webex\n  PublisherName: Cisco Webex\n  InvoiceIssuerName: Cisco Webex\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n\
  \    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Webex Meetings API\n    baseURL: https://webexapis.com/v1\n    tags:\n      - Attendees\n      - Conferencing\n      - Meetings\n      - Scheduling\n      - Video\n    serviceName: Webex Meetings API\n    serviceCategory: API\n  - name: Webex Messaging API\n    baseURL: https://webexapis.com/v1\n    tags:\n      - Chat\n      - Collaboration\n      - Messaging\n      - Spaces\n      - Teams\n    serviceName: Webex Messaging API\n    serviceCategory: API\n  - name: Webex People API\n    baseURL: https://webexapis.com/v1\n    tags:\n      - Contacts\n      - Directory\n      - People\n      - Profiles\n      - Users\n    serviceName: Webex People API\n    serviceCategory:\
  \ API\n  - name: Webex Teams API\n    baseURL: https://webexapis.com/v1\n    tags:\n      - Collaboration\n      - Groups\n      - Membership\n      - Organization\n      - Teams\n    serviceName: Webex Teams API\n    serviceCategory: API\n  - name: Webex Rooms API\n    baseURL: https://webexapis.com/v1\n    tags:\n      - Channels\n      - Collaboration\n      - Messaging\n      - Rooms\n      - Spaces\n    serviceName: Webex Rooms API\n    serviceCategory: API\n  - name: Webex Webhooks API\n    baseURL: https://webexapis.com/v1\n    tags:\n      - Callbacks\n      - Events\n      - Notifications\n      - Real-Time\n      - Webhooks\n    serviceName: Webex Webhooks API\n    serviceCategory: API\n  - name: Webex Devices API\n    baseURL: https://webexapis.com/v1\n    tags:\n      - Devices\n      - Hardware\n      - Management\n      - Room Systems\n      - Workspaces\n    serviceName: Webex Devices API\n    serviceCategory: API\n  - name: Webex Memberships API\n    baseURL: https://webexapis.com/v1\n\
  \    tags:\n      - Access Control\n      - Memberships\n      - Permissions\n      - Rooms\n      - Users\n    serviceName: Webex Memberships API\n    serviceCategory: API\n  - name: Webex Team Memberships API\n    baseURL: https://webexapis.com/v1\n    tags:\n      - Access Control\n      - Collaboration\n      - Roles\n      - Team Memberships\n      - Teams\n    serviceName: Webex Team Memberships API\n    serviceCategory: API\n  - name: Webex Events API\n    baseURL: https://webexapis.com/v1\n    tags:\n      - Activity\n      - Auditing\n      - Compliance\n      - Events\n      - Monitoring\n    serviceName: Webex Events API\n    serviceCategory: API\n  - name: Webex Recordings API\n    baseURL: https://webexapis.com/v1\n    tags:\n      - Compliance\n      - Media\n      - Meetings\n      - Recordings\n      - Storage\n    serviceName: Webex Recordings API\n    serviceCategory: API\n  - name: Webex Call Controls API\n    baseURL: https://webexapis.com/v1\n    tags:\n      - Call\
  \ Control\n      - Calling\n      - Communications\n      - Telephony\n      - Voice\n    serviceName: Webex Call Controls API\n    serviceCategory: API\n  - name: Webex Attachment Actions API\n    baseURL: https://webexapis.com/v1\n    tags:\n      - Attachment Actions\n      - Buttons\n      - Cards\n      - Interactive\n      - Messaging\n    serviceName: Webex Attachment Actions API\n    serviceCategory: API\n  - name: Webex Organizations API\n    baseURL: https://webexapis.com/v1\n    tags:\n      - Administration\n      - Enterprise\n      - Management\n      - Organizations\n      - Settings\n    serviceName: Webex Organizations API\n    serviceCategory: API\n  - name: Webex Licenses API\n    baseURL: https://webexapis.com/v1\n    tags:\n      - Administration\n      - Entitlements\n      - Licenses\n      - Management\n      - Provisioning\n    serviceName: Webex Licenses API\n    serviceCategory: API\n  - name: Webex Roles API\n    baseURL: https://webexapis.com/v1\n    tags:\n\
  \      - Access Control\n      - Administration\n      - Permissions\n      - Roles\n      - Security\n    serviceName: Webex Roles API\n    serviceCategory: API\n  - name: Webex Workspaces API\n    baseURL: https://webexapis.com/v1\n    tags:\n      - Devices\n      - Facilities\n      - Locations\n      - Management\n      - Workspaces\n    serviceName: Webex Workspaces API\n    serviceCategory: API\n  - name: Webex Admin Audit Events API\n    baseURL: https://webexapis.com/v1\n    tags:\n      - Administration\n      - Audit\n      - Compliance\n      - Events\n      - Security\n    serviceName: Webex Admin Audit Events API\n    serviceCategory: API\n  - name: Webex Converged Recordings API\n    baseURL: https://webexapis.com/v1\n    tags:\n      - Calling\n      - Compliance\n      - Media\n      - Meetings\n      - Recordings\n    serviceName: Webex Converged Recordings API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests\
  \ / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n    url: https://developer.webex.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/cisco-webex/refs/heads/main/finops/cisco-webex-finops.yml
sources: []
specification: FinOps Framework
tags:
- Collaboration
- Communications
- Meetings
- Messaging
- Teams
- Video Conferencing
- FinOps
- Cost Management
- FOCUS
---
