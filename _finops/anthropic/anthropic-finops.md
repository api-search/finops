---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: anthropic-messages-api-openapi.yml
  format: yaml
  label: Anthropic Messages API
  slug: anthropic-messages-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/anthropic/refs/heads/main/openapi/anthropic-messages-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  - Tax
  - Credit
  - Adjustment
  pricingCategory: Usage-Based
  primaryUnit: token
  secondaryUnits:
  - search
  - container_hour
  - session_hour
description: FOCUS-aligned FinOps definition for Anthropic's Claude API. Token-based metering with prompt-caching and batch-processing discount lanes.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Anthropic
  PricingCategory: Usage-Based
  PricingUnit: MTok
  ProviderName: Anthropic
  PublisherName: Anthropic
  ServiceCategory: AI and Machine Learning
  ServiceName: Anthropic API
layout: finops
meters:
- aggregation: sum
  dimensions:
  - model
  - workspace
  - service_tier
  - inference_geo
  name: input_tokens
  unit: token
- aggregation: sum
  dimensions:
  - model
  - workspace
  - service_tier
  - inference_geo
  name: output_tokens
  unit: token
- aggregation: sum
  dimensions:
  - model
  - cache_ttl
  name: cache_creation_input_tokens
  unit: token
- aggregation: sum
  dimensions:
  - model
  name: cache_read_input_tokens
  unit: token
- aggregation: sum
  dimensions:
  - workspace
  name: web_search_requests
  unit: search
- aggregation: sum
  dimensions:
  - workspace
  name: code_execution_container_hours
  unit: container_hour
name: Anthropic Finops
provider_name: Anthropic
provider_slug: anthropic
publisher_name: Anthropic
service_category: AI and Machine Learning
slug: anthropic-finops
source_filename: anthropic-finops.yml
source_heading: FinOps Profile
source_url: https://www.anthropic.com/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Anthropic\nproviderId: anthropic\ncreated: '2026-05-04'\nmodified: '2026-05-04'\nreconciled: true\ntags:\n  - FinOps\n  - Cost Management\n  - FOCUS\n  - AI\n  - Tokens\ndescription: FOCUS-aligned FinOps definition for Anthropic's Claude API. Token-based metering with prompt-caching\n  and batch-processing discount lanes.\nsources:\n  - https://www.anthropic.com/pricing\n  - https://platform.claude.com/docs/en/docs/about-claude/pricing\n  - https://platform.claude.com/docs/en/api/rate-limits\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Anthropic\nserviceCategory: AI and Machine Learning\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency:\
  \ USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  primaryUnit: token\n  secondaryUnits:\n    - search\n    - container_hour\n    - session_hour\nfocusColumns:\n  ServiceName: Anthropic API\n  ServiceCategory: AI and Machine Learning\n  ProviderName: Anthropic\n  PublisherName: Anthropic\n  InvoiceIssuerName: Anthropic\n  PricingCategory: Usage-Based\n  PricingUnit: MTok\n  BillingCurrency: USD\nmeters:\n  - name: input_tokens\n    unit: token\n    aggregation: sum\n    dimensions:\n      - model\n      - workspace\n      - service_tier\n      - inference_geo\n  - name: output_tokens\n    unit: token\n    aggregation: sum\n    dimensions:\n      - model\n      - workspace\n      - service_tier\n      - inference_geo\n  - name: cache_creation_input_tokens\n    unit: token\n    aggregation: sum\n    dimensions:\n      - model\n      - cache_ttl\n  - name: cache_read_input_tokens\n    unit: token\n    aggregation: sum\n    dimensions:\n \
  \     - model\n  - name: web_search_requests\n    unit: search\n    aggregation: sum\n    dimensions:\n      - workspace\n  - name: code_execution_container_hours\n    unit: container_hour\n    aggregation: sum\n    dimensions:\n      - workspace\ndiscountModels:\n  - name: Prompt caching\n    discount: Cache reads at 0.1x base input price\n  - name: Batch API\n    discount: 50% off both input and output tokens\n  - name: Volume / Enterprise\n    discount: Custom; contact sales\nunitEconomics:\n  - name: Cost per 1M input tokens (Sonnet)\n    metric: billed_cost / (input_tokens / 1_000_000)\n    target: $3.00\n  - name: Cache hit rate\n    metric: cache_read_input_tokens / total_input_tokens\n    target: '>50%'\n  - name: Effective input rate with caching\n    metric: (uncached_input * $3 + cached_input * $0.30) / total_input\n    target: <$1.50/MTok\nprinciples:\n  - name: Visibility\n    description: Use the Usage & Cost Admin API to surface per-workspace spend to teams in near real-time.\n\
  \  - name: Allocation\n    description: Tag requests with workspace, application, and feature dimensions for chargeback/showback.\n  - name: Optimization\n    description: Drive cache hit rates >50%, batch non-interactive workloads (50% discount), pick smallest\n      viable model.\n  - name: Accountability\n    description: Set per-workspace spend limits below tier ceilings to bound team budgets.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/anthropic/refs/heads/main/finops/anthropic-finops.yml
sources:
- https://www.anthropic.com/pricing
- https://platform.claude.com/docs/en/docs/about-claude/pricing
- https://platform.claude.com/docs/en/api/rate-limits
specification: FinOps Framework
tags:
- FinOps
- Cost Management
- FOCUS
- AI
- Tokens
---
