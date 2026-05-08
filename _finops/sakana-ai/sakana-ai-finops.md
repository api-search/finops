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
  pricingCategory: Beta (Pricing TBD)
description: FOCUS-aligned FinOps placeholder for Sakana AI Fugu. Billing model not yet published as Fugu is in beta. Anticipated meter dimensions include orchestrated-task counts and underlying-model token spend pass-through.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Sakana AI
  ProviderName: Sakana AI
  PublisherName: Sakana AI
  ServiceCategory: AI and Machine Learning
  ServiceName: Sakana Fugu
layout: finops
meters:
- aggregation: sum
  description: Tasks routed by Fugu (anticipated meter).
  dimensions:
  - variant
  - account
  name: orchestrated_tasks
  unit: tasks
- aggregation: sum
  description: Pass-through cost of underlying frontier model calls (anticipated).
  dimensions:
  - provider
  - model
  - account
  name: underlying_model_spend
  unit: usd
name: Sakana Ai Finops
provider_name: Sakana AI
provider_slug: sakana-ai
publisher_name: Sakana AI
service_category: AI and Machine Learning
slug: sakana-ai-finops
source_filename: sakana-ai-finops.yml
source_heading: FinOps Profile
source_url: https://sakana.ai/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Sakana AI\nproviderId: sakana-ai\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: false\ntags:\n- AI\n- LLM\n- Research\n- Multi-Agent\n- FinOps\n- FOCUS\ndescription: >-\n  FOCUS-aligned FinOps placeholder for Sakana AI Fugu. Billing model not yet published as\n  Fugu is in beta. Anticipated meter dimensions include orchestrated-task counts and\n  underlying-model token spend pass-through.\nnotes: Update once Fugu pricing surfaces.\nsources:\n- https://sakana.ai/\n- https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Sakana AI\nserviceCategory: AI and Machine Learning\nbillingModel:\n  pricingCategory: Beta (Pricing TBD)\n\
  \  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n  - Usage\n  - Purchase\n  - Adjustment\nfocusColumns:\n  ServiceName: Sakana Fugu\n  ServiceCategory: AI and Machine Learning\n  ProviderName: Sakana AI\n  PublisherName: Sakana AI\n  InvoiceIssuerName: Sakana AI\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n- name: orchestrated_tasks\n  description: Tasks routed by Fugu (anticipated meter).\n  unit: tasks\n  aggregation: sum\n  dimensions: [variant, account]\n- name: underlying_model_spend\n  description: Pass-through cost of underlying frontier model calls (anticipated).\n  unit: usd\n  aggregation: sum\n  dimensions: [provider, model, account]\nprinciples:\n- name: Visibility\n  description: Beta participants should track Fugu usage and underlying model costs separately.\n- name: Allocation\n  description: Use API key per workload/team; map underlying model spend to consumers.\n- name: Optimization\n  description: Choose Fugu Mini for low-latency\
  \ paths; Fugu Ultra for complex orchestrations.\n- name: Accountability\n  description: Engage Sakana for production pricing once GA.\nmaintainers:\n- FN: Kin Lane\n  email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/sakana-ai/refs/heads/main/finops/sakana-ai-finops.yml
sources:
- https://sakana.ai/
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- AI
- LLM
- Research
- Multi-Agent
- FinOps
- FOCUS
---
