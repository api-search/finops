---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: google-gemini-api-openapi.yml
  format: yaml
  label: Gemini API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/google-gemini/refs/heads/main/openapi/google-gemini-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  - Tax
  - Adjustment
  - Credit
  pricingCategory: Token-Based Usage
description: 'FOCUS-aligned FinOps for Gemini API: per-model token-based pay-as-you-go pricing with separate input vs output rates and multimodal-vs-audio bands; long-context price tiers above 200K-token prompts; Batch API offering 50% off; optional Google Search grounding meter; Enterprise via Vertex AI with provisioned throughput. Spend rolls into the standard Google Cloud Billing pipeline.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Google LLC
  ProviderName: Google Cloud
  PublisherName: Google LLC
  ServiceCategory: AI Infrastructure
  ServiceName: Gemini API
layout: finops
meters:
- aggregation: sum
  description: Input tokens billed per model and modality band
  dimensions:
  - model
  - modality
  - prompt_length_band
  - project
  name: tokens_input
  unit: token
- aggregation: sum
  description: Output tokens billed per model and band
  dimensions:
  - model
  - prompt_length_band
  - project
  name: tokens_output
  unit: token
- aggregation: sum
  description: Tokens served from context cache (lower rate than fresh input)
  dimensions:
  - model
  - cache_id
  - project
  name: tokens_cached
  unit: token
- aggregation: sum
  description: Input tokens billed via the Batch API (50% discount)
  dimensions:
  - model
  - project
  name: batch_tokens_input
  unit: token
- aggregation: sum
  description: Output tokens billed via the Batch API (50% discount)
  dimensions:
  - model
  - project
  name: batch_tokens_output
  unit: token
- aggregation: sum
  description: Google Search grounding queries (free up to 5K/month, then $14/1K)
  dimensions:
  - model
  - project
  name: search_grounding_queries
  unit: request
- aggregation: sum
  description: Reserved Gemini capacity hours via Vertex AI Enterprise
  dimensions:
  - model
  - region
  - project
  name: provisioned_throughput
  unit: hour
name: Google Gemini Finops
provider_name: Google Gemini
provider_slug: google-gemini
publisher_name: Google LLC
service_category: AI Infrastructure / LLM
slug: google-gemini-finops
source_filename: google-gemini-finops.yml
source_heading: FinOps Profile
source_url: https://ai.google.dev/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Google Gemini\nproviderId: google-gemini\npublisherName: Google LLC\nserviceCategory: AI Infrastructure / LLM\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - Generative AI\n  - LLM\n  - AI Infrastructure\n  - Google\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps for Gemini API: per-model token-based pay-as-you-go pricing with separate\n  input vs output rates and multimodal-vs-audio bands; long-context price tiers above 200K-token prompts;\n  Batch API offering 50% off; optional Google Search grounding meter; Enterprise via Vertex AI with provisioned\n  throughput. Spend rolls into the standard Google Cloud\
  \ Billing pipeline.'\nsources:\n  - https://ai.google.dev/pricing\n  - https://ai.google.dev/gemini-api/docs/rate-limits\n  - https://cloud.google.com/vertex-ai/generative-ai/pricing\nbillingModel:\n  pricingCategory: Token-Based Usage\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Adjustment\n    - Credit\nfocusColumns:\n  ServiceName: Gemini API\n  ServiceCategory: AI Infrastructure\n  ProviderName: Google Cloud\n  PublisherName: Google LLC\n  InvoiceIssuerName: Google LLC\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: tokens_input\n    description: Input tokens billed per model and modality band\n    unit: token\n    aggregation: sum\n    dimensions:\n      - model\n      - modality\n      - prompt_length_band\n      - project\n  - name: tokens_output\n    description: Output tokens billed per model and band\n    unit: token\n    aggregation: sum\n    dimensions:\n      - model\n      - prompt_length_band\n\
  \      - project\n  - name: tokens_cached\n    description: Tokens served from context cache (lower rate than fresh input)\n    unit: token\n    aggregation: sum\n    dimensions:\n      - model\n      - cache_id\n      - project\n  - name: batch_tokens_input\n    description: Input tokens billed via the Batch API (50% discount)\n    unit: token\n    aggregation: sum\n    dimensions:\n      - model\n      - project\n  - name: batch_tokens_output\n    description: Output tokens billed via the Batch API (50% discount)\n    unit: token\n    aggregation: sum\n    dimensions:\n      - model\n      - project\n  - name: search_grounding_queries\n    description: Google Search grounding queries (free up to 5K/month, then $14/1K)\n    unit: request\n    aggregation: sum\n    dimensions:\n      - model\n      - project\n  - name: provisioned_throughput\n    description: Reserved Gemini capacity hours via Vertex AI Enterprise\n    unit: hour\n    aggregation: sum\n    dimensions:\n      - model\n\
  \      - region\n      - project\napis:\n  - name: Gemini API (AI Studio)\n    baseURL: https://generativelanguage.googleapis.com\n    serviceName: Gemini API\n    serviceCategory: AI Infrastructure\n  - name: Gemini via Vertex AI\n    baseURL: https://aiplatform.googleapis.com\n    serviceName: Vertex AI Generative AI\n    serviceCategory: AI Infrastructure\nprinciples:\n  - name: Visibility\n    description: Enable Cloud Billing detailed export to BigQuery filtered to the Gemini API SKU; surface\n      per-call token counts via the response usage metadata and your application logs for per-feature\n      attribution.\n  - name: Allocation\n    description: Tag Gemini calls with team/feature labels; use separate API keys (or Cloud projects)\n      per team for first-class cost allocation; for Vertex AI usage, tag the Vertex AI endpoint with org\n      labels.\n  - name: Optimization\n    description: Choose the smallest model that meets quality (Flash-Lite for routine traffic, Flash for\n\
  \      mixed workloads, Pro only for high-stakes prompts); enable context caching for repeated long-system-prompt\n      patterns; route async/non-latency-sensitive workloads through the Batch API for 50% discount; trim\n      prompts to stay under the 200K-token long-context band; share the 5K free Search grounding allowance\n      across teams.\n  - name: Accountability\n    description: Set per-project Cloud Billing budgets aligned with Gemini API tier caps ($250/$2,000/$20,000+);\n      designate a model owner per feature; review monthly token burn vs business value (cost-per-resolved-ticket,\n      cost-per-classification, etc.).\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/google-gemini/refs/heads/main/finops/google-gemini-finops.yml
sources:
- https://ai.google.dev/pricing
- https://ai.google.dev/gemini-api/docs/rate-limits
- https://cloud.google.com/vertex-ai/generative-ai/pricing
specification: FinOps Framework
tags:
- Generative AI
- LLM
- AI Infrastructure
- Google
- FinOps
- FOCUS
---
