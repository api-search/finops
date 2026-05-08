---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: azure-devops-work-items-openapi.yml
  format: yaml
  label: Azure DevOps Work Item Tracking API
  slug: azure-devops-work-item-tracking-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/azure-devops/refs/heads/main/openapi/azure-devops-work-items-openapi.yml
- filename: azure-devops-pipelines-openapi.yml
  format: yaml
  label: Azure DevOps Pipelines API
  slug: azure-devops-pipelines-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/azure-devops/refs/heads/main/openapi/azure-devops-pipelines-openapi.yml
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
description: FinOps framework definition for the Azure DevOps API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Azure DevOps
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Azure DevOps
  PublisherName: Azure DevOps
  ServiceCategory: Developer Tools / API
  ServiceName: Azure DevOps
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
name: Azure Devops Finops
provider_name: Azure DevOps
provider_slug: azure-devops
publisher_name: Azure DevOps
service_category: API
slug: azure-devops-finops
source_filename: azure-devops-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Azure DevOps\nproviderId: azure-devops\npublisherName: Azure DevOps\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Azure\n  - CI/CD\n  - DevOps\n  - Pipelines\n  - Work Items\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Azure DevOps API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the\
  \ consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps\
  \ Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Azure DevOps\n  ServiceCategory: Developer Tools / API\n  ProviderName: Azure DevOps\n  PublisherName: Azure DevOps\n  InvoiceIssuerName: Azure DevOps\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation:\
  \ sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Azure DevOps Work Item Tracking API\n    baseURL: https://dev.azure.com/{organization}\n    tags:\n      - Azure\n      - CI/CD\n      - DevOps\n      - Project Management\n      - Work Items\n    serviceName: Azure DevOps Work Item Tracking API\n    serviceCategory: API\n  - name: Azure DevOps Git Repositories API\n    baseURL: https://dev.azure.com/{organization}\n    tags:\n      - Azure\n      - CI/CD\n      - DevOps\n      - Git\n      - Pull Requests\n      - Version Control\n    serviceName: Azure DevOps Git Repositories API\n    serviceCategory: API\n  - name: Azure DevOps Pipelines API\n    baseURL: https://dev.azure.com/{organization}\n    tags:\n      - Azure\n      - Build\n      -\
  \ CI/CD\n      - DevOps\n      - Pipelines\n      - Release\n    serviceName: Azure DevOps Pipelines API\n    serviceCategory: API\n  - name: Azure DevOps Artifacts API\n    baseURL: https://pkgs.dev.azure.com/{organization}\n    tags:\n      - Artifacts\n      - Azure\n      - CI/CD\n      - DevOps\n      - Npm\n      - NuGet\n      - Package Management\n    serviceName: Azure DevOps Artifacts API\n    serviceCategory: API\n  - name: Azure DevOps Test Plans API\n    baseURL: https://dev.azure.com/{organization}\n    tags:\n      - Azure\n      - CI/CD\n      - DevOps\n      - Test Plans\n      - Testing\n    serviceName: Azure DevOps Test Plans API\n    serviceCategory: API\n  - name: Azure DevOps Release API\n    baseURL: https://vsrm.dev.azure.com/{organization}\n    tags:\n      - Azure\n      - CI/CD\n      - Deployment\n      - DevOps\n      - Release Management\n    serviceName: Azure DevOps Release API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n\
  \    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/azure-devops/refs/heads/main/finops/azure-devops-finops.yml
sources: []
specification: FinOps Framework
tags:
- Azure
- CI/CD
- DevOps
- Pipelines
- Work Items
- FinOps
- Cost Management
- FOCUS
---
