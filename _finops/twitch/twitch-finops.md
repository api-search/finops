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
  billingFrequency: On-Demand
  chargeCategories:
  - Usage
  pricingCategory: Free
description: FOCUS-aligned FinOps for the Twitch developer surface — the Helix and Extensions APIs are free of charge under Twitch's developer terms, so the FinOps surface is governance-focused (rate-limit budgets and bucket consumption) rather than dollar-cost. There is no metered invoice line; cost lives in the indirect engineering and infrastructure cost of operating against Twitch's APIs.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Twitch Interactive, Inc.
  ProviderName: Twitch
  PublisherName: Twitch Interactive, Inc.
  ServiceCategory: Streaming Developer API
  ServiceName: Twitch Helix API
layout: finops
meters:
- aggregation: sum
  description: Helix API requests issued by your registered application; consumes points from the relevant bucket.
  dimensions:
  - client_id
  - token_type
  - endpoint
  name: helix_requests
  unit: request
- aggregation: sum
  description: Points deducted from the token bucket; the practical FinOps unit since Twitch does not charge in dollars.
  dimensions:
  - client_id
  - token_type
  name: bucket_points
  unit: point
- aggregation: max
  description: Active EventSub webhook subscriptions on the application.
  dimensions:
  - client_id
  name: eventsub_subscriptions
  unit: subscription
name: Twitch Finops
provider_name: Twitch
provider_slug: twitch
publisher_name: Twitch Interactive, Inc.
service_category: Streaming Developer API
slug: twitch-finops
source_filename: twitch-finops.yml
source_heading: FinOps Profile
source_url: https://dev.twitch.tv/docs/api/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Twitch\nproviderId: twitch\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - Streaming\n  - Developer API\n  - Free\n  - FinOps\n  - FOCUS\ndescription: FOCUS-aligned FinOps for the Twitch developer surface — the Helix and Extensions APIs are\n  free of charge under Twitch's developer terms, so the FinOps surface is governance-focused (rate-limit\n  budgets and bucket consumption) rather than dollar-cost. There is no metered invoice line; cost lives\n  in the indirect engineering and infrastructure cost of operating against Twitch's APIs.\nsources:\n  - https://dev.twitch.tv/docs/api/\n  - https://dev.twitch.tv/docs/api/guide/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\n\
  publisherName: Twitch Interactive, Inc.\nserviceCategory: Streaming Developer API\nbillingModel:\n  pricingCategory: Free\n  billingFrequency: On-Demand\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\nfocusColumns:\n  ServiceName: Twitch Helix API\n  ServiceCategory: Streaming Developer API\n  ProviderName: Twitch\n  PublisherName: Twitch Interactive, Inc.\n  InvoiceIssuerName: Twitch Interactive, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: helix_requests\n    description: Helix API requests issued by your registered application; consumes points from the relevant\n      bucket.\n    unit: request\n    aggregation: sum\n    dimensions:\n      - client_id\n      - token_type\n      - endpoint\n  - name: bucket_points\n    description: Points deducted from the token bucket; the practical FinOps unit since Twitch does not\n      charge in dollars.\n    unit: point\n    aggregation: sum\n    dimensions:\n      - client_id\n      - token_type\n  - name: eventsub_subscriptions\n\
  \    description: Active EventSub webhook subscriptions on the application.\n    unit: subscription\n    aggregation: max\n    dimensions:\n      - client_id\nprinciples:\n  - name: Visibility\n    description: Use the Ratelimit-Limit / Remaining / Reset response headers and per-application logging\n      to track point consumption across app and user buckets in real time.\n  - name: Allocation\n    description: Allocate \"cost\" to the consuming feature by tagging requests with the originating internal\n      service or feature flag; bucket headroom is the budget being allocated.\n  - name: Optimization\n    description: Cache responses, prefer EventSub webhooks over polling, batch lookups (e.g. bulk Get\n      Users), and use app tokens for non-user-scoped reads to avoid per-user bucket pressure.\n  - name: Accountability\n    description: Assign a developer owner per Twitch application (client ID); they are responsible for\n      respecting the bucket, handling 429s with backoff, and\
  \ migrating away from deprecated endpoints.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/twitch/refs/heads/main/finops/twitch-finops.yml
sources:
- https://dev.twitch.tv/docs/api/
- https://dev.twitch.tv/docs/api/guide/
specification: FinOps Framework
tags:
- Streaming
- Developer API
- Free
- FinOps
- FOCUS
---
