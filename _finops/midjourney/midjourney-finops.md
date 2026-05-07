---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: midjourney-image-generation-openapi.yml
  format: yaml
  label: Midjourney Image Generation API
  slug: image-generation-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/midjourney/refs/heads/main/openapi/midjourney-image-generation-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Purchase
  - Tax
  - Adjustment
  pricingCategory: Tiered Subscription
description: 'FOCUS-aligned FinOps for Midjourney: tiered consumer subscription billed monthly (or annually at a discount) with implicit Fast GPU-minute budgets per tier. There is no usage-based meter exposed to customers beyond the included entitlement.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Midjourney, Inc.
  PricingUnit: seat-month
  ProviderName: Midjourney
  PublisherName: Midjourney, Inc.
  ServiceCategory: AI Infrastructure
  ServiceName: Midjourney
  ServiceSubcategory: Image Generation
layout: finops
meters:
- aggregation: sum
  dimensions:
  - tier
  - billing_cadence
  name: subscription_seats
  unit: seat-month
- aggregation: sum
  dimensions:
  - account
  - tier
  name: fast_gpu_minutes_consumed
  unit: gpu-minute
- aggregation: sum
  dimensions:
  - account
  - tier
  name: relax_gpu_minutes_consumed
  unit: gpu-minute
- aggregation: sum
  dimensions:
  - account
  name: fast_topup_purchases
  unit: gpu-minute
name: Midjourney Finops
provider_name: midjourney
provider_slug: midjourney
publisher_name: Midjourney, Inc.
service_category: AI / Image Generation
slug: midjourney-finops
source_filename: midjourney-finops.yml
source_heading: FinOps Profile
source_url: https://docs.midjourney.com
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Midjourney\nproviderId: midjourney\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Cost Management\n  - AI\n  - Image Generation\ndescription: 'FOCUS-aligned FinOps for Midjourney: tiered consumer subscription billed monthly (or\n  annually at a discount) with implicit Fast GPU-minute budgets per tier. There is no usage-based meter\n  exposed to customers beyond the included entitlement.'\nsources:\n  - https://docs.midjourney.com\nnotes: docs.midjourney.com refused automated fetches (403). Reconciliation deferred — confirm tier\n  prices and Fast GPU minute allotments from the live page.\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName:\
  \ Midjourney, Inc.\nserviceCategory: AI / Image Generation\nbillingModel:\n  pricingCategory: Tiered Subscription\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Tax\n    - Adjustment\nfocusColumns:\n  ServiceName: Midjourney\n  ServiceCategory: AI Infrastructure\n  ServiceSubcategory: Image Generation\n  ProviderName: Midjourney\n  PublisherName: Midjourney, Inc.\n  InvoiceIssuerName: Midjourney, Inc.\n  BillingCurrency: USD\n  PricingUnit: seat-month\n  ChargeCategory: Purchase\nmeters:\n  - name: subscription_seats\n    unit: seat-month\n    aggregation: sum\n    dimensions:\n      - tier\n      - billing_cadence\n  - name: fast_gpu_minutes_consumed\n    unit: gpu-minute\n    aggregation: sum\n    dimensions:\n      - account\n      - tier\n  - name: relax_gpu_minutes_consumed\n    unit: gpu-minute\n    aggregation: sum\n    dimensions:\n      - account\n      - tier\n  - name: fast_topup_purchases\n    unit: gpu-minute\n    aggregation:\
  \ sum\n    dimensions:\n      - account\nprinciples:\n  - name: Visibility\n    description: Track Fast GPU minutes consumed via the Midjourney account info command (e.g.\n      /info on Discord); inspect monthly invoice for tier and any Fast top-up purchases.\n  - name: Allocation\n    description: Allocate seats by user/team; Stealth-mode usage may indicate an enterprise / brand\n      project worth tagging separately for chargeback.\n  - name: Optimization\n    description: Move heavy users to higher tiers (better $/minute) before paying top-ups; rely on\n      Relax mode for non-urgent ideation; downgrade when Fast minutes consistently underused.\n  - name: Accountability\n    description: Designate a creative-team owner per seat; review monthly Fast-minute usage versus\n      tier entitlement.\nmaintainers: []\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/midjourney/refs/heads/main/finops/midjourney-finops.yml
sources:
- https://docs.midjourney.com
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Cost Management
- AI
- Image Generation
---
