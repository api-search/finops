---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: tiktok-display-openapi.yml
  format: yaml
  label: TikTok Display API
  slug: tiktok-display-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/tiktok-for-developers/refs/heads/main/openapi/tiktok-display-openapi.yml
- filename: tiktok-content-posting-openapi.yml
  format: yaml
  label: TikTok Content Posting API
  slug: tiktok-content-posting-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/tiktok-for-developers/refs/heads/main/openapi/tiktok-content-posting-openapi.yml
- filename: tiktok-research-openapi.yml
  format: yaml
  label: TikTok Research API
  slug: tiktok-research-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/tiktok-for-developers/refs/heads/main/openapi/tiktok-research-openapi.yml
- filename: tiktok-login-kit-openapi.yml
  format: yaml
  label: TikTok Login Kit
  slug: tiktok-login-kit
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/tiktok-for-developers/refs/heads/main/openapi/tiktok-login-kit-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: N/A
  chargeCategories:
  - Usage
  pricingCategory: Free / Approval-Gated
description: 'FOCUS-aligned FinOps for the TikTok for Developers platform: free, approval-gated access with no per-call billing. FinOps focus is on quota burn against the published 600 rpm limits and approval-tier entitlements.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  ProviderName: TikTok
  PublisherName: TikTok Pte. Ltd.
  ServiceCategory: Social Platform APIs
  ServiceName: TikTok for Developers
layout: finops
meters:
- aggregation: sum
  dimensions:
  - client_key
  - endpoint
  name: user_info_requests
  unit: request
- aggregation: sum
  dimensions:
  - client_key
  - endpoint
  name: video_query_requests
  unit: request
- aggregation: sum
  dimensions:
  - client_key
  - endpoint
  name: video_list_requests
  unit: request
name: Tiktok For Developers Finops
provider_name: TikTok for Developers
provider_slug: tiktok-for-developers
publisher_name: TikTok Pte. Ltd.
service_category: Social Platform APIs
slug: tiktok-for-developers-finops
source_filename: tiktok-for-developers-finops.yml
source_heading: FinOps Profile
source_url: https://developers.tiktok.com/products
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: TikTok for Developers\nproviderId: tiktok-for-developers\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - Social\n  - Video\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps for the TikTok for Developers platform: free, approval-gated access\n  with no per-call billing. FinOps focus is on quota burn against the published 600 rpm limits and approval-tier\n  entitlements.'\nsources:\n  - https://developers.tiktok.com/products\n  - https://developers.tiktok.com/doc/tiktok-api-v2-rate-limit\n  - https://focus.finops.org/focus-specification/v1-3/\nnotes: TikTok does not bill developers per call; there is no usage-based invoice surface. FinOps observability\n  is internal telemetry against the documented 600 rpm sliding window per endpoint.\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n\
  \  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: TikTok Pte. Ltd.\nserviceCategory: Social Platform APIs\nbillingModel:\n  pricingCategory: Free / Approval-Gated\n  billingFrequency: N/A\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\nfocusColumns:\n  ServiceName: TikTok for Developers\n  ServiceCategory: Social Platform APIs\n  ProviderName: TikTok\n  PublisherName: TikTok Pte. Ltd.\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: user_info_requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - client_key\n      - endpoint\n  - name: video_query_requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - client_key\n      - endpoint\n  - name: video_list_requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - client_key\n      - endpoint\nprinciples:\n  - name: Visibility\n    description: Track per-client_key request volume\
  \ against the 600 rpm sliding window for the documented\n      v2 endpoints to anticipate 429 throttling.\n  - name: Allocation\n    description: Issue a distinct client key per app and environment so quota and approval-tier entitlements\n      can be attributed to the consuming product team.\n  - name: Optimization\n    description: Cache user_info responses, batch video queries, and avoid redundant list polls before\n      requesting a quota raise via TikTok Support.\n  - name: Accountability\n    description: Designate a developer-relations owner accountable for app review status, approval-tier\n      renewal, and Support tickets for limit increases.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/tiktok-for-developers/refs/heads/main/finops/tiktok-for-developers-finops.yml
sources:
- https://developers.tiktok.com/products
- https://developers.tiktok.com/doc/tiktok-api-v2-rate-limit
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Social
- Video
- FinOps
- FOCUS
---
