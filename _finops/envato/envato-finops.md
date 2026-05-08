---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: One-time / Monthly
  chargeCategories:
  - Purchase
  - Subscription
  pricingCategory: Per-Asset / Subscription
description: FOCUS-aligned FinOps profile for Envato. Cost is per-asset (Market) or subscription (Elements). The Market API itself is free; purchases happen on the marketplace via the standard checkout. Elements is invoiced monthly/annually. Optimize Elements by matching seat tier to active users and consolidating Market purchases under a single buyer account for reporting.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Envato
  ProviderName: Envato
  PublisherName: Envato
  ServiceCategory: Stock Media
  ServiceName: Envato Market / Elements
layout: finops
meters:
- aggregation: sum
  description: Per-asset purchases on Envato Market.
  dimensions:
  - marketplace
  - asset_type
  name: market_purchases
  unit: asset
- aggregation: max
  description: Envato Elements subscription seats.
  dimensions:
  - tier
  name: elements_subscription
  unit: seat-month
name: Envato Finops
provider_name: Envato
provider_slug: envato
publisher_name: Envato
service_category: Stock Media / Digital Marketplace
slug: envato-finops
source_filename: envato-finops.yml
source_heading: FinOps Profile
source_url: https://elements.envato.com/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Envato\nproviderId: envato\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: true\ntags:\n- Stock Media\n- Marketplace\n- Themes\n- Audio\n- Video\n- Graphics\n- Subscription\n- FinOps\n- Cost Management\n- FOCUS\ndescription: >-\n  FOCUS-aligned FinOps profile for Envato. Cost is per-asset (Market) or subscription (Elements). The\n  Market API itself is free; purchases happen on the marketplace via the standard checkout. Elements\n  is invoiced monthly/annually. Optimize Elements by matching seat tier to active users and\n  consolidating Market purchases under a single buyer account for reporting.\nnotes: \"Two cost paths: Market per-asset and Elements subscription.\"\nsources:\n- https://elements.envato.com/pricing\n- https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n\
  \  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Envato\nserviceCategory: Stock Media / Digital Marketplace\nbillingModel:\n  pricingCategory: Per-Asset / Subscription\n  billingFrequency: One-time / Monthly\n  billingCurrency: USD\n  chargeCategories:\n  - Purchase\n  - Subscription\nfocusColumns:\n  ServiceName: Envato Market / Elements\n  ServiceCategory: Stock Media\n  ProviderName: Envato\n  PublisherName: Envato\n  InvoiceIssuerName: Envato\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n- name: market_purchases\n  description: Per-asset purchases on Envato Market.\n  unit: asset\n  aggregation: sum\n  dimensions:\n  - marketplace\n  - asset_type\n- name: elements_subscription\n  description: Envato Elements subscription seats.\n  unit: seat-month\n  aggregation: max\n  dimensions:\n  - tier\nprinciples:\n- name: Visibility\n  description: Centralize Market purchases under one buyer account;\
  \ pull Elements seat report monthly.\n- name: Allocation\n  description: Allocate Market purchases to project; Elements seats to consuming creative team.\n- name: Optimization\n  description: Use Elements for high-volume creative; reserve Market purchases for one-off items not on Elements.\n- name: Accountability\n  description: Creative ops owns Elements; product/dev owns Market app credentials and purchase reconciliation.\nmaintainers:\n- FN: Kin Lane\n  email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/envato/refs/heads/main/finops/envato-finops.yml
sources:
- https://elements.envato.com/pricing
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Stock Media
- Marketplace
- Themes
- Audio
- Video
- Graphics
- Subscription
- FinOps
- Cost Management
- FOCUS
---
