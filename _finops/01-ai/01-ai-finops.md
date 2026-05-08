---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: CNY/USD
  billingFrequency: On-Demand (Recharge)
  chargeCategories:
  - Usage
  - Purchase
  - Adjustment
  pricingCategory: Usage Based (Prepaid)
description: FOCUS-aligned FinOps profile for 01.AI / Lingyiwanwu. Pay-as-you-go usage billing against prepaid balance, plus free self-hosted open-weight option for Yi-34B and smaller variants.
focus_columns:
  BillingCurrency: CNY
  ChargeCategory: Usage
  InvoiceIssuerName: 01.AI
  ProviderName: 01.AI
  PublisherName: 01.AI
  ServiceCategory: AI and Machine Learning
  ServiceName: Lingyiwanwu Platform
layout: finops
meters:
- aggregation: sum
  description: Input tokens by Yi model.
  dimensions:
  - model
  - account
  name: input_tokens
  unit: tokens
- aggregation: sum
  description: Output tokens by Yi model.
  dimensions:
  - model
  - account
  name: output_tokens
  unit: tokens
name: 01 Ai Finops
provider_name: 01.AI
provider_slug: 01-ai
publisher_name: 01.AI
service_category: AI and Machine Learning
slug: 01-ai-finops
source_filename: 01-ai-finops.yml
source_heading: FinOps Profile
source_url: https://platform.lingyiwanwu.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: 01.AI\nproviderId: 01-ai\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: true\ntags:\n- AI\n- LLM\n- Yi\n- FinOps\n- FOCUS\ndescription: >-\n  FOCUS-aligned FinOps profile for 01.AI / Lingyiwanwu. Pay-as-you-go usage billing against\n  prepaid balance, plus free self-hosted open-weight option for Yi-34B and smaller variants.\nnotes: Pricing primarily published in CNY on the Lingyiwanwu console; Yi-Lightning ~$0.14/M tokens.\nsources:\n- https://platform.lingyiwanwu.com/\n- https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: 01.AI\nserviceCategory: AI and Machine Learning\nbillingModel:\n  pricingCategory: Usage Based (Prepaid)\n\
  \  billingFrequency: On-Demand (Recharge)\n  billingCurrency: CNY/USD\n  chargeCategories:\n  - Usage\n  - Purchase\n  - Adjustment\nfocusColumns:\n  ServiceName: Lingyiwanwu Platform\n  ServiceCategory: AI and Machine Learning\n  ProviderName: 01.AI\n  PublisherName: 01.AI\n  InvoiceIssuerName: 01.AI\n  BillingCurrency: CNY\n  ChargeCategory: Usage\nmeters:\n- name: input_tokens\n  description: Input tokens by Yi model.\n  unit: tokens\n  aggregation: sum\n  dimensions: [model, account]\n- name: output_tokens\n  description: Output tokens by Yi model.\n  unit: tokens\n  aggregation: sum\n  dimensions: [model, account]\nprinciples:\n- name: Visibility\n  description: Lingyiwanwu console reports balance and usage; track spend per API key.\n- name: Allocation\n  description: Tag API keys by workload to attribute Yi spend.\n- name: Optimization\n  description: Use Yi-Lightning-Lite for non-critical paths; consider self-hosted Yi-34B for batch workloads.\n- name: Accountability\n  description:\
  \ Set balance alerts; reconcile invoice currency exposure.\nmaintainers:\n- FN: Kin Lane\n  email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/01-ai/refs/heads/main/finops/01-ai-finops.yml
sources:
- https://platform.lingyiwanwu.com/
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- AI
- LLM
- Yi
- FinOps
- FOCUS
---
