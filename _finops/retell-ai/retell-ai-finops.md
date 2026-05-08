---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: retell-ai-openapi.yml
  format: yaml
  label: Retell AI Platform API
  slug: platform
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/retell-ai/refs/heads/main/openapi/retell-ai-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  - Adjustment
  pricingCategory: Usage-Based (Per Minute Components + Per Message)
description: 'FOCUS-aligned FinOps view of Retell AI. Retell uses a component-based per-minute model: Retell infrastructure fee plus pass-through TTS, LLM, and telephony charges. Chat agents are priced per message. Concurrent call slots over 20 are billed monthly at $8/slot.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Retell AI
  ProviderName: Retell AI
  PublisherName: Retell AI
  ServiceCategory: AI
  ServiceName: Retell AI Voice and Chat Agents
layout: finops
meters:
- aggregation: sum
  description: Retell platform per-minute fee (~$0.055/min).
  dimensions:
  - account
  - call_id
  name: voice_infrastructure_minutes
  unit: minute
- aggregation: sum
  description: Pass-through TTS cost per minute.
  dimensions:
  - account
  - voice_provider
  name: tts_minutes
  unit: minute
- aggregation: sum
  description: Pass-through LLM cost per minute.
  dimensions:
  - account
  - model
  name: llm_minutes
  unit: minute
- aggregation: sum
  description: Pass-through telephony cost per minute.
  dimensions:
  - account
  - country
  name: telephony_minutes
  unit: minute
- aggregation: sum
  description: Per-message charge for chat agent usage.
  dimensions:
  - account
  - chat_agent
  name: chat_messages
  unit: message
- aggregation: sum
  description: Monthly fee for additional concurrent call slots beyond the included 20.
  dimensions:
  - account
  name: concurrency_slots
  unit: slot-month
name: Retell Ai Finops
provider_name: Retell AI
provider_slug: retell-ai
publisher_name: Retell AI
service_category: AI
slug: retell-ai-finops
source_filename: retell-ai-finops.yml
source_heading: FinOps Profile
source_url: https://www.retellai.com/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Retell AI\nproviderId: retell-ai\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: true\ntags:\n- AI\n- Voice\n- Agents\n- Realtime\n- Conversational\n- FinOps\n- Cost Management\n- FOCUS\ndescription: >-\n  FOCUS-aligned FinOps view of Retell AI. Retell uses a component-based per-minute model:\n  Retell infrastructure fee plus pass-through TTS, LLM, and telephony charges. Chat agents\n  are priced per message. Concurrent call slots over 20 are billed monthly at $8/slot.\nnotes: Choice of LLM and TTS provider materially changes per-minute cost; FinOps optimization usually centers on those.\nsources:\n- https://www.retellai.com/pricing\n- https://docs.retellai.com/\n- https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion:\
  \ '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Retell AI\nserviceCategory: AI\nbillingModel:\n  pricingCategory: Usage-Based (Per Minute Components + Per Message)\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n  - Usage\n  - Purchase\n  - Adjustment\nfocusColumns:\n  ServiceName: Retell AI Voice and Chat Agents\n  ServiceCategory: AI\n  ProviderName: Retell AI\n  PublisherName: Retell AI\n  InvoiceIssuerName: Retell AI\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n- name: voice_infrastructure_minutes\n  description: Retell platform per-minute fee (~$0.055/min).\n  unit: minute\n  aggregation: sum\n  dimensions:\n  - account\n  - call_id\n- name: tts_minutes\n  description: Pass-through TTS cost per minute.\n  unit: minute\n  aggregation: sum\n  dimensions:\n  - account\n  - voice_provider\n- name: llm_minutes\n  description: Pass-through LLM cost per minute.\n  unit: minute\n  aggregation: sum\n  dimensions:\n\
  \  - account\n  - model\n- name: telephony_minutes\n  description: Pass-through telephony cost per minute.\n  unit: minute\n  aggregation: sum\n  dimensions:\n  - account\n  - country\n- name: chat_messages\n  description: Per-message charge for chat agent usage.\n  unit: message\n  aggregation: sum\n  dimensions:\n  - account\n  - chat_agent\n- name: concurrency_slots\n  description: Monthly fee for additional concurrent call slots beyond the included 20.\n  unit: slot-month\n  aggregation: sum\n  dimensions:\n  - account\nprinciples:\n- name: Visibility\n  description: Use Retell call analytics and per-call cost breakdowns (product_costs, combined_cost) returned by the API.\n- name: Allocation\n  description: Tag agents and phone numbers to business units to allocate per-call cost.\n- name: Optimization\n  description: Switch LLM models and TTS voices to control cost per minute; right-size concurrency slot purchases.\n- name: Accountability\n  description: Assign owners for each component\
  \ vendor (TTS, LLM, telephony) since pricing flows through.\nmaintainers:\n- FN: Kin Lane\n  email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/retell-ai/refs/heads/main/finops/retell-ai-finops.yml
sources:
- https://www.retellai.com/pricing
- https://docs.retellai.com/
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- AI
- Voice
- Agents
- Realtime
- Conversational
- FinOps
- Cost Management
- FOCUS
---
