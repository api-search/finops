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
  pricingCategory: Usage
description: FOCUS-aligned FinOps profile for Daily. Daily's billing is consumption-based on participant-minutes (Video SDK), agent runtime minutes (Pipecat Cloud) and underlying WebRTC infrastructure usage; bills are invoiced monthly in USD.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Daily
  PricingUnit: participant-minute
  ProviderName: Daily
  PublisherName: Daily
  ServiceCategory: Realtime Communications
  ServiceName: Daily Video SDK
layout: finops
meters:
- aggregation: sum
  description: Participant-minutes consumed in Daily rooms (primary Video SDK meter).
  dimensions:
  - account
  - room
  - meeting
  name: participant_minutes
  unit: minute
- aggregation: sum
  description: Cloud recording minutes generated.
  dimensions:
  - account
  - room
  name: recording_minutes
  unit: minute
- aggregation: sum
  description: Speech-to-text transcription minutes generated.
  dimensions:
  - account
  - room
  name: transcription_minutes
  unit: minute
- aggregation: sum
  description: Voice-AI agent runtime minutes on Pipecat Cloud.
  dimensions:
  - account
  - agent
  name: pipecat_agent_minutes
  unit: minute
- aggregation: sum
  description: PSTN/SIP dial-out minutes (separately metered).
  dimensions:
  - account
  - destination
  name: dial_out_minutes
  unit: minute
name: Daily Co Finops
provider_name: Daily
provider_slug: daily-co
publisher_name: Daily
service_category: Realtime Communications
slug: daily-co-finops
source_filename: daily-co-finops.yml
source_heading: FinOps Profile
source_url: https://www.daily.co/pricing/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Daily\nproviderId: daily-co\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: true\ntags:\n- Realtime\n- WebRTC\n- Video\n- Audio\n- SDK\n- FinOps\n- Cost Management\n- FOCUS\ndescription: >-\n  FOCUS-aligned FinOps profile for Daily. Daily's billing is consumption-based on\n  participant-minutes (Video SDK), agent runtime minutes (Pipecat Cloud) and\n  underlying WebRTC infrastructure usage; bills are invoiced monthly in USD.\nnotes: >-\n  Daily exposes per-room and per-meeting analytics via the REST API\n  (/meetings, /meetings/:meeting/participants), which can be used to allocate\n  participant-minute consumption back to internal cost centers.\nsources:\n- https://www.daily.co/pricing/\n- https://docs.daily.co/reference/rest-api/meetings\n- https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n\
  \  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Daily\nserviceCategory: Realtime Communications\nbillingModel:\n  pricingCategory: Usage\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n  - Usage\n  - Purchase\n  - Adjustment\nfocusColumns:\n  ServiceName: Daily Video SDK\n  ServiceCategory: Realtime Communications\n  ProviderName: Daily\n  PublisherName: Daily\n  InvoiceIssuerName: Daily\n  BillingCurrency: USD\n  ChargeCategory: Usage\n  PricingUnit: participant-minute\nmeters:\n- name: participant_minutes\n  description: Participant-minutes consumed in Daily rooms (primary Video SDK meter).\n  unit: minute\n  aggregation: sum\n  dimensions:\n  - account\n  - room\n  - meeting\n- name: recording_minutes\n  description: Cloud recording minutes generated.\n  unit: minute\n  aggregation: sum\n  dimensions:\n  - account\n  - room\n-\
  \ name: transcription_minutes\n  description: Speech-to-text transcription minutes generated.\n  unit: minute\n  aggregation: sum\n  dimensions:\n  - account\n  - room\n- name: pipecat_agent_minutes\n  description: Voice-AI agent runtime minutes on Pipecat Cloud.\n  unit: minute\n  aggregation: sum\n  dimensions:\n  - account\n  - agent\n- name: dial_out_minutes\n  description: PSTN/SIP dial-out minutes (separately metered).\n  unit: minute\n  aggregation: sum\n  dimensions:\n  - account\n  - destination\nprinciples:\n- name: Visibility\n  description: Use /meetings and /meetings/:meeting/participants to pull near-real-time minute consumption.\n- name: Allocation\n  description: Tag rooms with cost-center identifiers in their name or metadata to allocate participant-minutes downstream.\n- name: Optimization\n  description: Right-size recording (cloud-recording vs. raw-tracks) and disable transcription when not needed; negotiate volume discounts above sustained monthly minute thresholds.\n\
  - name: Accountability\n  description: Assign owners per top-level domain/sub-account; review monthly invoices against /meetings analytics.\nmaintainers:\n- FN: Kin Lane\n  email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/daily-co/refs/heads/main/finops/daily-co-finops.yml
sources:
- https://www.daily.co/pricing/
- https://docs.daily.co/reference/rest-api/meetings
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Realtime
- WebRTC
- Video
- Audio
- SDK
- FinOps
- Cost Management
- FOCUS
---
