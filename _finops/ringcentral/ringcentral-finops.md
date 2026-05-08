---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: ringcentral-platform-openapi.yml
  format: yaml
  label: RingCentral Voice API
  slug: ringcentral-voice-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/ringcentral/refs/heads/main/openapi/ringcentral-platform-openapi.yml
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
description: FinOps framework definition for the RingCentral API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: RingCentral
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: RingCentral
  PublisherName: RingCentral
  ServiceCategory: Developer Tools / API
  ServiceName: RingCentral
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
name: Ringcentral Finops
provider_name: RingCentral
provider_slug: ringcentral
publisher_name: RingCentral
service_category: API
slug: ringcentral-finops
source_filename: ringcentral-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: RingCentral\nproviderId: ringcentral\npublisherName: RingCentral\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Communications\n  - UCaaS\n  - Voice\n  - Video\n  - Contact Center\n  - SMS\n  - Messaging\n  - Fax\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the RingCentral API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag\
  \ every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n\
  \    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: RingCentral\n  ServiceCategory: Developer Tools / API\n  ProviderName: RingCentral\n  PublisherName: RingCentral\n  InvoiceIssuerName: RingCentral\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n\
  \    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: RingCentral Voice API\n    baseURL: ''\n    tags:\n      - Voice\n      - Telephony\n      - Call Control\n      - RingOut\n    serviceName: RingCentral Voice API\n    serviceCategory: API\n  - name: RingCentral SMS API\n    baseURL: ''\n    tags:\n      - SMS\n      - Messaging\n      - A2P\n      - Compliance\n    serviceName: RingCentral SMS API\n    serviceCategory: API\n  - name: RingCentral Team Messaging API\n    baseURL: ''\n    tags:\n      - Team Messaging\n      - Chat\n      - Bots\n      - Add-ins\n    serviceName: RingCentral Team Messaging API\n    serviceCategory: API\n  - name: RingCentral Video API\n    baseURL: ''\n    tags:\n      - Video\n    \
  \  - Meetings\n      - Webinars\n      - Conferencing\n    serviceName: RingCentral Video API\n    serviceCategory: API\n  - name: RingCentral Fax API\n    baseURL: ''\n    tags:\n      - Fax\n      - Documents\n    serviceName: RingCentral Fax API\n    serviceCategory: API\n  - name: RingCentral Data API\n    baseURL: ''\n    tags:\n      - Compliance\n      - Data\n      - Recordings\n      - Exports\n    serviceName: RingCentral Data API\n    serviceCategory: API\n  - name: RingCentral Audio and Video AI API\n    baseURL: ''\n    tags:\n      - AI\n      - Transcription\n      - Summarization\n      - Speech-to-Text\n    serviceName: RingCentral Audio and Video AI API\n    serviceCategory: API\n  - name: RingCentral Call Log API\n    baseURL: ''\n    tags:\n      - Call Log\n      - Analytics\n      - History\n    serviceName: RingCentral Call Log API\n    serviceCategory: API\n  - name: RingCentral Call Analytics API\n    baseURL: ''\n    tags:\n      - Analytics\n      - KPIs\n  \
  \    - Reporting\n    serviceName: RingCentral Call Analytics API\n    serviceCategory: API\n  - name: RingCentral Presence API\n    baseURL: ''\n    tags:\n      - Presence\n      - Status\n      - Real-Time\n    serviceName: RingCentral Presence API\n    serviceCategory: API\n  - name: RingCentral Voicemail API\n    baseURL: ''\n    tags:\n      - Voicemail\n      - Messaging\n    serviceName: RingCentral Voicemail API\n    serviceCategory: API\n  - name: RingCentral Provisioning API\n    baseURL: ''\n    tags:\n      - Provisioning\n      - Account\n      - Extensions\n      - Phone Numbers\n    serviceName: RingCentral Provisioning API\n    serviceCategory: API\n  - name: RingCentral Webhooks and Subscriptions API\n    baseURL: ''\n    tags:\n      - Webhooks\n      - Events\n      - Subscriptions\n      - PubNub\n    serviceName: RingCentral Webhooks and Subscriptions API\n    serviceCategory: API\n  - name: RingCentral Contact Center API\n    baseURL: ''\n    tags:\n      - Contact\
  \ Center\n      - CCaaS\n      - Agents\n      - Routing\n    serviceName: RingCentral Contact Center API\n    serviceCategory: API\n  - name: RingCentral Events API\n    baseURL: ''\n    tags:\n      - Events\n      - Webinars\n      - Hub\n    serviceName: RingCentral Events API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/ringcentral/refs/heads/main/finops/ringcentral-finops.yml
sources: []
specification: FinOps Framework
tags:
- Communications
- UCaaS
- Voice
- Video
- Contact Center
- SMS
- Messaging
- Fax
- FinOps
- Cost Management
- FOCUS
---
