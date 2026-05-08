---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: swagger
  format: yaml
  label: iStock API (Getty Platform)
  slug: platform
  spec_type: OpenAPI
  url: https://api.gettyimages.com/swagger
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly / Annual
  chargeCategories:
  - Subscription
  - Purchase
  pricingCategory: Subscription + Credits
description: FOCUS-aligned FinOps profile for iStock. Cost is driven by credit-pack purchases and/or monthly subscription downloads. For consumers/SMB this is direct on iStock.com; for API partners cost flows through the Getty enterprise contract. Optimize by matching subscription size to download cadence and avoiding mid-cycle credit top-ups.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Subscription
  InvoiceIssuerName: iStock
  ProviderName: Getty Images
  PublisherName: iStock
  ServiceCategory: Stock Media
  ServiceName: iStock
layout: finops
meters:
- aggregation: sum
  description: Asset downloads consumed against subscription or credit pack.
  dimensions:
  - collection
  - asset_type
  name: downloads
  unit: download
- aggregation: sum
  description: One-time credit pack purchases.
  dimensions:
  - pack_size
  name: credit_packs
  unit: pack
name: Istock Finops
provider_name: iStock
provider_slug: istock
publisher_name: Getty Images / iStock
service_category: Stock Media
slug: istock-finops
source_filename: istock-finops.yml
source_heading: FinOps Profile
source_url: https://www.istockphoto.com/plans-and-pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: iStock\nproviderId: istock\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: true\ntags:\n- Stock Media\n- Images\n- Video\n- Illustrations\n- Royalty-Free\n- Getty\n- FinOps\n- Cost Management\n- FOCUS\ndescription: >-\n  FOCUS-aligned FinOps profile for iStock. Cost is driven by credit-pack purchases and/or monthly\n  subscription downloads. For consumers/SMB this is direct on iStock.com; for API partners cost flows\n  through the Getty enterprise contract. Optimize by matching subscription size to download cadence\n  and avoiding mid-cycle credit top-ups.\nnotes: \"Two cost paths: consumer/SMB on iStock.com vs. enterprise API via Getty contract.\"\nsources:\n- https://www.istockphoto.com/plans-and-pricing\n- https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n\
  \  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Getty Images / iStock\nserviceCategory: Stock Media\nbillingModel:\n  pricingCategory: Subscription + Credits\n  billingFrequency: Monthly / Annual\n  billingCurrency: USD\n  chargeCategories:\n  - Subscription\n  - Purchase\nfocusColumns:\n  ServiceName: iStock\n  ServiceCategory: Stock Media\n  ProviderName: Getty Images\n  PublisherName: iStock\n  InvoiceIssuerName: iStock\n  BillingCurrency: USD\n  ChargeCategory: Subscription\nmeters:\n- name: downloads\n  description: Asset downloads consumed against subscription or credit pack.\n  unit: download\n  aggregation: sum\n  dimensions:\n  - collection\n  - asset_type\n- name: credit_packs\n  description: One-time credit pack purchases.\n  unit: pack\n  aggregation: sum\n  dimensions:\n  - pack_size\nprinciples:\n- name: Visibility\n  description: Pull download history from iStock dashboard or API.\n- name: Allocation\n\
  \  description: Allocate downloads to consuming brand/team.\n- name: Optimization\n  description: Choose subscription over credit packs when monthly cadence is steady; avoid Signature collection unless required.\n- name: Accountability\n  description: Creative team owns the iStock subscription.\nmaintainers:\n- FN: Kin Lane\n  email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/istock/refs/heads/main/finops/istock-finops.yml
sources:
- https://www.istockphoto.com/plans-and-pricing
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Stock Media
- Images
- Video
- Illustrations
- Royalty-Free
- Getty
- FinOps
- Cost Management
- FOCUS
---
