---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: vapi-openapi.yml
  format: yaml
  label: Vapi Platform API
  slug: platform
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/vapi/refs/heads/main/openapi/vapi-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  - Adjustment
  pricingCategory: Usage-Based (Per Minute)
description: FOCUS-aligned FinOps view of Vapi. Vapi's billing model is consumption-based per minute of voice agent runtime, with pass-through component costs for transcription, LLM, TTS, and telephony. Total cost ownership requires tracking each provider in the stack.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Vapi
  ProviderName: Vapi
  PublisherName: Vapi
  ServiceCategory: AI
  ServiceName: Vapi Voice AI Platform
layout: finops
meters:
- aggregation: sum
  description: Per-minute platform fee for voice agent runtime.
  dimensions:
  - account
  - assistant
  - call
  name: voice_minutes
  unit: minute
- aggregation: sum
  description: Pass-through telephony charges for inbound/outbound PSTN calls.
  dimensions:
  - account
  - phone_number
  name: telephony_minutes
  unit: minute
- aggregation: sum
  description: Pass-through STT cost for voice transcription.
  dimensions:
  - account
  - provider
  name: transcription_minutes
  unit: minute
- aggregation: sum
  description: Pass-through TTS cost for synthesized voice output.
  dimensions:
  - account
  - voice_provider
  name: tts_minutes
  unit: minute
- aggregation: sum
  description: Pass-through LLM token cost for assistant reasoning.
  dimensions:
  - account
  - model
  name: llm_tokens
  unit: token
name: Vapi Finops
provider_name: Vapi
provider_slug: vapi
publisher_name: Vapi
service_category: AI
slug: vapi-finops
source_filename: vapi-finops.yml
source_heading: FinOps Profile
source_url: https://vapi.ai/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Vapi\nproviderId: vapi\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: true\ntags:\n- AI\n- Voice\n- Agents\n- Realtime\n- CPaaS\n- FinOps\n- Cost Management\n- FOCUS\ndescription: >-\n  FOCUS-aligned FinOps view of Vapi. Vapi's billing model is consumption-based per minute of\n  voice agent runtime, with pass-through component costs for transcription, LLM, TTS, and\n  telephony. Total cost ownership requires tracking each provider in the stack.\nnotes: Cost optimization on Vapi often means rightsizing the LLM/voice provider stack rather than the Vapi platform fee itself.\nsources:\n- https://vapi.ai/pricing\n- https://docs.vapi.ai/\n- https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl:\
  \ https://focus.finops.org/focus-specification/v1-3/\npublisherName: Vapi\nserviceCategory: AI\nbillingModel:\n  pricingCategory: Usage-Based (Per Minute)\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n  - Usage\n  - Purchase\n  - Adjustment\nfocusColumns:\n  ServiceName: Vapi Voice AI Platform\n  ServiceCategory: AI\n  ProviderName: Vapi\n  PublisherName: Vapi\n  InvoiceIssuerName: Vapi\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n- name: voice_minutes\n  description: Per-minute platform fee for voice agent runtime.\n  unit: minute\n  aggregation: sum\n  dimensions:\n  - account\n  - assistant\n  - call\n- name: telephony_minutes\n  description: Pass-through telephony charges for inbound/outbound PSTN calls.\n  unit: minute\n  aggregation: sum\n  dimensions:\n  - account\n  - phone_number\n- name: transcription_minutes\n  description: Pass-through STT cost for voice transcription.\n  unit: minute\n  aggregation: sum\n  dimensions:\n  - account\n\
  \  - provider\n- name: tts_minutes\n  description: Pass-through TTS cost for synthesized voice output.\n  unit: minute\n  aggregation: sum\n  dimensions:\n  - account\n  - voice_provider\n- name: llm_tokens\n  description: Pass-through LLM token cost for assistant reasoning.\n  unit: token\n  aggregation: sum\n  dimensions:\n  - account\n  - model\nprinciples:\n- name: Visibility\n  description: Use Vapi call analytics plus underlying provider invoices to assemble total cost per call.\n- name: Allocation\n  description: Tag assistants and phone numbers to business units so call charges can be split in your FinOps store.\n- name: Optimization\n  description: Cheaper LLM and TTS providers usually drive far more savings than negotiating the Vapi platform fee.\n- name: Accountability\n  description: Assign owners for each component vendor (LLM, STT, TTS, telephony) since Vapi pass-through pricing depends on those contracts.\nmaintainers:\n- FN: Kin Lane\n  email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/vapi/refs/heads/main/finops/vapi-finops.yml
sources:
- https://vapi.ai/pricing
- https://docs.vapi.ai/
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- AI
- Voice
- Agents
- Realtime
- CPaaS
- FinOps
- Cost Management
- FOCUS
---
