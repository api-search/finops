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
  - Credit
  - Adjustment
  chargeFrequency: Recurring
  pricingCategory: Usage-Based
description: FinOps framework definition for the Claude API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Claude
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Claude
  PublisherName: Claude
  ServiceCategory: Developer Tools / API
  ServiceName: Claude
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
name: Claude Finops
provider_name: Claude
provider_slug: claude
publisher_name: Claude
service_category: API
slug: claude-finops
source_filename: claude-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Claude\nproviderId: claude\npublisherName: Claude\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Artificial Intelligence\n  - Chatbot\n  - Conversational AI\n  - Generative AI\n  - Large Language Models\n  - Machine Learning\n  - Natural Language Processing\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Claude API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n\
  \  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and\
  \ SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Claude\n  ServiceCategory: Developer Tools / API\n  ProviderName: Claude\n  PublisherName: Claude\n  InvoiceIssuerName: Claude\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned\
  \ over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Claude Messages API\n    baseURL: https://api.anthropic.com/v1\n    tags:\n      - AI\n      - Conversational AI\n      - Large Language Models\n      - Natural Language Processing\n    serviceName: Claude Messages API\n    serviceCategory: API\n  - name: Claude Message Batches API\n    baseURL: https://api.anthropic.com/v1\n    tags:\n      - AI\n      - Asynchronous\n      - Batch Processing\n      - Large Language Models\n    serviceName: Claude Message Batches API\n    serviceCategory: API\n  - name: Claude Models API\n    baseURL: https://api.anthropic.com/v1\n    tags:\n      - AI\n      - Large Language Models\n      - Models\n\
  \    serviceName: Claude Models API\n    serviceCategory: API\n  - name: Claude Files API\n    baseURL: https://api.anthropic.com/v1\n    tags:\n      - AI\n      - Document Processing\n      - File Management\n      - Files\n    serviceName: Claude Files API\n    serviceCategory: API\n  - name: Claude Admin API\n    baseURL: https://api.anthropic.com/v1\n    tags:\n      - Administration\n      - AI\n      - API Keys\n      - Organization Management\n      - Workspaces\n    serviceName: Claude Admin API\n    serviceCategory: API\n  - name: Claude Usage and Cost API\n    baseURL: https://api.anthropic.com/v1\n    tags:\n      - AI\n      - Analytics\n      - Cost Tracking\n      - Usage\n    serviceName: Claude Usage and Cost API\n    serviceCategory: API\n  - name: Claude Text Completions API\n    baseURL: https://api.anthropic.com/v1\n    tags:\n      - AI\n      - Large Language Models\n      - Legacy\n      - Text Completion\n    serviceName: Claude Text Completions API\n    serviceCategory:\
  \ API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - name: Kin Lane\n    email: kin@apievangelist.com\n    url: https://apievangelist.com\n  - name: Anthropic\n    email: support@anthropic.com\n    url: https://www.anthropic.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/claude/refs/heads/main/finops/claude-finops.yml
sources: []
specification: FinOps Framework
tags:
- Artificial Intelligence
- Chatbot
- Conversational AI
- Generative AI
- Large Language Models
- Machine Learning
- Natural Language Processing
- FinOps
- Cost Management
- FOCUS
---
