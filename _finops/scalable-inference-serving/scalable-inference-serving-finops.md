---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: kserve-open-inference-protocol-openapi.yml
  format: yaml
  label: KServe Open Inference Protocol API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/scalable-inference-serving/main/openapi/kserve-open-inference-protocol-openapi.yml
billing_model:
  billingCurrency: USD (varies by contract)
  billingFrequency: Per-Contract
  chargeCategories:
  - Purchase
  - Usage
  - Adjustment
  pricingCategory: Contract / Negotiated
description: 'FOCUS-aligned FinOps shape for the Scalable Inference Serving stack: open-source software (KServe, BentoML, vLLM, Triton) with no software license fee; FinOps cost is the underlying GPU / Kubernetes infrastructure on the deploying cloud account.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Various (open source)
  ProviderName: Scalable Inference Serving
  PublisherName: Various (open source)
  ServiceCategory: AI Infrastructure
  ServiceName: Scalable Inference Serving
layout: finops
meters:
- aggregation: sum
  name: contracted_consumption
  unit: varies
name: Scalable Inference Serving Finops
provider_name: Scalable Inference Serving
provider_slug: scalable-inference-serving
publisher_name: Various (open source)
service_category: AI Infrastructure
slug: scalable-inference-serving-finops
source_filename: scalable-inference-serving-finops.yml
source_heading: FinOps Profile
source_url: https://kserve.github.io/website/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Scalable Inference Serving\nproviderId: scalable-inference-serving\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n- FinOps\n- FOCUS\n- AI\n- Inference\n- Open Source\ndescription: 'FOCUS-aligned FinOps shape for the Scalable Inference Serving stack: open-source software\n  (KServe, BentoML, vLLM, Triton) with no software license fee; FinOps cost is the underlying GPU / Kubernetes\n  infrastructure on the deploying cloud account.'\nnotes: Scalable Inference Serving is an aggregate index of open-source model-serving projects (KServe,\n  BentoML, vLLM, NVIDIA Triton) rather than a single commercial provider. The component projects are free\n  / Apache-2.0; cost arises from the underlying compute (GPUs, Kubernetes) on whichever cloud the operator\n  runs them. No unified plans or pricing.\nsources:\n- https://kserve.github.io/website/\n-\
  \ https://docs.bentoml.com/\n- https://docs.vllm.ai/\n- https://github.com/triton-inference-server/server\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Various (open source)\nserviceCategory: AI Infrastructure\nbillingModel:\n  pricingCategory: Contract / Negotiated\n  billingFrequency: Per-Contract\n  billingCurrency: USD (varies by contract)\n  chargeCategories:\n  - Purchase\n  - Usage\n  - Adjustment\nfocusColumns:\n  ServiceName: Scalable Inference Serving\n  ServiceCategory: AI Infrastructure\n  ProviderName: Scalable Inference Serving\n  PublisherName: Various (open source)\n  InvoiceIssuerName: Various (open source)\n  BillingCurrency: USD\nmeters:\n- name: contracted_consumption\n  unit: varies\n  aggregation: sum\nprinciples:\n- name: Visibility\n  description: Consumption visibility comes\
  \ from the Scalable Inference Serving account / partner reporting\n    surface (invoices, account dashboards) rather than a public usage API.\n- name: Allocation\n  description: Allocate cost through the Scalable Inference Serving contract structure (entitlement, project,\n    business unit) and reconcile against internal cost centers.\n- name: Optimization\n  description: 'Optimization levers are commercial: renegotiation cadence, commitment sizing, and consolidation\n    of Scalable Inference Serving entitlements.'\n- name: Accountability\n  description: Assign a contract owner who reconciles Scalable Inference Serving invoices against contracted\n    entitlements each billing cycle.\nmaintainers:\n- FN: Kin Lane\n  email: kin@apievangelist.com\n  url: https://apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/scalable-inference-serving/refs/heads/main/finops/scalable-inference-serving-finops.yml
sources:
- https://kserve.github.io/website/
- https://docs.bentoml.com/
- https://docs.vllm.ai/
- https://github.com/triton-inference-server/server
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- AI
- Inference
- Open Source
---
