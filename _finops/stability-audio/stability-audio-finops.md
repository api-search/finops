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
  pricingCategory: Prepaid Credits + Per-Generation Usage
description: FOCUS-aligned FinOps view of Stable Audio. Stability runs a credit-based platform (1 credit = $0.01) shared across all developer-platform models. Stable Audio 2.5 generations are reported at $0.20 each (20 credits) regardless of duration. API Membership ($20/mo) bundles 6,000 credits.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Stability AI
  ProviderName: Stability AI
  PublisherName: Stability AI
  ServiceCategory: AI
  ServiceName: Stable Audio API
layout: finops
meters:
- aggregation: sum
  description: Stable Audio 2.5 generations (20 credits each = $0.20).
  dimensions:
  - account
  - model
  name: stable_audio_generations
  unit: generation
- aggregation: sum
  description: Prepaid credit purchases.
  dimensions:
  - account
  name: credits_purchased
  unit: USD
- aggregation: sum
  description: API Membership monthly fee ($20/month, 6,000 credits included).
  dimensions:
  - account
  name: api_membership
  unit: month
name: Stability Audio Finops
provider_name: Stability Audio
provider_slug: stability-audio
publisher_name: Stability AI
service_category: AI
slug: stability-audio-finops
source_filename: stability-audio-finops.yml
source_heading: FinOps Profile
source_url: https://platform.stability.ai/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Stability Audio\nproviderId: stability-audio\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: true\ntags:\n- AI\n- Audio\n- Music Generation\n- SFX\n- Stability\n- FinOps\n- Cost Management\n- FOCUS\ndescription: >-\n  FOCUS-aligned FinOps view of Stable Audio. Stability runs a credit-based platform\n  (1 credit = $0.01) shared across all developer-platform models. Stable Audio 2.5\n  generations are reported at $0.20 each (20 credits) regardless of duration. API\n  Membership ($20/mo) bundles 6,000 credits.\nnotes: Decide between PAYG credit packs and the $20/mo membership based on monthly Stable Audio call volume.\nsources:\n- https://platform.stability.ai/pricing\n- https://stability.ai/stable-audio\n- https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n\
  \  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Stability AI\nserviceCategory: AI\nbillingModel:\n  pricingCategory: Prepaid Credits + Per-Generation Usage\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n  - Usage\n  - Purchase\n  - Adjustment\nfocusColumns:\n  ServiceName: Stable Audio API\n  ServiceCategory: AI\n  ProviderName: Stability AI\n  PublisherName: Stability AI\n  InvoiceIssuerName: Stability AI\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n- name: stable_audio_generations\n  description: Stable Audio 2.5 generations (20 credits each = $0.20).\n  unit: generation\n  aggregation: sum\n  dimensions:\n  - account\n  - model\n- name: credits_purchased\n  description: Prepaid credit purchases.\n  unit: USD\n  aggregation: sum\n  dimensions:\n  - account\n- name: api_membership\n  description: API Membership monthly fee ($20/month, 6,000 credits included).\n  unit:\
  \ month\n  aggregation: sum\n  dimensions:\n  - account\nprinciples:\n- name: Visibility\n  description: Track per-call credit consumption in Stability platform billing dashboard.\n- name: Allocation\n  description: Tag generations per creative project / consuming product.\n- name: Optimization\n  description: At ~300+ generations/month consider $20 membership over PAYG to lock in ~3.3K credits effective rate.\n- name: Accountability\n  description: Assign a credit-budget owner per consuming product.\nmaintainers:\n- FN: Kin Lane\n  email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/stability-audio/refs/heads/main/finops/stability-audio-finops.yml
sources:
- https://platform.stability.ai/pricing
- https://stability.ai/stable-audio
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- AI
- Audio
- Music Generation
- SFX
- Stability
- FinOps
- Cost Management
- FOCUS
---
