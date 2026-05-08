---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: ideogram-openapi.yml
  format: yaml
  label: Ideogram API
  slug: platform
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/ideogram/refs/heads/main/openapi/ideogram-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  - Adjustment
  pricingCategory: Usage-Based (Per Image)
description: FOCUS-aligned FinOps view of Ideogram. Ideogram bills per image generated with rate based on rendering tier (Turbo / Default / Quality). Custom model training, dataset uploads, and editing operations consume additional cost. Tier choice is the dominant cost lever.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Ideogram
  ProviderName: Ideogram
  PublisherName: Ideogram
  ServiceCategory: AI
  ServiceName: Ideogram API
layout: finops
meters:
- aggregation: sum
  description: Image generations charged by rendering tier (Turbo/Default/Quality).
  dimensions:
  - account
  - tier
  - model
  name: image_generations
  unit: image
- aggregation: sum
  description: Edit / inpaint / remix / reframe / replace-background calls.
  dimensions:
  - account
  - operation
  name: image_edits
  unit: image
- aggregation: sum
  description: Custom model training jobs and dataset asset uploads.
  dimensions:
  - account
  - dataset
  name: custom_model_training
  unit: training_job
name: Ideogram Finops
provider_name: Ideogram
provider_slug: ideogram
publisher_name: Ideogram
service_category: AI
slug: ideogram-finops
source_filename: ideogram-finops.yml
source_heading: FinOps Profile
source_url: https://ideogram.ai/features/api-pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Ideogram\nproviderId: ideogram\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: true\ntags:\n- AI\n- Image Generation\n- Text\n- Realistic\n- Editing\n- FinOps\n- Cost Management\n- FOCUS\ndescription: >-\n  FOCUS-aligned FinOps view of Ideogram. Ideogram bills per image generated with rate based\n  on rendering tier (Turbo / Default / Quality). Custom model training, dataset uploads, and\n  editing operations consume additional cost. Tier choice is the dominant cost lever.\nnotes: Use Turbo for high-volume / draft workflows; switch to Quality only for final assets.\nsources:\n- https://ideogram.ai/features/api-pricing\n- https://docs.ideogram.ai/\n- https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n\
  \  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Ideogram\nserviceCategory: AI\nbillingModel:\n  pricingCategory: Usage-Based (Per Image)\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n  - Usage\n  - Purchase\n  - Adjustment\nfocusColumns:\n  ServiceName: Ideogram API\n  ServiceCategory: AI\n  ProviderName: Ideogram\n  PublisherName: Ideogram\n  InvoiceIssuerName: Ideogram\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n- name: image_generations\n  description: Image generations charged by rendering tier (Turbo/Default/Quality).\n  unit: image\n  aggregation: sum\n  dimensions:\n  - account\n  - tier\n  - model\n- name: image_edits\n  description: Edit / inpaint / remix / reframe / replace-background calls.\n  unit: image\n  aggregation: sum\n  dimensions:\n  - account\n  - operation\n- name: custom_model_training\n  description: Custom model training jobs and dataset asset uploads.\n  unit: training_job\n  aggregation:\
  \ sum\n  dimensions:\n  - account\n  - dataset\nprinciples:\n- name: Visibility\n  description: Track per-tier image usage and editing operations in the developer dashboard.\n- name: Allocation\n  description: Tag generations to creative project / brand to allocate spend.\n- name: Optimization\n  description: Default to Turbo for drafts; reserve Quality for hero assets and final output.\n- name: Accountability\n  description: Assign budget owners per creative workflow.\nmaintainers:\n- FN: Kin Lane\n  email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/ideogram/refs/heads/main/finops/ideogram-finops.yml
sources:
- https://ideogram.ai/features/api-pricing
- https://docs.ideogram.ai/
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- AI
- Image Generation
- Text
- Realistic
- Editing
- FinOps
- Cost Management
- FOCUS
---
