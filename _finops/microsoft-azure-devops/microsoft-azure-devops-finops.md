---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: openapi.yaml
  format: yaml
  label: Azure DevOps Services REST API
  slug: azure-devops-services-rest-api
  spec_type: OpenAPI
  url: https://learn.microsoft.com/en-us/rest/api/azure/devops/
- filename: azure-devops-work-items-api-openapi.yml
  format: yaml
  label: Azure DevOps Boards API
  slug: azure-devops-boards-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-azure-devops/refs/heads/main/openapi/azure-devops-work-items-api-openapi.yml
- filename: azure-devops-git-api-openapi.yml
  format: yaml
  label: Azure DevOps Repos API
  slug: azure-devops-repos-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-azure-devops/refs/heads/main/openapi/azure-devops-git-api-openapi.yml
- filename: azure-devops-pipelines-api-openapi.yml
  format: yaml
  label: Azure DevOps Pipelines API
  slug: azure-devops-pipelines-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-azure-devops/refs/heads/main/openapi/azure-devops-pipelines-api-openapi.yml
- filename: azure-devops-builds-api-openapi.yml
  format: yaml
  label: Azure DevOps Build API
  slug: azure-devops-build-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-azure-devops/refs/heads/main/openapi/azure-devops-builds-api-openapi.yml
- filename: azure-devops-releases-api-openapi.yml
  format: yaml
  label: Azure DevOps Release API
  slug: azure-devops-release-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-azure-devops/refs/heads/main/openapi/azure-devops-releases-api-openapi.yml
- filename: azure-devops-test-plans-api-openapi.yml
  format: yaml
  label: Azure DevOps Test Plans API
  slug: azure-devops-test-plans-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-azure-devops/refs/heads/main/openapi/azure-devops-test-plans-api-openapi.yml
- filename: azure-devops-artifacts-api-openapi.yml
  format: yaml
  label: Azure DevOps Artifacts API
  slug: azure-devops-artifacts-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-azure-devops/refs/heads/main/openapi/azure-devops-artifacts-api-openapi.yml
- filename: azure-devops-service-hooks-api-openapi.yml
  format: yaml
  label: Azure DevOps Service Hooks API
  slug: azure-devops-service-hooks-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-azure-devops/refs/heads/main/openapi/azure-devops-service-hooks-api-openapi.yml
- filename: azure-devops-wiki-api-openapi.yml
  format: yaml
  label: Azure DevOps Wiki API
  slug: azure-devops-wiki-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-azure-devops/refs/heads/main/openapi/azure-devops-wiki-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  - Tax
  - Adjustment
  - Credit
  pricingCategory: Tiered Subscription
description: 'FOCUS-aligned FinOps for Azure DevOps Services: per-user license subscriptions (Basic, Basic + Test Plans, Stakeholder free) plus pay-per-slot Microsoft-hosted and self-hosted Pipelines parallel jobs and tiered Artifacts storage.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Microsoft Corporation
  ProviderName: Microsoft
  PublisherName: Microsoft Corporation
  ServiceCategory: DevOps
  ServiceName: Azure DevOps Services
layout: finops
meters:
- aggregation: sum
  dimensions:
  - organization
  - team
  name: basic_user_seats
  unit: seat-month
- aggregation: sum
  dimensions:
  - organization
  - team
  name: basic_test_plans_seats
  unit: seat-month
- aggregation: sum
  dimensions:
  - organization
  - project
  name: ms_hosted_parallel_jobs
  unit: parallel_job-month
- aggregation: sum
  dimensions:
  - organization
  name: self_hosted_parallel_jobs
  unit: parallel_job-month
- aggregation: avg
  dimensions:
  - organization
  - feed
  name: artifacts_storage
  unit: GB-month
name: Microsoft Azure Devops Finops
provider_name: Azure DevOps
provider_slug: microsoft-azure-devops
publisher_name: Microsoft Corporation
service_category: DevOps / Developer Tools
slug: microsoft-azure-devops-finops
source_filename: microsoft-azure-devops-finops.yml
source_heading: FinOps Profile
source_url: https://azure.microsoft.com/en-us/pricing/details/devops/azure-devops-services/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Azure DevOps\nproviderId: microsoft-azure-devops\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - DevOps\n  - Microsoft Azure\ndescription: 'FOCUS-aligned FinOps for Azure DevOps Services: per-user license subscriptions (Basic,\n  Basic + Test Plans, Stakeholder free) plus pay-per-slot Microsoft-hosted and self-hosted Pipelines\n  parallel jobs and tiered Artifacts storage.'\nsources:\n  - https://azure.microsoft.com/en-us/pricing/details/devops/azure-devops-services/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Microsoft Corporation\nserviceCategory: DevOps / Developer Tools\nbillingModel:\n  pricingCategory: Tiered Subscription\n\
  \  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Adjustment\n    - Credit\nfocusColumns:\n  ServiceName: Azure DevOps Services\n  ServiceCategory: DevOps\n  ProviderName: Microsoft\n  PublisherName: Microsoft Corporation\n  InvoiceIssuerName: Microsoft Corporation\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: basic_user_seats\n    unit: seat-month\n    aggregation: sum\n    dimensions:\n      - organization\n      - team\n  - name: basic_test_plans_seats\n    unit: seat-month\n    aggregation: sum\n    dimensions:\n      - organization\n      - team\n  - name: ms_hosted_parallel_jobs\n    unit: parallel_job-month\n    aggregation: sum\n    dimensions:\n      - organization\n      - project\n  - name: self_hosted_parallel_jobs\n    unit: parallel_job-month\n    aggregation: sum\n    dimensions:\n      - organization\n  - name: artifacts_storage\n    unit: GB-month\n    aggregation: avg\n    dimensions:\n\
  \      - organization\n      - feed\nprinciples:\n  - name: Visibility\n    description: Use the Azure DevOps organization Billing settings page and Azure Cost Management\n      filtered to Azure DevOps for license, pipelines, and artifacts breakdown by organization.\n  - name: Allocation\n    description: Allocate cost by organization, project, and team using project ownership metadata;\n      tag billing subscriptions per business unit.\n  - name: Optimization\n    description: Reclaim Basic licenses from inactive users on a quarterly cadence; downgrade non-contributors\n      to Stakeholder; right-size parallel job slots vs queue time; move high-volume builds to self-hosted\n      agents for cost savings.\n  - name: Accountability\n    description: Assign org admins as cost owners; set per-org spend alerts in Azure Cost Management;\n      review at quarterly Microsoft EA true-up.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/microsoft-azure-devops/refs/heads/main/finops/microsoft-azure-devops-finops.yml
sources:
- https://azure.microsoft.com/en-us/pricing/details/devops/azure-devops-services/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- DevOps
- Microsoft Azure
---
