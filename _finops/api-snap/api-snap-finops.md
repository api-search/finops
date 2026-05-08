---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: api-snap-openapi.yml
  format: yaml
  label: QR Code API
  slug: qr
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/api-snap/refs/heads/main/openapi/api-snap-openapi.yml
- filename: api-snap-openapi.yml
  format: yaml
  label: Screenshot API
  slug: screenshot
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/api-snap/refs/heads/main/openapi/api-snap-openapi.yml
- filename: api-snap-openapi.yml
  format: yaml
  label: Image Resize API
  slug: resize
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/api-snap/refs/heads/main/openapi/api-snap-openapi.yml
- filename: api-snap-openapi.yml
  format: yaml
  label: PDF API
  slug: pdf
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/api-snap/refs/heads/main/openapi/api-snap-openapi.yml
- filename: api-snap-openapi.yml
  format: yaml
  label: Markdown API
  slug: markdown
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/api-snap/refs/heads/main/openapi/api-snap-openapi.yml
- filename: api-snap-openapi.yml
  format: yaml
  label: URL Metadata API
  slug: meta
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/api-snap/refs/heads/main/openapi/api-snap-openapi.yml
- filename: api-snap-openapi.yml
  format: yaml
  label: Hash API
  slug: hash
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/api-snap/refs/heads/main/openapi/api-snap-openapi.yml
- filename: api-snap-openapi.yml
  format: yaml
  label: JWT Decode API
  slug: jwt-decode
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/api-snap/refs/heads/main/openapi/api-snap-openapi.yml
- filename: api-snap-openapi.yml
  format: yaml
  label: Base64 API
  slug: base64
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/api-snap/refs/heads/main/openapi/api-snap-openapi.yml
- filename: api-snap-openapi.yml
  format: yaml
  label: UUID API
  slug: uuid
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/api-snap/refs/heads/main/openapi/api-snap-openapi.yml
- filename: api-snap-openapi.yml
  format: yaml
  label: Color API
  slug: color
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/api-snap/refs/heads/main/openapi/api-snap-openapi.yml
- filename: api-snap-openapi.yml
  format: yaml
  label: Lorem Ipsum API
  slug: lorem
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/api-snap/refs/heads/main/openapi/api-snap-openapi.yml
- filename: api-snap-openapi.yml
  format: yaml
  label: Placeholder Image API
  slug: placeholder
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/api-snap/refs/heads/main/openapi/api-snap-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Purchase
  - Usage
  - Adjustment
  - Refund
  - Credit
  pricingCategory: Tiered Subscription
description: FOCUS-aligned FinOps for API Snap - flat tiered subscription (Free / Hobby / Pro / Business) with a single monthly request quota that covers all 13+ utility endpoints under one API key. No per-endpoint billing or per-call overage charges are published; consumption telemetry surfaces via the X-RateLimit-* response headers and the in-product API usage dashboard offered on Hobby and above. reconciled is false because the public-facing FinOps surface (overage handling, invoice line items) is not documented separately from the pricing page.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: API Snap
  PricingCategory: Tiered Subscription
  PricingUnit: month
  ProviderName: API Snap
  PublisherName: API Snap
  ServiceCategory: Developer Utilities
  ServiceName: API Snap
layout: finops
meters:
- aggregation: count
  description: Monthly subscription line for the active plan tier (Hobby / Pro / Business). Free tier has no plan_month line.
  dimensions:
  - plan
  name: plan_month
  unit: month
- aggregation: max
  description: Plan-tier monthly request quota (100 / 5,000 / 50,000 / 500,000) covering all 13+ endpoints under one API key.
  dimensions:
  - plan
  - api_key
  name: monthly_request_quota
  unit: request
- aggregation: sum
  description: Actual request count made against the API key, drawn from the monthly quota. Surfaced via X-RateLimit-Limit and X-RateLimit-Remaining response headers and the in-product API usage dashboard.
  dimensions:
  - api_key
  - endpoint
  - status_code
  name: requests_consumed
  unit: request
- aggregation: sum
  description: Count of HTTP 429 responses returned to the client; signals that the monthly quota or plan rate ceiling is being hit. Each 429 body includes usage, limit, and an upgrade_url.
  dimensions:
  - api_key
  - endpoint
  name: rate_throttle_events
  unit: event
name: Api Snap Finops
provider_name: API Snap
provider_slug: api-snap
publisher_name: API Snap
service_category: Developer Utilities
slug: api-snap-finops
source_filename: api-snap-finops.yml
source_heading: FinOps Profile
source_url: https://api-snap.com/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: API Snap\nproviderId: api-snap\ncreated: '2026-05-06'\nmodified: '2026-05-06'\nreconciled: false\ntags:\n  - Developer Utilities\n  - API Subscription\n  - FinOps\n  - FOCUS\ndescription: >-\n  FOCUS-aligned FinOps for API Snap - flat tiered subscription (Free / Hobby /\n  Pro / Business) with a single monthly request quota that covers all 13+\n  utility endpoints under one API key. No per-endpoint billing or per-call\n  overage charges are published; consumption telemetry surfaces via the\n  X-RateLimit-* response headers and the in-product API usage dashboard offered\n  on Hobby and above. reconciled is false because the public-facing FinOps\n  surface (overage handling, invoice line items) is not documented separately\n  from the pricing page.\nsources:\n  - https://api-snap.com/pricing\n  - https://api-snap.com/\n  - https://focus.finops.org/focus-specification/v1-3/\n\
  alignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: API Snap\nserviceCategory: Developer Utilities\nbillingModel:\n  pricingCategory: Tiered Subscription\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\n    - Adjustment\n    - Refund\n    - Credit\nfocusColumns:\n  ServiceName: API Snap\n  ServiceCategory: Developer Utilities\n  ProviderName: API Snap\n  PublisherName: API Snap\n  InvoiceIssuerName: API Snap\n  BillingCurrency: USD\n  ChargeCategory: Purchase\n  PricingCategory: Tiered Subscription\n  PricingUnit: month\nmeters:\n  - name: plan_month\n    description: Monthly subscription line for the active plan tier (Hobby / Pro / Business). Free tier has no plan_month line.\n    unit: month\n    aggregation: count\n    dimensions:\n      - plan\n  -\
  \ name: monthly_request_quota\n    description: Plan-tier monthly request quota (100 / 5,000 / 50,000 / 500,000) covering all 13+ endpoints under one API key.\n    unit: request\n    aggregation: max\n    dimensions:\n      - plan\n      - api_key\n  - name: requests_consumed\n    description: Actual request count made against the API key, drawn from the monthly quota. Surfaced via X-RateLimit-Limit and X-RateLimit-Remaining response headers and the in-product API usage dashboard.\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api_key\n      - endpoint\n      - status_code\n  - name: rate_throttle_events\n    description: Count of HTTP 429 responses returned to the client; signals that the monthly quota or plan rate ceiling is being hit. Each 429 body includes usage, limit, and an upgrade_url.\n    unit: event\n    aggregation: sum\n    dimensions:\n      - api_key\n      - endpoint\nprinciples:\n  - name: Visibility\n    description: >-\n      Read X-RateLimit-Limit\
  \ and X-RateLimit-Remaining headers on every\n      response; on Hobby and above, watch the in-product API usage dashboard\n      to track consumption against the monthly quota. The 429 body returns\n      `usage`, `limit`, and an `upgrade_url` for in-product upgrade prompts.\n  - name: Allocation\n    description: >-\n      API Snap issues a single key per account; for multi-product attribution\n      tag outbound requests with a per-service correlation header on the\n      caller side and aggregate by `endpoint` dimension in the meter.\n  - name: Optimization\n    description: >-\n      Cache image, screenshot, PDF, and metadata responses aggressively at\n      the consumer side - many of these endpoints produce deterministic or\n      slowly-changing outputs. Right-size the plan tier monthly: 100 free\n      calls, 5,000 hobby, 50,000 pro, 500,000 business. Negotiate custom\n      rate limits at the Business tier when burst patterns require them.\n  - name: Accountability\n    description:\
  \ >-\n      Engineering owns the API key and caching layer; the consuming product\n      team owns the monthly request budget. The owner of the API Snap\n      account holds the upgrade decision when the in-product upgrade_url\n      surfaces in 429 responses.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/api-snap/refs/heads/main/finops/api-snap-finops.yml
sources:
- https://api-snap.com/pricing
- https://api-snap.com/
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Developer Utilities
- API Subscription
- FinOps
- FOCUS
---
