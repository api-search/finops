---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Purchase
  - Usage
  - Adjustment
  pricingCategory: Subscription with Credit Allocation + Per-Task Usage
description: FOCUS-aligned FinOps view of Meshy. Meshy bundles monthly credits in subscription tiers (Free 100, Pro 1,000, Studio 4,000, Enterprise custom). Per-task credit cost is returned as consumed_credits in the API response. Free retries (4 Pro / 8 Studio / unlimited Enterprise) reduce the effective per-asset cost.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Meshy
  ProviderName: Meshy
  PublisherName: Meshy
  ServiceCategory: AI
  ServiceName: Meshy 3D API
layout: finops
meters:
- aggregation: sum
  description: Credits consumed by Text-to-3D tasks (preview + refine).
  dimensions:
  - account
  - phase
  name: text_to_3d_credits
  unit: credit
- aggregation: sum
  description: Credits consumed by Image-to-3D and Multi Image-to-3D tasks.
  dimensions:
  - account
  name: image_to_3d_credits
  unit: credit
- aggregation: sum
  description: Credits consumed by Rigging / Animation / Retexture / Remesh tasks.
  dimensions:
  - account
  - operation
  name: animation_credits
  unit: credit
- aggregation: sum
  description: Credits consumed by Multi-Color Print, Analyze Printability, and Repair Printability tasks.
  dimensions:
  - account
  name: print_analysis_credits
  unit: credit
- aggregation: max
  description: Plan-tier monthly credit allocation.
  dimensions:
  - account
  - plan
  name: monthly_credits_allocated
  unit: credit
name: Meshy Finops
provider_name: Meshy
provider_slug: meshy
publisher_name: Meshy
service_category: AI
slug: meshy-finops
source_filename: meshy-finops.yml
source_heading: FinOps Profile
source_url: https://www.meshy.ai/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Meshy\nproviderId: meshy\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: true\ntags:\n- AI\n- 3D\n- Generation\n- Texturing\n- Animation\n- FinOps\n- Cost Management\n- FOCUS\ndescription: >-\n  FOCUS-aligned FinOps view of Meshy. Meshy bundles monthly credits in subscription tiers\n  (Free 100, Pro 1,000, Studio 4,000, Enterprise custom). Per-task credit cost is returned\n  as consumed_credits in the API response. Free retries (4 Pro / 8 Studio / unlimited\n  Enterprise) reduce the effective per-asset cost.\nnotes: Right-size the plan tier vs expected monthly credit burn; plan upgrade is the dominant cost lever.\nsources:\n- https://www.meshy.ai/pricing\n- https://docs.meshy.ai/\n- https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec:\
  \ FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Meshy\nserviceCategory: AI\nbillingModel:\n  pricingCategory: Subscription with Credit Allocation + Per-Task Usage\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n  - Purchase\n  - Usage\n  - Adjustment\nfocusColumns:\n  ServiceName: Meshy 3D API\n  ServiceCategory: AI\n  ProviderName: Meshy\n  PublisherName: Meshy\n  InvoiceIssuerName: Meshy\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n- name: text_to_3d_credits\n  description: Credits consumed by Text-to-3D tasks (preview + refine).\n  unit: credit\n  aggregation: sum\n  dimensions:\n  - account\n  - phase\n- name: image_to_3d_credits\n  description: Credits consumed by Image-to-3D and Multi Image-to-3D tasks.\n  unit: credit\n  aggregation: sum\n  dimensions:\n  - account\n- name: animation_credits\n  description: Credits consumed by Rigging / Animation / Retexture / Remesh tasks.\n\
  \  unit: credit\n  aggregation: sum\n  dimensions:\n  - account\n  - operation\n- name: print_analysis_credits\n  description: Credits consumed by Multi-Color Print, Analyze Printability, and Repair Printability tasks.\n  unit: credit\n  aggregation: sum\n  dimensions:\n  - account\n- name: monthly_credits_allocated\n  description: Plan-tier monthly credit allocation.\n  unit: credit\n  aggregation: max\n  dimensions:\n  - account\n  - plan\nprinciples:\n- name: Visibility\n  description: Read consumed_credits from each API response and aggregate per task type.\n- name: Allocation\n  description: Tag tasks to consuming game/app/team.\n- name: Optimization\n  description: Use Pro/Studio retries before paying for re-generation; right-size plan to match monthly credit burn.\n- name: Accountability\n  description: Assign credit-budget owner per consuming workspace.\nmaintainers:\n- FN: Kin Lane\n  email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/meshy/refs/heads/main/finops/meshy-finops.yml
sources:
- https://www.meshy.ai/pricing
- https://docs.meshy.ai/
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- AI
- 3D
- Generation
- Texturing
- Animation
- FinOps
- Cost Management
- FOCUS
---
