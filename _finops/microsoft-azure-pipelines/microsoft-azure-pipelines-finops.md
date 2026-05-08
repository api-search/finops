---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: api
  format: yaml
  label: Azure Pipelines REST API
  slug: ''
  spec_type: OpenAPI
  url: https://dev.azure.com/{organization}/_apis/public/api
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
description: FinOps framework definition for the Azure Pipelines API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Azure Pipelines
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Azure Pipelines
  PublisherName: Azure Pipelines
  ServiceCategory: Developer Tools / API
  ServiceName: Azure Pipelines
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
name: Microsoft Azure Pipelines Finops
provider_name: Azure Pipelines
provider_slug: microsoft-azure-pipelines
publisher_name: Azure Pipelines
service_category: API
slug: microsoft-azure-pipelines-finops
source_filename: microsoft-azure-pipelines-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Azure Pipelines\nproviderId: microsoft-azure-pipelines\npublisherName: Azure Pipelines\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Automation\n  - Build\n  - CI/CD\n  - Deployment\n  - DevOps\n  - Pipelines\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Azure Pipelines API surface. Provides a FOCUS-aligned\n  mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description:\
  \ Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n\
  \    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Azure Pipelines\n  ServiceCategory: Developer Tools / API\n  ProviderName: Azure Pipelines\n  PublisherName: Azure Pipelines\n  InvoiceIssuerName: Azure Pipelines\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the\
  \ network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Azure Pipelines REST API\n    baseURL: https://dev.azure.com/{organization}/{project}/_apis\n    tags:\n      - CI/CD\n      - Pipelines\n      - REST\n    serviceName: Azure Pipelines REST API\n    serviceCategory: API\n  - name: Azure Pipelines Build REST API\n    baseURL: https://dev.azure.com/{organization}/{project}/_apis/build\n    tags:\n      - Artifacts\n      - Build\n      - Continuous Integration\n      - Definitions\n    serviceName: Azure Pipelines Build REST API\n    serviceCategory: API\n  - name: Azure Pipelines Release REST API\n    baseURL: https://vsrm.dev.azure.com/{organization}/{project}/_apis/release\n    tags:\n \
  \     - Approvals\n      - Continuous Delivery\n      - Deployment\n      - Release\n    serviceName: Azure Pipelines Release REST API\n    serviceCategory: API\n  - name: Azure Pipelines Approvals and Checks REST API\n    baseURL: https://dev.azure.com/{organization}/{project}/_apis/pipelines\n    tags:\n      - Approvals\n      - Checks\n      - Governance\n      - Security\n    serviceName: Azure Pipelines Approvals and Checks REST API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/microsoft-azure-pipelines/refs/heads/main/finops/microsoft-azure-pipelines-finops.yml
sources: []
specification: FinOps Framework
tags:
- Automation
- Build
- CI/CD
- Deployment
- DevOps
- Pipelines
- FinOps
- Cost Management
- FOCUS
---
