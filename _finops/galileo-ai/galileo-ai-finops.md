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
description: FOCUS-aligned FinOps profile for Galileo. Cost is driven by tier (seats) plus metered traces/evaluations. Optimize by using sampling in high-volume production paths, choosing cheaper judge models within Galileo evaluators, and aligning tier with actual usage at renewal.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Subscription
  InvoiceIssuerName: Galileo
  ProviderName: Galileo
  PublisherName: Galileo
  ServiceCategory: AI Observability
  ServiceName: Galileo
layout: finops
meters:
- aggregation: max
  description: Active users with platform access.
  dimensions:
  - team
  name: seats
  unit: seat-month
- aggregation: sum
  description: Traces ingested into Galileo.
  dimensions:
  - project
  name: traces
  unit: trace
- aggregation: sum
  description: Evaluation runs executed.
  dimensions:
  - project
  name: evaluations
  unit: eval
name: Galileo Ai Finops
provider_name: Galileo
provider_slug: galileo-ai
publisher_name: Galileo
service_category: AI Observability
slug: galileo-ai-finops
source_filename: galileo-ai-finops.yml
source_heading: FinOps Profile
source_url: https://galileo.ai/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Galileo\nproviderId: galileo-ai\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: true\ntags:\n- AI Evaluation\n- Observability\n- GenAI\n- Guardrails\n- Agentic AI\n- LLM\n- FinOps\n- Cost Management\n- FOCUS\ndescription: >-\n  FOCUS-aligned FinOps profile for Galileo. Cost is driven by tier (seats) plus metered\n  traces/evaluations. Optimize by using sampling in high-volume production paths, choosing cheaper\n  judge models within Galileo evaluators, and aligning tier with actual usage at renewal.\nnotes: Seat + metered traces/evals; sampling and judge-model choice are key levers.\nsources:\n- https://galileo.ai/pricing\n- https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\n\
  publisherName: Galileo\nserviceCategory: AI Observability\nbillingModel:\n  pricingCategory: Subscription + Usage\n  billingFrequency: Monthly / Annual\n  billingCurrency: USD\n  chargeCategories:\n  - Subscription\n  - Usage\nfocusColumns:\n  ServiceName: Galileo\n  ServiceCategory: AI Observability\n  ProviderName: Galileo\n  PublisherName: Galileo\n  InvoiceIssuerName: Galileo\n  BillingCurrency: USD\n  ChargeCategory: Subscription\nmeters:\n- name: seats\n  description: Active users with platform access.\n  unit: seat-month\n  aggregation: max\n  dimensions:\n  - team\n- name: traces\n  description: Traces ingested into Galileo.\n  unit: trace\n  aggregation: sum\n  dimensions:\n  - project\n- name: evaluations\n  description: Evaluation runs executed.\n  unit: eval\n  aggregation: sum\n  dimensions:\n  - project\nprinciples:\n- name: Visibility\n  description: Track trace and eval volume per project monthly.\n- name: Allocation\n  description: Allocate cost per AI feature or model\
  \ team.\n- name: Optimization\n  description: Sample traces in production; pick cheaper judge models in evaluators.\n- name: Accountability\n  description: AI/ML platform team owns Galileo contract and tier.\nmaintainers:\n- FN: Kin Lane\n  email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/galileo-ai/refs/heads/main/finops/galileo-ai-finops.yml
sources:
- https://galileo.ai/pricing
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- AI Evaluation
- Observability
- GenAI
- Guardrails
- Agentic AI
- LLM
- FinOps
- Cost Management
- FOCUS
---
