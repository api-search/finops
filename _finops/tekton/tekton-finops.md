---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: tekton-pipeline-openapi.json
  format: json
  label: Tekton Task CRD
  slug: tekton-task-crd
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/tekton/refs/heads/main/openapi/tekton-pipeline-openapi.json
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
description: FinOps framework definition for the Tekton API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Tekton
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Tekton
  PublisherName: Tekton
  ServiceCategory: Developer Tools / API
  ServiceName: Tekton
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
name: Tekton Finops
provider_name: Tekton
provider_slug: tekton
publisher_name: Tekton
service_category: API
slug: tekton-finops
source_filename: tekton-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Tekton\nproviderId: tekton\npublisherName: Tekton\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - DevOps\n  - CI/CD\n  - Kubernetes\n  - CNCF\n  - Pipelines\n  - Open Source\n  - CRD\n  - Operator\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Tekton API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API\
  \ call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n\
  \      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Tekton\n  ServiceCategory: Developer Tools / API\n  ProviderName: Tekton\n  PublisherName: Tekton\n  InvoiceIssuerName: Tekton\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation:\
  \ sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Tekton Task CRD\n    baseURL: ''\n    tags:\n      - CRD\n      - Tasks\n      - Steps\n      - Build\n    serviceName: Tekton Task CRD\n    serviceCategory: API\n  - name: Tekton TaskRun CRD\n    baseURL: ''\n    tags:\n      - CRD\n      - TaskRuns\n      - Execution\n    serviceName: Tekton TaskRun CRD\n    serviceCategory: API\n  - name: Tekton Pipeline CRD\n    baseURL: ''\n    tags:\n      - CRD\n      - Pipelines\n      - Workflows\n    serviceName: Tekton Pipeline CRD\n    serviceCategory: API\n  - name: Tekton PipelineRun CRD\n    baseURL: ''\n    tags:\n      - CRD\n      - PipelineRuns\n      - Execution\n    serviceName: Tekton PipelineRun CRD\n    serviceCategory: API\n  - name: Tekton\
  \ ClusterTask CRD\n    baseURL: ''\n    tags:\n      - CRD\n      - ClusterTasks\n      - Cluster-Scoped\n    serviceName: Tekton ClusterTask CRD\n    serviceCategory: API\n  - name: Tekton StepAction CRD\n    baseURL: ''\n    tags:\n      - CRD\n      - StepActions\n      - Reusable\n    serviceName: Tekton StepAction CRD\n    serviceCategory: API\n  - name: Tekton CustomRun CRD\n    baseURL: ''\n    tags:\n      - CRD\n      - CustomRun\n      - Extension\n    serviceName: Tekton CustomRun CRD\n    serviceCategory: API\n  - name: Tekton Resolver Framework\n    baseURL: ''\n    tags:\n      - Resolution\n      - Resolvers\n      - Remote\n    serviceName: Tekton Resolver Framework\n    serviceCategory: API\n  - name: Tekton EventListener CRD\n    baseURL: ''\n    tags:\n      - CRD\n      - EventListener\n      - Triggers\n      - Webhooks\n    serviceName: Tekton EventListener CRD\n    serviceCategory: API\n  - name: Tekton Trigger CRD\n    baseURL: ''\n    tags:\n      - CRD\n     \
  \ - Trigger\n      - TriggerBinding\n      - TriggerTemplate\n    serviceName: Tekton Trigger CRD\n    serviceCategory: API\n  - name: Tekton TriggerBinding CRD\n    baseURL: ''\n    tags:\n      - CRD\n      - TriggerBinding\n    serviceName: Tekton TriggerBinding CRD\n    serviceCategory: API\n  - name: Tekton TriggerTemplate CRD\n    baseURL: ''\n    tags:\n      - CRD\n      - TriggerTemplate\n    serviceName: Tekton TriggerTemplate CRD\n    serviceCategory: API\n  - name: Tekton ClusterInterceptor CRD\n    baseURL: ''\n    tags:\n      - CRD\n      - Interceptor\n      - Filtering\n    serviceName: Tekton ClusterInterceptor CRD\n    serviceCategory: API\n  - name: Tekton Results API\n    baseURL: ''\n    tags:\n      - Results\n      - History\n      - Storage\n      - GRPC\n    serviceName: Tekton Results API\n    serviceCategory: API\n  - name: Tekton Chains\n    baseURL: ''\n    tags:\n      - Supply Chain\n      - Provenance\n      - SLSA\n      - Signing\n    serviceName: Tekton\
  \ Chains\n    serviceCategory: API\n  - name: Tekton Pipelines as Code\n    baseURL: ''\n    tags:\n      - Pipelines as Code\n      - GitOps\n      - GitHub\n      - GitLab\n    serviceName: Tekton Pipelines as Code\n    serviceCategory: API\n  - name: Tekton Dashboard API\n    baseURL: ''\n    tags:\n      - Dashboard\n      - UI\n      - Backend\n    serviceName: Tekton Dashboard API\n    serviceCategory: API\n  - name: Tekton CLI (tkn)\n    baseURL: ''\n    tags:\n      - CLI\n      - tkn\n      - Operations\n    serviceName: Tekton CLI (tkn)\n    serviceCategory: API\n  - name: Tekton Operator CRDs\n    baseURL: ''\n    tags:\n      - CRD\n      - Operator\n      - Lifecycle\n      - TektonConfig\n    serviceName: Tekton Operator CRDs\n    serviceCategory: API\n  - name: Tekton Hub API\n    baseURL: ''\n    tags:\n      - Hub\n      - Catalog\n      - Discovery\n    serviceName: Tekton Hub API\n    serviceCategory: API\n  - name: Tekton Catalog\n    baseURL: ''\n    tags:\n      -\
  \ Catalog\n      - Library\n      - Reusable\n    serviceName: Tekton Catalog\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/tekton/refs/heads/main/finops/tekton-finops.yml
sources: []
specification: FinOps Framework
tags:
- DevOps
- CI/CD
- Kubernetes
- CNCF
- Pipelines
- Open Source
- CRD
- Operator
- FinOps
- Cost Management
- FOCUS
---
