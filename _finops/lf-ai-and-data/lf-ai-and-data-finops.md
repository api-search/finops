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
description: FinOps framework definition for the LF AI and Data API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: LF AI and Data
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: LF AI and Data
  PublisherName: LF AI and Data
  ServiceCategory: Developer Tools / API
  ServiceName: LF AI and Data
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
name: Lf Ai And Data Finops
provider_name: LF AI and Data
provider_slug: lf-ai-and-data
publisher_name: LF AI and Data
service_category: API
slug: lf-ai-and-data-finops
source_filename: lf-ai-and-data-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: LF AI and Data\nproviderId: lf-ai-and-data\npublisherName: LF AI and Data\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Artificial Intelligence\n  - Machine Learning\n  - Data\n  - Linux Foundation\n  - Open Source\n  - MLOps\n  - Vector Database\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the LF AI and Data API surface. Provides a FOCUS-aligned\n  mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n \
  \ - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n\
  \  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: LF AI and Data\n  ServiceCategory: Developer Tools / API\n  ProviderName: LF AI and Data\n  PublisherName: LF AI and Data\n  InvoiceIssuerName: LF AI and Data\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description:\
  \ Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: ONNX\n    baseURL: ''\n    tags:\n      - AI\n      - Machine Learning\n      - Model Format\n      - Interoperability\n    serviceName: ONNX\n    serviceCategory: API\n  - name: Milvus\n    baseURL: ''\n    tags:\n      - Vector Database\n      - AI\n      - Search\n    serviceName: Milvus\n    serviceCategory: API\n  - name: Horovod\n    baseURL: ''\n    tags:\n      - Deep Learning\n      - Distributed Training\n      - GPU\n    serviceName: Horovod\n    serviceCategory: API\n  - name: Flyte\n    baseURL: ''\n    tags:\n      - Workflow Orchestration\n      - MLOps\n      - Cloud Native\n    serviceName: Flyte\n\
  \    serviceCategory: API\n  - name: Kedro\n    baseURL: ''\n    tags:\n      - Data Science\n      - Python\n      - Pipelines\n    serviceName: Kedro\n    serviceCategory: API\n  - name: OpenLineage\n    baseURL: ''\n    tags:\n      - Data Lineage\n      - Metadata\n      - Standards\n    serviceName: OpenLineage\n    serviceCategory: API\n  - name: Marquez\n    baseURL: ''\n    tags:\n      - Metadata\n      - Data Ecosystem\n      - Lineage\n    serviceName: Marquez\n    serviceCategory: API\n  - name: Egeria\n    baseURL: ''\n    tags:\n      - Metadata\n      - Data Governance\n      - Enterprise\n    serviceName: Egeria\n    serviceCategory: API\n  - name: Adversarial Robustness Toolbox\n    baseURL: ''\n    tags:\n      - AI Security\n      - Machine Learning\n      - Adversarial\n    serviceName: Adversarial Robustness Toolbox\n    serviceCategory: API\n  - name: Delta Lake\n    baseURL: ''\n    tags:\n      - Data Lake\n      - ACID\n      - Storage\n    serviceName: Delta Lake\n\
  \    serviceCategory: API\n  - name: Feast\n    baseURL: ''\n    tags:\n      - Feature Store\n      - Machine Learning\n      - MLOps\n    serviceName: Feast\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: info@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/lf-ai-and-data/refs/heads/main/finops/lf-ai-and-data-finops.yml
sources: []
specification: FinOps Framework
tags:
- Artificial Intelligence
- Machine Learning
- Data
- Linux Foundation
- Open Source
- MLOps
- Vector Database
- FinOps
- Cost Management
- FOCUS
---
