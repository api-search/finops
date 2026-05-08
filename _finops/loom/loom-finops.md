---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly or Annual
  chargeCategories:
  - Purchase
  - Adjustment
  pricingCategory: Subscription (Per Seat)
description: FOCUS-aligned FinOps profile for Loom. Loom bills primarily as a per-seat monthly subscription across Starter (free), Business, Business + AI, and Enterprise tiers. Developer SDK use does not add metered API charges; cost scales with seat count and selected tier.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Atlassian
  ProviderName: Loom
  PublisherName: Atlassian
  ServiceCategory: Productivity
  ServiceName: Loom
layout: finops
meters:
- aggregation: sum
  description: Per-user monthly subscription. Business $18/seat, Business+AI $24/seat, Enterprise contract.
  dimensions:
  - workspace
  - plan
  name: seats
  unit: seat
name: Loom Finops
provider_name: Loom
provider_slug: loom
publisher_name: Atlassian (Loom)
service_category: Productivity
slug: loom-finops
source_filename: loom-finops.yml
source_heading: FinOps Profile
source_url: https://www.loom.com/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Loom\nproviderId: loom\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: true\ntags:\n- Productivity\n- Video\n- Async\n- Communication\n- SaaS\n- FinOps\n- Cost Management\n- FOCUS\ndescription: FOCUS-aligned FinOps profile for Loom. Loom bills primarily as a per-seat\n  monthly subscription across Starter (free), Business, Business + AI, and Enterprise\n  tiers. Developer SDK use does not add metered API charges; cost scales with seat count\n  and selected tier.\nsources:\n- https://www.loom.com/pricing\n- https://dev.loom.com/\n- https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Atlassian (Loom)\nserviceCategory: Productivity\n\
  billingModel:\n  pricingCategory: Subscription (Per Seat)\n  billingFrequency: Monthly or Annual\n  billingCurrency: USD\n  chargeCategories:\n  - Purchase\n  - Adjustment\nfocusColumns:\n  ServiceName: Loom\n  ServiceCategory: Productivity\n  ProviderName: Loom\n  PublisherName: Atlassian\n  InvoiceIssuerName: Atlassian\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n- name: seats\n  description: Per-user monthly subscription. Business $18/seat, Business+AI $24/seat,\n    Enterprise contract.\n  unit: seat\n  aggregation: sum\n  dimensions:\n  - workspace\n  - plan\nprinciples:\n- name: Visibility\n  description: Use Loom workspace billing reports to inventory active seats per workspace\n    and plan.\n- name: Allocation\n  description: Allocate seats by team membership; tag enterprise contracts to the procuring\n    business unit.\n- name: Optimization\n  description: Reclaim seats from inactive users; choose annual billing for the 17%\n    discount; downgrade Business+AI\
  \ seats that don't use AI features.\n- name: Accountability\n  description: Assign a workspace owner; review monthly seat counts against active-user\n    reports.\nmaintainers:\n- FN: Kin Lane\n  email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/loom/refs/heads/main/finops/loom-finops.yml
sources:
- https://www.loom.com/pricing
- https://dev.loom.com/
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Productivity
- Video
- Async
- Communication
- SaaS
- FinOps
- Cost Management
- FOCUS
---
