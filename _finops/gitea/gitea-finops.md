---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: swagger.v1.json
  format: json
  label: Gitea REST API
  slug: gitea-rest-api
  spec_type: OpenAPI
  url: https://demo.gitea.com/swagger.v1.json
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly (annual commitment for Enterprise)
  chargeCategories:
  - Usage
  - Purchase
  - Tax
  - Credit
  - Adjustment
  chargeFrequency: Recurring
  pricingCategory: Subscription + Usage-Based Add-Ons
description: FinOps framework definition for the Gitea API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the Gitea Enterprise per-user subscription and the Gitea Cloud single-tenant managed offering. The pure open-source Gitea distribution carries no software cost; FinOps reporting on OSS deployments is limited to underlying infrastructure (compute, storage, network) and operational labour.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: CommitGo, Inc.
  PricingCategory: Subscription
  PricingUnit: user-month
  ProviderName: Gitea
  PublisherName: CommitGo, Inc.
  ServiceCategory: Developer Tools / DevOps
  ServiceName: Gitea
layout: finops
meters:
- aggregation: max
  description: Active Gitea Enterprise per-user license seats
  dimensions:
  - instance
  - team
  - cost_center
  name: enterprise_seats
  unit: user-month
- aggregation: max
  description: Recurring Gitea Cloud instance subscription
  dimensions:
  - instance
  - region
  - tier
  - team
  - cost_center
  name: cloud_subscription
  unit: instance-month
- aggregation: max
  description: Object Storage add-on capacity used for LFS and packages
  dimensions:
  - instance
  - region
  - tier
  name: object_storage
  unit: GB-month
- aggregation: sum
  description: Outbound network traffic from a Gitea Cloud instance
  dimensions:
  - instance
  - region
  name: outbound_traffic
  unit: GB
- aggregation: sum
  description: Compute minutes consumed by Gitea Actions runner jobs
  dimensions:
  - instance
  - repository
  - workflow
  - runner_label
  name: actions_minutes
  unit: minute
- aggregation: sum
  description: REST API request volume (operator-visible signal; not directly billed)
  dimensions:
  - api
  - endpoint
  - tier
  - consumer
  name: api_requests
  unit: request
name: Gitea Finops
provider_name: Gitea
provider_slug: gitea
publisher_name: CommitGo, Inc.
service_category: Developer Tools / DevOps
slug: gitea-finops
source_filename: gitea-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Gitea\nproviderId: gitea\npublisherName: CommitGo, Inc.\nserviceCategory: Developer Tools / DevOps\ncreated: '2026-05-06'\nmodified: '2026-05-06'\ntags:\n  - Git\n  - Source Control\n  - DevOps\n  - CI/CD\n  - Code Hosting\n  - Open Source\n  - Self Hosted\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: >-\n  FinOps framework definition for the Gitea API surface. Provides a\n  FOCUS-aligned mapping for cost allocation, usage measurement, and\n  unit-economics reporting across the Gitea Enterprise per-user\n  subscription and the Gitea Cloud single-tenant managed offering.\n  The pure open-source Gitea distribution carries no software cost;\n  FinOps reporting on OSS deployments\
  \ is limited to underlying\n  infrastructure (compute, storage, network) and operational labour.\nprinciples:\n  - name: Visibility\n    description: >-\n      Make Gitea Enterprise license costs and Gitea Cloud subscription\n      costs visible to engineering, platform, and finance teams in\n      near real-time, including add-on charges (Object Storage) and\n      outbound network traffic.\n  - name: Allocation\n    description: >-\n      Tag every chargeable Gitea resource (Cloud instance, Enterprise\n      seat, Object Storage add-on, runner consumption) with the\n      consuming team, environment, application, and cost centre so\n      cost can be allocated.\n  - name: Optimization\n    description: >-\n      Continuously evaluate user counts, Cloud tier selection,\n      retention policies on packages and artifacts, and Actions\n      runner utilization to reduce cost per useful unit of work.\n  - name: Accountability\n    description: >-\n      Establish budget owners for the Gitea\
  \ instance, Actions usage,\n      and package storage. Implement chargeback or showback flows for\n      each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Subscription + Usage-Based Add-Ons\n  billingFrequency: Monthly\
  \ (annual commitment for Enterprise)\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Gitea\n  ServiceCategory: Developer Tools / DevOps\n  ProviderName: Gitea\n  PublisherName: CommitGo, Inc.\n  InvoiceIssuerName: CommitGo, Inc.\n  PricingCategory: Subscription\n  PricingUnit: user-month\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: enterprise_seats\n    description: Active Gitea Enterprise per-user license seats\n    unit: user-month\n    aggregation: max\n    dimensions:\n      - instance\n      - team\n      - cost_center\n  - name: cloud_subscription\n    description: Recurring Gitea Cloud instance subscription\n    unit: instance-month\n    aggregation: max\n    dimensions:\n      - instance\n      - region\n      - tier\n      - team\n      - cost_center\n  - name: object_storage\n    description: Object Storage add-on capacity used\
  \ for LFS and packages\n    unit: GB-month\n    aggregation: max\n    dimensions:\n      - instance\n      - region\n      - tier\n  - name: outbound_traffic\n    description: Outbound network traffic from a Gitea Cloud instance\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - instance\n      - region\n  - name: actions_minutes\n    description: Compute minutes consumed by Gitea Actions runner jobs\n    unit: minute\n    aggregation: sum\n    dimensions:\n      - instance\n      - repository\n      - workflow\n      - runner_label\n  - name: api_requests\n    description: REST API request volume (operator-visible signal; not directly billed)\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - consumer\napis:\n  - name: Gitea REST API\n    baseURL: https://gitea.com/api/v1\n    tags:\n      - REST\n      - Git\n      - Code Hosting\n    serviceName: Gitea REST API\n    serviceCategory: API\n  - name: Gitea Actions\
  \ API\n    baseURL: https://gitea.com/api/v1\n    tags:\n      - CI/CD\n      - Workflows\n    serviceName: Gitea Actions API\n    serviceCategory: API\n  - name: Gitea Package Registry\n    baseURL: https://gitea.com/api/packages\n    tags:\n      - Packages\n      - Registry\n    serviceName: Gitea Package Registry\n    serviceCategory: API\n  - name: Gitea Webhooks\n    baseURL: ''\n    tags:\n      - Webhooks\n      - Events\n    serviceName: Gitea Webhooks\n    serviceCategory: API\n  - name: Gitea Cloud Management API\n    baseURL: https://cloud.gitea.com\n    tags:\n      - Cloud\n      - Management\n    serviceName: Gitea Cloud Management API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost Per Active Developer\n    metric: billed_cost / active_users\n    target: TBD\n  - name: Cost Per 1K API Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost Per Actions Minute\n    metric: billed_cost / actions_minutes\n    target: TBD\n  - name:\
  \ Cost Per GB Stored\n    metric: billed_cost / object_storage_gb\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kinlane@gmail.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/gitea/refs/heads/main/finops/gitea-finops.yml
sources: []
specification: FinOps Framework
tags:
- Git
- Source Control
- DevOps
- CI/CD
- Code Hosting
- Open Source
- Self Hosted
- FinOps
- Cost Management
- FOCUS
---
