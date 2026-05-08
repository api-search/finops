---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD/CNY
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  - Adjustment
  pricingCategory: Usage Based (Tiered Context)
description: FOCUS-aligned FinOps profile for Qwen via Alibaba Cloud Model Studio (DashScope). Pay-as-you-go per-token pricing tiered by context-length window, billed alongside Alibaba Cloud account. International USD vs. mainland-China CNY pricing differ.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Alibaba Cloud
  ProviderName: Alibaba Cloud
  PublisherName: Alibaba Cloud
  ServiceCategory: AI and Machine Learning
  ServiceName: Alibaba Cloud Model Studio (DashScope)
layout: finops
meters:
- aggregation: sum
  description: Input tokens 0-32K context window.
  dimensions:
  - model
  - region
  - account
  name: input_tokens_tier1
  unit: tokens
- aggregation: sum
  description: Input tokens 32-128K context window.
  dimensions:
  - model
  - region
  - account
  name: input_tokens_tier2
  unit: tokens
- aggregation: sum
  description: Input tokens 128K-1M context window.
  dimensions:
  - model
  - region
  - account
  name: input_tokens_tier3
  unit: tokens
- aggregation: sum
  description: Output tokens billed by tier.
  dimensions:
  - model
  - region
  - account
  name: output_tokens
  unit: tokens
- aggregation: sum
  description: Image generation calls.
  dimensions:
  - model
  - account
  name: image_generations
  unit: images
- aggregation: sum
  description: Video generation calls.
  dimensions:
  - model
  - account
  name: video_generations
  unit: videos
- aggregation: sum
  description: TTS/ASR seconds.
  dimensions:
  - model
  - account
  name: audio_seconds
  unit: seconds
name: Qwen Finops
provider_name: Qwen
provider_slug: qwen
publisher_name: Alibaba Cloud
service_category: AI and Machine Learning
slug: qwen-finops
source_filename: qwen-finops.yml
source_heading: FinOps Profile
source_url: https://www.alibabacloud.com/help/en/model-studio/models
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Qwen\nproviderId: qwen\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: true\ntags:\n- AI\n- LLM\n- Alibaba\n- FinOps\n- FOCUS\ndescription: >-\n  FOCUS-aligned FinOps profile for Qwen via Alibaba Cloud Model Studio (DashScope). Pay-as-you-go\n  per-token pricing tiered by context-length window, billed alongside Alibaba Cloud account.\n  International USD vs. mainland-China CNY pricing differ.\nnotes: >-\n  Spend appears on the Alibaba Cloud invoice under Model Studio / DashScope SKUs. Free\n  self-hosting option exists for open-weight Qwen variants.\nsources:\n- https://www.alibabacloud.com/help/en/model-studio/models\n- https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\n\
  publisherName: Alibaba Cloud\nserviceCategory: AI and Machine Learning\nbillingModel:\n  pricingCategory: Usage Based (Tiered Context)\n  billingFrequency: Monthly\n  billingCurrency: USD/CNY\n  chargeCategories:\n  - Usage\n  - Purchase\n  - Adjustment\nfocusColumns:\n  ServiceName: Alibaba Cloud Model Studio (DashScope)\n  ServiceCategory: AI and Machine Learning\n  ProviderName: Alibaba Cloud\n  PublisherName: Alibaba Cloud\n  InvoiceIssuerName: Alibaba Cloud\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n- name: input_tokens_tier1\n  description: Input tokens 0-32K context window.\n  unit: tokens\n  aggregation: sum\n  dimensions: [model, region, account]\n- name: input_tokens_tier2\n  description: Input tokens 32-128K context window.\n  unit: tokens\n  aggregation: sum\n  dimensions: [model, region, account]\n- name: input_tokens_tier3\n  description: Input tokens 128K-1M context window.\n  unit: tokens\n  aggregation: sum\n  dimensions: [model, region, account]\n- name:\
  \ output_tokens\n  description: Output tokens billed by tier.\n  unit: tokens\n  aggregation: sum\n  dimensions: [model, region, account]\n- name: image_generations\n  description: Image generation calls.\n  unit: images\n  aggregation: sum\n  dimensions: [model, account]\n- name: video_generations\n  description: Video generation calls.\n  unit: videos\n  aggregation: sum\n  dimensions: [model, account]\n- name: audio_seconds\n  description: TTS/ASR seconds.\n  unit: seconds\n  aggregation: sum\n  dimensions: [model, account]\nprinciples:\n- name: Visibility\n  description: Alibaba Cloud Console exports DashScope usage and invoice line items.\n- name: Allocation\n  description: Use workspace IDs and API key tagging to attribute spend across teams.\n- name: Optimization\n  description: Choose Flash/Plus tiers for non-critical paths; bound prompts under tier-1 context window; consider self-hosting open-weight Qwen for batch.\n- name: Accountability\n  description: Renewal review of CommitRate\
  \ or enterprise discounts for high-volume workloads.\nmaintainers:\n- FN: Kin Lane\n  email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/qwen/refs/heads/main/finops/qwen-finops.yml
sources:
- https://www.alibabacloud.com/help/en/model-studio/models
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- AI
- LLM
- Alibaba
- FinOps
- FOCUS
---
