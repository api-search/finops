---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: ludo-ai-rest-api-openapi.yml
  format: yaml
  label: Ludo.ai REST API
  slug: rest-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/ludo-ai/refs/heads/main/openapi/ludo-ai-rest-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Usage
  - Purchase
  - Tax
  - Credit
  - Refund
  pricingCategory: Subscription + Prepaid Credits
description: 'FOCUS-aligned FinOps for Ludo.ai: tiered annual subscription with upfront credit allotments consumed by asset generation; annual billing carries a 30-35% discount; API/MCP usage is gated by per-tier concurrency.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Ludo.ai
  ProviderName: Ludo.ai
  PublisherName: Ludo.ai
  ServiceCategory: AI Infrastructure
  ServiceName: Ludo.ai
layout: finops
meters:
- aggregation: sum
  dimensions:
  - tier
  name: subscription_fee
  unit: year
- aggregation: sum
  dimensions:
  - asset_type
  - api
  name: credits_consumed
  unit: credit
- aggregation: sum
  dimensions:
  - asset_type
  name: assets_generated
  unit: asset
- aggregation: max
  dimensions:
  - tier
  name: seats
  unit: seat
- aggregation: sum
  name: top_up_credits
  unit: credit
name: Ludo Ai Finops
provider_name: Ludo.ai
provider_slug: ludo-ai
publisher_name: Ludo.ai
service_category: AI Infrastructure
slug: ludo-ai-finops
source_filename: ludo-ai-finops.yml
source_heading: FinOps Profile
source_url: https://ludo.ai/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Ludo.ai\nproviderId: ludo-ai\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Generative AI\n  - Game Development\ndescription: 'FOCUS-aligned FinOps for Ludo.ai: tiered annual subscription with upfront credit allotments\n  consumed by asset generation; annual billing carries a 30-35% discount; API/MCP usage is gated by\n  per-tier concurrency.'\nsources:\n  - https://ludo.ai/pricing\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Ludo.ai\nserviceCategory: AI Infrastructure\nbillingModel:\n  pricingCategory: Subscription + Prepaid Credits\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n  \
  \  - Purchase\n    - Tax\n    - Credit\n    - Refund\nfocusColumns:\n  ServiceName: Ludo.ai\n  ServiceCategory: AI Infrastructure\n  ProviderName: Ludo.ai\n  PublisherName: Ludo.ai\n  InvoiceIssuerName: Ludo.ai\n  BillingCurrency: USD\nmeters:\n  - name: subscription_fee\n    unit: year\n    aggregation: sum\n    dimensions:\n      - tier\n  - name: credits_consumed\n    unit: credit\n    aggregation: sum\n    dimensions:\n      - asset_type\n      - api\n  - name: assets_generated\n    unit: asset\n    aggregation: sum\n    dimensions:\n      - asset_type\n  - name: seats\n    unit: seat\n    aggregation: max\n    dimensions:\n      - tier\n  - name: top_up_credits\n    unit: credit\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Track annual credit burn against the per-tier allotment in the Ludo.ai dashboard;\n      monitor concurrent-request saturation on Pro/Studio.\n  - name: Allocation\n    description: Tag generated assets by project; map projects to internal\
  \ product/team for chargeback.\n  - name: Optimization\n    description: Prefer annual billing for the 30-35% saving; right-size between Indie / Pro / Studio\n      based on annual credit need; use Top Up rather than upgrading mid-cycle.\n  - name: Accountability\n    description: Owners review credit burn quarterly; trigger Studio upgrade before Pro credits exhaust;\n      track refund-window thresholds at renewal.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/ludo-ai/refs/heads/main/finops/ludo-ai-finops.yml
sources:
- https://ludo.ai/pricing
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Generative AI
- Game Development
---
