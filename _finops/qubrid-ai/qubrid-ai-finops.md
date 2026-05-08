---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: qubrid-ai-inference-openapi.yml
  format: yaml
  label: Qubrid AI Inference API
  slug: inference
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/qubrid-ai/refs/heads/main/openapi/qubrid-ai-inference-openapi.yml
- filename: qubrid-ai-compute-openapi.yml
  format: yaml
  label: Qubrid AI Compute API
  slug: compute
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/qubrid-ai/refs/heads/main/openapi/qubrid-ai-compute-openapi.yml
- filename: qubrid-ai-fine-tuning-openapi.yml
  format: yaml
  label: Qubrid AI Fine-Tuning API
  slug: fine-tuning
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/qubrid-ai/refs/heads/main/openapi/qubrid-ai-fine-tuning-openapi.yml
- filename: qubrid-ai-rag-openapi.yml
  format: yaml
  label: Qubrid AI RAG API
  slug: rag
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/qubrid-ai/refs/heads/main/openapi/qubrid-ai-rag-openapi.yml
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
description: FinOps framework definition for the Qubrid AI API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Qubrid AI
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Qubrid AI
  PublisherName: Qubrid AI
  ServiceCategory: Developer Tools / API
  ServiceName: Qubrid AI
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
name: Qubrid Ai Finops
provider_name: Qubrid AI
provider_slug: qubrid-ai
publisher_name: Qubrid AI
service_category: API
slug: qubrid-ai-finops
source_filename: qubrid-ai-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Qubrid AI\nproviderId: qubrid-ai\npublisherName: Qubrid AI\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Artificial Intelligence\n  - Cloud Computing\n  - GPU\n  - Inference\n  - Large Language Models\n  - Machine Learning\n  - NVIDIA\n  - Serverless\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Qubrid AI API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  -\
  \ name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n\
  \  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Qubrid AI\n  ServiceCategory: Developer Tools / API\n  ProviderName: Qubrid AI\n  PublisherName: Qubrid AI\n  InvoiceIssuerName: Qubrid AI\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned\
  \ over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Qubrid AI Inference API\n    baseURL: https://platform.qubrid.com/api/v1\n    tags:\n      - Artificial Intelligence\n      - Inference\n      - Large Language Models\n      - Machine Learning\n      - NVIDIA\n      - Serverless\n    serviceName: Qubrid AI Inference API\n    serviceCategory: API\n  - name: Qubrid AI Compute API\n    baseURL: https://platform.qubrid.com/api/v1\n    tags:\n      - Cloud Computing\n      - GPU\n      - NVIDIA\n      - Infrastructure\n    serviceName: Qubrid AI Compute API\n    serviceCategory: API\n  - name: Qubrid AI Fine-Tuning API\n    baseURL: https://platform.qubrid.com/api/v1\n    tags:\n    \
  \  - Artificial Intelligence\n      - Fine-Tuning\n      - Machine Learning\n      - Model Training\n    serviceName: Qubrid AI Fine-Tuning API\n    serviceCategory: API\n  - name: Qubrid AI RAG API\n    baseURL: https://platform.qubrid.com/api/v1\n    tags:\n      - Artificial Intelligence\n      - RAG\n      - Retrieval Augmented Generation\n      - Search\n      - Knowledge Management\n    serviceName: Qubrid AI RAG API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: API Evangelist\n    email: info@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/qubrid-ai/refs/heads/main/finops/qubrid-ai-finops.yml
sources: []
specification: FinOps Framework
tags:
- Artificial Intelligence
- Cloud Computing
- GPU
- Inference
- Large Language Models
- Machine Learning
- NVIDIA
- Serverless
- FinOps
- Cost Management
- FOCUS
---
