---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
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
description: FinOps framework definition for the Hugging Face Transformers API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Hugging Face Transformers
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Hugging Face Transformers
  PublisherName: Hugging Face Transformers
  ServiceCategory: Developer Tools / API
  ServiceName: Hugging Face Transformers
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
name: Hugging Face Transformers Finops
provider_name: Hugging Face Transformers
provider_slug: hugging-face-transformers
publisher_name: Hugging Face Transformers
service_category: API
slug: hugging-face-transformers-finops
source_filename: hugging-face-transformers-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Hugging Face Transformers\nproviderId: hugging-face-transformers\npublisherName: Hugging Face Transformers\nserviceCategory: API\ncreated: '2026-05-04'\nmodified: '2026-05-04'\ntags:\n  - Artificial Intelligence\n  - Computer Vision\n  - Deep Learning\n  - Machine Learning\n  - Natural Language Processing\n  - Open Source\n  - Transformers\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Hugging Face Transformers API surface. Provides a FOCUS-aligned\n  mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to\
  \ engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload\
  \ Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Hugging Face Transformers\n  ServiceCategory: Developer Tools / API\n  ProviderName: Hugging Face Transformers\n  PublisherName: Hugging Face Transformers\n  InvoiceIssuerName: Hugging Face Transformers\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n\
  \      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Hugging Face Transformers Library\n    baseURL: ''\n    tags:\n      - Library\n      - Open Source\n      - Pipelines\n      - Python\n    serviceName: Hugging Face Transformers Library\n    serviceCategory: API\n  - name: Hugging Face Inference API\n    baseURL: https://api-inference.huggingface.co\n    tags:\n      - Inference\n      - Predictions\n      - Serverless\n    serviceName: Hugging Face Inference API\n    serviceCategory: API\n  - name: Hugging Face Hub API\n    baseURL: https://huggingface.co/api\n\
  \    tags:\n      - Datasets\n      - Hub\n      - Models\n      - Repositories\n    serviceName: Hugging Face Hub API\n    serviceCategory: API\n  - name: Hugging Face Spaces API\n    baseURL: https://huggingface.co/api/spaces\n    tags:\n      - Demos\n      - Deployment\n      - Gradio\n      - Spaces\n      - Streamlit\n    serviceName: Hugging Face Spaces API\n    serviceCategory: API\n  - name: Text Generation Inference (TGI)\n    baseURL: ''\n    tags:\n      - Inference Server\n      - LLM\n      - Streaming\n      - Text Generation\n    serviceName: Text Generation Inference (TGI)\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/hugging-face-transformers/refs/heads/main/finops/hugging-face-transformers-finops.yml
sources: []
specification: FinOps Framework
tags:
- Artificial Intelligence
- Computer Vision
- Deep Learning
- Machine Learning
- Natural Language Processing
- Open Source
- Transformers
- FinOps
- Cost Management
- FOCUS
---
