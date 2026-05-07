---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: x-api-openapi.json
  format: json
  label: X API
  slug: x-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/twitter/refs/heads/main/openapi/x-api-openapi.json
billing_model:
  billingCurrency: USD
  billingFrequency: On-Demand
  chargeCategories:
  - Purchase
  - Usage
  pricingCategory: Pay-As-You-Go
description: FOCUS-aligned FinOps for the X API v2 — credit-based pay-per-call with per-resource read pricing ($0.001 owned / $0.005 content / $0.010 identity), per-request write pricing ($0.015 standard, $0.200 with URL), 24-hour request deduplication, and configurable spending limits / auto-recharge in the Developer Console.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: X Corp.
  ProviderName: X (Twitter)
  PublisherName: X Corp.
  ServiceCategory: Social Media Developer API
  ServiceName: X API
layout: finops
meters:
- aggregation: sum
  description: Read of post / list / space / community / note / media / analytics resources at $0.005 each.
  dimensions:
  - resource_type
  - app
  name: read_resources_content
  unit: resource
- aggregation: sum
  description: Read of user / DM / following / followers / trends resources at $0.010 each.
  dimensions:
  - resource_type
  - app
  name: read_resources_identity
  unit: resource
- aggregation: sum
  description: Reads against your own data (own posts, bookmarks, followers) at $0.001 each.
  dimensions:
  - resource_type
  - app
  name: owned_reads
  unit: resource
- aggregation: sum
  description: Content-creation and basic write/interaction requests at $0.015 (interactions $0.005-$0.015).
  dimensions:
  - endpoint
  - app
  name: write_requests_standard
  unit: request
- aggregation: sum
  description: Content-creation requests that include a URL at $0.200 each.
  dimensions:
  - endpoint
  - app
  name: write_requests_with_url
  unit: request
- aggregation: sum
  description: Credits purchased upfront in the Developer Console; consumed by request meters.
  dimensions:
  - app
  name: credits_purchased
  unit: USD
name: Twitter Finops
provider_name: X (Twitter)
provider_slug: twitter
publisher_name: X Corp.
service_category: Social Media Developer API
slug: twitter-finops
source_filename: twitter-finops.yml
source_heading: FinOps Profile
source_url: https://docs.x.com/x-api/getting-started/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: X (Twitter)\nproviderId: twitter\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - Social Media\n  - Developer API\n  - Pay-Per-Use\n  - FinOps\n  - FOCUS\ndescription: FOCUS-aligned FinOps for the X API v2 — credit-based pay-per-call with per-resource read\n  pricing ($0.001 owned / $0.005 content / $0.010 identity), per-request write pricing ($0.015 standard,\n  $0.200 with URL), 24-hour request deduplication, and configurable spending limits / auto-recharge in\n  the Developer Console.\nsources:\n  - https://docs.x.com/x-api/getting-started/pricing\n  - https://docs.x.com/x-api/getting-started/about-x-api\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName:\
  \ X Corp.\nserviceCategory: Social Media Developer API\nbillingModel:\n  pricingCategory: Pay-As-You-Go\n  billingFrequency: On-Demand\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\nfocusColumns:\n  ServiceName: X API\n  ServiceCategory: Social Media Developer API\n  ProviderName: X (Twitter)\n  PublisherName: X Corp.\n  InvoiceIssuerName: X Corp.\n  BillingCurrency: USD\nmeters:\n  - name: read_resources_content\n    description: Read of post / list / space / community / note / media / analytics resources at $0.005\n      each.\n    unit: resource\n    aggregation: sum\n    dimensions:\n      - resource_type\n      - app\n  - name: read_resources_identity\n    description: Read of user / DM / following / followers / trends resources at $0.010 each.\n    unit: resource\n    aggregation: sum\n    dimensions:\n      - resource_type\n      - app\n  - name: owned_reads\n    description: Reads against your own data (own posts, bookmarks, followers) at $0.001 each.\n\
  \    unit: resource\n    aggregation: sum\n    dimensions:\n      - resource_type\n      - app\n  - name: write_requests_standard\n    description: Content-creation and basic write/interaction requests at $0.015 (interactions $0.005-$0.015).\n    unit: request\n    aggregation: sum\n    dimensions:\n      - endpoint\n      - app\n  - name: write_requests_with_url\n    description: Content-creation requests that include a URL at $0.200 each.\n    unit: request\n    aggregation: sum\n    dimensions:\n      - endpoint\n      - app\n  - name: credits_purchased\n    description: Credits purchased upfront in the Developer Console; consumed by request meters.\n    unit: USD\n    aggregation: sum\n    dimensions:\n      - app\nprinciples:\n  - name: Visibility\n    description: Use the X Developer Console real-time tracking to monitor credit balance, per-endpoint\n      cost, and request counts; rate-limit headers (x-rate-limit-remaining / reset) provide an additional\n      governance signal.\n\
  \  - name: Allocation\n    description: Allocate spend per Developer Console app (client) — each app has its own credit balance,\n      spending limit, and auto-recharge. Map apps to product features so credit consumption charges back\n      cleanly.\n  - name: Optimization\n    description: Lever the 24-hour request-deduplication window (do not re-fetch the same resource within\n      24 hours), prefer owned reads ($0.001) over content/identity reads where applicable, avoid posting\n      with URLs ($0.200) when a plain post ($0.015) suffices, and use streaming endpoints for real-time\n      data instead of poll-driven reads.\n  - name: Accountability\n    description: Each app's credit balance has an owner who configures the spending limit and auto-recharge\n      threshold; finance reviews credit-purchase invoices and the per-app monthly burn rate.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/twitter/refs/heads/main/finops/twitter-finops.yml
sources:
- https://docs.x.com/x-api/getting-started/pricing
- https://docs.x.com/x-api/getting-started/about-x-api
specification: FinOps Framework
tags:
- Social Media
- Developer API
- Pay-Per-Use
- FinOps
- FOCUS
---
