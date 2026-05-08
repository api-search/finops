---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: writer-openapi.yml
  format: yaml
  label: Writer Chat Completion API
  slug: writer-chat-completion-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/writer/refs/heads/main/openapi/writer-openapi.yml
- filename: writer-openapi.yml
  format: yaml
  label: Writer Text Generation API
  slug: writer-text-generation-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/writer/refs/heads/main/openapi/writer-openapi.yml
- filename: writer-openapi.yml
  format: yaml
  label: Writer Tool Calling API
  slug: writer-tool-calling-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/writer/refs/heads/main/openapi/writer-openapi.yml
- filename: writer-openapi.yml
  format: yaml
  label: Writer Knowledge Graph API
  slug: writer-knowledge-graph-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/writer/refs/heads/main/openapi/writer-openapi.yml
- filename: writer-openapi.yml
  format: yaml
  label: Writer Files API
  slug: writer-files-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/writer/refs/heads/main/openapi/writer-openapi.yml
- filename: writer-openapi.yml
  format: yaml
  label: Writer Applications API
  slug: writer-applications-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/writer/refs/heads/main/openapi/writer-openapi.yml
- filename: writer-openapi.yml
  format: yaml
  label: Writer Vision API
  slug: writer-vision-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/writer/refs/heads/main/openapi/writer-openapi.yml
- filename: writer-openapi.yml
  format: yaml
  label: Writer Web Search API
  slug: writer-web-search-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/writer/refs/heads/main/openapi/writer-openapi.yml
- filename: writer-openapi.yml
  format: yaml
  label: Writer Translation API
  slug: writer-translation-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/writer/refs/heads/main/openapi/writer-openapi.yml
- filename: writer-openapi.yml
  format: yaml
  label: Writer Models API
  slug: writer-models-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/writer/refs/heads/main/openapi/writer-openapi.yml
- filename: writer-openapi.yml
  format: yaml
  label: Writer Guardrails API
  slug: writer-guardrails-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/writer/refs/heads/main/openapi/writer-openapi.yml
- filename: writer-openapi.yml
  format: yaml
  label: Writer API Keys API
  slug: writer-api-keys-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/writer/refs/heads/main/openapi/writer-openapi.yml
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
description: FinOps framework definition for the Writer API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Writer
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Writer
  PublisherName: Writer
  ServiceCategory: Developer Tools / API
  ServiceName: Writer
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
name: Writer Finops
provider_name: Writer
provider_slug: writer
publisher_name: Writer
service_category: API
slug: writer-finops
source_filename: writer-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Writer\nproviderId: writer\npublisherName: Writer\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - AI\n  - LLM\n  - Enterprise\n  - Content Generation\n  - Palmyra\n  - Agents\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Writer API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming\
  \ team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice\
  \ Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Writer\n  ServiceCategory: Developer Tools / API\n  ProviderName: Writer\n  PublisherName: Writer\n  InvoiceIssuerName: Writer\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n\
  \      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Writer Chat Completion API\n    baseURL: https://api.writer.com/v1\n    tags:\n      - Chat\n      - Completions\n      - LLM\n    serviceName: Writer Chat Completion API\n    serviceCategory: API\n  - name: Writer Text Generation API\n    baseURL: https://api.writer.com/v1\n    tags:\n      - Completions\n      - Text Generation\n    serviceName: Writer Text Generation API\n    serviceCategory: API\n  - name: Writer Tool Calling API\n    baseURL: https://api.writer.com/v1\n    tags:\n      - Tools\n      - Function Calling\n    serviceName: Writer Tool Calling API\n    serviceCategory: API\n  - name: Writer Knowledge Graph API\n    baseURL: https://api.writer.com/v1\n    tags:\n      - Knowledge Graph\n      - RAG\n\
  \      - Retrieval\n    serviceName: Writer Knowledge Graph API\n    serviceCategory: API\n  - name: Writer Files API\n    baseURL: https://api.writer.com/v1\n    tags:\n      - Files\n      - Storage\n      - Documents\n    serviceName: Writer Files API\n    serviceCategory: API\n  - name: Writer Applications API\n    baseURL: https://api.writer.com/v1\n    tags:\n      - Applications\n      - No-Code\n      - Agents\n    serviceName: Writer Applications API\n    serviceCategory: API\n  - name: Writer Vision API\n    baseURL: https://api.writer.com/v1\n    tags:\n      - Vision\n      - Multimodal\n      - Documents\n    serviceName: Writer Vision API\n    serviceCategory: API\n  - name: Writer Web Search API\n    baseURL: https://api.writer.com/v1\n    tags:\n      - Web Search\n      - Real-Time\n    serviceName: Writer Web Search API\n    serviceCategory: API\n  - name: Writer Translation API\n    baseURL: https://api.writer.com/v1\n    tags:\n      - Translation\n      - Languages\n\
  \    serviceName: Writer Translation API\n    serviceCategory: API\n  - name: Writer Models API\n    baseURL: https://api.writer.com/v1\n    tags:\n      - Models\n      - Catalog\n    serviceName: Writer Models API\n    serviceCategory: API\n  - name: Writer Guardrails API\n    baseURL: https://api.writer.com/v1\n    tags:\n      - Guardrails\n      - Safety\n      - PII\n    serviceName: Writer Guardrails API\n    serviceCategory: API\n  - name: Writer API Keys API\n    baseURL: https://api.writer.com/v1\n    tags:\n      - API Keys\n      - Authentication\n    serviceName: Writer API Keys API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/writer/refs/heads/main/finops/writer-finops.yml
sources: []
specification: FinOps Framework
tags:
- AI
- LLM
- Enterprise
- Content Generation
- Palmyra
- Agents
- FinOps
- Cost Management
- FOCUS
---
