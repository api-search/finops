---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
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
description: FinOps framework definition for the Cisco Webex Meetings API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Cisco Webex Meetings
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Cisco Webex Meetings
  PublisherName: Cisco Webex Meetings
  ServiceCategory: Developer Tools / API
  ServiceName: Cisco Webex Meetings
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
name: Cisco Webex Meetings Finops
provider_name: Cisco Webex Meetings
provider_slug: cisco-webex-meetings
publisher_name: Cisco Webex Meetings
service_category: API
slug: cisco-webex-meetings-finops
source_filename: cisco-webex-meetings-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Cisco Webex Meetings\nproviderId: cisco-webex-meetings\npublisherName: Cisco Webex Meetings\nserviceCategory: API\ncreated: '2026-05-04'\nmodified: '2026-05-04'\ntags:\n  - Collaboration\n  - Communications\n  - Enterprise\n  - Meetings\n  - Video Conferencing\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Cisco Webex Meetings API surface. Provides a FOCUS-aligned\n  mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n\
  \    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage\
  \ the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Cisco Webex Meetings\n  ServiceCategory: Developer Tools / API\n  ProviderName: Cisco Webex Meetings\n  PublisherName: Cisco Webex Meetings\n  InvoiceIssuerName: Cisco Webex Meetings\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n\
  \    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Webex Meetings API\n    baseURL: https://webexapis.com/v1\n    tags:\n      - Conferencing\n      - Meetings\n      - Scheduling\n      - Video\n    serviceName: Webex Meetings API\n    serviceCategory: API\n  - name: Webex Meeting Invitees API\n    baseURL: https://webexapis.com/v1\n    tags:\n      - Attendees\n      - Invitees\n      - Meetings\n    serviceName: Webex Meeting Invitees API\n    serviceCategory: API\n  - name: Webex Meeting Participants API\n    baseURL: https://webexapis.com/v1\n    tags:\n      - Attendees\n      - Participants\n      - Real-Time\n    serviceName: Webex Meeting Participants\
  \ API\n    serviceCategory: API\n  - name: Webex Meeting Preferences API\n    baseURL: https://webexapis.com/v1\n    tags:\n      - Personal Room\n      - Preferences\n      - Settings\n    serviceName: Webex Meeting Preferences API\n    serviceCategory: API\n  - name: Webex Recordings API\n    baseURL: https://webexapis.com/v1\n    tags:\n      - Compliance\n      - Media\n      - Recordings\n      - Storage\n    serviceName: Webex Recordings API\n    serviceCategory: API\n  - name: Webex Meeting Transcripts API\n    baseURL: https://webexapis.com/v1\n    tags:\n      - Accessibility\n      - AI\n      - Captions\n      - Transcripts\n    serviceName: Webex Meeting Transcripts API\n    serviceCategory: API\n  - name: Webex Meeting Q and A API\n    baseURL: https://webexapis.com/v1\n    tags:\n      - Engagement\n      - Q and A\n      - Webinars\n    serviceName: Webex Meeting Q and A API\n    serviceCategory: API\n  - name: Webex Meeting Polls API\n    baseURL: https://webexapis.com/v1\n\
  \    tags:\n      - Engagement\n      - Polls\n      - Surveys\n    serviceName: Webex Meeting Polls API\n    serviceCategory: API\n  - name: Webex Meeting Chats API\n    baseURL: https://webexapis.com/v1\n    tags:\n      - Chat\n      - Compliance\n      - Meetings\n    serviceName: Webex Meeting Chats API\n    serviceCategory: API\n  - name: Webex XML API\n    baseURL: ''\n    tags:\n      - Enterprise\n      - Legacy\n      - SOAP\n      - XML\n    serviceName: Webex XML API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/cisco-webex-meetings/refs/heads/main/finops/cisco-webex-meetings-finops.yml
sources: []
specification: FinOps Framework
tags:
- Collaboration
- Communications
- Enterprise
- Meetings
- Video Conferencing
- FinOps
- Cost Management
- FOCUS
---
