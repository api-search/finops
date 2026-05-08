---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: osmapi-chat-completions-openapi.yml
  format: yaml
  label: osmAPI Chat Completions API
  slug: osmapi-chat-completions-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/osmapi/refs/heads/main/openapi/osmapi-chat-completions-openapi.yml
- filename: osmapi-anthropic-messages-openapi.yml
  format: yaml
  label: osmAPI Anthropic Messages API
  slug: osmapi-anthropic-messages-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/osmapi/refs/heads/main/openapi/osmapi-anthropic-messages-openapi.yml
- filename: osmapi-models-openapi.yml
  format: yaml
  label: osmAPI Models API
  slug: osmapi-models-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/osmapi/refs/heads/main/openapi/osmapi-models-openapi.yml
- filename: osmapi-health-openapi.yml
  format: yaml
  label: osmAPI Health API
  slug: osmapi-health-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/osmapi/refs/heads/main/openapi/osmapi-health-openapi.yml
billing_model:
  billingCurrency: USD (settlement); INR (top-up via Razorpay)
  billingFrequency: Continuous Settlement
  chargeCategories:
  - Usage
  - Purchase
  - Credit
  pricingCategory: Pay-As-You-Go (Prepaid Credit)
description: FOCUS-aligned FinOps definition for osmAPI. Pure pay-as-you-go pass-through model where each request returns its underlying-provider cost in the response, charged against prepaid credits.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: osmAPI
  ProviderName: osmAPI
  PublisherName: osmAPI
  ServiceCategory: AI Infrastructure
  ServiceName: osmAPI
layout: finops
meters:
- aggregation: sum
  description: Input/prompt tokens routed to upstream LLM provider
  dimensions:
  - model
  - upstream_provider
  - api_key
  name: tokens_input
  unit: token
- aggregation: sum
  description: Output/completion tokens returned by upstream LLM provider
  dimensions:
  - model
  - upstream_provider
  - api_key
  name: tokens_output
  unit: token
- aggregation: count
  description: Total request count for rate-limit accounting
  dimensions:
  - model
  - api_key
  - endpoint
  name: api_requests
  unit: request
- aggregation: sum
  description: Prepaid credit purchased via Razorpay, denominated in INR and converted to USD on use
  dimensions:
  - account
  name: credit_topup
  unit: INR
- aggregation: sum
  description: Credit drawn down by usage at upstream-provider rates
  dimensions:
  - account
  - model
  name: credit_consumed
  unit: USD
name: Osmapi Finops
provider_name: osmAPI
provider_slug: osmapi
publisher_name: osmAPI
service_category: AI Infrastructure
slug: osmapi-finops
source_filename: osmapi-finops.yml
source_heading: FinOps Profile
source_url: https://docs.osmapi.com/features/cost-breakdown
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: osmAPI\nproviderId: osmapi\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - AI\n  - LLM\n  - Gateway\ndescription: FOCUS-aligned FinOps definition for osmAPI. Pure pay-as-you-go pass-through model\n  where each request returns its underlying-provider cost in the response, charged against\n  prepaid credits.\nsources:\n  - https://docs.osmapi.com/features/cost-breakdown\n  - https://docs.osmapi.com/resources/rate-limits\n  - https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: osmAPI\nserviceCategory: AI Infrastructure\nbillingModel:\n  pricingCategory: Pay-As-You-Go (Prepaid Credit)\n\
  \  billingFrequency: Continuous Settlement\n  billingCurrency: USD (settlement); INR (top-up via Razorpay)\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Credit\nfocusColumns:\n  ServiceName: osmAPI\n  ServiceCategory: AI Infrastructure\n  ProviderName: osmAPI\n  PublisherName: osmAPI\n  InvoiceIssuerName: osmAPI\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: tokens_input\n    description: Input/prompt tokens routed to upstream LLM provider\n    unit: token\n    aggregation: sum\n    dimensions:\n      - model\n      - upstream_provider\n      - api_key\n  - name: tokens_output\n    description: Output/completion tokens returned by upstream LLM provider\n    unit: token\n    aggregation: sum\n    dimensions:\n      - model\n      - upstream_provider\n      - api_key\n  - name: api_requests\n    description: Total request count for rate-limit accounting\n    unit: request\n    aggregation: count\n    dimensions:\n      - model\n      - api_key\n      - endpoint\n\
  \  - name: credit_topup\n    description: Prepaid credit purchased via Razorpay, denominated in INR and converted to\n      USD on use\n    unit: INR\n    aggregation: sum\n    dimensions:\n      - account\n  - name: credit_consumed\n    description: Credit drawn down by usage at upstream-provider rates\n    unit: USD\n    aggregation: sum\n    dimensions:\n      - account\n      - model\nprinciples:\n  - name: Visibility\n    description: Every API response embeds cost data so consumers can track spend programmatically\n      per request. The dashboard at app.osmapi.com surfaces aggregate consumption.\n  - name: Allocation\n    description: Use distinct API keys per app/team to attribute token spend; the response-embedded\n      cost field can be logged to a downstream warehouse keyed by api_key, model, and consumer.\n  - name: Optimization\n    description: Route low-stakes/dev workloads to free models (200 rpm), reserve paid models\n      for production. Use osmAPI's smart routing to\
  \ pick lowest-cost provider for a given\n      capability, and turn on response caching where applicable.\n  - name: Accountability\n    description: Each API key should map to a budget owner. Monitor credit balance proactively;\n      account credit depletion stops further usage until top-up.\nmaintainers:\n  - FN: API Evangelist\n    email: info@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/osmapi/refs/heads/main/finops/osmapi-finops.yml
sources:
- https://docs.osmapi.com/features/cost-breakdown
- https://docs.osmapi.com/resources/rate-limits
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- AI
- LLM
- Gateway
---
