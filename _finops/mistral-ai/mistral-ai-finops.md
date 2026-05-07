---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: mistral-ai-chat-completions-openapi.yml
  format: yaml
  label: Mistral AI Chat Completions API
  slug: chat-completions
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/mistral-ai/refs/heads/main/openapi/mistral-ai-chat-completions-openapi.yml
- filename: mistral-ai-embeddings-openapi.yml
  format: yaml
  label: Mistral AI Embeddings API
  slug: embeddings
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/mistral-ai/refs/heads/main/openapi/mistral-ai-embeddings-openapi.yml
- filename: mistral-ai-agents-openapi.yml
  format: yaml
  label: Mistral AI Agents API
  slug: agents
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/mistral-ai/refs/heads/main/openapi/mistral-ai-agents-openapi.yml
- filename: mistral-ai-fine-tuning-openapi.yml
  format: yaml
  label: Mistral AI Fine-Tuning API
  slug: fine-tuning
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/mistral-ai/refs/heads/main/openapi/mistral-ai-fine-tuning-openapi.yml
- filename: mistral-ai-ocr-openapi.yml
  format: yaml
  label: Mistral AI OCR API
  slug: ocr
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/mistral-ai/refs/heads/main/openapi/mistral-ai-ocr-openapi.yml
- filename: mistral-ai-models-openapi.yml
  format: yaml
  label: Mistral AI Models API
  slug: models
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/mistral-ai/refs/heads/main/openapi/mistral-ai-models-openapi.yml
- filename: mistral-ai-forge-openapi.yml
  format: yaml
  label: Mistral AI Forge API
  slug: forge
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/mistral-ai/refs/heads/main/openapi/mistral-ai-forge-openapi.yml
- filename: mistral-ai-batch-openapi.yml
  format: yaml
  label: Mistral AI Batch API
  slug: batch
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/mistral-ai/refs/heads/main/openapi/mistral-ai-batch-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  - Tax
  - Adjustment
  - Credit
  pricingCategory: Token-Based Usage + Subscription
description: 'FOCUS-aligned FinOps for Mistral AI: dual model — token-based pay-as-you-go pricing on la Plateforme (per-million-token input/output rates per model) and tiered per-user subscriptions for Le Chat (Free, Pro $14.99, Team $24.99, Enterprise custom). Mistral AI Studio adds a custom enterprise contract for production deployments.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Mistral AI
  ProviderName: Mistral AI
  PublisherName: Mistral AI
  ServiceCategory: AI Infrastructure
  ServiceName: Mistral AI
  ServiceSubcategory: Large Language Models
layout: finops
meters:
- aggregation: sum
  dimensions:
  - model
  - workspace
  - api_key
  name: tokens_input
  unit: token
- aggregation: sum
  dimensions:
  - model
  - workspace
  - api_key
  name: tokens_output
  unit: token
- aggregation: sum
  dimensions:
  - model
  - workspace
  name: voxtral_audio_minutes
  unit: minute
- aggregation: sum
  dimensions:
  - model
  - workspace
  name: ocr_pages
  unit: page
- aggregation: sum
  dimensions:
  - account
  name: le_chat_pro_seats
  unit: seat-month
- aggregation: sum
  dimensions:
  - account
  - assigned_user
  name: le_chat_team_seats
  unit: seat-month
- aggregation: count
  dimensions:
  - account
  name: studio_contract
  unit: contract-year
name: Mistral Ai Finops
provider_name: Mistral AI
provider_slug: mistral-ai
publisher_name: Mistral AI
service_category: AI Infrastructure
slug: mistral-ai-finops
source_filename: mistral-ai-finops.yml
source_heading: FinOps Profile
source_url: https://mistral.ai/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Mistral AI\nproviderId: mistral-ai\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Cost Management\n  - AI\n  - Large Language Models\ndescription: 'FOCUS-aligned FinOps for Mistral AI: dual model — token-based pay-as-you-go pricing on\n  la Plateforme (per-million-token input/output rates per model) and tiered per-user subscriptions for\n  Le Chat (Free, Pro $14.99, Team $24.99, Enterprise custom). Mistral AI Studio adds a custom enterprise\n  contract for production deployments.'\nsources:\n  - https://mistral.ai/pricing\n  - https://docs.mistral.ai/getting-started/models/models_overview/\n  - https://mistral.ai/products/la-plateforme\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\n\
  publisherName: Mistral AI\nserviceCategory: AI Infrastructure\nbillingModel:\n  pricingCategory: Token-Based Usage + Subscription\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Adjustment\n    - Credit\nfocusColumns:\n  ServiceName: Mistral AI\n  ServiceCategory: AI Infrastructure\n  ServiceSubcategory: Large Language Models\n  ProviderName: Mistral AI\n  PublisherName: Mistral AI\n  InvoiceIssuerName: Mistral AI\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: tokens_input\n    unit: token\n    aggregation: sum\n    dimensions:\n      - model\n      - workspace\n      - api_key\n  - name: tokens_output\n    unit: token\n    aggregation: sum\n    dimensions:\n      - model\n      - workspace\n      - api_key\n  - name: voxtral_audio_minutes\n    unit: minute\n    aggregation: sum\n    dimensions:\n      - model\n      - workspace\n  - name: ocr_pages\n    unit: page\n    aggregation: sum\n   \
  \ dimensions:\n      - model\n      - workspace\n  - name: le_chat_pro_seats\n    unit: seat-month\n    aggregation: sum\n    dimensions:\n      - account\n  - name: le_chat_team_seats\n    unit: seat-month\n    aggregation: sum\n    dimensions:\n      - account\n      - assigned_user\n  - name: studio_contract\n    unit: contract-year\n    aggregation: count\n    dimensions:\n      - account\nprinciples:\n  - name: Visibility\n    description: Pull token consumption from the la Plateforme usage console / API; export per-key,\n      per-model breakdowns; correlate with invoice charges.\n  - name: Allocation\n    description: Issue one API key per consuming product / team and tag spending by key; allocate\n      Le Chat Team seats by Entra ID / IdP group.\n  - name: Optimization\n    description: Right-size models — use Ministral 3B / Small 4 for cheap throughput and reserve Large 3\n      / Magistral for high-value reasoning; cap reasoning-effort to control output-token spikes; consider\n\
  \      self-hosting Mistral open-weight models for sustained high-volume workloads to avoid per-token\n      charges.\n  - name: Accountability\n    description: Assign a budget owner per API key; review token consumption weekly; alert when token\n      spend deviates >25% from forecast.\nmaintainers: []\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/mistral-ai/refs/heads/main/finops/mistral-ai-finops.yml
sources:
- https://mistral.ai/pricing
- https://docs.mistral.ai/getting-started/models/models_overview/
- https://mistral.ai/products/la-plateforme
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Cost Management
- AI
- Large Language Models
---
