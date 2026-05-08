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
  - Credit
  - Adjustment
  chargeFrequency: Recurring
  pricingCategory: Usage-Based
description: FinOps framework definition for the Google Gemini API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Google Gemini
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Google Gemini
  PublisherName: Google Gemini
  ServiceCategory: Developer Tools / API
  ServiceName: Google Gemini
layout: finops
meters:
- aggregation: sum
  description: Count of billable API requests
  dimensions:
  - api
  - endpoint
  - tier
  - region
  - consumer
  name: api_requests
  unit: request
- aggregation: sum
  description: Bytes returned over the network in API responses
  dimensions:
  - api
  - region
  - consumer
  name: data_egress
  unit: GB
- aggregation: sum
  description: Server-side compute consumed by the request, where applicable
  dimensions:
  - api
  - endpoint
  - tier
  name: compute_seconds
  unit: second
name: Google Gemini Finops
provider_name: Google Gemini
provider_slug: google-gemini
publisher_name: Google Gemini
service_category: API
slug: google-gemini-finops
source_filename: google-gemini-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Google Gemini\nproviderId: google-gemini\npublisherName: Google Gemini\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Agentic AI\n  - Artificial Intelligence\n  - Code Generation\n  - Embeddings\n  - Generative AI\n  - Image Generation\n  - LLM\n  - Machine Learning\n  - Multimodal\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Google Gemini API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams\
  \ in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n\
  \      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Google Gemini\n  ServiceCategory: Developer Tools / API\n  ProviderName: Google Gemini\n  PublisherName: Google Gemini\n  InvoiceIssuerName: Google Gemini\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name:\
  \ data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Gemini API\n    baseURL: https://generativelanguage.googleapis.com\n    tags:\n      - Audio Understanding\n      - Chat\n      - Image Understanding\n      - Multimodal\n      - Structured Output\n      - Text Generation\n      - Video Understanding\n    serviceName: Gemini API\n    serviceCategory: API\n  - name: Gemini Pro API\n    baseURL: https://generativelanguage.googleapis.com/v1beta/models/gemini-pro\n    tags:\n      - Reasoning\n      - Text Generation\n    serviceName: Gemini Pro API\n    serviceCategory: API\n  - name: Gemini Pro Vision API\n    baseURL: https://generativelanguage.googleapis.com/v1beta/models/gemini-pro-vision\n\
  \    tags:\n      - Image Understanding\n      - Multimodal\n      - Vision\n    serviceName: Gemini Pro Vision API\n    serviceCategory: API\n  - name: Gemini Ultra API\n    baseURL: https://generativelanguage.googleapis.com/v1beta/models/gemini-ultra\n    tags:\n      - Advanced AI\n      - Complex Tasks\n    serviceName: Gemini Ultra API\n    serviceCategory: API\n  - name: Gemini Embedding API\n    baseURL: https://generativelanguage.googleapis.com\n    tags:\n      - Embeddings\n      - Retrieval\n      - Semantic Search\n      - Text Similarity\n    serviceName: Gemini Embedding API\n    serviceCategory: API\n  - name: Gemini Live API\n    baseURL: https://generativelanguage.googleapis.com\n    tags:\n      - Multimodal\n      - Real-Time\n      - Streaming\n      - Video\n      - Voice\n      - WebSockets\n    serviceName: Gemini Live API\n    serviceCategory: API\n  - name: Gemini Context Caching API\n    baseURL: https://generativelanguage.googleapis.com\n    tags:\n      - Caching\n\
  \      - Cost Optimization\n      - Performance\n    serviceName: Gemini Context Caching API\n    serviceCategory: API\n  - name: Gemini Fine-Tuning API\n    baseURL: https://generativelanguage.googleapis.com\n    tags:\n      - Fine-Tuning\n      - Model Customization\n      - Supervised Learning\n    serviceName: Gemini Fine-Tuning API\n    serviceCategory: API\n  - name: Gemini Interactions API\n    baseURL: https://generativelanguage.googleapis.com\n    tags:\n      - Agents\n      - Interactions\n      - Multi-Turn\n      - Tool Use\n    serviceName: Gemini Interactions API\n    serviceCategory: API\n  - name: Vertex AI Gemini API\n    baseURL: https://aiplatform.googleapis.com\n    tags:\n      - Enterprise\n      - Generative AI\n      - Google Cloud\n      - Vertex AI\n    serviceName: Vertex AI Gemini API\n    serviceCategory: API\n  - name: Vertex AI Imagen API\n    baseURL: https://aiplatform.googleapis.com\n    tags:\n      - Google Cloud\n      - Image Generation\n      -\
  \ Imagen\n      - Text-To-Image\n    serviceName: Vertex AI Imagen API\n    serviceCategory: API\n  - name: Vertex AI Gemini Live API\n    baseURL: https://aiplatform.googleapis.com\n    tags:\n      - Enterprise\n      - Real-Time\n      - Streaming\n      - Vertex AI\n      - Video\n      - Voice\n    serviceName: Vertex AI Gemini Live API\n    serviceCategory: API\n  - name: Vertex AI Text Embeddings API\n    baseURL: https://aiplatform.googleapis.com\n    tags:\n      - Embeddings\n      - Semantic Search\n      - Text Similarity\n      - Vertex AI\n    serviceName: Vertex AI Text Embeddings API\n    serviceCategory: API\n  - name: Firebase AI Logic API\n    baseURL: https://firebaseml.googleapis.com\n    tags:\n      - Client-Side\n      - Firebase\n      - Mobile\n      - Web\n    serviceName: Firebase AI Logic API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active\
  \ Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/google-gemini/refs/heads/main/finops/google-gemini-finops.yml
sources: []
specification: FinOps Framework
tags:
- Agentic AI
- Artificial Intelligence
- Code Generation
- Embeddings
- Generative AI
- Image Generation
- LLM
- Machine Learning
- Multimodal
- FinOps
- Cost Management
- FOCUS
---
