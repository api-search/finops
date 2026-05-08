---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: On Credit Purchase / Monthly
  chargeCategories:
  - Usage
  - Purchase
  - Adjustment
  pricingCategory: Prepaid Credits + Per-Generation Usage
description: FOCUS-aligned FinOps view of Black Forest Labs. BFL bills via prepaid credits drawn down per generation. Cost per image varies by Flux model variant, output dimensions, and number of input images. Schnell is free direct from BFL; Pro and 1.1 Pro list at ~$0.04/image.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Black Forest Labs
  ProviderName: Black Forest Labs
  PublisherName: Black Forest Labs
  ServiceCategory: AI
  ServiceName: BFL Flux Image Generation API
layout: finops
meters:
- aggregation: sum
  description: Image generations charged per call against credit balance.
  dimensions:
  - account
  - model
  - region
  - dimensions
  name: image_generations
  unit: image
- aggregation: sum
  description: Prepaid credit purchases.
  dimensions:
  - account
  name: credits_purchased
  unit: USD
name: Black Forest Labs Finops
provider_name: Black Forest Labs
provider_slug: black-forest-labs
publisher_name: Black Forest Labs
service_category: AI
slug: black-forest-labs-finops
source_filename: black-forest-labs-finops.yml
source_heading: FinOps Profile
source_url: https://bfl.ai/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Black Forest Labs\nproviderId: black-forest-labs\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: true\ntags:\n- AI\n- Image Generation\n- Flux\n- Open Weights\n- BFL\n- FinOps\n- Cost Management\n- FOCUS\ndescription: >-\n  FOCUS-aligned FinOps view of Black Forest Labs. BFL bills via prepaid credits drawn down\n  per generation. Cost per image varies by Flux model variant, output dimensions, and number\n  of input images. Schnell is free direct from BFL; Pro and 1.1 Pro list at ~$0.04/image.\nnotes: Cost optimization centers on model selection (Schnell free vs Pro paid) and output dimension control.\nsources:\n- https://bfl.ai/pricing\n- https://docs.bfl.ai/\n- https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion:\
  \ '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Black Forest Labs\nserviceCategory: AI\nbillingModel:\n  pricingCategory: Prepaid Credits + Per-Generation Usage\n  billingFrequency: On Credit Purchase / Monthly\n  billingCurrency: USD\n  chargeCategories:\n  - Usage\n  - Purchase\n  - Adjustment\nfocusColumns:\n  ServiceName: BFL Flux Image Generation API\n  ServiceCategory: AI\n  ProviderName: Black Forest Labs\n  PublisherName: Black Forest Labs\n  InvoiceIssuerName: Black Forest Labs\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n- name: image_generations\n  description: Image generations charged per call against credit balance.\n  unit: image\n  aggregation: sum\n  dimensions:\n  - account\n  - model\n  - region\n  - dimensions\n- name: credits_purchased\n  description: Prepaid credit purchases.\n  unit: USD\n  aggregation: sum\n  dimensions:\n  - account\nprinciples:\n- name: Visibility\n  description: Track per-call cost via\
  \ account credit drawdown reports.\n- name: Allocation\n  description: Tag generations to applications and creative workflows.\n- name: Optimization\n  description: Use Schnell or smaller variants for drafts, reserve Pro/Max for final assets; smaller dimensions cost less.\n- name: Accountability\n  description: Assign budget owners per workflow / creative team.\nmaintainers:\n- FN: Kin Lane\n  email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/black-forest-labs/refs/heads/main/finops/black-forest-labs-finops.yml
sources:
- https://bfl.ai/pricing
- https://docs.bfl.ai/
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- AI
- Image Generation
- Flux
- Open Weights
- BFL
- FinOps
- Cost Management
- FOCUS
---
