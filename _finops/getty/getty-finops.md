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
  label: Getty Images API
  slug: platform
  spec_type: OpenAPI
  url: https://api.gettyimages.com/swagger
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Subscription
  - Purchase
  pricingCategory: Subscription + Per-Asset
description: FOCUS-aligned FinOps profile for Getty Images. Cost driver is the licensing contract — typically annual subscription packs plus per-asset downloads outside the pack. The API does not bill calls; downloads consume entitlements. Optimize at renewal by aligning pack size to download volume and consolidating with iStock (same parent) where applicable.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Subscription
  InvoiceIssuerName: Getty Images
  ProviderName: Getty Images
  PublisherName: Getty Images
  ServiceCategory: Stock Media
  ServiceName: Getty Images API
layout: finops
meters:
- aggregation: sum
  description: Number of asset downloads consumed against entitlement.
  dimensions:
  - asset_type
  - license
  name: asset_downloads
  unit: download
- aggregation: max
  description: Annual subscription pack purchase.
  dimensions:
  - pack_type
  name: subscription_pack
  unit: year
name: Getty Finops
provider_name: Getty Images
provider_slug: getty
publisher_name: Getty Images
service_category: Stock Media Licensing
slug: getty-finops
source_filename: getty-finops.yml
source_heading: FinOps Profile
source_url: https://www.gettyimages.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Getty Images\nproviderId: getty\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: true\ntags:\n- Stock Media\n- Images\n- Editorial\n- Video\n- Music\n- Licensing\n- FinOps\n- Cost Management\n- FOCUS\ndescription: >-\n  FOCUS-aligned FinOps profile for Getty Images. Cost driver is the licensing contract — typically\n  annual subscription packs plus per-asset downloads outside the pack. The API does not bill calls;\n  downloads consume entitlements. Optimize at renewal by aligning pack size to download volume and\n  consolidating with iStock (same parent) where applicable.\nnotes: Annual contract; download volume drives optimization. iStock and Getty share entitlement infrastructure.\nsources:\n- https://www.gettyimages.com/\n- https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n\
  \  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Getty Images\nserviceCategory: Stock Media Licensing\nbillingModel:\n  pricingCategory: Subscription + Per-Asset\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n  - Subscription\n  - Purchase\nfocusColumns:\n  ServiceName: Getty Images API\n  ServiceCategory: Stock Media\n  ProviderName: Getty Images\n  PublisherName: Getty Images\n  InvoiceIssuerName: Getty Images\n  BillingCurrency: USD\n  ChargeCategory: Subscription\nmeters:\n- name: asset_downloads\n  description: Number of asset downloads consumed against entitlement.\n  unit: download\n  aggregation: sum\n  dimensions:\n  - asset_type\n  - license\n- name: subscription_pack\n  description: Annual subscription pack purchase.\n  unit: year\n  aggregation: max\n  dimensions:\n  - pack_type\nprinciples:\n- name: Visibility\n  description: Pull download reports monthly; reconcile against\
  \ entitlement.\n- name: Allocation\n  description: Allocate downloads to consuming brand/team.\n- name: Optimization\n  description: Right-size pack size at renewal; favor royalty-free over rights-managed where rights allow.\n- name: Accountability\n  description: Brand or creative-ops team owns the license and reconciliation.\nmaintainers:\n- FN: Kin Lane\n  email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/getty/refs/heads/main/finops/getty-finops.yml
sources:
- https://www.gettyimages.com/
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Stock Media
- Images
- Editorial
- Video
- Music
- Licensing
- FinOps
- Cost Management
- FOCUS
---
