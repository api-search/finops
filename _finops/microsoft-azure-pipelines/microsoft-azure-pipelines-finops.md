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
  slug: azure-pipelines-rest-api
  spec_type: OpenAPI
  url: https://dev.azure.com/{organization}/_apis/public/api
billing_model:
  billingCurrency: USD (settlement varies)
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  - Tax
  - Adjustment
  - Credit
  chargeFrequency: Recurring
  pricingCategory: Subscription (per Parallel Job)
description: FOCUS-aligned FinOps for Azure Pipelines — billed per parallel job (concurrency) per month rather than per build minute. Two SKUs (Microsoft-hosted at $40/job/month and self-hosted at $15/job/month) plus free grants. Optimization centers on right-sizing parallel-job count to actual queue depth, since over-provisioning concurrency is the primary waste mode.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Microsoft Corporation
  PricingCategory: Subscription
  PricingUnit: parallel-job-month
  ProviderName: Microsoft Azure DevOps
  PublisherName: Microsoft Corporation
  ServiceCategory: Developer Tools
  ServiceName: Azure Pipelines
layout: finops
meters:
- aggregation: max
  description: Microsoft-hosted parallel job concurrency purchased.
  dimensions:
  - organization
  - billing_subscription
  name: hosted_parallel_jobs
  unit: parallel-job-month
- aggregation: max
  description: Self-hosted parallel job concurrency purchased.
  dimensions:
  - organization
  name: selfhosted_parallel_jobs
  unit: parallel-job-month
- aggregation: sum
  description: Microsoft-hosted agent minutes used (informational; not billed under parallel-job plan, but exposed via Pool consumption report).
  dimensions:
  - pipeline
  - agent_image
  - project
  name: hosted_minutes_consumed
  unit: minute
- aggregation: avg
  description: Average queued-job time per pool, used to size parallelism.
  dimensions:
  - pool
  - hour_of_day
  name: queue_depth
  unit: minute
- aggregation: sum
  description: Per-minute usage for grandfathered customers ($0.05 / $0.01 tiers).
  dimensions:
  - tier_band
  name: legacy_minutes
  unit: minute
name: Microsoft Azure Pipelines Finops
provider_name: Azure Pipelines
provider_slug: microsoft-azure-pipelines
publisher_name: Microsoft Corporation
service_category: Developer Tools / CI-CD
slug: microsoft-azure-pipelines-finops
source_filename: microsoft-azure-pipelines-finops.yml
source_heading: FinOps Profile
source_url: https://azure.microsoft.com/pricing/details/devops/azure-devops-services/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Azure Pipelines\nproviderId: microsoft-azure-pipelines\npublisherName: Microsoft Corporation\nserviceCategory: Developer Tools / CI-CD\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - Automation\n  - Build\n  - CI/CD\n  - Deployment\n  - DevOps\n  - Pipelines\n  - FinOps\n  - FOCUS\ndescription: FOCUS-aligned FinOps for Azure Pipelines — billed per parallel job (concurrency)\n  per month rather than per build minute. Two SKUs (Microsoft-hosted at $40/job/month and\n  self-hosted at $15/job/month) plus free grants. Optimization centers on right-sizing\n  parallel-job count to actual queue depth, since over-provisioning\
  \ concurrency is the\n  primary waste mode.\nsources:\n  - https://azure.microsoft.com/pricing/details/devops/azure-devops-services/\n  - https://learn.microsoft.com/en-us/azure/devops/pipelines/licensing/concurrent-jobs\n  - https://learn.microsoft.com/en-us/azure/devops/pipelines/agents/pool-consumption-report\nbillingModel:\n  pricingCategory: Subscription (per Parallel Job)\n  billingFrequency: Monthly\n  billingCurrency: USD (settlement varies)\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Adjustment\n    - Credit\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Azure Pipelines\n  ServiceCategory: Developer Tools\n  ProviderName: Microsoft Azure DevOps\n  PublisherName: Microsoft Corporation\n  InvoiceIssuerName: Microsoft Corporation\n  PricingCategory: Subscription\n  PricingUnit: parallel-job-month\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: hosted_parallel_jobs\n    description: Microsoft-hosted parallel job concurrency\
  \ purchased.\n    unit: parallel-job-month\n    aggregation: max\n    dimensions:\n      - organization\n      - billing_subscription\n  - name: selfhosted_parallel_jobs\n    description: Self-hosted parallel job concurrency purchased.\n    unit: parallel-job-month\n    aggregation: max\n    dimensions:\n      - organization\n  - name: hosted_minutes_consumed\n    description: Microsoft-hosted agent minutes used (informational; not billed under parallel-job\n      plan, but exposed via Pool consumption report).\n    unit: minute\n    aggregation: sum\n    dimensions:\n      - pipeline\n      - agent_image\n      - project\n  - name: queue_depth\n    description: Average queued-job time per pool, used to size parallelism.\n    unit: minute\n    aggregation: avg\n    dimensions:\n      - pool\n      - hour_of_day\n  - name: legacy_minutes\n    description: Per-minute usage for grandfathered customers ($0.05 / $0.01 tiers).\n    unit: minute\n    aggregation: sum\n    dimensions:\n      -\
  \ tier_band\nprinciples:\n  - name: Visibility\n    description: Pool consumption report (Org Settings > Agent pools > Analytics) graphs\n      concurrent-running vs queued jobs over 30 days. Pull the same data via the Pipelines REST\n      API into BI. Cost Management surfaces parallel-job line items in FOCUS-aligned exports.\n  - name: Allocation\n    description: Tag pipelines with cost-center via pipeline variables and aggregate via REST\n      API. Multi-org billing under one Azure subscription centralizes parallel-job spend across\n      consuming teams.\n  - name: Optimization\n    description: Right-size parallel jobs to peak queue depth (rule of thumb 1 job per 4–5 devs).\n      Move long-running jobs to self-hosted ($15 vs $40). Use caching (artifact, package, Docker\n      layer) to shorten build duration. Disable scheduled pipelines on idle branches. Take\n      advantage of free public-project grant for OSS.\n  - name: Accountability\n    description: Project Collection Administrators\
  \ own parallel-job procurement. Set Cost\n      Management budgets at the Azure subscription with alerts at 80/100% of monthly target.\n      Quarterly review of utilization vs purchased capacity.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n    url: https://azure.microsoft.com/services/devops/pipelines/\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/microsoft-azure-pipelines/refs/heads/main/finops/microsoft-azure-pipelines-finops.yml
sources:
- https://azure.microsoft.com/pricing/details/devops/azure-devops-services/
- https://learn.microsoft.com/en-us/azure/devops/pipelines/licensing/concurrent-jobs
- https://learn.microsoft.com/en-us/azure/devops/pipelines/agents/pool-consumption-report
specification: FinOps Framework
tags:
- Automation
- Build
- CI/CD
- Deployment
- DevOps
- Pipelines
- FinOps
- FOCUS
---
