---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: stream-io-chat-openapi.yml
  format: yaml
  label: Stream Chat API
  slug: chat
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/stream-io/refs/heads/main/openapi/stream-io-chat-openapi.yml
- filename: stream-io-video-openapi.yml
  format: yaml
  label: Stream Video & Audio API
  slug: video
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/stream-io/refs/heads/main/openapi/stream-io-video-openapi.yml
- filename: stream-io-moderation-openapi.yml
  format: yaml
  label: Stream Moderation API
  slug: moderation
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/stream-io/refs/heads/main/openapi/stream-io-moderation-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  - Adjustment
  pricingCategory: Subscription + Usage
description: FOCUS-aligned FinOps profile for Stream. Stream charges a tiered subscription per Monthly Active Users (MAU) per product (Chat, Video, Feeds, Moderation), plus add-on usage meters for stored messages, API call overage, and CDN bandwidth/storage. Billed monthly in USD; annual contracts discounted.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Stream
  PricingUnit: MAU
  ProviderName: Stream
  PublisherName: Stream
  ServiceCategory: Realtime Communications
  ServiceName: Stream Chat
layout: finops
meters:
- aggregation: distinct_count
  description: Unique users that opened a session in the billing month (primary meter).
  dimensions:
  - app_id
  - product
  name: monthly_active_users
  unit: user
- aggregation: sum
  description: Total messages persisted in Stream Chat.
  dimensions:
  - app_id
  name: stored_messages
  unit: message
- aggregation: sum
  description: Server-side API calls metered above plan-included quota.
  dimensions:
  - app_id
  - endpoint
  name: api_calls
  unit: request
- aggregation: sum
  description: Bandwidth served from Stream's CDN for attachments and media.
  dimensions:
  - app_id
  name: cdn_bandwidth
  unit: GB
- aggregation: avg
  description: Storage of attachments on Stream's CDN.
  dimensions:
  - app_id
  name: cdn_storage
  unit: GB-month
- aggregation: sum
  description: Per-participant video/audio minutes for Stream Video.
  dimensions:
  - app_id
  - call_id
  name: video_minutes
  unit: minute
name: Stream Io Finops
provider_name: Stream
provider_slug: stream-io
publisher_name: Stream
service_category: Realtime Communications
slug: stream-io-finops
source_filename: stream-io-finops.yml
source_heading: FinOps Profile
source_url: https://getstream.io/pricing/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Stream\nproviderId: stream-io\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: true\ntags:\n- Realtime\n- Chat\n- Video\n- Activity Feeds\n- Moderation\n- SDK\n- FinOps\n- Cost Management\n- FOCUS\ndescription: >-\n  FOCUS-aligned FinOps profile for Stream. Stream charges a tiered subscription\n  per Monthly Active Users (MAU) per product (Chat, Video, Feeds, Moderation),\n  plus add-on usage meters for stored messages, API call overage, and CDN\n  bandwidth/storage. Billed monthly in USD; annual contracts discounted.\nnotes: >-\n  Pricing is denominated per-MAU per-product, so cost allocation works best by\n  tracking unique user IDs through Stream's app/key partitioning. Stored\n  messages and CDN bytes are separately metered and visible on the invoice.\nsources:\n- https://getstream.io/pricing/\n- https://getstream.io/chat/pricing/\n- https://focus.finops.org/focus-specification/v1-3/\n\
  alignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Stream\nserviceCategory: Realtime Communications\nbillingModel:\n  pricingCategory: Subscription + Usage\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n  - Usage\n  - Purchase\n  - Adjustment\nfocusColumns:\n  ServiceName: Stream Chat\n  ServiceCategory: Realtime Communications\n  ProviderName: Stream\n  PublisherName: Stream\n  InvoiceIssuerName: Stream\n  BillingCurrency: USD\n  ChargeCategory: Usage\n  PricingUnit: MAU\nmeters:\n- name: monthly_active_users\n  description: Unique users that opened a session in the billing month (primary meter).\n  unit: user\n  aggregation: distinct_count\n  dimensions:\n  - app_id\n  - product\n- name: stored_messages\n  description: Total messages persisted in Stream Chat.\n  unit: message\n\
  \  aggregation: sum\n  dimensions:\n  - app_id\n- name: api_calls\n  description: Server-side API calls metered above plan-included quota.\n  unit: request\n  aggregation: sum\n  dimensions:\n  - app_id\n  - endpoint\n- name: cdn_bandwidth\n  description: Bandwidth served from Stream's CDN for attachments and media.\n  unit: GB\n  aggregation: sum\n  dimensions:\n  - app_id\n- name: cdn_storage\n  description: Storage of attachments on Stream's CDN.\n  unit: GB-month\n  aggregation: avg\n  dimensions:\n  - app_id\n- name: video_minutes\n  description: Per-participant video/audio minutes for Stream Video.\n  unit: minute\n  aggregation: sum\n  dimensions:\n  - app_id\n  - call_id\nprinciples:\n- name: Visibility\n  description: Inspect Stream Dashboard usage tab and the monthly invoice to track MAU and usage meters.\n- name: Allocation\n  description: Use distinct app keys per product/team and embed cost-center IDs into user metadata for downstream allocation.\n- name: Optimization\n  description:\
  \ Right-size MAU tier annually; archive cold messages, prune stale users, offload large attachments to your own CDN where economical.\n- name: Accountability\n  description: Assign per-app owners; review MAU vs. tier ceiling monthly to avoid overage.\nmaintainers:\n- FN: Kin Lane\n  email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/stream-io/refs/heads/main/finops/stream-io-finops.yml
sources:
- https://getstream.io/pricing/
- https://getstream.io/chat/pricing/
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Realtime
- Chat
- Video
- Activity Feeds
- Moderation
- SDK
- FinOps
- Cost Management
- FOCUS
---
