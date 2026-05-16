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
  label: Mistral AI Chat API
  slug: mistral-ai-chat-api
  spec_type: OpenAPI
  url: https://docs.mistral.ai/openapi.json
- filename: mistral-embeddings-openapi.yml
  format: yaml
  label: Mistral Embeddings API
  slug: mistral-embeddings-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/mistral/refs/heads/main/openapi/mistral-embeddings-openapi.yml
- filename: mistral-moderation-openapi.yml
  format: yaml
  label: Mistral Moderation API
  slug: mistral-moderation-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/mistral/refs/heads/main/openapi/mistral-moderation-openapi.yml
- filename: mistral-agents-openapi.yml
  format: yaml
  label: Mistral AI Agents API
  slug: mistral-ai-agents-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/mistral/refs/heads/main/openapi/mistral-agents-openapi.yml
- filename: mistral-fim-openapi.yml
  format: yaml
  label: Mistral AI FIM API
  slug: mistral-ai-fim-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/mistral/refs/heads/main/openapi/mistral-fim-openapi.yml
- filename: mistral-ocr-openapi.yml
  format: yaml
  label: Mistral AI OCR API
  slug: mistral-ai-ocr-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/mistral/refs/heads/main/openapi/mistral-ocr-openapi.yml
- filename: mistral-fine-tuning-openapi.yml
  format: yaml
  label: Mistral AI Fine-Tuning API
  slug: mistral-ai-fine-tuning-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/mistral/refs/heads/main/openapi/mistral-fine-tuning-openapi.yml
- filename: mistral-files-openapi.yml
  format: yaml
  label: Mistral AI Files API
  slug: mistral-ai-files-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/mistral/refs/heads/main/openapi/mistral-files-openapi.yml
- filename: mistral-models-openapi.yml
  format: yaml
  label: Mistral AI Models API
  slug: mistral-ai-models-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/mistral/refs/heads/main/openapi/mistral-models-openapi.yml
- filename: mistral-batch-openapi.yml
  format: yaml
  label: Mistral AI Batch API
  slug: mistral-ai-batch-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/mistral/refs/heads/main/openapi/mistral-batch-openapi.yml
- filename: mistral-audio-transcription-openapi.yml
  format: yaml
  label: Mistral AI Audio Transcription API
  slug: mistral-ai-audio-transcription-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/mistral/refs/heads/main/openapi/mistral-audio-transcription-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  pricingCategory: Per-Token
description: FOCUS-aligned FinOps for Mistral AI.
focus_columns:
  BillingCurrency: USD
  ProviderName: Mistral AI
  PublisherName: Mistral AI
  ServiceCategory: AI and Machine Learning
  ServiceName: Mistral AI
layout: finops
meters:
- aggregation: sum
  dimensions:
  - model
  name: input_tokens
  unit: token
- aggregation: sum
  dimensions:
  - model
  name: output_tokens
  unit: token
- aggregation: sum
  name: embed_tokens
  unit: token
name: Mistral Finops
provider_name: Mistral AI
provider_slug: mistral
publisher_name: Mistral AI
service_category: AI and Machine Learning
slug: mistral-finops
source_filename: mistral-finops.yml
source_heading: FinOps Profile
source_url: https://mistral.ai/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Mistral AI\nproviderId: mistral\ncreated: '2026-05-04'\nmodified: '2026-05-04'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - AI and Machine Learning\ndescription: FOCUS-aligned FinOps for Mistral AI.\nsources:\n  - https://mistral.ai/pricing\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Mistral AI\nserviceCategory: AI and Machine Learning\nbillingModel:\n  pricingCategory: Per-Token\n  billingFrequency: Monthly\n  billingCurrency: USD\nfocusColumns:\n  ServiceName: Mistral AI\n  ServiceCategory: AI and Machine Learning\n  ProviderName: Mistral AI\n  PublisherName: Mistral AI\n  BillingCurrency: USD\nmeters:\n  - name: input_tokens\n    unit: token\n    aggregation: sum\n\
  \    dimensions:\n      - model\n  - name: output_tokens\n    unit: token\n    aggregation: sum\n    dimensions:\n      - model\n  - name: embed_tokens\n    unit: token\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Track Mistral AI consumption monthly via admin/billing exports.\n  - name: Allocation\n    description: Tag usage to teams or cost centers for chargeback.\n  - name: Optimization\n    description: Right-size models/tiers; use caching and batching.\n  - name: Accountability\n    description: Set hard spend limits; quarterly review.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/mistral/refs/heads/main/finops/mistral-finops.yml
sources:
- https://mistral.ai/pricing
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- AI and Machine Learning
---
