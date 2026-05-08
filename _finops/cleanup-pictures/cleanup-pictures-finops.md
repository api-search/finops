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
  pricingCategory: Prepaid Credits + Per-Call Usage
description: FOCUS-aligned FinOps view of Cleanup.pictures via the ClipDrop API. Cleanup is billed in credits (1 successful call = 1 credit). New developers receive 100 free credits. Failed calls do not consume credits. Cost is publisher-issued via Jasper.ai (ClipDrop owner).
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Jasper.ai
  ProviderName: Cleanup.pictures
  PublisherName: Jasper.ai (ClipDrop)
  ServiceCategory: AI
  ServiceName: Cleanup.pictures Inpainting API
layout: finops
meters:
- aggregation: sum
  description: Successful cleanup API calls at 1 credit each.
  dimensions:
  - account
  - mode
  name: cleanup_calls
  unit: credit
- aggregation: sum
  description: Prepaid credit pack purchases.
  dimensions:
  - account
  name: credits_purchased
  unit: USD
name: Cleanup Pictures Finops
provider_name: Cleanup.pictures
provider_slug: cleanup-pictures
publisher_name: Jasper.ai (ClipDrop)
service_category: AI
slug: cleanup-pictures-finops
source_filename: cleanup-pictures-finops.yml
source_heading: FinOps Profile
source_url: https://clipdrop.co/apis/docs/cleanup
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Cleanup.pictures\nproviderId: cleanup-pictures\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: true\ntags:\n- AI\n- Image Editing\n- Object Removal\n- Inpainting\n- Visual\n- FinOps\n- Cost Management\n- FOCUS\ndescription: >-\n  FOCUS-aligned FinOps view of Cleanup.pictures via the ClipDrop API. Cleanup is billed in\n  credits (1 successful call = 1 credit). New developers receive 100 free credits. Failed\n  calls do not consume credits. Cost is publisher-issued via Jasper.ai (ClipDrop owner).\nnotes: Track per-call mode (fast vs quality) since both consume the same credit but differ in latency.\nsources:\n- https://clipdrop.co/apis/docs/cleanup\n- https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n\
  \  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Jasper.ai (ClipDrop)\nserviceCategory: AI\nbillingModel:\n  pricingCategory: Prepaid Credits + Per-Call Usage\n  billingFrequency: On Credit Purchase\n  billingCurrency: USD\n  chargeCategories:\n  - Usage\n  - Purchase\n  - Adjustment\nfocusColumns:\n  ServiceName: Cleanup.pictures Inpainting API\n  ServiceCategory: AI\n  ProviderName: Cleanup.pictures\n  PublisherName: Jasper.ai (ClipDrop)\n  InvoiceIssuerName: Jasper.ai\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n- name: cleanup_calls\n  description: Successful cleanup API calls at 1 credit each.\n  unit: credit\n  aggregation: sum\n  dimensions:\n  - account\n  - mode\n- name: credits_purchased\n  description: Prepaid credit pack purchases.\n  unit: USD\n  aggregation: sum\n  dimensions:\n  - account\nprinciples:\n- name: Visibility\n  description: Use x-remaining-credits and x-credits-consumed headers per response to track burn.\n- name:\
  \ Allocation\n  description: Tag calls to product feature consuming the cleanup API.\n- name: Optimization\n  description: Pre-compute masks tightly to reduce retry rate; failed calls are free.\n- name: Accountability\n  description: Assign a credit budget owner per consuming product.\nmaintainers:\n- FN: Kin Lane\n  email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/cleanup-pictures/refs/heads/main/finops/cleanup-pictures-finops.yml
sources:
- https://clipdrop.co/apis/docs/cleanup
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- AI
- Image Editing
- Object Removal
- Inpainting
- Visual
- FinOps
- Cost Management
- FOCUS
---
