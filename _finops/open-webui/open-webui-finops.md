---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: N/A (project) / Variable (infra)
  chargeCategories:
  - Usage
  pricingCategory: Free / Self-Host
description: 'FOCUS-aligned FinOps profile for Open WebUI. The software itself is free. Real cost lines are: (1) compute and storage for the Open WebUI container and any local model storage, (2) GPU compute for Ollama or local model inference, and (3) per-token spend on connected commercial LLM backends. Optimize by right-sizing GPU, routing low-stakes prompts to cheaper models, and caching common prompts/RAG queries.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: N/A
  ProviderName: Open WebUI
  PublisherName: Open WebUI
  ServiceCategory: LLM Tooling
  ServiceName: Open WebUI
layout: finops
meters:
- aggregation: sum
  description: Compute hours for the Open WebUI container.
  dimensions:
  - instance
  name: compute_hours
  unit: hour
- aggregation: sum
  description: GPU hours for local inference (Ollama, llama.cpp, etc.).
  dimensions:
  - model
  name: gpu_hours
  unit: hour
- aggregation: sum
  description: Tokens billed by upstream LLM provider (OpenAI, Anthropic, etc.).
  dimensions:
  - provider
  - model
  name: upstream_tokens
  unit: token
name: Open Webui Finops
provider_name: Open WebUI
provider_slug: open-webui
publisher_name: Open WebUI
service_category: LLM Tooling
slug: open-webui-finops
source_filename: open-webui-finops.yml
source_heading: FinOps Profile
source_url: https://github.com/open-webui/open-webui
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Open WebUI\nproviderId: open-webui\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: true\ntags:\n- LLM\n- Open Source\n- Self-Hosted\n- Ollama\n- Chat UI\n- RAG\n- FinOps\n- Cost Management\n- FOCUS\ndescription: >-\n  FOCUS-aligned FinOps profile for Open WebUI. The software itself is free. Real cost lines are: (1)\n  compute and storage for the Open WebUI container and any local model storage, (2) GPU compute for\n  Ollama or local model inference, and (3) per-token spend on connected commercial LLM backends.\n  Optimize by right-sizing GPU, routing low-stakes prompts to cheaper models, and caching common\n  prompts/RAG queries.\nnotes: Free OSS; cost is your compute/GPU/storage + upstream LLM token spend.\nsources:\n- https://github.com/open-webui/open-webui\n- https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation\
  \ Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Open WebUI\nserviceCategory: LLM Tooling\nbillingModel:\n  pricingCategory: Free / Self-Host\n  billingFrequency: N/A (project) / Variable (infra)\n  billingCurrency: USD\n  chargeCategories:\n  - Usage\nfocusColumns:\n  ServiceName: Open WebUI\n  ServiceCategory: LLM Tooling\n  ProviderName: Open WebUI\n  PublisherName: Open WebUI\n  InvoiceIssuerName: N/A\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n- name: compute_hours\n  description: Compute hours for the Open WebUI container.\n  unit: hour\n  aggregation: sum\n  dimensions:\n  - instance\n- name: gpu_hours\n  description: GPU hours for local inference (Ollama, llama.cpp, etc.).\n  unit: hour\n  aggregation: sum\n  dimensions:\n  - model\n- name: upstream_tokens\n  description: Tokens billed by upstream LLM provider (OpenAI, Anthropic,\
  \ etc.).\n  unit: token\n  aggregation: sum\n  dimensions:\n  - provider\n  - model\nprinciples:\n- name: Visibility\n  description: Monitor container, GPU, and upstream LLM usage; consolidate into a single dashboard.\n- name: Allocation\n  description: Allocate by user/team using Open WebUI's user/group features.\n- name: Optimization\n  description: Route low-stakes chats to cheap local Ollama models; reserve expensive providers for hard tasks.\n- name: Accountability\n  description: Platform/infra team owns the Open WebUI deployment; AI team owns prompt/model choice.\nmaintainers:\n- FN: Kin Lane\n  email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/open-webui/refs/heads/main/finops/open-webui-finops.yml
sources:
- https://github.com/open-webui/open-webui
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- LLM
- Open Source
- Self-Hosted
- Ollama
- Chat UI
- RAG
- FinOps
- Cost Management
- FOCUS
---
