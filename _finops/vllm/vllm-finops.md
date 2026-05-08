---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: N/A (project) / Hourly (infra)
  chargeCategories:
  - Usage
  pricingCategory: Free OSS / Compute
description: FOCUS-aligned FinOps profile for vLLM. The software is free. Cost is GPU compute and storage on your chosen platform (cloud spot/on-demand GPUs, on-prem hardware, or a managed-vLLM provider). Optimize via continuous batching (default in vLLM), prefix caching, paged-attention sizing, model quantization (AWQ/GPTQ/INT8/FP8), and routing across instance sizes.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: N/A
  ProviderName: vLLM Project
  PublisherName: vLLM Project
  ServiceCategory: LLM Inference
  ServiceName: vLLM
layout: finops
meters:
- aggregation: sum
  description: GPU hours consumed by vLLM serving processes.
  dimensions:
  - gpu_type
  - model
  name: gpu_hours
  unit: hour
- aggregation: sum
  description: Output tokens generated (operational meter for $/token tracking).
  dimensions:
  - model
  name: tokens_served
  unit: token
name: Vllm Finops
provider_name: vLLM
provider_slug: vllm
publisher_name: vLLM Project
service_category: LLM Inference
slug: vllm-finops
source_filename: vllm-finops.yml
source_heading: FinOps Profile
source_url: https://docs.vllm.ai/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: vLLM\nproviderId: vllm\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: true\ntags:\n- LLM\n- Inference\n- Open Source\n- GPU\n- OpenAI Compatible\n- Self-Hosted\n- FinOps\n- Cost Management\n- FOCUS\ndescription: >-\n  FOCUS-aligned FinOps profile for vLLM. The software is free. Cost is GPU compute and storage on your\n  chosen platform (cloud spot/on-demand GPUs, on-prem hardware, or a managed-vLLM provider). Optimize\n  via continuous batching (default in vLLM), prefix caching, paged-attention sizing, model\n  quantization (AWQ/GPTQ/INT8/FP8), and routing across instance sizes.\nnotes: Cost is GPU infra; vLLM provides batching/quantization levers to reduce $/token.\nsources:\n- https://docs.vllm.ai/\n- https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n\
  \  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: vLLM Project\nserviceCategory: LLM Inference\nbillingModel:\n  pricingCategory: Free OSS / Compute\n  billingFrequency: N/A (project) / Hourly (infra)\n  billingCurrency: USD\n  chargeCategories:\n  - Usage\nfocusColumns:\n  ServiceName: vLLM\n  ServiceCategory: LLM Inference\n  ProviderName: vLLM Project\n  PublisherName: vLLM Project\n  InvoiceIssuerName: N/A\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n- name: gpu_hours\n  description: GPU hours consumed by vLLM serving processes.\n  unit: hour\n  aggregation: sum\n  dimensions:\n  - gpu_type\n  - model\n- name: tokens_served\n  description: Output tokens generated (operational meter for $/token tracking).\n  unit: token\n  aggregation: sum\n  dimensions:\n  - model\nprinciples:\n- name: Visibility\n  description: Pull GPU utilization and tokens-served metrics; compute effective $/1k tokens.\n\
  - name: Allocation\n  description: Allocate GPU hours to consuming AI features/teams.\n- name: Optimization\n  description: Use continuous batching, prefix caching, and quantization; right-size GPUs per workload.\n- name: Accountability\n  description: Infra/ML platform team owns vLLM deployment and GPU spend.\nmaintainers:\n- FN: Kin Lane\n  email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/vllm/refs/heads/main/finops/vllm-finops.yml
sources:
- https://docs.vllm.ai/
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- LLM
- Inference
- Open Source
- GPU
- OpenAI Compatible
- Self-Hosted
- FinOps
- Cost Management
- FOCUS
---
