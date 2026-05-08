---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: hashicorp-vault-openapi.yml
  format: yaml
  label: HashiCorp Vault
  slug: hashicorp-vault
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/hashicorp/refs/heads/main/openapi/hashicorp-vault-openapi.yml
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
description: 'FOCUS-aligned FinOps for HashiCorp: pay-as-you-go per-managed-resource billing on HCP Terraform (Essentials $0.10, Standard $0.47, Premium $0.99 per resource per month) plus custom-priced Enterprise (self-managed) and EU residency editions. Other product lines (Vault, Consul, Nomad, Boundary, Packer, Waypoint) bill per HCP product or via Enterprise license.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: HashiCorp, Inc.
  PricingCategory: Pay-As-You-Go
  PricingUnit: managed-resource
  ProviderName: HashiCorp
  PublisherName: HashiCorp, Inc. (an IBM company)
  ServiceCategory: Infrastructure / DevOps Platform
  ServiceName: HashiCorp
layout: finops
meters:
- aggregation: max
  description: Count of Terraform-managed resources, billed monthly per the active HCP Terraform tier
  dimensions:
  - tier
  - workspace
  - project
  - organization
  name: terraform_managed_resources
  unit: resource-month
- aggregation: sum
  description: Hourly metering of managed resources (alternative to monthly billing)
  dimensions:
  - tier
  - workspace
  - organization
  name: terraform_managed_resource_hours
  unit: resource-hour
- aggregation: sum
  description: HCP Terraform API requests for cost allocation and abuse monitoring
  dimensions:
  - endpoint
  - user
  - workspace
  name: api_requests
  unit: request
- aggregation: sum
  description: Consumption of the $500 new-customer HCP credit
  dimensions:
  - product
  name: hcp_credit_consumption
  unit: USD
- aggregation: sum
  description: Custom Enterprise (self-managed Terraform Enterprise / EU) subscription line
  dimensions:
  - edition
  - region
  name: enterprise_subscription
  unit: month
name: Hashicorp Finops
provider_name: HashiCorp
provider_slug: hashicorp
publisher_name: HashiCorp, Inc. (an IBM company)
service_category: Infrastructure / DevOps Platform
slug: hashicorp-finops
source_filename: hashicorp-finops.yml
source_heading: FinOps Profile
source_url: https://www.hashicorp.com/en/products/terraform/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: HashiCorp\nproviderId: hashicorp\npublisherName: HashiCorp, Inc. (an IBM company)\nserviceCategory: Infrastructure / DevOps Platform\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - Cloud\n  - DevOps\n  - Infrastructure\n  - Platform\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps for HashiCorp: pay-as-you-go per-managed-resource billing on\n  HCP Terraform (Essentials $0.10, Standard $0.47, Premium $0.99 per resource per month) plus\n  custom-priced Enterprise (self-managed) and EU residency editions. Other product lines (Vault,\n  Consul, Nomad, Boundary, Packer, Waypoint) bill per HCP\
  \ product or via Enterprise license.'\nsources:\n  - https://www.hashicorp.com/en/products/terraform/pricing\n  - https://developer.hashicorp.com/terraform/cloud-docs/api-docs\nprinciples:\n  - name: Visibility\n    description: Use HCP Terraform's billing dashboard and the workspaces/managed-resources counts;\n      tag workspaces by team / environment so consumption maps onto invoice lines.\n  - name: Allocation\n    description: Allocate HCP Terraform spend by Workspace and Project; map managed-resource counts\n      back to consuming application teams via workspace tags.\n  - name: Optimization\n    description: Reduce managed-resource counts via state pruning, module consolidation, and\n      ephemeral workspaces; choose the lowest tier (Essentials / Standard / Premium) that meets\n      governance needs; redeem the $500 new-customer credit.\n  - name: Accountability\n    description: Assign a HashiCorp account owner; review Terraform managed-resource growth monthly\n      against\
  \ the Enterprise commitment or PAYG run-rate.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Pay-As-You-Go + Committed Use\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n\
  \    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: HashiCorp\n  ServiceCategory: Infrastructure / DevOps Platform\n  ProviderName: HashiCorp\n  PublisherName: HashiCorp, Inc. (an IBM company)\n  InvoiceIssuerName: HashiCorp, Inc.\n  PricingCategory: Pay-As-You-Go\n  PricingUnit: managed-resource\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: terraform_managed_resources\n    description: Count of Terraform-managed resources, billed monthly per the active HCP Terraform\n      tier\n    unit: resource-month\n    aggregation: max\n    dimensions:\n      - tier\n      - workspace\n      - project\n      - organization\n  - name: terraform_managed_resource_hours\n    description: Hourly metering of managed resources (alternative to monthly billing)\n    unit: resource-hour\n    aggregation: sum\n    dimensions:\n      - tier\n      - workspace\n      - organization\n  - name: api_requests\n    description: HCP Terraform API requests\
  \ for cost allocation and abuse monitoring\n    unit: request\n    aggregation: sum\n    dimensions:\n      - endpoint\n      - user\n      - workspace\n  - name: hcp_credit_consumption\n    description: Consumption of the $500 new-customer HCP credit\n    unit: USD\n    aggregation: sum\n    dimensions:\n      - product\n  - name: enterprise_subscription\n    description: Custom Enterprise (self-managed Terraform Enterprise / EU) subscription line\n    unit: month\n    aggregation: sum\n    dimensions:\n      - edition\n      - region\napis:\n  - name: HashiCorp Vault\n    baseURL: ''\n    tags:\n      - Secrets Management\n      - Security\n    serviceName: HashiCorp Vault\n    serviceCategory: API\n  - name: HashiCorp Terraform\n    baseURL: ''\n    tags:\n      - Infrastructure as Code\n      - Provisioning\n    serviceName: HashiCorp Terraform\n    serviceCategory: API\n  - name: HashiCorp Nomad\n    baseURL: ''\n    tags:\n      - Orchestration\n      - Scheduling\n    serviceName:\
  \ HashiCorp Nomad\n    serviceCategory: API\n  - name: HashiCorp Consul\n    baseURL: ''\n    tags:\n      - Service Discovery\n      - Service Mesh\n    serviceName: HashiCorp Consul\n    serviceCategory: API\n  - name: HashiCorp Boundary\n    baseURL: ''\n    tags:\n      - Access Management\n      - Security\n    serviceName: HashiCorp Boundary\n    serviceCategory: API\n  - name: HashiCorp Vagrant\n    baseURL: ''\n    tags:\n      - Development Environments\n      - Virtual Machines\n    serviceName: HashiCorp Vagrant\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per Managed Resource\n    metric: billed_cost / terraform_managed_resources\n    target: TBD\n  - name: Cost per Workspace\n    metric: billed_cost / active_workspaces\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/hashicorp/refs/heads/main/finops/hashicorp-finops.yml
sources:
- https://www.hashicorp.com/en/products/terraform/pricing
- https://developer.hashicorp.com/terraform/cloud-docs/api-docs
specification: FinOps Framework
tags:
- Cloud
- DevOps
- Infrastructure
- Platform
- FinOps
- Cost Management
- FOCUS
---
