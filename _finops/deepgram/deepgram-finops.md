---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: deepgram-speech-to-text-openapi.yml
  format: yaml
  label: Deepgram Speech-To-Text API
  slug: speech-to-text-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/deepgram/refs/heads/main/openapi/deepgram-speech-to-text-openapi.yml
- filename: deepgram-text-to-speech-openapi.yml
  format: yaml
  label: Deepgram Text-To-Speech API
  slug: text-to-speech-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/deepgram/refs/heads/main/openapi/deepgram-text-to-speech-openapi.yml
- filename: deepgram-voice-agent-asyncapi.yml
  format: yaml
  label: Deepgram Voice Agent API
  slug: voice-agent-api
  spec_type: AsyncAPI
  url: https://raw.githubusercontent.com/api-evangelist/deepgram/refs/heads/main/asyncapi/deepgram-voice-agent-asyncapi.yml
- filename: deepgram-speech-to-text-openapi.yml
  format: yaml
  label: Deepgram Audio Intelligence API
  slug: audio-intelligence-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/deepgram/refs/heads/main/openapi/deepgram-speech-to-text-openapi.yml
- filename: deepgram-management-openapi.yml
  format: yaml
  label: Deepgram Management API
  slug: management-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/deepgram/refs/heads/main/openapi/deepgram-management-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  pricingCategory: Per-Minute / Per-Character
description: FOCUS-aligned FinOps for Deepgram.
focus_columns:
  BillingCurrency: USD
  ProviderName: Deepgram
  PublisherName: Deepgram
  ServiceCategory: Speech AI
  ServiceName: Deepgram
layout: finops
meters:
- aggregation: sum
  dimensions:
  - model
  - mode
  name: stt_minutes
  unit: minute
- aggregation: sum
  dimensions:
  - voice
  name: tts_characters
  unit: character
- aggregation: max
  name: concurrent_streams
  unit: stream
name: Deepgram Finops
provider_name: Deepgram
provider_slug: deepgram
publisher_name: Deepgram
service_category: Speech AI
slug: deepgram-finops
source_filename: deepgram-finops.yml
source_heading: FinOps Profile
source_url: https://deepgram.com/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Deepgram\nproviderId: deepgram\ncreated: '2026-05-04'\nmodified: '2026-05-04'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Speech AI\ndescription: FOCUS-aligned FinOps for Deepgram.\nsources:\n  - https://deepgram.com/pricing\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Deepgram\nserviceCategory: Speech AI\nbillingModel:\n  pricingCategory: Per-Minute / Per-Character\n  billingFrequency: Monthly\n  billingCurrency: USD\nfocusColumns:\n  ServiceName: Deepgram\n  ServiceCategory: Speech AI\n  ProviderName: Deepgram\n  PublisherName: Deepgram\n  BillingCurrency: USD\nmeters:\n  - name: stt_minutes\n    unit: minute\n    aggregation: sum\n    dimensions:\n      - model\n\
  \      - mode\n  - name: tts_characters\n    unit: character\n    aggregation: sum\n    dimensions:\n      - voice\n  - name: concurrent_streams\n    unit: stream\n    aggregation: max\nprinciples:\n  - name: Visibility\n    description: Track Deepgram consumption monthly via admin/billing exports.\n  - name: Allocation\n    description: Tag usage to teams or cost centers for chargeback.\n  - name: Optimization\n    description: Right-size models/tiers; use caching and batching.\n  - name: Accountability\n    description: Set hard spend limits; quarterly review.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/deepgram/refs/heads/main/finops/deepgram-finops.yml
sources:
- https://deepgram.com/pricing
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Speech AI
---
