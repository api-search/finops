---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: youtube-data-api-openapi.yml
  format: yaml
  label: Youtube Activities API
  slug: youtube-activities-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/youtube/refs/heads/main/openapi/youtube-data-api-openapi.yml
- filename: youtube-data-api-openapi.yml
  format: yaml
  label: Youtube Channels API
  slug: youtube-channels-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/youtube/refs/heads/main/openapi/youtube-data-api-openapi.yml
- filename: youtube-data-api-openapi.yml
  format: yaml
  label: Youtube Comments API
  slug: youtube-comments-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/youtube/refs/heads/main/openapi/youtube-data-api-openapi.yml
- filename: youtube-data-api-openapi.yml
  format: yaml
  label: Youtube Comment Threads API
  slug: youtube-comment-threads-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/youtube/refs/heads/main/openapi/youtube-data-api-openapi.yml
- filename: youtube-data-api-openapi.yml
  format: yaml
  label: Youtube Playlists API
  slug: youtube-playlists-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/youtube/refs/heads/main/openapi/youtube-data-api-openapi.yml
- filename: youtube-data-api-openapi.yml
  format: yaml
  label: Youtube Playlist Items API
  slug: youtube-playlist-items-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/youtube/refs/heads/main/openapi/youtube-data-api-openapi.yml
- filename: youtube-data-api-openapi.yml
  format: yaml
  label: Youtube Search API
  slug: youtube-search-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/youtube/refs/heads/main/openapi/youtube-data-api-openapi.yml
- filename: youtube-data-api-openapi.yml
  format: yaml
  label: Youtube Subscriptions API
  slug: youtube-subscriptions-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/youtube/refs/heads/main/openapi/youtube-data-api-openapi.yml
- filename: youtube-data-api-openapi.yml
  format: yaml
  label: Youtube Videos API
  slug: youtube-videos-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/youtube/refs/heads/main/openapi/youtube-data-api-openapi.yml
- filename: youtube-data-api-openapi.yml
  format: yaml
  label: Youtube Captions API
  slug: youtube-captions-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/youtube/refs/heads/main/openapi/youtube-data-api-openapi.yml
- filename: youtube-data-api-openapi.yml
  format: yaml
  label: Youtube Video Categories API
  slug: youtube-video-categories-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/youtube/refs/heads/main/openapi/youtube-data-api-openapi.yml
- filename: youtube-data-api-openapi.yml
  format: yaml
  label: Youtube I18n Languages API
  slug: youtube-i18n-languages-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/youtube/refs/heads/main/openapi/youtube-data-api-openapi.yml
- filename: youtube-data-api-openapi.yml
  format: yaml
  label: Youtube I18n Regions API
  slug: youtube-i18n-regions-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/youtube/refs/heads/main/openapi/youtube-data-api-openapi.yml
- filename: youtube-analytics-openapi.yml
  format: yaml
  label: YouTube Analytics API
  slug: youtube-analytics-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/youtube/refs/heads/main/openapi/youtube-analytics-openapi.yml
- filename: youtube-reporting-openapi.yml
  format: yaml
  label: YouTube Reporting API
  slug: youtube-reporting-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/youtube/refs/heads/main/openapi/youtube-reporting-openapi.yml
- filename: youtube-live-streaming-openapi.yml
  format: yaml
  label: YouTube Live Streaming API
  slug: youtube-live-streaming-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/youtube/refs/heads/main/openapi/youtube-live-streaming-openapi.yml
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
description: FinOps framework definition for the Youtube API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Youtube
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Youtube
  PublisherName: Youtube
  ServiceCategory: Developer Tools / API
  ServiceName: Youtube
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
name: Youtube Finops
provider_name: Youtube
provider_slug: youtube
publisher_name: Youtube
service_category: API
slug: youtube-finops
source_filename: youtube-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Youtube\nproviderId: youtube\npublisherName: Youtube\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Google\n  - Media\n  - Social\n  - Streaming\n  - Video\n  - Videos\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Youtube API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team,\
  \ environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n\
  \      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Youtube\n  ServiceCategory: Developer Tools / API\n  ProviderName: Youtube\n  PublisherName: Youtube\n  InvoiceIssuerName: Youtube\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      -\
  \ api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Youtube Activities API\n    baseURL: https://www.googleapis.com/youtube/v3\n    tags:\n      - Activities\n      - Videos\n    serviceName: Youtube Activities API\n    serviceCategory: API\n  - name: Youtube Channels API\n    baseURL: https://www.googleapis.com/youtube/v3\n    tags:\n      - Channels\n      - Videos\n    serviceName: Youtube Channels API\n    serviceCategory: API\n  - name: Youtube Comments API\n    baseURL: https://www.googleapis.com/youtube/v3\n    tags:\n      - Comments\n      - Videos\n    serviceName: Youtube Comments API\n    serviceCategory: API\n  - name: Youtube Comment Threads API\n    baseURL: https://www.googleapis.com/youtube/v3\n    tags:\n      - Comments\n      - Videos\n    serviceName: Youtube\
  \ Comment Threads API\n    serviceCategory: API\n  - name: Youtube Playlists API\n    baseURL: https://www.googleapis.com/youtube/v3\n    tags:\n      - Playlists\n      - Videos\n    serviceName: Youtube Playlists API\n    serviceCategory: API\n  - name: Youtube Playlist Items API\n    baseURL: https://www.googleapis.com/youtube/v3\n    tags:\n      - Playlists\n      - Videos\n    serviceName: Youtube Playlist Items API\n    serviceCategory: API\n  - name: Youtube Search API\n    baseURL: https://www.googleapis.com/youtube/v3\n    tags:\n      - Search\n      - Videos\n    serviceName: Youtube Search API\n    serviceCategory: API\n  - name: Youtube Subscriptions API\n    baseURL: https://www.googleapis.com/youtube/v3\n    tags:\n      - Subscriptions\n      - Videos\n    serviceName: Youtube Subscriptions API\n    serviceCategory: API\n  - name: Youtube Videos API\n    baseURL: https://www.googleapis.com/youtube/v3\n    tags:\n      - Videos\n    serviceName: Youtube Videos API\n   \
  \ serviceCategory: API\n  - name: Youtube Captions API\n    baseURL: https://www.googleapis.com/youtube/v3\n    tags:\n      - Captions\n      - Videos\n    serviceName: Youtube Captions API\n    serviceCategory: API\n  - name: Youtube Channel Sections API\n    baseURL: https://www.googleapis.com/youtube/v3\n    tags:\n      - Channels\n      - Videos\n    serviceName: Youtube Channel Sections API\n    serviceCategory: API\n  - name: Youtube Channel Banners API\n    baseURL: https://www.googleapis.com/youtube/v3\n    tags:\n      - Channels\n      - Videos\n    serviceName: Youtube Channel Banners API\n    serviceCategory: API\n  - name: Youtube Members API\n    baseURL: https://www.googleapis.com/youtube/v3\n    tags:\n      - Members\n      - Monetization\n      - Videos\n    serviceName: Youtube Members API\n    serviceCategory: API\n  - name: Youtube Memberships Levels API\n    baseURL: https://www.googleapis.com/youtube/v3\n    tags:\n      - Members\n      - Monetization\n      -\
  \ Videos\n    serviceName: Youtube Memberships Levels API\n    serviceCategory: API\n  - name: Youtube Thumbnails API\n    baseURL: https://www.googleapis.com/youtube/v3\n    tags:\n      - Thumbnails\n      - Videos\n    serviceName: Youtube Thumbnails API\n    serviceCategory: API\n  - name: Youtube Watermarks API\n    baseURL: https://www.googleapis.com/youtube/v3\n    tags:\n      - Videos\n      - Watermarks\n    serviceName: Youtube Watermarks API\n    serviceCategory: API\n  - name: Youtube Video Categories API\n    baseURL: https://www.googleapis.com/youtube/v3\n    tags:\n      - Categories\n      - Videos\n    serviceName: Youtube Video Categories API\n    serviceCategory: API\n  - name: Youtube Video Abuse Report Reasons API\n    baseURL: https://www.googleapis.com/youtube/v3\n    tags:\n      - Moderation\n      - Videos\n    serviceName: Youtube Video Abuse Report Reasons API\n    serviceCategory: API\n  - name: Youtube I18n Languages API\n    baseURL: https://www.googleapis.com/youtube/v3\n\
  \    tags:\n      - Localization\n      - Videos\n    serviceName: Youtube I18n Languages API\n    serviceCategory: API\n  - name: Youtube I18n Regions API\n    baseURL: https://www.googleapis.com/youtube/v3\n    tags:\n      - Localization\n      - Videos\n    serviceName: Youtube I18n Regions API\n    serviceCategory: API\n  - name: YouTube Analytics API\n    baseURL: https://youtubeanalytics.googleapis.com/v2\n    tags:\n      - Analytics\n      - Reporting\n      - Videos\n    serviceName: YouTube Analytics API\n    serviceCategory: API\n  - name: YouTube Reporting API\n    baseURL: https://youtubereporting.googleapis.com\n    tags:\n      - Analytics\n      - Reporting\n      - Videos\n    serviceName: YouTube Reporting API\n    serviceCategory: API\n  - name: YouTube Live Streaming API\n    baseURL: https://www.googleapis.com/youtube/v3\n    tags:\n      - Broadcasting\n      - Live Streaming\n      - Videos\n    serviceName: YouTube Live Streaming API\n    serviceCategory: API\n\
  \  - name: YouTube IFrame Player API\n    baseURL: ''\n    tags:\n      - Embed\n      - Player\n      - Videos\n    serviceName: YouTube IFrame Player API\n    serviceCategory: API\n  - name: YouTube Subscribe Button\n    baseURL: ''\n    tags:\n      - Embed\n      - Videos\n      - Widgets\n    serviceName: YouTube Subscribe Button\n    serviceCategory: API\n  - name: Youtube Playlist Images API\n    baseURL: https://www.googleapis.com/youtube/v3\n    tags:\n      - Images\n      - Playlists\n      - Videos\n    serviceName: Youtube Playlist Images API\n    serviceCategory: API\n  - name: YouTube Content ID API\n    baseURL: https://www.googleapis.com/youtube/partner/v1\n    tags:\n      - Content ID\n      - Monetization\n      - Rights Management\n      - Videos\n    serviceName: YouTube Content ID API\n    serviceCategory: API\n  - name: YouTube oEmbed API\n    baseURL: https://www.youtube.com/oembed\n    tags:\n      - Embed\n      - oEmbed\n      - Videos\n    serviceName: YouTube\
  \ oEmbed API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    url: https://apievangelist.com\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/youtube/refs/heads/main/finops/youtube-finops.yml
sources: []
specification: FinOps Framework
tags:
- Google
- Media
- Social
- Streaming
- Video
- Videos
- FinOps
- Cost Management
- FOCUS
---
