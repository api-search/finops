---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: photoroom-openapi.yml
  format: yaml
  label: Photoroom API
  slug: platform
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/photoroom/refs/heads/main/openapi/photoroom-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  - Adjustment
  pricingCategory: Subscription + Per-Image Usage
description: FOCUS-aligned FinOps view of Photoroom. Photoroom uses per-image usage billing across Basic ($0.02) and Plus ($0.10) plans, with Plus calls counted as 5x Basic calls. API Partner programs reduce per-image cost to $0.01 for high-volume consumer apps. Enterprise contracts require 200K image annual minimum.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Photoroom
  ProviderName: Photoroom
  PublisherName: Photoroom
  ServiceCategory: AI
  ServiceName: Photoroom API
layout: finops
meters:
- aggregation: sum
  description: Remove Background API images at $0.02 each (Basic).
  dimensions:
  - account
  name: bg_remove_images
  unit: image
- aggregation: sum
  description: Image Editing API calls at $0.10 each (Plus).
  dimensions:
  - account
  - operation
  name: image_edit_calls
  unit: image
- aggregation: sum
  description: API Partner program calls at $0.01 each (qualifying consumer apps).
  dimensions:
  - account
  name: api_partner_images
  unit: image
name: Photoroom Finops
provider_name: Photoroom
provider_slug: photoroom
publisher_name: Photoroom
service_category: AI
slug: photoroom-finops
source_filename: photoroom-finops.yml
source_heading: FinOps Profile
source_url: https://www.photoroom.com/api/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Photoroom\nproviderId: photoroom\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: true\ntags:\n- AI\n- Image Editing\n- Background Removal\n- E-commerce\n- Visual\n- FinOps\n- Cost Management\n- FOCUS\ndescription: >-\n  FOCUS-aligned FinOps view of Photoroom. Photoroom uses per-image usage billing across\n  Basic ($0.02) and Plus ($0.10) plans, with Plus calls counted as 5x Basic calls. API\n  Partner programs reduce per-image cost to $0.01 for high-volume consumer apps. Enterprise\n  contracts require 200K image annual minimum.\nnotes: Volume threshold to qualify for API Partner ($0.01) is the largest unit-cost lever.\nsources:\n- https://www.photoroom.com/api/pricing\n- https://docs.photoroom.com/\n- https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n\
  \  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Photoroom\nserviceCategory: AI\nbillingModel:\n  pricingCategory: Subscription + Per-Image Usage\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n  - Usage\n  - Purchase\n  - Adjustment\nfocusColumns:\n  ServiceName: Photoroom API\n  ServiceCategory: AI\n  ProviderName: Photoroom\n  PublisherName: Photoroom\n  InvoiceIssuerName: Photoroom\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n- name: bg_remove_images\n  description: Remove Background API images at $0.02 each (Basic).\n  unit: image\n  aggregation: sum\n  dimensions:\n  - account\n- name: image_edit_calls\n  description: Image Editing API calls at $0.10 each (Plus).\n  unit: image\n  aggregation: sum\n  dimensions:\n  - account\n  - operation\n- name: api_partner_images\n  description: API Partner program calls at $0.01 each (qualifying consumer apps).\n  unit: image\n\
  \  aggregation: sum\n  dimensions:\n  - account\nprinciples:\n- name: Visibility\n  description: Track per-API call counts via Photoroom API dashboard.\n- name: Allocation\n  description: Tag calls to product/marketplace use case.\n- name: Optimization\n  description: Use Basic plan for plain background removal; reserve Plus for AI Backgrounds and Shadows. Negotiate API Partner if volume qualifies.\n- name: Accountability\n  description: Assign budget owner per product surface that consumes Photoroom.\nmaintainers:\n- FN: Kin Lane\n  email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/photoroom/refs/heads/main/finops/photoroom-finops.yml
sources:
- https://www.photoroom.com/api/pricing
- https://docs.photoroom.com/
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- AI
- Image Editing
- Background Removal
- E-commerce
- Visual
- FinOps
- Cost Management
- FOCUS
---
