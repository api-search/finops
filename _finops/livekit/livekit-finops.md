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
  - Subscription
  - Usage
  - Adjustment
  pricingCategory: Subscription + Usage
description: FinOps view of LiveKit Cloud. Usage-based billing with multiple meters - realtime media (per-minute connection time and per-GB data), Agent session minutes, Inference (STT seconds, LLM tokens, TTS characters), and SIP (per inbound minute + monthly per number rental). Each resource is rounded up to the minimum increment.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: LiveKit
  ProviderName: LiveKit
  PublisherName: LiveKit
  ServiceCategory: Realtime Infrastructure
  ServiceName: LiveKit Cloud
layout: finops
meters:
- aggregation: sum
  description: Per-minute participant connection time.
  dimensions:
  - project
  - room
  name: connection_minutes
  unit: minute
- aggregation: sum
  description: Per-GB media and signaling data transfer.
  dimensions:
  - project
  name: data_gb
  unit: gb
- aggregation: sum
  description: Per-minute agent session time.
  dimensions:
  - project
  - agent
  name: agent_session_minutes
  unit: minute
- aggregation: sum
  description: STT inference seconds.
  dimensions:
  - project
  name: stt_seconds
  unit: second
- aggregation: sum
  description: LLM input/output tokens billed via Inference.
  dimensions:
  - project
  - model
  name: llm_tokens
  unit: token
- aggregation: sum
  description: TTS character count.
  dimensions:
  - project
  name: tts_characters
  unit: character
- aggregation: sum
  description: SIP inbound call minutes.
  dimensions:
  - project
  - phone_number
  name: sip_inbound_minutes
  unit: minute
- aggregation: sum
  description: Monthly phone number rental.
  dimensions:
  - project
  - phone_number
  name: phone_number_rental
  unit: month
name: Livekit Finops
provider_name: LiveKit
provider_slug: livekit
publisher_name: LiveKit
service_category: Realtime Infrastructure
slug: livekit-finops
source_filename: livekit-finops.yml
source_heading: FinOps Profile
source_url: https://livekit.io/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: LiveKit\nproviderId: livekit\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: true\ntags:\n  - Realtime\n  - WebRTC\n  - FinOps\n  - FOCUS\ndescription: >-\n  FinOps view of LiveKit Cloud. Usage-based billing with multiple meters - realtime media\n  (per-minute connection time and per-GB data), Agent session minutes, Inference (STT seconds,\n  LLM tokens, TTS characters), and SIP (per inbound minute + monthly per number rental). Each\n  resource is rounded up to the minimum increment.\nsources:\n  - https://livekit.io/pricing\n  - https://docs.livekit.io/home/cloud/billing/\n  - https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName:\
  \ LiveKit\nserviceCategory: Realtime Infrastructure\nbillingModel:\n  pricingCategory: Subscription + Usage\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Subscription\n    - Usage\n    - Adjustment\nfocusColumns:\n  ServiceName: LiveKit Cloud\n  ServiceCategory: Realtime Infrastructure\n  ProviderName: LiveKit\n  PublisherName: LiveKit\n  InvoiceIssuerName: LiveKit\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: connection_minutes\n    description: Per-minute participant connection time.\n    unit: minute\n    aggregation: sum\n    dimensions:\n      - project\n      - room\n  - name: data_gb\n    description: Per-GB media and signaling data transfer.\n    unit: gb\n    aggregation: sum\n    dimensions:\n      - project\n  - name: agent_session_minutes\n    description: Per-minute agent session time.\n    unit: minute\n    aggregation: sum\n    dimensions:\n      - project\n      - agent\n  - name: stt_seconds\n    description: STT\
  \ inference seconds.\n    unit: second\n    aggregation: sum\n    dimensions:\n      - project\n  - name: llm_tokens\n    description: LLM input/output tokens billed via Inference.\n    unit: token\n    aggregation: sum\n    dimensions:\n      - project\n      - model\n  - name: tts_characters\n    description: TTS character count.\n    unit: character\n    aggregation: sum\n    dimensions:\n      - project\n  - name: sip_inbound_minutes\n    description: SIP inbound call minutes.\n    unit: minute\n    aggregation: sum\n    dimensions:\n      - project\n      - phone_number\n  - name: phone_number_rental\n    description: Monthly phone number rental.\n    unit: month\n    aggregation: sum\n    dimensions:\n      - project\n      - phone_number\nprinciples:\n  - name: Visibility\n    description: Pull LiveKit usage exports into FinOps store; tag by project and room.\n  - name: Allocation\n    description: Allocate connection-minute and Inference cost to consuming product.\n  - name: Optimization\n\
  \    description: Choose lower-cost STT/TTS providers via Inference; close idle rooms; right-size Agents concurrency.\n  - name: Accountability\n    description: Assign a billing owner per project; review monthly.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/livekit/refs/heads/main/finops/livekit-finops.yml
sources:
- https://livekit.io/pricing
- https://docs.livekit.io/home/cloud/billing/
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Realtime
- WebRTC
- FinOps
- FOCUS
---
