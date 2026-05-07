---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: tiktok-business-openapi.yml
  format: yaml
  label: TikTok API for Business
  slug: tiktok-business-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/tiktok/refs/heads/main/openapi/tiktok-business-openapi.yml
- filename: tiktok-shop-openapi.yml
  format: yaml
  label: TikTok Shop API
  slug: tiktok-shop-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/tiktok/refs/heads/main/openapi/tiktok-shop-openapi.yml
- filename: tiktok-data-portability-openapi.yml
  format: yaml
  label: TikTok Data Portability API
  slug: tiktok-data-portability-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/tiktok/refs/heads/main/openapi/tiktok-data-portability-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: N/A
  chargeCategories:
  - Usage
  pricingCategory: Free / Approval-Gated
description: 'FOCUS-aligned FinOps for the TikTok developer APIs: free, approval-gated access with no per-call billing. FinOps focus is on quota burn and approval-tier entitlements rather than cost.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  ProviderName: TikTok
  PublisherName: TikTok Pte. Ltd.
  ServiceCategory: Social Platform APIs
  ServiceName: TikTok Developer Platform
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
name: Tiktok Finops
provider_name: TikTok
provider_slug: tiktok
publisher_name: TikTok Pte. Ltd.
service_category: Social Platform APIs
slug: tiktok-finops
source_filename: tiktok-finops.yml
source_heading: FinOps Profile
source_url: https://developers.tiktok.com/products
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: TikTok\nproviderId: tiktok\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - Social\n  - Video\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps for the TikTok developer APIs: free, approval-gated access with no\n  per-call billing. FinOps focus is on quota burn and approval-tier entitlements rather than cost.'\nsources:\n  - https://developers.tiktok.com/products\n  - https://developers.tiktok.com/doc/tiktok-api-v2-rate-limit\n  - https://focus.finops.org/focus-specification/v1-3/\nnotes: TikTok does not bill developers per call. There is no usage-based invoice surface; FinOps observability\n  is limited to internal telemetry against the published 600 rpm per-endpoint limits.\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n\
  \  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: TikTok Pte. Ltd.\nserviceCategory: Social Platform APIs\nbillingModel:\n  pricingCategory: Free / Approval-Gated\n  billingFrequency: N/A\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\nfocusColumns:\n  ServiceName: TikTok Developer Platform\n  ServiceCategory: Social Platform APIs\n  ProviderName: TikTok\n  PublisherName: TikTok Pte. Ltd.\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: user_info_requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - client_key\n      - endpoint\n  - name: video_query_requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - client_key\n      - endpoint\n  - name: video_list_requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - client_key\n      - endpoint\nprinciples:\n  - name: Visibility\n    description: Track per-client_key request volume against the 600 rpm sliding window for\
  \ /v2/user/info,\n      /v2/video/query, and /v2/video/list to anticipate 429s.\n  - name: Allocation\n    description: Issue distinct client keys per app so quota burn and approval-tier entitlements (Research,\n      Commercial Content) can be attributed to the consuming product team.\n  - name: Optimization\n    description: Cache user_info responses, batch video queries, and avoid redundant list polls; request\n      a quota raise via TikTok Support before redesigning around the limit.\n  - name: Accountability\n    description: Designate a developer-relations owner accountable for the TikTok app review status,\n      approval-tier renewals, and Support tickets for limit increases.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/tiktok/refs/heads/main/finops/tiktok-finops.yml
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
