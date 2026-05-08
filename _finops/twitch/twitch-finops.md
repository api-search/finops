---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: reference
  format: yaml
  label: Twitch API
  slug: ''
  spec_type: OpenAPI
  url: https://dev.twitch.tv/docs/api/reference
- filename: twitch-eventsub-asyncapi.yml
  format: yaml
  label: Twitch EventSub
  slug: ''
  spec_type: AsyncAPI
  url: https://raw.githubusercontent.com/api-evangelist/twitch/refs/heads/main/asyncapi/twitch-eventsub-asyncapi.yml
- filename: twitch-extensions-openapi.yml
  format: yaml
  label: Twitch Extensions API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/twitch/refs/heads/main/openapi/twitch-extensions-openapi.yml
- filename: twitch-drops-openapi.yml
  format: yaml
  label: Twitch Drops API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/twitch/refs/heads/main/openapi/twitch-drops-openapi.yml
- filename: twitch-video-broadcast-openapi.yml
  format: yaml
  label: Twitch Video Broadcast API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/twitch/refs/heads/main/openapi/twitch-video-broadcast-openapi.yml
- filename: twitch-insights-analytics-openapi.yml
  format: yaml
  label: Twitch Insights and Analytics API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/twitch/refs/heads/main/openapi/twitch-insights-analytics-openapi.yml
- filename: twitch-igdb-openapi.yml
  format: yaml
  label: IGDB API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/twitch/refs/heads/main/openapi/twitch-igdb-openapi.yml
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
description: FinOps framework definition for the Twitch API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Twitch
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Twitch
  PublisherName: Twitch
  ServiceCategory: Developer Tools / API
  ServiceName: Twitch
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
name: Twitch Finops
provider_name: Twitch
provider_slug: twitch
publisher_name: Twitch
service_category: API
slug: twitch-finops
source_filename: twitch-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Twitch\nproviderId: twitch\npublisherName: Twitch\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Entertainment\n  - Gaming\n  - Live Video\n  - Streaming\n  - Video\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Twitch API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team,\
  \ environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n\
  \      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Twitch\n  ServiceCategory: Developer Tools / API\n  ProviderName: Twitch\n  PublisherName: Twitch\n  InvoiceIssuerName: Twitch\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n\
  \      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Twitch API\n    baseURL: https://api.twitch.tv/helix\n    tags:\n      - Chat\n      - Gaming\n      - Streaming\n      - Video\n    serviceName: Twitch API\n    serviceCategory: API\n  - name: Twitch EventSub\n    baseURL: https://api.twitch.tv/helix/eventsub\n    tags:\n      - Events\n      - Notifications\n      - Webhooks\n    serviceName: Twitch EventSub\n    serviceCategory: API\n  - name: Twitch Chat API\n    baseURL: wss://irc-ws.chat.twitch.tv:443\n    tags:\n      - Chat\n      - Irc\n      - Messaging\n      - Websocket\n    serviceName: Twitch Chat API\n    serviceCategory: API\n  - name: Twitch Embed API\n    baseURL: https://embed.twitch.tv\n    tags:\n      - Chat\n      - Clips\n      - Embed\n      - Player\n  \
  \    - Video\n    serviceName: Twitch Embed API\n    serviceCategory: API\n  - name: Twitch Extensions API\n    baseURL: https://api.twitch.tv/helix/extensions\n    tags:\n      - Extensions\n      - Interactive\n      - Overlays\n      - Panels\n    serviceName: Twitch Extensions API\n    serviceCategory: API\n  - name: Twitch Drops API\n    baseURL: https://api.twitch.tv/helix\n    tags:\n      - Campaigns\n      - Drops\n      - Gaming\n      - Rewards\n    serviceName: Twitch Drops API\n    serviceCategory: API\n  - name: Twitch Video Broadcast API\n    baseURL: https://ingest.twitch.tv\n    tags:\n      - Broadcast\n      - Ingest\n      - Rtmp\n      - Streaming\n      - Video\n    serviceName: Twitch Video Broadcast API\n    serviceCategory: API\n  - name: Twitch Insights and Analytics API\n    baseURL: https://api.twitch.tv/helix/analytics\n    tags:\n      - Analytics\n      - Insights\n      - Metrics\n      - Reporting\n    serviceName: Twitch Insights and Analytics API\n  \
  \  serviceCategory: API\n  - name: IGDB API\n    baseURL: https://api.igdb.com/v4\n    tags:\n      - Database\n      - Games\n      - Metadata\n      - Ratings\n    serviceName: IGDB API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/twitch/refs/heads/main/finops/twitch-finops.yml
sources: []
specification: FinOps Framework
tags:
- Entertainment
- Gaming
- Live Video
- Streaming
- Video
- FinOps
- Cost Management
- FOCUS
---
