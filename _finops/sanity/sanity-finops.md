---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: sanity-openapi.yml
  format: yaml
  label: Sanity Query API
  slug: sanity-query-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/sanity/refs/heads/main/openapi/sanity-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  - Tax
  - Adjustment
  - Refund
  - Credit
  pricingCategory: Tiered Subscription + Usage Overage
description: FOCUS-aligned FinOps for Sanity. Tiered SaaS subscription (per-seat) with included monthly quotas and metered overages on CDN requests, direct API requests, asset storage, and bandwidth.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Sanity.io
  PricingUnit: seat-month, request, GB
  ProviderName: Sanity
  PublisherName: Sanity.io
  ServiceCategory: Developer Tools
  ServiceName: Sanity
  ServiceSubcategory: Headless CMS
layout: finops
meters:
- aggregation: sum
  description: Per-seat monthly subscription on Growth ($15/seat/month, up to 50 seats).
  dimensions:
  - plan
  - role
  name: seat_subscription
  unit: seat-month
- aggregation: sum
  description: API CDN request count; first 1M/month included on Free and Growth, then $1 per 250K on Growth.
  dimensions:
  - dataset
  - plan
  name: api_cdn_requests
  unit: request
- aggregation: sum
  description: Direct (non-CDN) API request count; first 250K/month included on Free and Growth, then $1 per 25K on Growth.
  dimensions:
  - dataset
  - api
  - plan
  name: api_requests
  unit: request
- aggregation: max
  description: Asset storage in GB; first 100 GB included on Free and Growth, then $0.50/GB on Growth.
  dimensions:
  - dataset
  - plan
  name: asset_storage
  unit: GB-month
- aggregation: sum
  description: Outbound bandwidth in GB; first 100 GB/month included on Free and Growth, then $0.30/GB on Growth.
  dimensions:
  - dataset
  - plan
  name: bandwidth
  unit: GB
- aggregation: max
  description: Document count cap by plan (10K Free / 25K Growth).
  dimensions:
  - dataset
  - plan
  name: documents
  unit: document
- aggregation: sum
  description: Flat-rate Growth add-ons (SAML SSO $1,399/mo, Dedicated Support $799/mo, Increased Quota $299/mo, Extra Dataset $999/dataset).
  dimensions:
  - addon
  name: addons
  unit: month
name: Sanity Finops
provider_name: Sanity
provider_slug: sanity
publisher_name: Sanity.io
service_category: Developer Tools / Headless CMS
slug: sanity-finops
source_filename: sanity-finops.yml
source_heading: FinOps Profile
source_url: https://www.sanity.io/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Sanity\nproviderId: sanity\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Headless CMS\n  - Content Management\n  - Developer Platform\ndescription: FOCUS-aligned FinOps for Sanity. Tiered SaaS subscription (per-seat) with included monthly\n  quotas and metered overages on CDN requests, direct API requests, asset storage, and bandwidth.\nsources:\n  - https://www.sanity.io/pricing\n  - https://www.sanity.io/docs/api-cdn\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Sanity.io\nserviceCategory: Developer Tools / Headless CMS\nbillingModel:\n  pricingCategory: Tiered Subscription + Usage Overage\n  billingFrequency: Monthly\n\
  \  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Adjustment\n    - Refund\n    - Credit\nfocusColumns:\n  ServiceName: Sanity\n  ServiceCategory: Developer Tools\n  ServiceSubcategory: Headless CMS\n  ProviderName: Sanity\n  PublisherName: Sanity.io\n  InvoiceIssuerName: Sanity.io\n  BillingCurrency: USD\n  ChargeCategory: Usage\n  PricingUnit: seat-month, request, GB\nmeters:\n  - name: seat_subscription\n    description: Per-seat monthly subscription on Growth ($15/seat/month, up to 50 seats).\n    unit: seat-month\n    aggregation: sum\n    dimensions:\n      - plan\n      - role\n  - name: api_cdn_requests\n    description: API CDN request count; first 1M/month included on Free and Growth, then $1 per 250K\n      on Growth.\n    unit: request\n    aggregation: sum\n    dimensions:\n      - dataset\n      - plan\n  - name: api_requests\n    description: Direct (non-CDN) API request count; first 250K/month included on Free and Growth, then\n\
  \      $1 per 25K on Growth.\n    unit: request\n    aggregation: sum\n    dimensions:\n      - dataset\n      - api\n      - plan\n  - name: asset_storage\n    description: Asset storage in GB; first 100 GB included on Free and Growth, then $0.50/GB on Growth.\n    unit: GB-month\n    aggregation: max\n    dimensions:\n      - dataset\n      - plan\n  - name: bandwidth\n    description: Outbound bandwidth in GB; first 100 GB/month included on Free and Growth, then $0.30/GB\n      on Growth.\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - dataset\n      - plan\n  - name: documents\n    description: Document count cap by plan (10K Free / 25K Growth).\n    unit: document\n    aggregation: max\n    dimensions:\n      - dataset\n      - plan\n  - name: addons\n    description: Flat-rate Growth add-ons (SAML SSO $1,399/mo, Dedicated Support $799/mo, Increased Quota\n      $299/mo, Extra Dataset $999/dataset).\n    unit: month\n    aggregation: sum\n    dimensions:\n      - addon\n\
  principles:\n  - name: Visibility\n    description: Use the Sanity project usage dashboard to see CDN requests, direct API requests, asset\n      storage, and bandwidth against included quotas; the same numbers determine overage charges on Growth.\n  - name: Allocation\n    description: Allocate cost by dataset (each Growth project includes 2 datasets, additional datasets\n      are $999/each) and by seat (each Growth seat is $15/month). Use dataset naming conventions to map\n      to teams or environments.\n  - name: Optimization\n    description: \"Drive reads through the API CDN (`useCdn: true`) — cached responses are not rate limited and don't consume the direct-API quota. Right-size seat counts (Growth caps at 50 seats; move to Enterprise when sustained) and consolidate small datasets to avoid the per-dataset add-on.\"\n  - name: Accountability\n    description: A single billing owner per project receives Sanity invoices; map overage line items\n      (CDN requests, API requests,\
  \ assets, bandwidth) back to the responsible team via dataset tags before\n      chargeback.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/sanity/refs/heads/main/finops/sanity-finops.yml
sources:
- https://www.sanity.io/pricing
- https://www.sanity.io/docs/api-cdn
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Headless CMS
- Content Management
- Developer Platform
---
