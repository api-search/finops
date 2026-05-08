---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly / Annual
  chargeCategories:
  - Subscription
  - Usage
  pricingCategory: Subscription + Usage
description: FOCUS-aligned FinOps profile for Patronus AI. Cost is metered evaluator calls plus seat-based subscription. Optimize by sampling production traffic, batching evaluator runs, and consolidating around the strongest evaluators (Lynx for hallucination, Glider for general critique).
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Subscription
  InvoiceIssuerName: Patronus AI
  ProviderName: Patronus AI
  PublisherName: Patronus AI
  ServiceCategory: AI Evaluation
  ServiceName: Patronus AI
layout: finops
meters:
- aggregation: sum
  description: Evaluator API calls.
  dimensions:
  - evaluator
  - project
  name: evaluator_calls
  unit: call
- aggregation: max
  description: Active users with platform access.
  dimensions:
  - team
  name: seats
  unit: seat-month
name: Patronus Finops
provider_name: Patronus AI
provider_slug: patronus
publisher_name: Patronus AI
service_category: AI Evaluation
slug: patronus-finops
source_filename: patronus-finops.yml
source_heading: FinOps Profile
source_url: https://www.patronus.ai/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Patronus AI\nproviderId: patronus\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: true\ntags:\n- AI Evaluation\n- GenAI\n- Guardrails\n- Hallucination Detection\n- LLM\n- Agents\n- FinOps\n- Cost Management\n- FOCUS\ndescription: >-\n  FOCUS-aligned FinOps profile for Patronus AI. Cost is metered evaluator calls plus seat-based\n  subscription. Optimize by sampling production traffic, batching evaluator runs, and consolidating\n  around the strongest evaluators (Lynx for hallucination, Glider for general critique).\nnotes: Seat + metered evaluator calls; sampling is the primary lever.\nsources:\n- https://www.patronus.ai/pricing\n- https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\n\
  publisherName: Patronus AI\nserviceCategory: AI Evaluation\nbillingModel:\n  pricingCategory: Subscription + Usage\n  billingFrequency: Monthly / Annual\n  billingCurrency: USD\n  chargeCategories:\n  - Subscription\n  - Usage\nfocusColumns:\n  ServiceName: Patronus AI\n  ServiceCategory: AI Evaluation\n  ProviderName: Patronus AI\n  PublisherName: Patronus AI\n  InvoiceIssuerName: Patronus AI\n  BillingCurrency: USD\n  ChargeCategory: Subscription\nmeters:\n- name: evaluator_calls\n  description: Evaluator API calls.\n  unit: call\n  aggregation: sum\n  dimensions:\n  - evaluator\n  - project\n- name: seats\n  description: Active users with platform access.\n  unit: seat-month\n  aggregation: max\n  dimensions:\n  - team\nprinciples:\n- name: Visibility\n  description: Track evaluator calls per project monthly.\n- name: Allocation\n  description: Allocate to the AI feature/team being evaluated.\n- name: Optimization\n  description: Sample production traffic; consolidate around the highest-signal\
  \ evaluators.\n- name: Accountability\n  description: AI/ML platform team owns the contract.\nmaintainers:\n- FN: Kin Lane\n  email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/patronus/refs/heads/main/finops/patronus-finops.yml
sources:
- https://www.patronus.ai/pricing
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- AI Evaluation
- GenAI
- Guardrails
- Hallucination Detection
- LLM
- Agents
- FinOps
- Cost Management
- FOCUS
---
