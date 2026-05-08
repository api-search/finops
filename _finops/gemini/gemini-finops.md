---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: rest
  format: yaml
  label: Gemini REST API
  slug: ''
  spec_type: OpenAPI
  url: https://generativelanguage.googleapis.com/$discovery/rest?version=v1beta&key=YOUR_API_KEY
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
description: FinOps framework definition for the Gemini API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Gemini
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Gemini
  PublisherName: Gemini
  ServiceCategory: Developer Tools / API
  ServiceName: Gemini
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
name: Gemini Finops
provider_name: Gemini
provider_slug: gemini
publisher_name: Gemini
service_category: API
slug: gemini-finops
source_filename: gemini-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Gemini\nproviderId: gemini\npublisherName: Gemini\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Agents\n  - Artificial Intelligence\n  - Audio Understanding\n  - Batch Processing\n  - Deep Research\n  - Document Understanding\n  - Embeddings\n  - Function Calling\n  - Generative Ai\n  - Image Generation\n  - Large Language Models\n  - Machine Learning\n  - Multimodal\n  - Structured Output\n  - Text-To-Speech\n  - Video Generation\n  - Video Understanding\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Gemini API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics\
  \ reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n\
  \  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Gemini\n  ServiceCategory: Developer Tools / API\n  ProviderName: Gemini\n  PublisherName: Gemini\n  InvoiceIssuerName: Gemini\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n\
  \    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Gemini REST API\n    baseURL: https://generativelanguage.googleapis.com\n    tags:\n      - Chat\n      - Embeddings\n      - Generative Ai\n      - Multimodal\n      - Rest\n      - Streaming\n      - Text Generation\n    serviceName: Gemini REST API\n    serviceCategory: API\n  - name: Gemini Python SDK\n    baseURL: https://pypi.org/project/google-generativeai/\n    tags:\n      - Client Library\n      - Python\n      - Sdk\n    serviceName:\
  \ Gemini Python SDK\n    serviceCategory: API\n  - name: Gemini Node.js SDK\n    baseURL: https://www.npmjs.com/package/@google/generative-ai\n    tags:\n      - Client Library\n      - Javascript\n      - Nodejs\n      - Sdk\n      - Typescript\n    serviceName: Gemini Node.js SDK\n    serviceCategory: API\n  - name: Gemini Go SDK\n    baseURL: https://pkg.go.dev/google.golang.org/genai\n    tags:\n      - Client Library\n      - Go\n      - Golang\n      - Sdk\n    serviceName: Gemini Go SDK\n    serviceCategory: API\n  - name: Gemini Java SDK\n    baseURL: https://central.sonatype.com/artifact/com.google.genai/google-genai\n    tags:\n      - Client Library\n      - Java\n      - Sdk\n    serviceName: Gemini Java SDK\n    serviceCategory: API\n  - name: Gemini C# SDK\n    baseURL: https://www.nuget.org/packages/Google.GenAI\n    tags:\n      - Client Library\n      - Csharp\n      - Dotnet\n      - Sdk\n    serviceName: Gemini C# SDK\n    serviceCategory: API\n  - name: Gemini Live\
  \ API\n    baseURL: https://generativelanguage.googleapis.com\n    tags:\n      - Live\n      - Real-Time\n      - Streaming\n      - Video\n      - Voice\n      - Websocket\n    serviceName: Gemini Live API\n    serviceCategory: API\n  - name: Gemini Interactions API\n    baseURL: https://generativelanguage.googleapis.com\n    tags:\n      - Agents\n      - Interactions\n      - State Management\n      - Tool Orchestration\n    serviceName: Gemini Interactions API\n    serviceCategory: API\n  - name: Gemini Image Generation API\n    baseURL: https://generativelanguage.googleapis.com\n    tags:\n      - Generative Ai\n      - Image Editing\n      - Image Generation\n      - Text-To-Image\n    serviceName: Gemini Image Generation API\n    serviceCategory: API\n  - name: Gemini Video Generation API\n    baseURL: https://generativelanguage.googleapis.com\n    tags:\n      - Generative Ai\n      - Image-To-Video\n      - Text-To-Video\n      - Veo\n      - Video Generation\n    serviceName:\
  \ Gemini Video Generation API\n    serviceCategory: API\n  - name: Gemini Text-to-Speech API\n    baseURL: https://generativelanguage.googleapis.com\n    tags:\n      - Audio Generation\n      - Multi-Speaker\n      - Speech Synthesis\n      - Text-To-Speech\n      - Tts\n    serviceName: Gemini Text-to-Speech API\n    serviceCategory: API\n  - name: Gemini Files API\n    baseURL: https://generativelanguage.googleapis.com\n    tags:\n      - Documents\n      - Files\n      - Media\n      - Storage\n      - Upload\n    serviceName: Gemini Files API\n    serviceCategory: API\n  - name: Gemini Embeddings API\n    baseURL: https://generativelanguage.googleapis.com\n    tags:\n      - Embeddings\n      - Rag\n      - Semantic Search\n      - Text Embeddings\n      - Vector Search\n    serviceName: Gemini Embeddings API\n    serviceCategory: API\n  - name: Gemini Batch API\n    baseURL: https://generativelanguage.googleapis.com\n    tags:\n      - Asynchronous\n      - Batch\n      - Bulk Processing\n\
  \      - Cost Optimization\n    serviceName: Gemini Batch API\n    serviceCategory: API\n  - name: Gemini Deep Research API\n    baseURL: https://generativelanguage.googleapis.com\n    tags:\n      - Agents\n      - Deep Research\n      - Reports\n      - Research\n      - Web Search\n    serviceName: Gemini Deep Research API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n    url: https://apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/gemini/refs/heads/main/finops/gemini-finops.yml
sources: []
specification: FinOps Framework
tags:
- Agents
- Artificial Intelligence
- Audio Understanding
- Batch Processing
- Deep Research
- Document Understanding
- Embeddings
- Function Calling
- Generative Ai
- Image Generation
- Large Language Models
- Machine Learning
- Multimodal
- Structured Output
- Text-To-Speech
- Video Generation
- Video Understanding
- FinOps
- Cost Management
- FOCUS
---
