---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: tetrate-service-bridge-openapi.yml
  format: yaml
  label: Tetrate Service Bridge REST API
  slug: tsb-rest-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/tetrate/refs/heads/main/openapi/tetrate-service-bridge-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Per-Invoice
  chargeCategories:
  - Usage
  - Purchase
  - Credit
  pricingCategory: Subscription
description: FOCUS-aligned FinOps for Tetrate's Agent Router (LLM Gateway, MCP Gateway, AI Guardrails) and enterprise AI cost-governance platform. Tetrate itself markets AI Cost Governance as a solution, so the FinOps shape combines Tetrate's own subscription with the underlying LLM provider spend that the gateway routes.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Tetrate, Inc.
  ProviderName: Tetrate
  PublisherName: Tetrate, Inc.
  ServiceCategory: AI Gateway / Governance
  ServiceName: Tetrate Agent Router
layout: finops
meters:
- aggregation: sum
  dimensions:
  - product
  - model
  - tenant
  name: gateway_requests
  unit: request
- aggregation: sum
  dimensions:
  - model
  - direction
  - tenant
  name: tokens_routed
  unit: token
- aggregation: sum
  dimensions:
  - product
  name: developer_credits_consumed
  unit: request
name: Tetrate Finops
provider_name: Tetrate
provider_slug: tetrate
publisher_name: Tetrate, Inc.
service_category: AI Gateway / Governance
slug: tetrate-finops
source_filename: tetrate-finops.yml
source_heading: FinOps Profile
source_url: https://tetrate.io/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Tetrate\nproviderId: tetrate\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - AI Gateway\n  - LLM Gateway\ndescription: >-\n  FOCUS-aligned FinOps for Tetrate's Agent Router (LLM Gateway, MCP Gateway, AI Guardrails) and enterprise\n  AI cost-governance platform. Tetrate itself markets AI Cost Governance as a solution, so the FinOps\n  shape combines Tetrate's own subscription with the underlying LLM provider spend that the gateway routes.\nsources:\n  - https://tetrate.io/\n  - https://router.tetrate.ai/sign-in\n  - https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Tetrate, Inc.\n\
  serviceCategory: AI Gateway / Governance\nbillingModel:\n  pricingCategory: Subscription\n  billingFrequency: Per-Invoice\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Credit\nfocusColumns:\n  ServiceName: Tetrate Agent Router\n  ServiceCategory: AI Gateway / Governance\n  ProviderName: Tetrate\n  PublisherName: Tetrate, Inc.\n  InvoiceIssuerName: Tetrate, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: gateway_requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - product\n      - model\n      - tenant\n  - name: tokens_routed\n    unit: token\n    aggregation: sum\n    dimensions:\n      - model\n      - direction\n      - tenant\n  - name: developer_credits_consumed\n    unit: request\n    aggregation: sum\n    dimensions:\n      - product\nprinciples:\n  - name: Visibility\n    description: Use Tetrate Agent Router's own AI Cost Governance dashboards to see per-model and per-tenant\n      LLM spend; correlate with each upstream\
  \ model provider's invoice for ground truth.\n  - name: Allocation\n    description: Allocate routed-LLM cost via the Agent Router's tenant / project tagging so spend can\n      be attributed back to consuming agents and teams.\n  - name: Optimization\n    description: Use approved-model catalog routing, automatic fallback to cheaper models, and AI Guardrails\n      to cap runaway agent spend; review token-per-task and per-model unit economics regularly.\n  - name: Accountability\n    description: Platform team owning the Agent Router deployment is accountable for total LLM spend and\n      reviews credit / token consumption with model owners on a regular cadence.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/tetrate/refs/heads/main/finops/tetrate-finops.yml
sources:
- https://tetrate.io/
- https://router.tetrate.ai/sign-in
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- AI Gateway
- LLM Gateway
---
