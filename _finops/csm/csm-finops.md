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
  pricingCategory: Subscription with Plan-Gated API Access
description: FOCUS-aligned FinOps view of Common Sense Machines. CSM bills as Cube subscription tiers with API access bundled into mid-tier and enterprise plans. Per-API rate sheet is not openly published; track generation count via CSM dashboard.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Common Sense Machines
  ProviderName: Common Sense Machines
  PublisherName: Common Sense Machines
  ServiceCategory: AI
  ServiceName: CSM 3D Generation API
layout: finops
meters:
- aggregation: max
  description: Cube plan tier seats / subscription fee.
  dimensions:
  - account
  - plan
  name: cube_subscription
  unit: seat-month
- aggregation: sum
  description: 3D model generations performed via API.
  dimensions:
  - account
  - model_pipeline
  name: 3d_generations
  unit: generation
name: Csm Finops
provider_name: Common Sense Machines
provider_slug: csm
publisher_name: Common Sense Machines
service_category: AI
slug: csm-finops
source_filename: csm-finops.yml
source_heading: FinOps Profile
source_url: https://www.csm.ai/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Common Sense Machines\nproviderId: csm\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: partial\ntags:\n- AI\n- 3D\n- World Models\n- Scene Generation\n- Generative\n- FinOps\n- Cost Management\n- FOCUS\ndescription: >-\n  FOCUS-aligned FinOps view of Common Sense Machines. CSM bills as Cube subscription tiers\n  with API access bundled into mid-tier and enterprise plans. Per-API rate sheet is not\n  openly published; track generation count via CSM dashboard.\nnotes: Plan tier choice (Cube mid-tier vs Enterprise) is the dominant cost lever; per-call rates not public.\nsources:\n- https://www.csm.ai/\n- https://docs.csm.ai/\n- https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\n\
  publisherName: Common Sense Machines\nserviceCategory: AI\nbillingModel:\n  pricingCategory: Subscription with Plan-Gated API Access\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n  - Purchase\n  - Usage\n  - Adjustment\nfocusColumns:\n  ServiceName: CSM 3D Generation API\n  ServiceCategory: AI\n  ProviderName: Common Sense Machines\n  PublisherName: Common Sense Machines\n  InvoiceIssuerName: Common Sense Machines\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n- name: cube_subscription\n  description: Cube plan tier seats / subscription fee.\n  unit: seat-month\n  aggregation: max\n  dimensions:\n  - account\n  - plan\n- name: 3d_generations\n  description: 3D model generations performed via API.\n  unit: generation\n  aggregation: sum\n  dimensions:\n  - account\n  - model_pipeline\nprinciples:\n- name: Visibility\n  description: Track generations and plan tier in CSM dashboard.\n- name: Allocation\n  description: Tag generations per consuming\
  \ game/robotics/synthetic-data product.\n- name: Optimization\n  description: Move to Enterprise when production volume exceeds Cube mid-tier limits.\n- name: Accountability\n  description: Assign budget owner per consuming workspace.\nmaintainers:\n- FN: Kin Lane\n  email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/csm/refs/heads/main/finops/csm-finops.yml
sources:
- https://www.csm.ai/
- https://docs.csm.ai/
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- AI
- 3D
- World Models
- Scene Generation
- Generative
- FinOps
- Cost Management
- FOCUS
---
