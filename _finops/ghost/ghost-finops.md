---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: ghost-content-api-openapi.yml
  format: yaml
  label: Ghost Content API
  slug: content-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/ghost/refs/heads/main/openapi/ghost-content-api-openapi.yml
- filename: ghost-admin-api-openapi.yml
  format: yaml
  label: Ghost Admin API
  slug: admin-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/ghost/refs/heads/main/openapi/ghost-admin-api-openapi.yml
- filename: ghost-webhooks-asyncapi.yml
  format: yaml
  label: Ghost Webhooks
  slug: webhooks
  spec_type: AsyncAPI
  url: https://raw.githubusercontent.com/api-evangelist/ghost/refs/heads/main/asyncapi/ghost-webhooks-asyncapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Purchase
  - Usage
  - Adjustment
  - Credit
  pricingCategory: Tiered Subscription
description: 'FOCUS-aligned FinOps for Ghost(Pro): tiered SaaS subscription priced on staff seats, included members, and feature access; no per-API-call billing.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Ghost Foundation
  PricingCategory: Subscription
  PricingUnit: month
  ProviderName: Ghost
  PublisherName: Ghost Foundation
  ServiceCategory: Content Management
  ServiceName: Ghost(Pro)
layout: finops
meters:
- aggregation: sum
  description: Monthly Ghost(Pro) plan fee charged per blog/site
  dimensions:
  - plan
  - site_id
  name: subscription_fees
  unit: month
- aggregation: max
  description: Number of staff users included on the plan
  dimensions:
  - plan
  name: staff_seats
  unit: seat
- aggregation: max
  description: Number of paid/free members the plan supports
  dimensions:
  - plan
  name: members_included
  unit: member
- aggregation: max
  description: Number of newsletters configured under the plan
  name: newsletters
  unit: newsletter
- aggregation: sum
  description: Cumulative file uploads bound by the per-file size cap of the plan
  name: file_storage
  unit: GB
name: Ghost Finops
provider_name: Ghost
provider_slug: ghost
publisher_name: Ghost Foundation
service_category: Content Management / Publishing
slug: ghost-finops
source_filename: ghost-finops.yml
source_heading: FinOps Profile
source_url: https://ghost.org/pricing/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Ghost\nproviderId: ghost\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Content Management\n  - Publishing\n  - SaaS\ndescription: 'FOCUS-aligned FinOps for Ghost(Pro): tiered SaaS subscription priced on staff seats, included\n  members, and feature access; no per-API-call billing.'\nsources:\n  - https://ghost.org/pricing/\n  - https://ghost.org/docs/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Ghost Foundation\nserviceCategory: Content Management / Publishing\nbillingModel:\n  pricingCategory: Tiered Subscription\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\n   \
  \ - Adjustment\n    - Credit\nfocusColumns:\n  ServiceName: Ghost(Pro)\n  ServiceCategory: Content Management\n  ProviderName: Ghost\n  PublisherName: Ghost Foundation\n  InvoiceIssuerName: Ghost Foundation\n  BillingCurrency: USD\n  ChargeCategory: Purchase\n  PricingCategory: Subscription\n  PricingUnit: month\nmeters:\n  - name: subscription_fees\n    description: Monthly Ghost(Pro) plan fee charged per blog/site\n    unit: month\n    aggregation: sum\n    dimensions:\n      - plan\n      - site_id\n  - name: staff_seats\n    description: Number of staff users included on the plan\n    unit: seat\n    aggregation: max\n    dimensions:\n      - plan\n  - name: members_included\n    description: Number of paid/free members the plan supports\n    unit: member\n    aggregation: max\n    dimensions:\n      - plan\n  - name: newsletters\n    description: Number of newsletters configured under the plan\n    unit: newsletter\n    aggregation: max\n  - name: file_storage\n    description: Cumulative\
  \ file uploads bound by the per-file size cap of the plan\n    unit: GB\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Track Ghost(Pro) invoices via the billing email and admin Settings - Subscription pages;\n      surface seat counts and active member totals through the Admin API for finance reporting.\n  - name: Allocation\n    description: Tag site-level subscriptions to the owning content team; multi-property publishers should\n      attribute each Ghost(Pro) instance to its content unit.\n  - name: Optimization\n    description: Annual billing offers material discount over monthly; consolidate low-traffic sites onto\n      a single Creator/Team plan rather than maintaining multiple Starters; archive inactive members to\n      stay within tier caps.\n  - name: Accountability\n    description: Editorial leads own the Ghost(Pro) seat allocation and member-tier expansion decisions;\n      finance reviews annual renewal vs self-host trade-off.\nmaintainers:\n\
  \  - FN: API Evangelist\n    email: info@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/ghost/refs/heads/main/finops/ghost-finops.yml
sources:
- https://ghost.org/pricing/
- https://ghost.org/docs/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Content Management
- Publishing
- SaaS
---
