---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: On Credit Purchase
  chargeCategories:
  - Usage
  - Purchase
  - Adjustment
  pricingCategory: Prepaid Credits + Per-Operation Usage
description: FOCUS-aligned FinOps view of Recraft. Recraft uses prepaid API Units (1,000 units = $1) consumed per operation. Cost dominance comes from raster vs vector and version (V4 Pro is ~6x V4 cost). Editing operations are largely cheap ($0.004-$0.08); only Creative upscale matches V4 Pro pricing.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Recraft
  ProviderName: Recraft
  PublisherName: Recraft
  ServiceCategory: AI
  ServiceName: Recraft API
layout: finops
meters:
- aggregation: sum
  description: Raster image generation (V2/V3/V4/V4 Pro).
  dimensions:
  - account
  - model
  name: raster_generations
  unit: image
- aggregation: sum
  description: Vector image generation (V2/V3/V4/V4 Pro Vector).
  dimensions:
  - account
  - model
  name: vector_generations
  unit: image
- aggregation: sum
  description: Image-to-image, inpainting, background replace, style creation, vectorize, bg-remove, upscale, region-erase.
  dimensions:
  - account
  - operation
  name: edit_operations
  unit: image
- aggregation: sum
  description: Prepaid API Unit purchases.
  dimensions:
  - account
  name: api_units_purchased
  unit: USD
name: Recraft Finops
provider_name: Recraft
provider_slug: recraft
publisher_name: Recraft
service_category: AI
slug: recraft-finops
source_filename: recraft-finops.yml
source_heading: FinOps Profile
source_url: https://www.recraft.ai/docs/api-reference/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Recraft\nproviderId: recraft\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: true\ntags:\n- AI\n- Image Generation\n- Design\n- Vector\n- Style\n- FinOps\n- Cost Management\n- FOCUS\ndescription: >-\n  FOCUS-aligned FinOps view of Recraft. Recraft uses prepaid API Units (1,000 units = $1)\n  consumed per operation. Cost dominance comes from raster vs vector and version (V4 Pro is\n  ~6x V4 cost). Editing operations are largely cheap ($0.004-$0.08); only Creative upscale\n  matches V4 Pro pricing.\nnotes: Right-size model version per workload; reserve V4 Pro for hero assets only.\nsources:\n- https://www.recraft.ai/docs/api-reference/pricing\n- https://www.recraft.ai/docs/api-reference/getting-started\n- https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n\
  \  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Recraft\nserviceCategory: AI\nbillingModel:\n  pricingCategory: Prepaid Credits + Per-Operation Usage\n  billingFrequency: On Credit Purchase\n  billingCurrency: USD\n  chargeCategories:\n  - Usage\n  - Purchase\n  - Adjustment\nfocusColumns:\n  ServiceName: Recraft API\n  ServiceCategory: AI\n  ProviderName: Recraft\n  PublisherName: Recraft\n  InvoiceIssuerName: Recraft\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n- name: raster_generations\n  description: Raster image generation (V2/V3/V4/V4 Pro).\n  unit: image\n  aggregation: sum\n  dimensions:\n  - account\n  - model\n- name: vector_generations\n  description: Vector image generation (V2/V3/V4/V4 Pro Vector).\n  unit: image\n  aggregation: sum\n  dimensions:\n  - account\n  - model\n- name: edit_operations\n  description: Image-to-image, inpainting, background replace, style creation, vectorize,\
  \ bg-remove, upscale, region-erase.\n  unit: image\n  aggregation: sum\n  dimensions:\n  - account\n  - operation\n- name: api_units_purchased\n  description: Prepaid API Unit purchases.\n  unit: USD\n  aggregation: sum\n  dimensions:\n  - account\nprinciples:\n- name: Visibility\n  description: Track unit drawdown by operation in Recraft profile.\n- name: Allocation\n  description: Tag generations to creative project / brand.\n- name: Optimization\n  description: Use V4 (not V4 Pro) for general work; reserve V4 Pro and Creative upscale for hero assets.\n- name: Accountability\n  description: Assign budget owners per creative team / brand.\nmaintainers:\n- FN: Kin Lane\n  email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/recraft/refs/heads/main/finops/recraft-finops.yml
sources:
- https://www.recraft.ai/docs/api-reference/pricing
- https://www.recraft.ai/docs/api-reference/getting-started
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- AI
- Image Generation
- Design
- Vector
- Style
- FinOps
- Cost Management
- FOCUS
---
