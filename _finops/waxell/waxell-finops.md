---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: waxell-observe-openapi.yml
  format: yaml
  label: Waxell Observe API
  slug: observe
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/waxell/refs/heads/main/openapi/waxell-observe-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  - Tax
  - Adjustment
  - Credit
  pricingCategory: Pay-As-You-Go + Subscription
description: 'FOCUS-aligned FinOps shape for Waxell: a usage-based AI agent governance and observability platform metering ingested LLM calls, governance policy evaluations, MCP tool calls, and durable runtime executions, with subscription add-ons for enterprise governance and seats.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Callsine, Inc.
  ProviderName: Waxell
  PublisherName: Callsine, Inc.
  RegionId: us-east-1, eu-west-1
  ServiceCategory: AI Agent Governance and Observability
  ServiceName: Waxell
layout: finops
meters:
- aggregation: count
  dimensions:
  - agent_name
  - tenant
  name: agent_runs
  unit: request
- aggregation: count
  dimensions:
  - provider
  - model
  - agent_name
  name: llm_calls_ingested
  unit: request
- aggregation: sum
  dimensions:
  - provider
  - model
  name: tokens_input
  unit: token
- aggregation: sum
  dimensions:
  - provider
  - model
  name: tokens_output
  unit: token
- aggregation: count
  dimensions:
  - category
  - decision
  name: policy_evaluations
  unit: request
- aggregation: count
  dimensions:
  - mcp_server
  - tool_name
  name: mcp_tool_calls
  unit: request
- aggregation: sum
  dimensions:
  - workflow_name
  name: durable_runtime_executions
  unit: instance-hour
- aggregation: avg
  dimensions:
  - data_class
  name: data_retention
  unit: GB-month
- aggregation: max
  dimensions:
  - role
  name: seats
  unit: seat
name: Waxell Finops
provider_name: Waxell
provider_slug: waxell
publisher_name: Callsine, Inc. (dba Waxell)
service_category: AI Agent Governance and Observability
slug: waxell-finops
source_filename: waxell-finops.yml
source_heading: FinOps Profile
source_url: https://waxell.ai/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Waxell\nproviderId: waxell\ncreated: '2026-05-06'\nmodified: '2026-05-06'\nreconciled: false\nnotes: >-\n  Waxell is currently in beta with all commercial pricing routed through a\n  sales call; the public site does not publish per-meter prices. Meters and\n  charge categories below model the platform's documented telemetry surface\n  (Observe runs, LLM calls, governance policy evaluations, MCP tool calls,\n  workflow runtime executions) but unit prices are not yet known. Set\n  reconciled to true after pricing is published or confirmed in a customer\n  agreement.\ntags:\n  - FinOps\n  - FOCUS\n  - AI Agent Governance\n  - Observability\ndescription: >-\n  FOCUS-aligned FinOps shape for Waxell: a usage-based AI agent governance and\n  observability platform metering ingested LLM calls, governance policy\n  evaluations, MCP tool calls, and durable runtime executions,\
  \ with subscription\n  add-ons for enterprise governance and seats.\nsources:\n  - https://waxell.ai/\n  - https://waxell.ai/get-access\n  - https://waxell.ai/docs/observe/features/cost-management\n  - https://waxell.ai/docs/observe/api/endpoints\n  - https://waxell.ai/docs/security\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Callsine, Inc. (dba Waxell)\nserviceCategory: AI Agent Governance and Observability\nbillingModel:\n  pricingCategory: Pay-As-You-Go + Subscription\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Adjustment\n    - Credit\nfocusColumns:\n  ServiceName: Waxell\n  ServiceCategory: AI Agent Governance and Observability\n  ProviderName: Waxell\n  PublisherName: Callsine, Inc.\n  InvoiceIssuerName: Callsine, Inc.\n\
  \  BillingCurrency: USD\n  ChargeCategory: Usage\n  RegionId: us-east-1, eu-west-1\nmeters:\n  - name: agent_runs\n    unit: request\n    aggregation: count\n    dimensions:\n      - agent_name\n      - tenant\n  - name: llm_calls_ingested\n    unit: request\n    aggregation: count\n    dimensions:\n      - provider\n      - model\n      - agent_name\n  - name: tokens_input\n    unit: token\n    aggregation: sum\n    dimensions:\n      - provider\n      - model\n  - name: tokens_output\n    unit: token\n    aggregation: sum\n    dimensions:\n      - provider\n      - model\n  - name: policy_evaluations\n    unit: request\n    aggregation: count\n    dimensions:\n      - category\n      - decision\n  - name: mcp_tool_calls\n    unit: request\n    aggregation: count\n    dimensions:\n      - mcp_server\n      - tool_name\n  - name: durable_runtime_executions\n    unit: instance-hour\n    aggregation: sum\n    dimensions:\n      - workflow_name\n  - name: data_retention\n    unit: GB-month\n\
  \    aggregation: avg\n    dimensions:\n      - data_class\n  - name: seats\n    unit: seat\n    aggregation: max\n    dimensions:\n      - role\nprinciples:\n  - name: Visibility\n    description: Use the Waxell control plane dashboard at https://waxell.dev plus the Observe REST API (`/runs`, `/llm-calls`, `/spans`, `/events`) and the `estimate_cost()` SDK helper to see token, dollar, and policy-decision consumption per agent and per user.\n  - name: Allocation\n    description: Tag every run with `agent_name`, `session_id`, and `user_id` plus free-form metadata via WaxellContext to attribute LLM and governance spend to the team or product owning the agent.\n  - name: Optimization\n    description: Use `model-costs` overrides to reflect negotiated rates from upstream LLM vendors; use Cost Management governance policies to set budgets that warn, throttle, or block when an agent or tenant approaches a spend ceiling; use the prompt manager to roll back regressions that inflate token usage.\n\
  \  - name: Accountability\n    description: SOC 2 Type II is in progress; immutable audit trails (`/events/`) plus the kill-switch policy and human-in-the-loop approval handlers (Slack, webhooks) give a single owner the levers to halt or escalate spend in real time.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/waxell/refs/heads/main/finops/waxell-finops.yml
sources:
- https://waxell.ai/
- https://waxell.ai/get-access
- https://waxell.ai/docs/observe/features/cost-management
- https://waxell.ai/docs/observe/api/endpoints
- https://waxell.ai/docs/security
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- AI Agent Governance
- Observability
---
