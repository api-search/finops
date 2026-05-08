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
  pricingCategory: Usage + Provisioned Throughput
description: FOCUS-aligned FinOps view of Luma AI Dream Machine API. Build-tier is per-second video ($0.08/s for Ray-2) and per-request/per-pixel image generation. Scale-tier is provisioned throughput at $2,100-$3,800/month per unit (8-unit minimum). Note that Dream Machine consumer credits do not transfer to API.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Luma AI
  ProviderName: Luma AI
  PublisherName: Luma AI
  ServiceCategory: AI
  ServiceName: Luma Dream Machine API
layout: finops
meters:
- aggregation: sum
  description: Seconds of generated video (Ray series).
  dimensions:
  - account
  - model
  name: video_seconds
  unit: second
- aggregation: sum
  description: Per-request image generation/edit calls (uni-1 Photon).
  dimensions:
  - account
  - model
  - operation
  name: image_requests
  unit: request
- aggregation: sum
  description: Million-pixel-based Photon image billing.
  dimensions:
  - account
  name: image_pixels
  unit: million_pixels
- aggregation: max
  description: Reserved capacity units on Scale plans.
  dimensions:
  - account
  name: provisioned_units
  unit: unit-month
name: Luma Ai Finops
provider_name: Luma AI
provider_slug: luma-ai
publisher_name: Luma AI
service_category: AI
slug: luma-ai-finops
source_filename: luma-ai-finops.yml
source_heading: FinOps Profile
source_url: https://lumalabs.ai/dream-machine/api
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Luma AI\nproviderId: luma-ai\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: true\ntags:\n- AI\n- Video Generation\n- Image Generation\n- 3D\n- Dream Machine\n- Multimodal\n- FinOps\n- Cost Management\n- FOCUS\ndescription: >-\n  FOCUS-aligned FinOps view of Luma AI Dream Machine API. Build-tier is per-second video\n  ($0.08/s for Ray-2) and per-request/per-pixel image generation. Scale-tier is provisioned\n  throughput at $2,100-$3,800/month per unit (8-unit minimum). Note that Dream Machine\n  consumer credits do not transfer to API.\nnotes: Right-size between Build (PAYG) and Scale (provisioned) based on predictable monthly burn.\nsources:\n- https://lumalabs.ai/dream-machine/api\n- https://docs.lumalabs.ai/\n- https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n\
  \  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Luma AI\nserviceCategory: AI\nbillingModel:\n  pricingCategory: Usage + Provisioned Throughput\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n  - Usage\n  - Purchase\n  - Adjustment\nfocusColumns:\n  ServiceName: Luma Dream Machine API\n  ServiceCategory: AI\n  ProviderName: Luma AI\n  PublisherName: Luma AI\n  InvoiceIssuerName: Luma AI\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n- name: video_seconds\n  description: Seconds of generated video (Ray series).\n  unit: second\n  aggregation: sum\n  dimensions:\n  - account\n  - model\n- name: image_requests\n  description: Per-request image generation/edit calls (uni-1 Photon).\n  unit: request\n  aggregation: sum\n  dimensions:\n  - account\n  - model\n  - operation\n- name: image_pixels\n  description: Million-pixel-based Photon image billing.\n  unit: million_pixels\n\
  \  aggregation: sum\n  dimensions:\n  - account\n- name: provisioned_units\n  description: Reserved capacity units on Scale plans.\n  unit: unit-month\n  aggregation: max\n  dimensions:\n  - account\nprinciples:\n- name: Visibility\n  description: Track video seconds and image requests in Luma billing dashboard.\n- name: Allocation\n  description: Tag generations to creative project / app surface.\n- name: Optimization\n  description: Pre-purchase Scale capacity if monthly Build burn exceeds Scale break-even.\n- name: Accountability\n  description: Assign budget owners for Build (variable) vs Scale (committed) allocations.\nmaintainers:\n- FN: Kin Lane\n  email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/luma-ai/refs/heads/main/finops/luma-ai-finops.yml
sources:
- https://lumalabs.ai/dream-machine/api
- https://docs.lumalabs.ai/
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- AI
- Video Generation
- Image Generation
- 3D
- Dream Machine
- Multimodal
- FinOps
- Cost Management
- FOCUS
---
