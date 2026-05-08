---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Usage
  - Purchase
  - Tax
  - Credit
  - Adjustment
  chargeFrequency: Recurring
  pricingCategory: Tiered Subscription
description: 'FOCUS-aligned FinOps for the Harness DevOps platform: tiered subscription (Free / Essentials / Enterprise) with per-module activation and capacity ceilings such as concurrent pipeline executions and Code Repository storage.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Harness, Inc.
  PricingCategory: Tiered Subscription
  PricingUnit: module + capacity
  ProviderName: Harness
  PublisherName: Harness, Inc.
  ServiceCategory: Developer Tools / DevOps Platform
  ServiceName: Harness
layout: finops
meters:
- aggregation: sum
  description: Pipeline runs across CI and CD modules
  dimensions:
  - module
  - project
  - org
  name: pipeline_executions
  unit: execution
- aggregation: max
  description: Peak number of concurrently executing pipelines (capacity ceiling per plan)
  dimensions:
  - module
  - account
  name: concurrent_pipelines
  unit: concurrent_executions
- aggregation: max
  description: Storage consumed by the Harness Code Repository module
  dimensions:
  - account
  - org
  name: code_repo_storage
  unit: GB-month
- aggregation: sum
  description: Feature flag evaluations served by the FME module
  dimensions:
  - environment
  - module
  name: feature_flag_evaluations
  unit: evaluation
- aggregation: sum
  description: Underlying cloud spend brought under Harness Cloud Cost Management
  dimensions:
  - cloud_provider
  - account
  name: cloud_cost_managed
  unit: USD
- aggregation: sum
  description: Active modules enabled on the Harness account (per FOCUS Purchase line)
  dimensions:
  - module
  - plan
  name: module_subscriptions
  unit: module-month
name: Harness Finops
provider_name: Harness
provider_slug: harness
publisher_name: Harness, Inc.
service_category: Developer Tools / DevOps Platform
slug: harness-finops
source_filename: harness-finops.yml
source_heading: FinOps Profile
source_url: https://www.harness.io/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Harness\nproviderId: harness\npublisherName: Harness, Inc.\nserviceCategory: Developer Tools / DevOps Platform\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - DevOps\n  - GitOps\n  - Internal Developer Portal\n  - Lifecycle\n  - Software Delivery\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps for the Harness DevOps platform: tiered subscription (Free /\n  Essentials / Enterprise) with per-module activation and capacity ceilings such as concurrent\n  pipeline executions and Code Repository storage.'\nsources:\n  - https://www.harness.io/pricing\n  - https://apidocs.harness.io/\nprinciples:\n\
  \  - name: Visibility\n    description: Use the Harness Cloud Cost Management module and Software Engineering Insights for\n      pipeline-level cost and engineering productivity telemetry.\n  - name: Allocation\n    description: Tag deployments and pipelines with team / service / environment labels at the\n      Harness Project and Org level so spend can be attributed.\n  - name: Optimization\n    description: Right-size concurrent pipeline parallelism, prune idle Code Repository storage, and\n      consolidate modules at the Enterprise tier rather than buying point tools.\n  - name: Accountability\n    description: Assign budget owners per Harness Org / Project; review module enablement and\n      pipeline volume monthly against the negotiated Enterprise commitment.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n\
  \      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Tiered Subscription\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Harness\n  ServiceCategory: Developer Tools / DevOps Platform\n  ProviderName: Harness\n  PublisherName: Harness, Inc.\n  InvoiceIssuerName: Harness, Inc.\n  PricingCategory: Tiered Subscription\n\
  \  PricingUnit: module + capacity\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: pipeline_executions\n    description: Pipeline runs across CI and CD modules\n    unit: execution\n    aggregation: sum\n    dimensions:\n      - module\n      - project\n      - org\n  - name: concurrent_pipelines\n    description: Peak number of concurrently executing pipelines (capacity ceiling per plan)\n    unit: concurrent_executions\n    aggregation: max\n    dimensions:\n      - module\n      - account\n  - name: code_repo_storage\n    description: Storage consumed by the Harness Code Repository module\n    unit: GB-month\n    aggregation: max\n    dimensions:\n      - account\n      - org\n  - name: feature_flag_evaluations\n    description: Feature flag evaluations served by the FME module\n    unit: evaluation\n    aggregation: sum\n    dimensions:\n      - environment\n      - module\n  - name: cloud_cost_managed\n    description: Underlying cloud spend brought under Harness\
  \ Cloud Cost Management\n    unit: USD\n    aggregation: sum\n    dimensions:\n      - cloud_provider\n      - account\n  - name: module_subscriptions\n    description: Active modules enabled on the Harness account (per FOCUS Purchase line)\n    unit: module-month\n    aggregation: sum\n    dimensions:\n      - module\n      - plan\napis:\n  - name: Harness Platform API\n    baseURL: ''\n    tags:\n      - Access Management\n      - Accounts\n      - Administration\n      - Organizations\n      - Platform\n      - Projects\n    serviceName: Harness Platform API\n    serviceCategory: API\n  - name: Harness Continuous Integration API\n    baseURL: ''\n    tags:\n      - Builds\n      - CI\n      - Continuous Integration\n      - Pipelines\n    serviceName: Harness Continuous Integration API\n    serviceCategory: API\n  - name: Harness Continuous Delivery and GitOps API\n    baseURL: ''\n    tags:\n      - CD\n      - Continuous Delivery\n      - Deployments\n      - GitOps\n      - Pipelines\n\
  \    serviceName: Harness Continuous Delivery and GitOps API\n    serviceCategory: API\n  - name: Harness Feature Management and Experimentation API\n    baseURL: ''\n    tags:\n      - A/B Testing\n      - Experimentation\n      - Feature Flags\n      - Feature Management\n    serviceName: Harness Feature Management and Experimentation API\n    serviceCategory: API\n  - name: Harness Cloud Cost Management API\n    baseURL: ''\n    tags:\n      - CCM\n      - Cloud Cost Management\n      - Cost Optimization\n      - FinOps\n    serviceName: Harness Cloud Cost Management API\n    serviceCategory: API\n  - name: Harness Chaos Engineering API\n    baseURL: ''\n    tags:\n      - Chaos Engineering\n      - Reliability\n      - Resilience Testing\n    serviceName: Harness Chaos Engineering API\n    serviceCategory: API\n  - name: Harness Security Testing Orchestration API\n    baseURL: ''\n    tags:\n      - DevSecOps\n      - Security Testing\n      - STO\n      - Vulnerability Scanning\n\
  \    serviceName: Harness Security Testing Orchestration API\n    serviceCategory: API\n  - name: Harness Internal Developer Portal API\n    baseURL: ''\n    tags:\n      - Backstage\n      - Developer Experience\n      - IDP\n      - Software Catalog\n    serviceName: Harness Internal Developer Portal API\n    serviceCategory: API\n  - name: Harness Code Repository API\n    baseURL: ''\n    tags:\n      - Code Repository\n      - Git\n      - Source Control\n    serviceName: Harness Code Repository API\n    serviceCategory: API\n  - name: Harness Service Reliability Management API\n    baseURL: ''\n    tags:\n      - Monitoring\n      - Service Reliability\n      - SLO\n      - SRM\n    serviceName: Harness Service Reliability Management API\n    serviceCategory: API\n  - name: Harness Infrastructure as Code Management API\n    baseURL: ''\n    tags:\n      - IaCM\n      - Infrastructure as Code\n      - Provisioning\n      - Terraform\n    serviceName: Harness Infrastructure as Code\
  \ Management API\n    serviceCategory: API\n  - name: Harness Supply Chain Security API\n    baseURL: ''\n    tags:\n      - Compliance\n      - SBOM\n      - Software Supply Chain\n      - Supply Chain Security\n    serviceName: Harness Supply Chain Security API\n    serviceCategory: API\n  - name: Harness Software Engineering Insights API\n    baseURL: ''\n    tags:\n      - Analytics\n      - Engineering Productivity\n      - SEI\n    serviceName: Harness Software Engineering Insights API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per Pipeline Execution\n    metric: billed_cost / pipeline_executions\n    target: TBD\n  - name: Cost per Active Module\n    metric: billed_cost / module_subscriptions\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n    url: https://apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/harness/refs/heads/main/finops/harness-finops.yml
sources:
- https://www.harness.io/pricing
- https://apidocs.harness.io/
specification: FinOps Framework
tags:
- DevOps
- GitOps
- Internal Developer Portal
- Lifecycle
- Software Delivery
- FinOps
- Cost Management
- FOCUS
---
