---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: kubernetes-operators-watch-asyncapi.yml
  format: yaml
  label: Kubernetes Operators
  slug: kubernetes-operators
  spec_type: AsyncAPI
  url: https://raw.githubusercontent.com/api-evangelist/kubernetes-operators/refs/heads/main/asyncapi/kubernetes-operators-watch-asyncapi.yml
- filename: kubernetes-crd-openapi.yml
  format: yaml
  label: Kubernetes Custom Resource Definitions
  slug: custom-resource-definitions
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/kubernetes-operators/refs/heads/main/openapi/kubernetes-crd-openapi.yml
- filename: kubernetes-olm-openapi.yml
  format: yaml
  label: Operator Lifecycle Manager
  slug: operator-lifecycle-manager
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/kubernetes-operators/refs/heads/main/openapi/kubernetes-olm-openapi.yml
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
description: FinOps framework definition for the Kubernetes Operators API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Kubernetes Operators
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Kubernetes Operators
  PublisherName: Kubernetes Operators
  ServiceCategory: Developer Tools / API
  ServiceName: Kubernetes Operators
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
name: Kubernetes Operators Finops
provider_name: Kubernetes Operators
provider_slug: kubernetes-operators
publisher_name: Kubernetes Operators
service_category: API
slug: kubernetes-operators-finops
source_filename: kubernetes-operators-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Kubernetes Operators\nproviderId: kubernetes-operators\npublisherName: Kubernetes Operators\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Automation\n  - Cloud Native\n  - DevOps\n  - Infrastructure\n  - Kubernetes\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Kubernetes Operators API surface. Provides a FOCUS-aligned\n  mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description:\
  \ Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n\
  \    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Kubernetes Operators\n  ServiceCategory: Developer Tools / API\n  ProviderName: Kubernetes Operators\n  PublisherName: Kubernetes Operators\n  InvoiceIssuerName: Kubernetes Operators\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes\
  \ returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Kubernetes Operators\n    baseURL: ''\n    tags:\n      - Automation\n      - Cloud Native\n      - Custom Resources\n      - Kubernetes\n    serviceName: Kubernetes Operators\n    serviceCategory: API\n  - name: Kubernetes Custom Resource Definitions\n    baseURL: ''\n    tags:\n      - API Extension\n      - Cloud Native\n      - Custom Resources\n      - Kubernetes\n    serviceName: Kubernetes Custom Resource Definitions\n    serviceCategory: API\n  - name: Operator SDK\n    baseURL: ''\n    tags:\n      - Go\n      - Kubernetes\n      - Operators\n      - SDK\n    serviceName: Operator SDK\n    serviceCategory: API\n\
  \  - name: Operator Lifecycle Manager\n    baseURL: ''\n    tags:\n      - Cloud Native\n      - Kubernetes\n      - Lifecycle Management\n      - Operators\n    serviceName: Operator Lifecycle Manager\n    serviceCategory: API\n  - name: OperatorHub\n    baseURL: ''\n    tags:\n      - Community\n      - Kubernetes\n      - Operators\n      - Registry\n    serviceName: OperatorHub\n    serviceCategory: API\n  - name: Controller-Runtime\n    baseURL: ''\n    tags:\n      - Controllers\n      - Go\n      - Kubernetes\n      - SDK\n    serviceName: Controller-Runtime\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/kubernetes-operators/refs/heads/main/finops/kubernetes-operators-finops.yml
sources: []
specification: FinOps Framework
tags:
- Automation
- Cloud Native
- DevOps
- Infrastructure
- Kubernetes
- FinOps
- Cost Management
- FOCUS
---
