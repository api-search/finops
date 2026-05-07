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
  pricingCategory: Pay-As-You-Go + Committed Use
description: 'FOCUS-aligned FinOps for HashiCorp Cloud Platform: pay-as-you-go per-managed-resource pricing on HCP Terraform (Essentials $0.10, Standard $0.47, Premium $0.99 per resource per month; hourly rates also published) plus per-product meters for Vault Secrets, Consul, Boundary, Packer, and Waypoint. New-customer $500 platform credit is recognized as a FOCUS Credit line.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: HashiCorp, Inc.
  PricingCategory: Pay-As-You-Go
  PricingUnit: managed-resource / cluster-hour
  ProviderName: HashiCorp Cloud Platform
  PublisherName: HashiCorp, Inc. (an IBM company)
  ServiceCategory: Cloud / Managed Infrastructure Services
  ServiceName: HashiCorp Cloud Platform
layout: finops
meters:
- aggregation: max
  description: Count of Terraform-managed resources, billed monthly per the active HCP Terraform tier (Essentials / Standard / Premium)
  dimensions:
  - tier
  - workspace
  - project
  - organization
  name: terraform_managed_resources
  unit: resource-month
- aggregation: sum
  description: Hourly metering of managed Terraform resources
  dimensions:
  - tier
  - workspace
  - organization
  name: terraform_managed_resource_hours
  unit: resource-hour
- aggregation: sum
  description: Cluster-hours for HCP Vault / Consul / Boundary / Packer / Waypoint
  dimensions:
  - product
  - tier
  - region
  name: hcp_cluster_hours
  unit: cluster-hour
- aggregation: max
  description: HCP Vault Secrets stored / synced
  dimensions:
  - cluster
  - app
  name: vault_secrets
  unit: secret
- aggregation: sum
  description: Consumption of the $500 new-customer HCP credit
  dimensions:
  - product
  name: hcp_credit_consumption
  unit: USD
- aggregation: sum
  description: HCP API requests (allocation / abuse-monitoring meter; not directly billable)
  dimensions:
  - api
  - endpoint
  - region
  - consumer
  name: api_requests
  unit: request
name: Hcp Finops
provider_name: HashiCorp Cloud Platform
provider_slug: hcp
publisher_name: HashiCorp, Inc. (an IBM company)
service_category: Cloud / Managed Infrastructure Services
slug: hcp-finops
source_filename: hcp-finops.yml
source_heading: FinOps Profile
source_url: https://www.hashicorp.com/en/products/terraform/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: HashiCorp Cloud Platform\nproviderId: hcp\npublisherName: HashiCorp, Inc. (an IBM company)\nserviceCategory: Cloud / Managed Infrastructure Services\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - Cloud\n  - Infrastructure\n  - DevOps\n  - Secrets Management\n  - Service Networking\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps for HashiCorp Cloud Platform: pay-as-you-go per-managed-resource\n  pricing on HCP Terraform (Essentials $0.10, Standard $0.47, Premium $0.99 per resource per month;\n  hourly rates also published) plus per-product meters for Vault Secrets, Consul, Boundary, Packer,\n\
  \  and Waypoint. New-customer $500 platform credit is recognized as a FOCUS Credit line.'\nsources:\n  - https://www.hashicorp.com/en/products/terraform/pricing\n  - https://developer.hashicorp.com/terraform/cloud-docs/api-docs\nprinciples:\n  - name: Visibility\n    description: Use the HCP billing dashboard and per-product usage views; export usage for\n      Terraform managed-resource counts and HCP cluster hours into your FOCUS billing pipeline.\n  - name: Allocation\n    description: Allocate Terraform spend by Workspace and Project; allocate Vault / Consul /\n      Boundary spend by HCP cluster (and the application teams that mount them).\n  - name: Optimization\n    description: Reduce managed-resource counts via state pruning and module consolidation; pick\n      the lowest HCP Terraform tier (Essentials / Standard / Premium) that meets governance needs;\n      consume the $500 new-customer credit before committing to PAYG.\n  - name: Accountability\n    description: Assign a HashiCorp\
  \ account owner per HCP Organization; review managed-resource\n      growth and HCP cluster hours monthly against the run-rate.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Pay-As-You-Go + Committed Use\n  billingFrequency: Monthly\n\
  \  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: HashiCorp Cloud Platform\n  ServiceCategory: Cloud / Managed Infrastructure Services\n  ProviderName: HashiCorp Cloud Platform\n  PublisherName: HashiCorp, Inc. (an IBM company)\n  InvoiceIssuerName: HashiCorp, Inc.\n  PricingCategory: Pay-As-You-Go\n  PricingUnit: managed-resource / cluster-hour\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: terraform_managed_resources\n    description: Count of Terraform-managed resources, billed monthly per the active HCP Terraform\n      tier (Essentials / Standard / Premium)\n    unit: resource-month\n    aggregation: max\n    dimensions:\n      - tier\n      - workspace\n      - project\n      - organization\n  - name: terraform_managed_resource_hours\n    description: Hourly metering of managed Terraform resources\n    unit: resource-hour\n    aggregation:\
  \ sum\n    dimensions:\n      - tier\n      - workspace\n      - organization\n  - name: hcp_cluster_hours\n    description: Cluster-hours for HCP Vault / Consul / Boundary / Packer / Waypoint\n    unit: cluster-hour\n    aggregation: sum\n    dimensions:\n      - product\n      - tier\n      - region\n  - name: vault_secrets\n    description: HCP Vault Secrets stored / synced\n    unit: secret\n    aggregation: max\n    dimensions:\n      - cluster\n      - app\n  - name: hcp_credit_consumption\n    description: Consumption of the $500 new-customer HCP credit\n    unit: USD\n    aggregation: sum\n    dimensions:\n      - product\n  - name: api_requests\n    description: HCP API requests (allocation / abuse-monitoring meter; not directly billable)\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - region\n      - consumer\napis:\n  - name: HCP Vault Secrets API\n    baseURL: https://api.cloud.hashicorp.com\n    tags:\n      - Secrets Management\n\
  \      - Vault\n      - Cloud\n    serviceName: HCP Vault Secrets API\n    serviceCategory: API\n  - name: HCP Packer API\n    baseURL: https://api.cloud.hashicorp.com\n    tags:\n      - Packer\n      - Images\n      - DevOps\n    serviceName: HCP Packer API\n    serviceCategory: API\n  - name: HCP Consul API\n    baseURL: https://api.cloud.hashicorp.com\n    tags:\n      - Consul\n      - Service Mesh\n      - Service Networking\n    serviceName: HCP Consul API\n    serviceCategory: API\n  - name: HCP Boundary API\n    baseURL: https://api.cloud.hashicorp.com\n    tags:\n      - Boundary\n      - Remote Access\n      - Identity\n    serviceName: HCP Boundary API\n    serviceCategory: API\n  - name: HCP Waypoint API\n    baseURL: https://api.cloud.hashicorp.com\n    tags:\n      - Waypoint\n      - Application Delivery\n      - DevOps\n    serviceName: HCP Waypoint API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per Managed Resource\n    metric: billed_cost / terraform_managed_resources\n\
  \    target: TBD\n  - name: Cost per Cluster-Hour\n    metric: billed_cost / hcp_cluster_hours\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/hcp/refs/heads/main/finops/hcp-finops.yml
sources:
- https://www.hashicorp.com/en/products/terraform/pricing
- https://developer.hashicorp.com/terraform/cloud-docs/api-docs
specification: FinOps Framework
tags:
- Cloud
- Infrastructure
- DevOps
- Secrets Management
- Service Networking
- FinOps
- Cost Management
- FOCUS
---
