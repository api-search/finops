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
  - Purchase
  - Usage
  - Adjustment
  pricingCategory: Subscription + Usage (Per-Agent + Per-Second + LLM Pass-Through)
description: FOCUS-aligned FinOps view of Letta. Letta Cloud combines a $20/month base with per-active-agent ($0.10/mo) and per-second tool execution ($0.00015/sec) usage components. Underlying LLM tokens are pass-through at provider cost. Self-hosted Letta removes Letta charges entirely; you pay only infra and LLM bills.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Letta
  ProviderName: Letta
  PublisherName: Letta
  ServiceCategory: AI
  ServiceName: Letta Cloud
layout: finops
meters:
- aggregation: sum
  description: Letta Cloud monthly base fee ($20/month on API Plan).
  dimensions:
  - account
  name: plan_fee
  unit: month
- aggregation: max
  description: Active agent count, billed at $0.10/agent/month.
  dimensions:
  - account
  name: active_agents
  unit: agent-month
- aggregation: sum
  description: Tool execution time at $0.00015/sec.
  dimensions:
  - account
  - tool
  name: tool_execution_seconds
  unit: second
- aggregation: sum
  description: Pass-through LLM token usage at provider cost.
  dimensions:
  - account
  - model
  name: llm_tokens
  unit: token
name: Letta Finops
provider_name: Letta
provider_slug: letta
publisher_name: Letta
service_category: AI
slug: letta-finops
source_filename: letta-finops.yml
source_heading: FinOps Profile
source_url: https://docs.letta.com/guides/api/plans
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Letta\nproviderId: letta\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: true\ntags:\n- AI\n- Agents\n- Memory\n- MemGPT\n- Stateful\n- FinOps\n- Cost Management\n- FOCUS\ndescription: >-\n  FOCUS-aligned FinOps view of Letta. Letta Cloud combines a $20/month base with\n  per-active-agent ($0.10/mo) and per-second tool execution ($0.00015/sec) usage\n  components. Underlying LLM tokens are pass-through at provider cost. Self-hosted Letta\n  removes Letta charges entirely; you pay only infra and LLM bills.\nnotes: Active agent count is the dominant Letta-specific cost lever; LLM token cost typically dominates the total bill.\nsources:\n- https://docs.letta.com/guides/api/plans\n- https://www.letta.com/\n- https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n\
  \  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Letta\nserviceCategory: AI\nbillingModel:\n  pricingCategory: Subscription + Usage (Per-Agent + Per-Second + LLM Pass-Through)\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n  - Purchase\n  - Usage\n  - Adjustment\nfocusColumns:\n  ServiceName: Letta Cloud\n  ServiceCategory: AI\n  ProviderName: Letta\n  PublisherName: Letta\n  InvoiceIssuerName: Letta\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n- name: plan_fee\n  description: Letta Cloud monthly base fee ($20/month on API Plan).\n  unit: month\n  aggregation: sum\n  dimensions:\n  - account\n- name: active_agents\n  description: Active agent count, billed at $0.10/agent/month.\n  unit: agent-month\n  aggregation: max\n  dimensions:\n  - account\n- name: tool_execution_seconds\n  description: Tool execution time at $0.00015/sec.\n  unit: second\n  aggregation: sum\n\
  \  dimensions:\n  - account\n  - tool\n- name: llm_tokens\n  description: Pass-through LLM token usage at provider cost.\n  unit: token\n  aggregation: sum\n  dimensions:\n  - account\n  - model\nprinciples:\n- name: Visibility\n  description: Track active agent count, tool execution time, and LLM token spend in Letta dashboard.\n- name: Allocation\n  description: Tag agents to consuming product surfaces.\n- name: Optimization\n  description: Archive idle agents to drop active agent count; switch to cheaper LLM models where possible; self-host for high-volume workloads.\n- name: Accountability\n  description: Assign owners for plan fee, agent fleet, tool budget, and LLM provider contracts separately.\nmaintainers:\n- FN: Kin Lane\n  email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/letta/refs/heads/main/finops/letta-finops.yml
sources:
- https://docs.letta.com/guides/api/plans
- https://www.letta.com/
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- AI
- Agents
- Memory
- MemGPT
- Stateful
- FinOps
- Cost Management
- FOCUS
---
