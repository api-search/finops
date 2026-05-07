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
  - Purchase
  - Usage
  - Tax
  - Adjustment
  pricingCategory: Tiered Subscription
description: 'FOCUS-aligned FinOps for Azure DevOps Services: per-user-per-month subscription pricing for Basic and Basic + Test Plans, separate parallel-job pricing for CI/CD, and tiered storage pricing for Azure Artifacts. Billed via the Azure subscription tied to the organization.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Microsoft Corporation
  PricingCategory: Subscription
  ProviderName: Microsoft
  PublisherName: Microsoft Corporation
  ServiceCategory: Developer Tools
  ServiceName: Azure DevOps
layout: finops
meters:
- aggregation: max
  description: Per-user-month for Basic and Basic + Test Plans access levels
  dimensions:
  - access_level
  - organization
  name: licensed_users
  unit: seat
- aggregation: max
  description: Microsoft-hosted CI/CD parallel jobs above the free job
  dimensions:
  - organization
  name: parallel_jobs_hosted
  unit: parallel_job
- aggregation: max
  description: Self-hosted CI/CD parallel jobs above the free job
  dimensions:
  - organization
  name: parallel_jobs_self_hosted
  unit: parallel_job
- aggregation: avg
  description: Azure Artifacts package feed storage above 2 GB free
  dimensions:
  - organization
  - tier
  name: artifacts_storage
  unit: GB-month
- aggregation: sum
  description: Build minute consumption on Microsoft-hosted agents
  dimensions:
  - pipeline
  - organization
  name: hosted_pipeline_minutes
  unit: minute
name: Azure Devops Finops
provider_name: Azure DevOps
provider_slug: azure-devops
publisher_name: Microsoft Corporation
service_category: Developer Tools
slug: azure-devops-finops
source_filename: azure-devops-finops.yml
source_heading: FinOps Profile
source_url: https://azure.microsoft.com/en-us/pricing/details/devops/azure-devops-services/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Azure DevOps\nproviderId: azure-devops\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - DevOps\n  - CI/CD\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps for Azure DevOps Services: per-user-per-month subscription pricing\n  for Basic and Basic + Test Plans, separate parallel-job pricing for CI/CD, and tiered storage pricing\n  for Azure Artifacts. Billed via the Azure subscription tied to the organization.'\nsources:\n  - https://azure.microsoft.com/en-us/pricing/details/devops/azure-devops-services/\n  - https://learn.microsoft.com/en-us/azure/devops/organizations/billing/buy-basic-access-add-users\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName:\
  \ Microsoft Corporation\nserviceCategory: Developer Tools\nbillingModel:\n  pricingCategory: Tiered Subscription\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\n    - Tax\n    - Adjustment\nfocusColumns:\n  ServiceName: Azure DevOps\n  ServiceCategory: Developer Tools\n  ProviderName: Microsoft\n  PublisherName: Microsoft Corporation\n  InvoiceIssuerName: Microsoft Corporation\n  PricingCategory: Subscription\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: licensed_users\n    description: Per-user-month for Basic and Basic + Test Plans access levels\n    unit: seat\n    aggregation: max\n    dimensions:\n      - access_level\n      - organization\n  - name: parallel_jobs_hosted\n    description: Microsoft-hosted CI/CD parallel jobs above the free job\n    unit: parallel_job\n    aggregation: max\n    dimensions:\n      - organization\n  - name: parallel_jobs_self_hosted\n    description: Self-hosted CI/CD parallel\
  \ jobs above the free job\n    unit: parallel_job\n    aggregation: max\n    dimensions:\n      - organization\n  - name: artifacts_storage\n    description: Azure Artifacts package feed storage above 2 GB free\n    unit: GB-month\n    aggregation: avg\n    dimensions:\n      - organization\n      - tier\n  - name: hosted_pipeline_minutes\n    description: Build minute consumption on Microsoft-hosted agents\n    unit: minute\n    aggregation: sum\n    dimensions:\n      - pipeline\n      - organization\nprinciples:\n  - name: Visibility\n    description: Use Organization Settings -> Billing and Usage to see paid users, parallel jobs, Artifacts\n      storage, and pipeline-minute consumption; export to Azure Cost Management.\n  - name: Allocation\n    description: Tag projects and pipelines; map organization billing to Azure subscription / cost center;\n      use multi-organization billing to dedupe per-user costs across orgs.\n  - name: Optimization\n    description: Reclaim Stakeholder\
  \ seats from inactive Basic users (sort by Last Access); auto-detect\n      Visual Studio subscribers; consolidate Microsoft-hosted parallel jobs vs self-hosted based on workload\n      mix.\n  - name: Accountability\n    description: Assign Project Collection Administrators as billing owners; review Artifacts storage\n      growth and pipeline TSTU consumption monthly to avoid throttling.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/azure-devops/refs/heads/main/finops/azure-devops-finops.yml
sources:
- https://azure.microsoft.com/en-us/pricing/details/devops/azure-devops-services/
- https://learn.microsoft.com/en-us/azure/devops/organizations/billing/buy-basic-access-add-users
specification: FinOps Framework
tags:
- DevOps
- CI/CD
- FinOps
- FOCUS
---
