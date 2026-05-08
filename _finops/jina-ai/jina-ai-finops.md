---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: jina-ai-embeddings-openapi.yml
  format: yaml
  label: Jina AI Embeddings API
  slug: embeddings-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/jina-ai/refs/heads/main/openapi/jina-ai-embeddings-openapi.yml
- filename: jina-ai-reader-openapi.yml
  format: yaml
  label: Jina AI Reader API
  slug: reader-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/jina-ai/refs/heads/main/openapi/jina-ai-reader-openapi.yml
- filename: jina-ai-reranker-openapi.yml
  format: yaml
  label: Jina AI Reranker API
  slug: reranker-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/jina-ai/refs/heads/main/openapi/jina-ai-reranker-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: On-Demand
  chargeCategories:
  - Purchase
  - Usage
  - Refund
  - Credit
  pricingCategory: Token-Based Usage
description: 'FOCUS-aligned FinOps for Jina AI: token-based pay-as-you-go metering across Embeddings, Reranker, Reader, Classifier, Segmenter, and DeepSearch. Token balance on the API key drives both cost and the rate-limit tier (Free / Paid / Premium). Cloud-marketplace procurement available via AWS, Azure, GCP.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Jina AI GmbH
  ProviderName: Jina AI
  PublisherName: Jina AI GmbH
  ServiceCategory: AI Infrastructure
  ServiceName: Jina AI
layout: finops
meters:
- aggregation: sum
  dimensions:
  - service
  - model
  - api_key
  name: tokens_consumed
  unit: token
- aggregation: sum
  dimensions:
  - model
  - input_modality
  name: embedding_requests
  unit: request
- aggregation: sum
  dimensions:
  - model
  name: reranker_requests
  unit: request
- aggregation: sum
  dimensions:
  - mode
  name: reader_requests
  unit: request
- aggregation: max
  dimensions:
  - api_key
  name: token_balance
  unit: token
name: Jina Ai Finops
provider_name: Jina AI
provider_slug: jina-ai
publisher_name: Jina AI GmbH
service_category: AI Infrastructure
slug: jina-ai-finops
source_filename: jina-ai-finops.yml
source_heading: FinOps Profile
source_url: https://jina.ai/embeddings/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Jina AI\nproviderId: jina-ai\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - AI\n  - Embeddings\n  - LLM\ndescription: 'FOCUS-aligned FinOps for Jina AI: token-based pay-as-you-go metering across Embeddings,\n  Reranker, Reader, Classifier, Segmenter, and DeepSearch. Token balance on the API key drives both\n  cost and the rate-limit tier (Free / Paid / Premium). Cloud-marketplace procurement available via\n  AWS, Azure, GCP.'\nsources:\n  - https://jina.ai/embeddings/\n  - https://jina.ai/api-dashboard/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Jina AI GmbH\nserviceCategory: AI Infrastructure\nbillingModel:\n  pricingCategory:\
  \ Token-Based Usage\n  billingFrequency: On-Demand\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\n    - Refund\n    - Credit\nfocusColumns:\n  ServiceName: Jina AI\n  ServiceCategory: AI Infrastructure\n  ProviderName: Jina AI\n  PublisherName: Jina AI GmbH\n  InvoiceIssuerName: Jina AI GmbH\n  BillingCurrency: USD\nmeters:\n  - name: tokens_consumed\n    unit: token\n    aggregation: sum\n    dimensions:\n      - service\n      - model\n      - api_key\n  - name: embedding_requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - model\n      - input_modality\n  - name: reranker_requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - model\n  - name: reader_requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - mode\n  - name: token_balance\n    unit: token\n    aggregation: max\n    dimensions:\n      - api_key\nprinciples:\n  - name: Visibility\n    description: Use the Jina API Dashboard to monitor\
  \ remaining token balance per API key and per-service\n      consumption; export usage to your data warehouse for FOCUS-aligned reporting.\n  - name: Allocation\n    description: Issue separate API keys per team / product / environment so token consumption maps\n      cleanly to a chargeback dimension; tag application traces with the key identifier.\n  - name: Optimization\n    description: Choose the smallest model that hits quality bar (e.g., jina-embeddings-v2 vs v3),\n      truncate input text before embedding, cache embeddings of stable corpora, batch reranker queries,\n      and use the Reader caching path (r.jina.ai) for stable URLs.\n  - name: Accountability\n    description: AI / Search platform owner reconciles monthly Stripe invoices (or marketplace bills)\n      against forecasted token spend; sets balance-low alerts on production keys.\nmaintainers:\n  - FN: API Evangelist\n    email: info@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/jina-ai/refs/heads/main/finops/jina-ai-finops.yml
sources:
- https://jina.ai/embeddings/
- https://jina.ai/api-dashboard/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- AI
- Embeddings
- LLM
---
