---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: langfuse-openapi.yml
  format: yaml
  label: Langfuse Tracing API
  slug: langfuse-tracing-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/langfuse/refs/heads/main/openapi/langfuse-openapi.yml
- filename: langfuse-openapi.yml
  format: yaml
  label: Langfuse Observations API
  slug: langfuse-observations-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/langfuse/refs/heads/main/openapi/langfuse-openapi.yml
- filename: langfuse-openapi.yml
  format: yaml
  label: Langfuse Metrics API
  slug: langfuse-metrics-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/langfuse/refs/heads/main/openapi/langfuse-openapi.yml
- filename: langfuse-openapi.yml
  format: yaml
  label: Langfuse Prompt Management API
  slug: langfuse-prompts-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/langfuse/refs/heads/main/openapi/langfuse-openapi.yml
- filename: langfuse-openapi.yml
  format: yaml
  label: Langfuse Datasets API
  slug: langfuse-datasets-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/langfuse/refs/heads/main/openapi/langfuse-openapi.yml
- filename: langfuse-openapi.yml
  format: yaml
  label: Langfuse Evaluations API
  slug: langfuse-evaluations-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/langfuse/refs/heads/main/openapi/langfuse-openapi.yml
- filename: langfuse-openapi.yml
  format: yaml
  label: Langfuse Scores API
  slug: langfuse-scores-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/langfuse/refs/heads/main/openapi/langfuse-openapi.yml
- filename: langfuse-openapi.yml
  format: yaml
  label: Langfuse Organizations & Projects API
  slug: langfuse-organizations-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/langfuse/refs/heads/main/openapi/langfuse-openapi.yml
- filename: langfuse-openapi.yml
  format: yaml
  label: Langfuse Instance Management API
  slug: langfuse-instance-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/langfuse/refs/heads/main/openapi/langfuse-openapi.yml
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
description: FinOps framework definition for the Langfuse API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Langfuse
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Langfuse
  PublisherName: Langfuse
  ServiceCategory: Developer Tools / API
  ServiceName: Langfuse
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
name: Langfuse Finops
provider_name: Langfuse
provider_slug: langfuse
publisher_name: Langfuse
service_category: API
slug: langfuse-finops
source_filename: langfuse-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Langfuse\nproviderId: langfuse\npublisherName: Langfuse\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - AI\n  - LLM\n  - Observability\n  - Open Source\n  - Evaluations\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Langfuse API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming\
  \ team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice\
  \ Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Langfuse\n  ServiceCategory: Developer Tools / API\n  ProviderName: Langfuse\n  PublisherName: Langfuse\n  InvoiceIssuerName: Langfuse\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n\
  \      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Langfuse Tracing API\n    baseURL: https://cloud.langfuse.com/api/public\n    tags:\n      - Tracing\n      - OpenTelemetry\n      - Ingestion\n    serviceName: Langfuse Tracing API\n    serviceCategory: API\n  - name: Langfuse Observations API\n    baseURL: https://cloud.langfuse.com/api/public\n    tags:\n      - Observations\n      - Spans\n      - Generations\n    serviceName: Langfuse Observations API\n    serviceCategory: API\n  - name: Langfuse Metrics API\n    baseURL: https://cloud.langfuse.com/api/public\n    tags:\n      - Metrics\n      - Analytics\n      - Reporting\n    serviceName: Langfuse Metrics API\n    serviceCategory: API\n  - name: Langfuse Prompt Management API\n    baseURL: https://cloud.langfuse.com/api/public\n\
  \    tags:\n      - Prompts\n      - Versioning\n      - Prompt Management\n    serviceName: Langfuse Prompt Management API\n    serviceCategory: API\n  - name: Langfuse Datasets API\n    baseURL: https://cloud.langfuse.com/api/public\n    tags:\n      - Datasets\n      - Test Data\n      - Evaluations\n    serviceName: Langfuse Datasets API\n    serviceCategory: API\n  - name: Langfuse Evaluations API\n    baseURL: https://cloud.langfuse.com/api/public\n    tags:\n      - Evaluations\n      - Scoring\n      - LLM-as-Judge\n    serviceName: Langfuse Evaluations API\n    serviceCategory: API\n  - name: Langfuse Scores API\n    baseURL: https://cloud.langfuse.com/api/public\n    tags:\n      - Scores\n      - Feedback\n      - Quality\n    serviceName: Langfuse Scores API\n    serviceCategory: API\n  - name: Langfuse Organizations & Projects API\n    baseURL: https://cloud.langfuse.com/api/public\n    tags:\n      - Organizations\n      - Projects\n      - Provisioning\n    serviceName:\
  \ Langfuse Organizations & Projects API\n    serviceCategory: API\n  - name: Langfuse Instance Management API\n    baseURL: https://cloud.langfuse.com/api/public\n    tags:\n      - Self-Hosted\n      - Administration\n      - Instance\n    serviceName: Langfuse Instance Management API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/langfuse/refs/heads/main/finops/langfuse-finops.yml
sources: []
specification: FinOps Framework
tags:
- AI
- LLM
- Observability
- Open Source
- Evaluations
- FinOps
- Cost Management
- FOCUS
---
