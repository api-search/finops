---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: sync-labs-openapi.yml
  format: yaml
  label: Sync Labs API
  slug: sync-labs-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/sync-labs/refs/heads/main/openapi/sync-labs-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  pricingCategory: Subscription + Pay-As-You-Go
description: FOCUS-aligned FinOps for Sync Labs - hybrid Subscription + Pay-As-You-Go billed per video-generation second, with tier-gated usage discounts (5%-20%) and Batch API access on Scale and Enterprise.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Sync Labs, Inc.
  ProviderName: Sync Labs
  PublisherName: Sync Labs, Inc.
  ServiceCategory: AI Infrastructure / Media Generation
  ServiceName: Sync Labs API
layout: finops
meters:
- aggregation: sum
  description: Monthly flat subscription per plan (Hobbyist $5, Creator $19, Growth $49, Scale $249, Enterprise custom).
  dimensions:
  - plan
  name: subscription_fee
  unit: month
- aggregation: sum
  description: Seconds of generated lip-sync video; metered on completed generations at the plan's per-second rate ($0.05, $0.05, $0.0475, $0.04, custom).
  dimensions:
  - plan
  - model
  - api_key
  name: generation_seconds
  unit: second
- aggregation: max
  description: Voice clone slots used; capped per plan (3 / 5 / 15 / 50 / custom).
  dimensions:
  - plan
  name: voice_clones
  unit: clones
- aggregation: max
  description: Team seats consumed against per-plan caps (Growth 3, Scale 5, Enterprise custom).
  dimensions:
  - plan
  name: team_seats
  unit: seat
name: Sync Labs Finops
provider_name: Sync Labs
provider_slug: sync-labs
publisher_name: Sync Labs, Inc.
service_category: AI Infrastructure / Media Generation
slug: sync-labs-finops
source_filename: sync-labs-finops.yml
source_heading: FinOps Profile
source_url: https://sync.so/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Sync Labs\nproviderId: sync-labs\npublisherName: Sync Labs, Inc.\nserviceCategory: AI Infrastructure / Media Generation\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - AI Infrastructure\n  - Lip Sync\n  - Video\n  - FinOps\n  - FOCUS\ndescription: FOCUS-aligned FinOps for Sync Labs - hybrid Subscription + Pay-As-You-Go billed per video-generation second, with tier-gated usage discounts (5%-20%) and Batch API access on Scale and Enterprise.\nsources:\n  - https://sync.so/pricing\n  - https://sync.so/docs/api-reference/guides/rate-limits\nbillingModel:\n  pricingCategory: Subscription + Pay-As-You-Go\n  billingFrequency:\
  \ Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\nfocusColumns:\n  ServiceName: Sync Labs API\n  ServiceCategory: AI Infrastructure / Media Generation\n  ProviderName: Sync Labs\n  PublisherName: Sync Labs, Inc.\n  InvoiceIssuerName: Sync Labs, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: subscription_fee\n    description: Monthly flat subscription per plan (Hobbyist $5, Creator $19, Growth $49, Scale $249, Enterprise custom).\n    unit: month\n    aggregation: sum\n    dimensions:\n      - plan\n  - name: generation_seconds\n    description: Seconds of generated lip-sync video; metered on completed generations at the plan's per-second rate ($0.05, $0.05, $0.0475, $0.04, custom).\n    unit: second\n    aggregation: sum\n    dimensions:\n      - plan\n      - model\n      - api_key\n  - name: voice_clones\n    description: Voice clone slots used; capped per plan (3 / 5 / 15 / 50 / custom).\n    unit: clones\n    aggregation: max\n    dimensions:\n\
  \      - plan\n  - name: team_seats\n    description: Team seats consumed against per-plan caps (Growth 3, Scale 5, Enterprise custom).\n    unit: seat\n    aggregation: max\n    dimensions:\n      - plan\nprinciples:\n  - name: Visibility\n    description: The Sync dashboard shows generation history; clients can use the List Generations endpoint and webhooks to track per-key usage in near real-time and reconcile against the per-second rate at their plan tier.\n  - name: Allocation\n    description: Tag spend by API key and (optionally) team seat to attribute generation cost to the consuming product, customer, or workflow. Batch API jobs carry batch identifiers for cleaner allocation.\n  - name: Optimization\n    description: Move heavy workloads to Growth/Scale to capture the 5%-20% per-second usage discount; use the Batch API on Scale/Enterprise to amortize concurrency caps; cap max video length at the source to avoid paying for trimmed seconds.\n  - name: Accountability\n    description:\
  \ Plan owner controls the subscription tier and seat caps; per-key generation rates make it straightforward to assign per-team or per-product chargeback against the plan's per-second rate.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/sync-labs/refs/heads/main/finops/sync-labs-finops.yml
sources:
- https://sync.so/pricing
- https://sync.so/docs/api-reference/guides/rate-limits
specification: FinOps Framework
tags:
- AI Infrastructure
- Lip Sync
- Video
- FinOps
- FOCUS
---
