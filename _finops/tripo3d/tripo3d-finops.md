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
  - Usage
  - Purchase
  - Adjustment
  pricingCategory: Prepaid Credits + Per-Task Usage
description: FOCUS-aligned FinOps view of Tripo3D. Tripo Platform bills API usage on a task-credit basis (separate from consumer subscriptions). Per-task credit costs vary by task type (text-to-3D, image-to-3D, refinement, retexture, rigging, animation).
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Tripo3D
  ProviderName: Tripo3D
  PublisherName: Tripo3D (VAST)
  ServiceCategory: AI
  ServiceName: Tripo3D Platform API
layout: finops
meters:
- aggregation: sum
  description: Text-to-3D generation tasks.
  dimensions:
  - account
  name: text_to_3d_tasks
  unit: task
- aggregation: sum
  description: Image-to-3D generation tasks.
  dimensions:
  - account
  name: image_to_3d_tasks
  unit: task
- aggregation: sum
  description: Mesh refinement / retexture / rigging / animation tasks.
  dimensions:
  - account
  - operation
  name: refinement_tasks
  unit: task
- aggregation: sum
  description: Prepaid Tripo platform credit purchases.
  dimensions:
  - account
  name: credits_purchased
  unit: USD
name: Tripo3D Finops
provider_name: Tripo3D
provider_slug: tripo3d
publisher_name: Tripo3D (VAST)
service_category: AI
slug: tripo3d-finops
source_filename: tripo3d-finops.yml
source_heading: FinOps Profile
source_url: https://platform.tripo3d.ai/docs/billing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Tripo3D\nproviderId: tripo3d\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: partial\ntags:\n- AI\n- 3D\n- Generation\n- API\n- Mesh\n- Texturing\n- FinOps\n- Cost Management\n- FOCUS\ndescription: >-\n  FOCUS-aligned FinOps view of Tripo3D. Tripo Platform bills API usage on a task-credit\n  basis (separate from consumer subscriptions). Per-task credit costs vary by task type\n  (text-to-3D, image-to-3D, refinement, retexture, rigging, animation).\nnotes: Track per-task credit consumption to attribute spend to creative workflows.\nsources:\n- https://platform.tripo3d.ai/docs/billing\n- https://www.tripo3d.ai/api\n- https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\n\
  publisherName: Tripo3D (VAST)\nserviceCategory: AI\nbillingModel:\n  pricingCategory: Prepaid Credits + Per-Task Usage\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n  - Usage\n  - Purchase\n  - Adjustment\nfocusColumns:\n  ServiceName: Tripo3D Platform API\n  ServiceCategory: AI\n  ProviderName: Tripo3D\n  PublisherName: Tripo3D (VAST)\n  InvoiceIssuerName: Tripo3D\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n- name: text_to_3d_tasks\n  description: Text-to-3D generation tasks.\n  unit: task\n  aggregation: sum\n  dimensions:\n  - account\n- name: image_to_3d_tasks\n  description: Image-to-3D generation tasks.\n  unit: task\n  aggregation: sum\n  dimensions:\n  - account\n- name: refinement_tasks\n  description: Mesh refinement / retexture / rigging / animation tasks.\n  unit: task\n  aggregation: sum\n  dimensions:\n  - account\n  - operation\n- name: credits_purchased\n  description: Prepaid Tripo platform credit purchases.\n  unit: USD\n  aggregation:\
  \ sum\n  dimensions:\n  - account\nprinciples:\n- name: Visibility\n  description: Track credit drawdown per task type in Tripo platform billing dashboard.\n- name: Allocation\n  description: Tag tasks to consuming game / app / studio.\n- name: Optimization\n  description: Use Text-to-3D for drafts; reserve refinement / retexture only for final assets.\n- name: Accountability\n  description: Assign credit-budget owner per consuming product.\nmaintainers:\n- FN: Kin Lane\n  email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/tripo3d/refs/heads/main/finops/tripo3d-finops.yml
sources:
- https://platform.tripo3d.ai/docs/billing
- https://www.tripo3d.ai/api
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- AI
- 3D
- Generation
- API
- Mesh
- Texturing
- FinOps
- Cost Management
- FOCUS
---
