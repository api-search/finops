---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: zoom-chat--openapi-original.yml
  format: yaml
  label: Zoom Chat API
  slug: zoom-chat-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/zoom/refs/heads/main/openapi/zoom-chat--openapi-original.yml
- filename: zoom-group--openapi-original.yml
  format: yaml
  label: Zoom Group API
  slug: zoom-group-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/zoom/refs/heads/main/openapi/zoom-group--openapi-original.yml
- filename: zoom-device--openapi-original.yml
  format: yaml
  label: Zoom Device API
  slug: zoom-device-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/zoom/refs/heads/main/openapi/zoom-device--openapi-original.yml
- filename: zoom-im--openapi-original.yml
  format: yaml
  label: Zoom Instant Message API
  slug: zoom-instant-message-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/zoom/refs/heads/main/openapi/zoom-im--openapi-original.yml
- filename: zoom-account--openapi-original.yml
  format: yaml
  label: Zoom Account API
  slug: zoom-account-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/zoom/refs/heads/main/openapi/zoom-account--openapi-original.yml
- filename: zoom-recording--openapi-original.yml
  format: yaml
  label: Zoom Recording API
  slug: zoom-recording-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/zoom/refs/heads/main/openapi/zoom-recording--openapi-original.yml
- filename: zoom-meeting--openapi-original.yml
  format: yaml
  label: Zoom Meeting API
  slug: zoom-meeting-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/zoom/refs/heads/main/openapi/zoom-meeting--openapi-original.yml
- filename: zoom-metrics--openapi-original.yml
  format: yaml
  label: Zoom Metrics API
  slug: zoom-metrics-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/zoom/refs/heads/main/openapi/zoom-metrics--openapi-original.yml
- filename: zoom-report--openapi-original.yml
  format: yaml
  label: Zoom Report API
  slug: zoom-report-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/zoom/refs/heads/main/openapi/zoom-report--openapi-original.yml
- filename: zoom-user--openapi-original.yml
  format: yaml
  label: Zoom User API
  slug: zoom-user-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/zoom/refs/heads/main/openapi/zoom-user--openapi-original.yml
- filename: zoom-webinar--openapi-original.yml
  format: yaml
  label: Zoom Webinar API
  slug: zoom-webinar-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/zoom/refs/heads/main/openapi/zoom-webinar--openapi-original.yml
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
description: FinOps framework definition for the Zoom API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Zoom
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Zoom
  PublisherName: Zoom
  ServiceCategory: Developer Tools / API
  ServiceName: Zoom
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
name: Zoom Finops
provider_name: Zoom
provider_slug: zoom
publisher_name: Zoom
service_category: API
slug: zoom-finops
source_filename: zoom-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Zoom\nproviderId: zoom\npublisherName: Zoom\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Chat\n  - Collaboration\n  - Communications\n  - Meetings\n  - Video Conferencing\n  - Videos\n  - Webinars\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Zoom API surface. Provides a FOCUS-aligned mapping for\n  cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API\
  \ call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n\
  \      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Zoom\n  ServiceCategory: Developer Tools / API\n  ProviderName: Zoom\n  PublisherName: Zoom\n  InvoiceIssuerName: Zoom\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n\
  \    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Zoom Chat API\n    baseURL: https://api.zoom.us/v2\n    tags:\n      - Chat\n    serviceName: Zoom Chat API\n    serviceCategory: API\n  - name: Zoom Group API\n    baseURL: https://api.zoom.us/v2\n    tags:\n      - Edit\n      - Groups\n      - Members\n    serviceName: Zoom Group API\n    serviceCategory: API\n  - name: Zoom Device API\n    baseURL: https://api.zoom.us/v2\n    tags:\n      - Device\n      - H323\n    serviceName: Zoom Device API\n    serviceCategory: API\n  - name: Zoom Instant Message API\n    baseURL: https://api.zoom.us/v2\n    tags:\n      - Edit\n      - Groups\n      - Members\n    serviceName: Zoom Instant Message API\n    serviceCategory: API\n  - name: Zoom Account API\n\
  \    baseURL: https://api.zoom.us/v2\n    tags:\n      - Accounts\n      - Billing\n      - Plan\n      - Subscribe\n    serviceName: Zoom Account API\n    serviceCategory: API\n  - name: Zoom Recording API\n    baseURL: https://api.zoom.us/v2\n    tags:\n      - Mc\n      - Recording\n    serviceName: Zoom Recording API\n    serviceCategory: API\n  - name: Zoom Meeting API\n    baseURL: https://api.zoom.us/v2\n    tags:\n      - Live\n      - Meetings\n      - Register\n    serviceName: Zoom Meeting API\n    serviceCategory: API\n  - name: Zoom Metrics API\n    baseURL: https://api.zoom.us/v2\n    tags:\n      - Crc\n      - Meetingdetail\n      - Meetings\n      - Metrics\n      - Qos\n      - Webinardetail\n      - Webinars\n      - Zoomroomdetail\n      - Zoomrooms\n    serviceName: Zoom Metrics API\n    serviceCategory: API\n  - name: Zoom Report API\n    baseURL: https://api.zoom.us/v2\n    tags:\n      - Reports\n    serviceName: Zoom Report API\n    serviceCategory: API\n  - name:\
  \ Zoom User API\n    baseURL: https://api.zoom.us/v2\n    tags:\n      - Activate\n      - Assistants\n      - Autocreate\n      - Checkemail\n      - Checkzpk\n      - Custcreate\n      - Deactivate\n      - Getbyemail\n      - Pending\n      - Permanentdelete\n      - Revoketoken\n      - Scheduleforhost\n      - Sets\n      - Ssocreate\n      - Updatepassword\n      - Users\n    serviceName: Zoom User API\n    serviceCategory: API\n  - name: Zoom Webinar API\n    baseURL: https://api.zoom.us/v2\n    tags:\n      - Approve\n      - Attendees\n      - Cancel\n      - Panelists\n      - Polls\n      - Questions\n      - Register\n      - Registrants\n      - Registrations\n      - Uu\n      - Webinar\n    serviceName: Zoom Webinar API\n    serviceCategory: API\n  - name: Zoom Phone API\n    baseURL: https://api.zoom.us/v2\n    tags:\n      - Calling\n      - Phone\n      - Voice\n    serviceName: Zoom Phone API\n    serviceCategory: API\n  - name: Zoom Team Chat API\n    baseURL: https://api.zoom.us/v2\n\
  \    tags:\n      - Channels\n      - Chat\n      - Collaboration\n      - Messaging\n    serviceName: Zoom Team Chat API\n    serviceCategory: API\n  - name: Zoom Contact Center API\n    baseURL: https://api.zoom.us/v2\n    tags:\n      - Agents\n      - Contact Center\n      - Customer Service\n    serviceName: Zoom Contact Center API\n    serviceCategory: API\n  - name: Zoom Webinars Plus and Events API\n    baseURL: https://api.zoom.us/v2\n    tags:\n      - Conferences\n      - Events\n      - Registrations\n      - Webinars\n    serviceName: Zoom Webinars Plus and Events API\n    serviceCategory: API\n  - name: Zoom Marketplace API\n    baseURL: https://api.zoom.us/v2\n    tags:\n      - Apps\n      - Integrations\n      - Marketplace\n    serviceName: Zoom Marketplace API\n    serviceCategory: API\n  - name: Zoom Revenue Accelerator API\n    baseURL: https://api.zoom.us/v2\n    tags:\n      - Analytics\n      - CRM\n      - Revenue\n      - Sales\n    serviceName: Zoom Revenue Accelerator\
  \ API\n    serviceCategory: API\n  - name: Zoom Whiteboard API\n    baseURL: https://api.zoom.us/v2\n    tags:\n      - Collaboration\n      - Drawing\n      - Whiteboard\n    serviceName: Zoom Whiteboard API\n    serviceCategory: API\n  - name: Zoom Rooms API\n    baseURL: https://api.zoom.us/v2\n    tags:\n      - Conference Rooms\n      - Devices\n      - Rooms\n      - Workspaces\n    serviceName: Zoom Rooms API\n    serviceCategory: API\n  - name: Zoom Clips API\n    baseURL: https://api.zoom.us/v2\n    tags:\n      - Clips\n      - Recording\n      - Sharing\n      - Video\n    serviceName: Zoom Clips API\n    serviceCategory: API\n  - name: Zoom Mail API\n    baseURL: https://api.zoom.us/v2\n    tags:\n      - Email\n      - Mail\n      - Messaging\n    serviceName: Zoom Mail API\n    serviceCategory: API\n  - name: Zoom Calendar API\n    baseURL: https://api.zoom.us/v2\n    tags:\n      - Calendar\n      - Events\n      - Scheduling\n    serviceName: Zoom Calendar API\n    serviceCategory:\
  \ API\n  - name: Zoom Scheduler API\n    baseURL: https://api.zoom.us/v2\n    tags:\n      - Appointments\n      - Booking\n      - Scheduler\n    serviceName: Zoom Scheduler API\n    serviceCategory: API\n  - name: Zoom Chatbot API\n    baseURL: https://api.zoom.us/v2\n    tags:\n      - Automation\n      - Bots\n      - Chatbot\n    serviceName: Zoom Chatbot API\n    serviceCategory: API\n  - name: Zoom AI Companion API\n    baseURL: https://api.zoom.us/v2\n    tags:\n      - AI\n      - Artificial Intelligence\n      - Companion\n    serviceName: Zoom AI Companion API\n    serviceCategory: API\n  - name: Zoom Docs API\n    baseURL: https://api.zoom.us/v2\n    tags:\n      - Collaboration\n      - Documents\n      - Files\n    serviceName: Zoom Docs API\n    serviceCategory: API\n  - name: Zoom Tasks API\n    baseURL: https://api.zoom.us/v2\n    tags:\n      - Productivity\n      - Project Management\n      - Tasks\n    serviceName: Zoom Tasks API\n    serviceCategory: API\n  - name:\
  \ Zoom CRC API\n    baseURL: https://api.zoom.us/v2\n    tags:\n      - Conference Room Connector\n      - Devices\n      - H323\n      - SIP\n    serviceName: Zoom CRC API\n    serviceCategory: API\n  - name: Zoom Virtual Agent API\n    baseURL: https://api.zoom.us/v2\n    tags:\n      - AI\n      - Chatbot\n      - Customer Support\n      - Virtual Agent\n    serviceName: Zoom Virtual Agent API\n    serviceCategory: API\n  - name: Zoom Number Management API\n    baseURL: https://api.zoom.us/v2\n    tags:\n      - BYOC\n      - Phone Numbers\n      - Provisioning\n    serviceName: Zoom Number Management API\n    serviceCategory: API\n  - name: Zoom Quality Management API\n    baseURL: https://api.zoom.us/v2\n    tags:\n      - Analytics\n      - Contact Center\n      - Evaluation\n      - Quality Management\n    serviceName: Zoom Quality Management API\n    serviceCategory: API\n  - name: Zoom Workforce Management API\n    baseURL: https://api.zoom.us/v2\n    tags:\n      - Forecasting\n\
  \      - Scheduling\n      - Workforce Management\n    serviceName: Zoom Workforce Management API\n    serviceCategory: API\n  - name: Zoom Commerce API\n    baseURL: https://api.zoom.us/v2\n    tags:\n      - Billing\n      - Commerce\n      - Partners\n      - Subscriptions\n    serviceName: Zoom Commerce API\n    serviceCategory: API\n  - name: Zoom Healthcare API\n    baseURL: https://api.zoom.us/v2\n    tags:\n      - Clinical Notes\n      - Healthcare\n      - Telehealth\n    serviceName: Zoom Healthcare API\n    serviceCategory: API\n  - name: Zoom Video Management API\n    baseURL: https://api.zoom.us/v2\n    tags:\n      - Channels\n      - Playlists\n      - Video Management\n    serviceName: Zoom Video Management API\n    serviceCategory: API\n  - name: Zoom Auto Dialer API\n    baseURL: https://api.zoom.us/v2\n    tags:\n      - Auto Dialer\n      - Calling\n      - Outreach\n    serviceName: Zoom Auto Dialer API\n    serviceCategory: API\n  - name: Zoom QSS API\n    baseURL:\
  \ https://api.zoom.us/v2\n    tags:\n      - Monitoring\n      - Network\n      - Quality of Service\n    serviceName: Zoom QSS API\n    serviceCategory: API\n  - name: Zoom SCIM2 API\n    baseURL: https://api.zoom.us/v2\n    tags:\n      - Identity\n      - Provisioning\n      - SCIM\n      - SSO\n    serviceName: Zoom SCIM2 API\n    serviceCategory: API\n  - name: Zoom Video SDK API\n    baseURL: https://api.zoom.us/v2\n    tags:\n      - Cloud Recording\n      - Sessions\n      - Video SDK\n    serviceName: Zoom Video SDK API\n    serviceCategory: API\n  - name: Zoom Meeting SDK\n    baseURL: https://api.zoom.us/v2\n    tags:\n      - Embed\n      - Integration\n      - Meeting SDK\n      - Web\n    serviceName: Zoom Meeting SDK\n    serviceCategory: API\n  - name: Zoom Cobrowse SDK API\n    baseURL: https://api.zoom.us/v2\n    tags:\n      - Cobrowse\n      - Customer Support\n      - Screen Sharing\n    serviceName: Zoom Cobrowse SDK API\n    serviceCategory: API\nunitEconomics:\n\
  \  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/zoom/refs/heads/main/finops/zoom-finops.yml
sources: []
specification: FinOps Framework
tags:
- Chat
- Collaboration
- Communications
- Meetings
- Video Conferencing
- Videos
- Webinars
- FinOps
- Cost Management
- FOCUS
---
