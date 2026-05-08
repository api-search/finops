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
  pricingCategory: Subscription + Usage (Per Minute)
description: FOCUS-aligned FinOps view of Bland AI. Bland bills a flat per-minute talk-time rate that bundles LLM, STT, TTS, and telephony costs, plus an optional monthly platform fee for paid tiers and per-minute transfer fees. Voice clones, knowledge bases, and concurrent call slots are capacity entitlements gated by plan.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Bland AI
  ProviderName: Bland AI
  PublisherName: Bland AI
  ServiceCategory: AI
  ServiceName: Bland AI Voice Agent Platform
layout: finops
meters:
- aggregation: sum
  description: Per-minute charge for AI voice agent talk time (bundles LLM/STT/TTS/telephony).
  dimensions:
  - account
  - call_id
  name: talk_time_minutes
  unit: minute
- aggregation: sum
  description: Per-minute charge applied while a call is transferred to a human agent.
  dimensions:
  - account
  - call_id
  name: transfer_minutes
  unit: minute
- aggregation: sum
  description: Monthly platform fee for paid tiers (Build, Scale).
  dimensions:
  - account
  - plan
  name: platform_fee
  unit: month
name: Bland Ai Finops
provider_name: Bland AI
provider_slug: bland-ai
publisher_name: Bland AI
service_category: AI
slug: bland-ai-finops
source_filename: bland-ai-finops.yml
source_heading: FinOps Profile
source_url: https://www.bland.ai/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Bland AI\nproviderId: bland-ai\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: true\ntags:\n- AI\n- Voice\n- Agents\n- Phone\n- Realtime\n- FinOps\n- Cost Management\n- FOCUS\ndescription: >-\n  FOCUS-aligned FinOps view of Bland AI. Bland bills a flat per-minute talk-time rate that\n  bundles LLM, STT, TTS, and telephony costs, plus an optional monthly platform fee for paid\n  tiers and per-minute transfer fees. Voice clones, knowledge bases, and concurrent call slots\n  are capacity entitlements gated by plan.\nnotes: Bland's \"flat per-minute\" model removes the multi-vendor cost stack typical of voice AI; FinOps focus shifts to plan-tier sizing.\nsources:\n- https://www.bland.ai/pricing\n- https://docs.bland.ai/\n- https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n\
  \  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Bland AI\nserviceCategory: AI\nbillingModel:\n  pricingCategory: Subscription + Usage (Per Minute)\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n  - Usage\n  - Purchase\n  - Adjustment\nfocusColumns:\n  ServiceName: Bland AI Voice Agent Platform\n  ServiceCategory: AI\n  ProviderName: Bland AI\n  PublisherName: Bland AI\n  InvoiceIssuerName: Bland AI\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n- name: talk_time_minutes\n  description: Per-minute charge for AI voice agent talk time (bundles LLM/STT/TTS/telephony).\n  unit: minute\n  aggregation: sum\n  dimensions:\n  - account\n  - call_id\n- name: transfer_minutes\n  description: Per-minute charge applied while a call is transferred to a human agent.\n  unit: minute\n  aggregation: sum\n  dimensions:\n  - account\n  - call_id\n- name: platform_fee\n  description: Monthly\
  \ platform fee for paid tiers (Build, Scale).\n  unit: month\n  aggregation: sum\n  dimensions:\n  - account\n  - plan\nprinciples:\n- name: Visibility\n  description: Use Bland's call analytics dashboard plus monthly invoice line items.\n- name: Allocation\n  description: Tag pathways and phone numbers to business units to allocate per-minute spend.\n- name: Optimization\n  description: Right-size the plan tier (Start vs Build vs Scale) based on actual concurrency and daily call volume.\n- name: Accountability\n  description: Assign a plan owner to monitor monthly burn against tier caps and trigger upgrades.\nmaintainers:\n- FN: Kin Lane\n  email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/bland-ai/refs/heads/main/finops/bland-ai-finops.yml
sources:
- https://www.bland.ai/pricing
- https://docs.bland.ai/
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- AI
- Voice
- Agents
- Phone
- Realtime
- FinOps
- Cost Management
- FOCUS
---
