---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: openapi
  format: yaml
  label: Microsoft Graph API
  slug: microsoft-graph-api
  spec_type: OpenAPI
  url: https://developer.microsoft.com/en-us/graph/docs/concepts/openapi
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
description: FinOps framework definition for the Microsoft 365 Copilot API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Microsoft 365 Copilot
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Microsoft 365 Copilot
  PublisherName: Microsoft 365 Copilot
  ServiceCategory: Developer Tools / API
  ServiceName: Microsoft 365 Copilot
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
name: Microsoft 365 Copilot Finops
provider_name: Microsoft 365 Copilot
provider_slug: microsoft-365-copilot
publisher_name: Microsoft 365 Copilot
service_category: API
slug: microsoft-365-copilot-finops
source_filename: microsoft-365-copilot-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Microsoft 365 Copilot\nproviderId: microsoft-365-copilot\npublisherName: Microsoft 365 Copilot\nserviceCategory: API\ncreated: '2026-05-04'\nmodified: '2026-05-04'\ntags:\n  - Artificial Intelligence\n  - Copilot\n  - Enterprise\n  - LLM\n  - Microsoft 365\n  - Natural Language Processing\n  - Productivity\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Microsoft 365 Copilot API surface. Provides a FOCUS-aligned\n  mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams\
  \ in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n\
  \      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Microsoft 365 Copilot\n  ServiceCategory: Developer Tools / API\n  ProviderName: Microsoft 365 Copilot\n  PublisherName: Microsoft 365 Copilot\n  InvoiceIssuerName: Microsoft 365 Copilot\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      -\
  \ region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Microsoft Graph API\n    baseURL: https://graph.microsoft.com/v1.0\n    tags:\n      - AI\n      - Data Integration\n      - Microsoft 365\n      - Productivity\n    serviceName: Microsoft Graph API\n    serviceCategory: API\n  - name: Microsoft Copilot Studio API\n    baseURL: https://api.powerplatform.com/\n    tags:\n      - AI Development\n      - Automation\n      - Custom Plugins\n      - Low Code\n    serviceName: Microsoft Copilot Studio API\n    serviceCategory: API\n  - name: Microsoft 365 Copilot Extensibility API\n    baseURL: https://api.microsoft365.com/copilot/v1\n\
  \    tags:\n      - Custom Skills\n      - Extensibility\n      - Integration\n      - Plugins\n    serviceName: Microsoft 365 Copilot Extensibility API\n    serviceCategory: API\n  - name: Azure OpenAI Service API\n    baseURL: https://{resource-name}.openai.azure.com/\n    tags:\n      - AI\n      - Azure\n      - GPT\n      - Language Models\n      - Machine Learning\n    serviceName: Azure OpenAI Service API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - name: Microsoft\n    email: support@microsoft.com\n    url: https://www.microsoft.com/\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/microsoft-365-copilot/refs/heads/main/finops/microsoft-365-copilot-finops.yml
sources: []
specification: FinOps Framework
tags:
- Artificial Intelligence
- Copilot
- Enterprise
- LLM
- Microsoft 365
- Natural Language Processing
- Productivity
- FinOps
- Cost Management
- FOCUS
---
