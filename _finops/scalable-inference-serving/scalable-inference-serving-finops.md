---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: kserve-open-inference-protocol-openapi.yml
  format: yaml
  label: KServe Open Inference Protocol API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/scalable-inference-serving/main/openapi/kserve-open-inference-protocol-openapi.yml
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
description: FinOps framework definition for the Scalable Inference Serving API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Scalable Inference Serving
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Scalable Inference Serving
  PublisherName: Scalable Inference Serving
  ServiceCategory: Developer Tools / API
  ServiceName: Scalable Inference Serving
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
name: Scalable Inference Serving Finops
provider_name: Scalable Inference Serving
provider_slug: scalable-inference-serving
publisher_name: Scalable Inference Serving
service_category: API
slug: scalable-inference-serving-finops
source_filename: scalable-inference-serving-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Scalable Inference Serving\nproviderId: scalable-inference-serving\npublisherName: Scalable Inference Serving\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - AI\n  - CNCF\n  - Deployment\n  - Inference\n  - Kubernetes\n  - LLM\n  - Machine Learning\n  - Model Serving\n  - MLOps\n  - Scalability\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Scalable Inference Serving API surface. Provides a FOCUS-aligned\n  mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering,\
  \ product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n\
  \      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Scalable Inference Serving\n  ServiceCategory: Developer Tools / API\n  ProviderName: Scalable Inference Serving\n  PublisherName: Scalable Inference Serving\n  InvoiceIssuerName: Scalable Inference Serving\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n  \
  \    - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: KServe Open Inference Protocol API\n    baseURL: ''\n    tags:\n      - CNCF\n      - Inference\n      - Kubernetes\n      - Model Serving\n      - Open Inference Protocol\n      - Open Source\n    serviceName: KServe Open Inference Protocol API\n    serviceCategory: API\n  - name: BentoML REST API\n    baseURL: ''\n    tags:\n      - Batching\n      - Inference\n      - Model Serving\n      - Open Source\n      - Python\n      - REST API\n    serviceName: BentoML REST API\n    serviceCategory: API\n\
  \  - name: vLLM OpenAI-Compatible API\n    baseURL: ''\n    tags:\n      - GPU\n      - Inference\n      - KV Cache\n      - LLM\n      - Model Serving\n      - Open Source\n      - OpenAI-Compatible\n    serviceName: vLLM OpenAI-Compatible API\n    serviceCategory: API\n  - name: NVIDIA Triton Inference Server HTTP API\n    baseURL: ''\n    tags:\n      - GPU\n      - Inference\n      - Model Serving\n      - NVIDIA\n      - Open Source\n      - TensorRT\n      - Triton\n    serviceName: NVIDIA Triton Inference Server HTTP API\n    serviceCategory: API\n  - name: MLflow Model Registry REST API\n    baseURL: ''\n    tags:\n      - Experiment Tracking\n      - Machine Learning\n      - Model Registry\n      - MLOps\n      - Open Source\n      - Versioning\n    serviceName: MLflow Model Registry REST API\n    serviceCategory: API\n  - name: Ray Serve REST API\n    baseURL: ''\n    tags:\n      - Autoscaling\n      - Inference\n      - Machine Learning\n      - Model Serving\n      - Open\
  \ Source\n      - Python\n      - Ray\n    serviceName: Ray Serve REST API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - name: API Evangelist\n    email: kin@apievangelist.com\n    url: https://apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/scalable-inference-serving/refs/heads/main/finops/scalable-inference-serving-finops.yml
sources: []
specification: FinOps Framework
tags:
- AI
- CNCF
- Deployment
- Inference
- Kubernetes
- LLM
- Machine Learning
- Model Serving
- MLOps
- Scalability
- FinOps
- Cost Management
- FOCUS
---
