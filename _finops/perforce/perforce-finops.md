---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: openapi.json
  format: json
  label: Perforce Helix Core API
  slug: perforce-helix-core-api
  spec_type: OpenAPI
  url: https://api.perforce.com/helix-core/openapi.json
- filename: perforce-helix-swarm-openapi.yml
  format: yaml
  label: Perforce Helix Swarm API
  slug: perforce-helix-swarm-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/perforce/refs/heads/main/openapi/perforce-helix-swarm-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  - Tax
  - Adjustment
  - Refund
  pricingCategory: Tiered Subscription
description: FOCUS-aligned FinOps for Perforce - per-user subscription model across the Helix / P4 product family with a published $39 per-user-per-month Cloud SKU and contact-sales tiers for Scale, Platform, and the broader portfolio. APIs are included with the product license rather than separately metered.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Perforce Software, Inc.
  PricingCategory: Subscription
  ProviderName: Perforce
  PublisherName: Perforce Software, Inc.
  ServiceCategory: Developer Tools
  ServiceName: Perforce
  ServiceSubcategory: Version Control
layout: finops
meters:
- aggregation: count
  description: Monthly per-user seat for the published P4 Cloud SKU ($39 per user per month).
  dimensions:
  - product
  - tenant
  name: p4_cloud_user_month
  unit: seat-month
- aggregation: count
  description: Annual per-user seat for self-hosted Helix Core (Free / Scale / Platform tiers).
  dimensions:
  - product
  - tier
  name: p4_self_hosted_user_year
  unit: seat-year
- aggregation: max
  description: Hosted Helix Core storage (64 GB included with Cloud; overage by upgrade / contact sales).
  dimensions:
  - tenant
  name: p4_cloud_storage
  unit: GB
- aggregation: count
  description: Per-user seat for Helix ALM (Issues / Test / Requirements). Quoted annually by sales.
  dimensions:
  - module
  name: helix_alm_user_year
  unit: seat-year
- aggregation: count
  description: Per-user seat for Hansoft Agile planning. Quoted annually by sales.
  dimensions:
  - team
  name: hansoft_user_year
  unit: seat-year
- aggregation: count
  description: Per-user seat for Helix TeamHub (Git collaboration). Quoted annually by sales.
  dimensions:
  - tenant
  name: teamhub_user_year
  unit: seat-year
- aggregation: count
  description: Per-user seat for P4 DAM (digital asset management). Bundled with Platform tier.
  dimensions:
  - tenant
  name: p4_dam_user_year
  unit: seat-year
name: Perforce Finops
provider_name: Perforce
provider_slug: perforce
publisher_name: Perforce Software, Inc.
service_category: Developer Tools
slug: perforce-finops
source_filename: perforce-finops.yml
source_heading: FinOps Profile
source_url: https://www.perforce.com/products/helix-core
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Perforce\nproviderId: perforce\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Version Control\n  - DevOps\n  - Application Lifecycle Management\ndescription: FOCUS-aligned FinOps for Perforce - per-user subscription model across the Helix /\n  P4 product family with a published $39 per-user-per-month Cloud SKU and contact-sales tiers for\n  Scale, Platform, and the broader portfolio. APIs are included with the product license rather\n  than separately metered.\nsources:\n  - https://www.perforce.com/products/helix-core\n  - https://www.perforce.com/resources/vcs/helix-core-pricing\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName:\
  \ Perforce Software, Inc.\nserviceCategory: Developer Tools\nbillingModel:\n  pricingCategory: Tiered Subscription\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Tax\n    - Adjustment\n    - Refund\nfocusColumns:\n  ServiceName: Perforce\n  ServiceCategory: Developer Tools\n  ServiceSubcategory: Version Control\n  ProviderName: Perforce\n  PublisherName: Perforce Software, Inc.\n  InvoiceIssuerName: Perforce Software, Inc.\n  BillingCurrency: USD\n  ChargeCategory: Purchase\n  PricingCategory: Subscription\nmeters:\n  - name: p4_cloud_user_month\n    description: Monthly per-user seat for the published P4 Cloud SKU ($39 per user per month).\n    unit: seat-month\n    aggregation: count\n    dimensions:\n      - product\n      - tenant\n  - name: p4_self_hosted_user_year\n    description: Annual per-user seat for self-hosted Helix Core (Free / Scale / Platform tiers).\n    unit: seat-year\n    aggregation: count\n    dimensions:\n      -\
  \ product\n      - tier\n  - name: p4_cloud_storage\n    description: Hosted Helix Core storage (64 GB included with Cloud; overage by upgrade /\n      contact sales).\n    unit: GB\n    aggregation: max\n    dimensions:\n      - tenant\n  - name: helix_alm_user_year\n    description: Per-user seat for Helix ALM (Issues / Test / Requirements). Quoted annually by\n      sales.\n    unit: seat-year\n    aggregation: count\n    dimensions:\n      - module\n  - name: hansoft_user_year\n    description: Per-user seat for Hansoft Agile planning. Quoted annually by sales.\n    unit: seat-year\n    aggregation: count\n    dimensions:\n      - team\n  - name: teamhub_user_year\n    description: Per-user seat for Helix TeamHub (Git collaboration). Quoted annually by sales.\n    unit: seat-year\n    aggregation: count\n    dimensions:\n      - tenant\n  - name: p4_dam_user_year\n    description: Per-user seat for P4 DAM (digital asset management). Bundled with Platform tier.\n    unit: seat-year\n\
  \    aggregation: count\n    dimensions:\n      - tenant\nprinciples:\n  - name: Visibility\n    description: Track named-user counts via each Perforce product's admin console (p4 users, Swarm\n      admin, Helix ALM admin); reconcile against the renewal SKU each year.\n  - name: Allocation\n    description: Allocate seats by tagging Perforce users to studios / business units in the user\n      directory or via Helix Authentication Service group claims; map game-studio or product-line\n      ownership to the renewal contract.\n  - name: Optimization\n    description: Move teams above 5 users from the Free tier to P4 Cloud (or self-host) before\n      hitting the 1000-file limit; consolidate Hansoft / Helix ALM / TeamHub renewals onto a\n      single Perforce contract for negotiation; right-size P4 Cloud storage to the 64 GB\n      included envelope.\n  - name: Accountability\n    description: Engineering / studio leadership owns the seat count per renewal; finance reviews\n      active-developer\
  \ counts against contracted seats annually before renewal.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n    url: https://apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/perforce/refs/heads/main/finops/perforce-finops.yml
sources:
- https://www.perforce.com/products/helix-core
- https://www.perforce.com/resources/vcs/helix-core-pricing
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Version Control
- DevOps
- Application Lifecycle Management
---
