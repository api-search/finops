---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: resemble-ai-openapi.yml
  format: yaml
  label: Resemble AI Platform API
  slug: platform
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/resemble-ai/refs/heads/main/openapi/resemble-ai-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  - Adjustment
  pricingCategory: Usage-Based (Per Second) + Subscription Add-ons
description: FOCUS-aligned FinOps view of Resemble AI. Resemble bills per second across TTS, voice agents, STT, audio detection, and video detection, with monthly add-ons for team seats and voice clones. Enterprise volume discounts can reach 80%.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Resemble AI
  ProviderName: Resemble AI
  PublisherName: Resemble AI
  ServiceCategory: AI
  ServiceName: Resemble AI
layout: finops
meters:
- aggregation: sum
  description: Synthesized TTS audio at $0.0005/sec.
  dimensions:
  - account
  - voice
  name: tts_seconds
  unit: second
- aggregation: sum
  description: Voice agent runtime at $0.001/sec.
  dimensions:
  - account
  - agent
  name: voice_agent_seconds
  unit: second
- aggregation: sum
  description: Speech-to-Text at $0.001/sec.
  dimensions:
  - account
  name: stt_seconds
  unit: second
- aggregation: sum
  description: Audio deepfake detection at $0.001/sec.
  dimensions:
  - account
  name: audio_detection_seconds
  unit: second
- aggregation: sum
  description: Video deepfake detection at $0.07/sec.
  dimensions:
  - account
  name: video_detection_seconds
  unit: second
- aggregation: max
  description: Monthly voice clone fees ($2 rapid / $5 professional).
  dimensions:
  - account
  - clone_type
  name: voice_clone_subscriptions
  unit: voice-month
- aggregation: max
  description: Team seat add-on at $20/user/month.
  dimensions:
  - account
  name: team_seats
  unit: user-month
name: Resemble Ai Finops
provider_name: Resemble AI
provider_slug: resemble-ai
publisher_name: Resemble AI
service_category: AI
slug: resemble-ai-finops
source_filename: resemble-ai-finops.yml
source_heading: FinOps Profile
source_url: https://www.resemble.ai/pricing/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Resemble AI\nproviderId: resemble-ai\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: true\ntags:\n- AI\n- Voice\n- TTS\n- Voice Cloning\n- Audio\n- FinOps\n- Cost Management\n- FOCUS\ndescription: >-\n  FOCUS-aligned FinOps view of Resemble AI. Resemble bills per second across TTS, voice\n  agents, STT, audio detection, and video detection, with monthly add-ons for team seats\n  and voice clones. Enterprise volume discounts can reach 80%.\nnotes: Per-second billing aligns FinOps reporting cleanly to call duration; track each service meter independently.\nsources:\n- https://www.resemble.ai/pricing/\n- https://docs.resemble.ai/\n- https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\n\
  publisherName: Resemble AI\nserviceCategory: AI\nbillingModel:\n  pricingCategory: Usage-Based (Per Second) + Subscription Add-ons\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n  - Usage\n  - Purchase\n  - Adjustment\nfocusColumns:\n  ServiceName: Resemble AI\n  ServiceCategory: AI\n  ProviderName: Resemble AI\n  PublisherName: Resemble AI\n  InvoiceIssuerName: Resemble AI\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n- name: tts_seconds\n  description: Synthesized TTS audio at $0.0005/sec.\n  unit: second\n  aggregation: sum\n  dimensions:\n  - account\n  - voice\n- name: voice_agent_seconds\n  description: Voice agent runtime at $0.001/sec.\n  unit: second\n  aggregation: sum\n  dimensions:\n  - account\n  - agent\n- name: stt_seconds\n  description: Speech-to-Text at $0.001/sec.\n  unit: second\n  aggregation: sum\n  dimensions:\n  - account\n- name: audio_detection_seconds\n  description: Audio deepfake detection at $0.001/sec.\n  unit: second\n\
  \  aggregation: sum\n  dimensions:\n  - account\n- name: video_detection_seconds\n  description: Video deepfake detection at $0.07/sec.\n  unit: second\n  aggregation: sum\n  dimensions:\n  - account\n- name: voice_clone_subscriptions\n  description: Monthly voice clone fees ($2 rapid / $5 professional).\n  unit: voice-month\n  aggregation: max\n  dimensions:\n  - account\n  - clone_type\n- name: team_seats\n  description: Team seat add-on at $20/user/month.\n  unit: user-month\n  aggregation: max\n  dimensions:\n  - account\nprinciples:\n- name: Visibility\n  description: Per-service second-level billing aligns to call duration; pull from Resemble usage dashboard.\n- name: Allocation\n  description: Tag voices, agents, and detection workflows to consuming business units.\n- name: Optimization\n  description: Right-size voice clone count (rapid vs professional); enterprise contracts deliver up to 80% discount at volume.\n- name: Accountability\n  description: Assign budget owners per consuming\
  \ product (TTS, agents, detection).\nmaintainers:\n- FN: Kin Lane\n  email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/resemble-ai/refs/heads/main/finops/resemble-ai-finops.yml
sources:
- https://www.resemble.ai/pricing/
- https://docs.resemble.ai/
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- AI
- Voice
- TTS
- Voice Cloning
- Audio
- FinOps
- Cost Management
- FOCUS
---
