---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: openapi.json
  format: json
  label: OpenRouter
  slug: openrouter
  spec_type: OpenAPI
  url: https://openrouter.ai/openapi.json
- filename: openapi.json
  format: json
  label: OpenRouter Chat Completions API
  slug: chat-completions-api
  spec_type: OpenAPI
  url: https://openrouter.ai/openapi.json
- filename: openapi.json
  format: json
  label: OpenRouter Models API
  slug: models-api
  spec_type: OpenAPI
  url: https://openrouter.ai/openapi.json
- filename: openapi.json
  format: json
  label: OpenRouter Generation API
  slug: generation-api
  spec_type: OpenAPI
  url: https://openrouter.ai/openapi.json
- filename: openapi.json
  format: json
  label: OpenRouter Keys Management API
  slug: keys-api
  spec_type: OpenAPI
  url: https://openrouter.ai/openapi.json
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  pricingCategory: Pay-As-You-Go (Provider Passthrough + 5.5% Platform Fee)
description: FOCUS-aligned FinOps for OpenRouter.
focus_columns:
  BillingCurrency: USD
  ProviderName: OpenRouter
  PublisherName: OpenRouter
  ServiceCategory: AI Model Aggregation
  ServiceName: OpenRouter
layout: finops
meters:
- aggregation: sum
  dimensions:
  - model
  - provider
  name: input_tokens
  unit: token
- aggregation: sum
  dimensions:
  - model
  - provider
  name: output_tokens
  unit: token
- aggregation: sum
  name: credits_purchased
  unit: USD
- aggregation: sum
  name: platform_fees
  unit: USD
name: Openrouter Finops
provider_name: OpenRouter
provider_slug: openrouter
publisher_name: OpenRouter
service_category: AI Model Aggregation
slug: openrouter-finops
source_filename: openrouter-finops.yml
source_heading: FinOps Profile
source_url: https://openrouter.ai/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: OpenRouter\nproviderId: openrouter\ncreated: '2026-05-04'\nmodified: '2026-05-04'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - AI Model Aggregation\ndescription: FOCUS-aligned FinOps for OpenRouter.\nsources:\n  - https://openrouter.ai/pricing\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: OpenRouter\nserviceCategory: AI Model Aggregation\nbillingModel:\n  pricingCategory: Pay-As-You-Go (Provider Passthrough + 5.5% Platform Fee)\n  billingFrequency: Monthly\n  billingCurrency: USD\nfocusColumns:\n  ServiceName: OpenRouter\n  ServiceCategory: AI Model Aggregation\n  ProviderName: OpenRouter\n  PublisherName: OpenRouter\n  BillingCurrency: USD\nmeters:\n  - name: input_tokens\n\
  \    unit: token\n    aggregation: sum\n    dimensions:\n      - model\n      - provider\n  - name: output_tokens\n    unit: token\n    aggregation: sum\n    dimensions:\n      - model\n      - provider\n  - name: credits_purchased\n    unit: USD\n    aggregation: sum\n  - name: platform_fees\n    unit: USD\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Track OpenRouter consumption monthly.\n  - name: Allocation\n    description: Tag usage to teams/cost centers.\n  - name: Optimization\n    description: Right-size; reclaim unused entitlements.\n  - name: Accountability\n    description: Set spend alerts; quarterly review.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/openrouter/refs/heads/main/finops/openrouter-finops.yml
sources:
- https://openrouter.ai/pricing
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- AI Model Aggregation
---
