---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: claude-messages-api.yml
  format: yaml
  label: Claude Messages API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/claude/refs/heads/main/openapi/claude-messages-api.yml
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
description: FOCUS-aligned FinOps for Claude. Cost is split between per-seat consumer / business plans (Free, Pro, Max, Team, Enterprise) and pay-as-you-go API usage metered in input / output / cache tokens per model, plus server-tool charges (web search at $10 / 1k searches, code execution beyond the 1,550-hour monthly free tier at $0.05 / container-hour, Managed Agents session runtime at $0.08 / session-hour). Spend is gated by usage tiers (Tier 1-4 ceilings of $100 / $500 / $1,000 / $200,000 per month) until the organization moves to Monthly Invoicing. Effective unit cost is materially reduced by prompt caching (cache reads at 0.1x input price; cache reads excluded from ITPM rate limit on Claude 4.x) and by the Batch API (50% discount on input and output).
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Anthropic, PBC
  PricingUnit: token
  ProviderName: Anthropic
  PublisherName: Anthropic, PBC
  ServiceCategory: AI Infrastructure
  ServiceName: Claude
layout: finops
meters:
- aggregation: sum
  description: Uncached input tokens billed at the model's base input rate (e.g. $5 / MTok for Opus 4.7, $3 / MTok for Sonnet 4.6, $1 / MTok for Haiku 4.5).
  dimensions:
  - model
  - workspace
  - inference_geo
  name: tokens_input
  unit: token
- aggregation: sum
  description: Output tokens billed at the model's output rate (e.g. $25 / MTok for Opus 4.7, $15 / MTok for Sonnet 4.6, $5 / MTok for Haiku 4.5).
  dimensions:
  - model
  - workspace
  - inference_geo
  name: tokens_output
  unit: token
- aggregation: sum
  description: 5-minute cache writes billed at 1.25x base input.
  dimensions:
  - model
  - workspace
  name: tokens_cache_write_5m
  unit: token
- aggregation: sum
  description: 1-hour cache writes billed at 2x base input.
  dimensions:
  - model
  - workspace
  name: tokens_cache_write_1h
  unit: token
- aggregation: sum
  description: Cache read / hit tokens billed at 0.1x base input. On Claude 4.x models these do not count toward ITPM rate limits.
  dimensions:
  - model
  - workspace
  name: tokens_cache_read
  unit: token
- aggregation: sum
  description: Server-tool web searches at $10 per 1,000.
  dimensions:
  - workspace
  name: web_search_requests
  unit: search
- aggregation: sum
  description: Code-execution container hours beyond the 1,550-hour monthly free tier, at $0.05 / hour per container.
  dimensions:
  - workspace
  name: code_execution_hours
  unit: container-hour
- aggregation: sum
  description: Claude Managed Agents session runtime at $0.08 per session-hour, metered while the session is running (not idle).
  dimensions:
  - workspace
  - agent
  name: managed_agent_session_runtime
  unit: session-hour
- aggregation: max
  description: Per-seat subscriptions for Pro, Max, Team, and Enterprise plans.
  dimensions:
  - plan
  - region
  name: consumer_seats
  unit: seat-month
name: Claude Finops
provider_name: Claude
provider_slug: claude
publisher_name: Anthropic, PBC
service_category: AI Infrastructure
slug: claude-finops
source_filename: claude-finops.yml
source_heading: FinOps Profile
source_url: https://platform.claude.com/docs/en/about-claude/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Claude\nproviderId: claude\npublisherName: Anthropic, PBC\nserviceCategory: AI Infrastructure\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - Artificial Intelligence\n  - Generative AI\n  - Large Language Models\n  - FinOps\n  - FOCUS\ndescription: >-\n  FOCUS-aligned FinOps for Claude. Cost is split between per-seat consumer / business plans (Free,\n  Pro, Max, Team, Enterprise) and pay-as-you-go API usage metered in input / output / cache tokens\n  per model, plus server-tool charges (web search at $10 / 1k searches, code execution beyond the\n  1,550-hour monthly free tier at $0.05 / container-hour, Managed Agents\
  \ session runtime at $0.08 /\n  session-hour). Spend is gated by usage tiers (Tier 1-4 ceilings of $100 / $500 / $1,000 / $200,000\n  per month) until the organization moves to Monthly Invoicing. Effective unit cost is materially\n  reduced by prompt caching (cache reads at 0.1x input price; cache reads excluded from ITPM rate\n  limit on Claude 4.x) and by the Batch API (50% discount on input and output).\nsources:\n  - https://platform.claude.com/docs/en/about-claude/pricing\n  - https://platform.claude.com/docs/en/api/rate-limits\n  - https://claude.com/pricing\nbillingModel:\n  pricingCategory: Pay-As-You-Go + Subscription\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Adjustment\n    - Credit\nfocusColumns:\n  ServiceName: Claude\n  ServiceCategory: AI Infrastructure\n  ProviderName: Anthropic\n  PublisherName: Anthropic, PBC\n  InvoiceIssuerName: Anthropic, PBC\n  BillingCurrency: USD\n  ChargeCategory: Usage\n\
  \  PricingUnit: token\nmeters:\n  - name: tokens_input\n    description: Uncached input tokens billed at the model's base input rate (e.g. $5 / MTok for\n      Opus 4.7, $3 / MTok for Sonnet 4.6, $1 / MTok for Haiku 4.5).\n    unit: token\n    aggregation: sum\n    dimensions:\n      - model\n      - workspace\n      - inference_geo\n  - name: tokens_output\n    description: Output tokens billed at the model's output rate (e.g. $25 / MTok for Opus 4.7,\n      $15 / MTok for Sonnet 4.6, $5 / MTok for Haiku 4.5).\n    unit: token\n    aggregation: sum\n    dimensions:\n      - model\n      - workspace\n      - inference_geo\n  - name: tokens_cache_write_5m\n    description: 5-minute cache writes billed at 1.25x base input.\n    unit: token\n    aggregation: sum\n    dimensions:\n      - model\n      - workspace\n  - name: tokens_cache_write_1h\n    description: 1-hour cache writes billed at 2x base input.\n    unit: token\n    aggregation: sum\n    dimensions:\n      - model\n      - workspace\n\
  \  - name: tokens_cache_read\n    description: Cache read / hit tokens billed at 0.1x base input. On Claude 4.x models these do\n      not count toward ITPM rate limits.\n    unit: token\n    aggregation: sum\n    dimensions:\n      - model\n      - workspace\n  - name: web_search_requests\n    description: Server-tool web searches at $10 per 1,000.\n    unit: search\n    aggregation: sum\n    dimensions:\n      - workspace\n  - name: code_execution_hours\n    description: Code-execution container hours beyond the 1,550-hour monthly free tier, at $0.05 /\n      hour per container.\n    unit: container-hour\n    aggregation: sum\n    dimensions:\n      - workspace\n  - name: managed_agent_session_runtime\n    description: Claude Managed Agents session runtime at $0.08 per session-hour, metered while the\n      session is running (not idle).\n    unit: session-hour\n    aggregation: sum\n    dimensions:\n      - workspace\n      - agent\n  - name: consumer_seats\n    description: Per-seat\
  \ subscriptions for Pro, Max, Team, and Enterprise plans.\n    unit: seat-month\n    aggregation: max\n    dimensions:\n      - plan\n      - region\nprinciples:\n  - name: Visibility\n    description: Use the Claude Console Usage page (token / request / rate-limit charts), the Rate\n      Limits API, and the anthropic-ratelimit-* response headers to track per-model consumption,\n      cache-hit rate, and headroom in real time.\n  - name: Allocation\n    description: Allocate cost via Workspaces (separate API keys, spend ceilings, and rate caps per\n      team / product) and the response usage object (input_tokens, cache_*_tokens, output_tokens,\n      server_tool_use). Tag invoices to the consuming product / cost center.\n  - name: Optimization\n    description: Lean into prompt caching (cache reads at 10% of input price and excluded from ITPM\n      on 4.x); use the Batch API (50% off) for non-interactive workloads; pick the right model\n      (Haiku for routine, Sonnet for general,\
  \ Opus for hardest reasoning); avoid Fast Mode (6x)\n      unless latency-critical; avoid US-only inference_geo (1.1x) unless residency is required;\n      monitor cache-hit rate on the Usage page.\n  - name: Accountability\n    description: Treat each Workspace as a budget owner with its own customer-set spend limit below\n      the tier ceiling. Engineering owns model / cache choices; finance owns tier progression\n      ($5 / $40 / $200 / $400 credit thresholds for Tier 1-4) and Monthly Invoicing transition.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/claude/refs/heads/main/finops/claude-finops.yml
sources:
- https://platform.claude.com/docs/en/about-claude/pricing
- https://platform.claude.com/docs/en/api/rate-limits
- https://claude.com/pricing
specification: FinOps Framework
tags:
- Artificial Intelligence
- Generative AI
- Large Language Models
- FinOps
- FOCUS
---
