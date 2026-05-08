---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: virtualMachines.json
  format: json
  label: Azure Virtual Machines REST API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/Azure/azure-rest-api-specs/main/specification/compute/resource-manager/Microsoft.Compute/ComputeRP/stable/2023-09-01/virtualMachines.json
billing_model:
  billingCurrency: USD (settlement varies)
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  - Tax
  - Adjustment
  - Refund
  - Credit
  chargeFrequency: Recurring
  pricingCategory: Pay-As-You-Go + Committed Use + Spot
description: FOCUS-aligned FinOps for Azure Virtual Machines — the largest single Azure spend category for most customers. Per-second metered with 1-minute minimum; multiple commitment paths (Reserved Instances, Savings Plans, Spot, Hybrid Benefit) drive 30–90% savings. Azure Advisor surfaces right-sizing opportunities; Cost Management exports are FOCUS-conformant.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Microsoft Corporation
  PricingCategory: Usage-Based
  PricingUnit: instance-hour
  ProviderName: Microsoft Azure
  PublisherName: Microsoft Corporation
  RegionId: varies (eastus, westeurope, ...)
  ServiceCategory: Compute
  ServiceName: Azure Virtual Machines
layout: finops
meters:
- aggregation: sum
  description: Pay-as-you-go VM compute hours by SKU and region.
  dimensions:
  - vm_size
  - region
  - os_type
  - resource_group
  name: vm_instance_hours
  unit: instance-hour
- aggregation: sum
  description: VM-hours covered by Reserved Instance commitments.
  dimensions:
  - vm_family
  - term_years
  - scope
  name: vm_reserved_hours
  unit: instance-hour
- aggregation: sum
  description: Azure Savings Plan for Compute hourly $-commitment.
  dimensions:
  - term_years
  - billing_account
  name: savings_plan_commitment
  unit: hour-commit
- aggregation: sum
  description: Spot VM hours consumed.
  dimensions:
  - vm_size
  - region
  - eviction_policy
  name: spot_instance_hours
  unit: instance-hour
- aggregation: max
  description: Premium SSD / Standard SSD / Standard HDD storage attached to VMs.
  dimensions:
  - disk_type
  - region
  name: managed_disk_gb_month
  unit: GB-month
- aggregation: sum
  description: VM outbound data transfer billed under Azure bandwidth meter.
  dimensions:
  - source_region
  - destination_zone
  name: data_egress
  unit: GB
- aggregation: sum
  description: Windows Server / SQL Server / RHEL / SUSE license premium per vCPU-hour (excluded if using Azure Hybrid Benefit).
  dimensions:
  - license_type
  - bring_your_own_license
  name: license_premium
  unit: vcpu-hour
name: Microsoft Azure Virtual Machines Finops
provider_name: Azure Virtual Machines
provider_slug: microsoft-azure-virtual-machines
publisher_name: Microsoft Corporation
service_category: Cloud Compute / IaaS
slug: microsoft-azure-virtual-machines-finops
source_filename: microsoft-azure-virtual-machines-finops.yml
source_heading: FinOps Profile
source_url: https://azure.microsoft.com/en-us/pricing/details/virtual-machines/linux/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Azure Virtual Machines\nproviderId: microsoft-azure-virtual-machines\npublisherName: Microsoft Corporation\nserviceCategory: Cloud Compute / IaaS\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - Cloud Computing\n  - Compute\n  - IaaS\n  - Infrastructure\n  - Virtual Machines\n  - FinOps\n  - FOCUS\ndescription: FOCUS-aligned FinOps for Azure Virtual Machines — the largest single Azure spend\n  category for most customers. Per-second metered with 1-minute minimum; multiple commitment\n  paths (Reserved Instances, Savings Plans, Spot, Hybrid Benefit) drive 30–90% savings.\n  Azure Advisor surfaces right-sizing opportunities;\
  \ Cost Management exports are FOCUS-conformant.\nsources:\n  - https://azure.microsoft.com/en-us/pricing/details/virtual-machines/linux/\n  - https://learn.microsoft.com/en-us/azure/cost-management-billing/\n  - https://learn.microsoft.com/en-us/azure/cost-management-billing/savings-plan/\n  - https://focus.finops.org/focus-specification/v1-3/\nbillingModel:\n  pricingCategory: Pay-As-You-Go + Committed Use + Spot\n  billingFrequency: Monthly\n  billingCurrency: USD (settlement varies)\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Adjustment\n    - Refund\n    - Credit\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Azure Virtual Machines\n  ServiceCategory: Compute\n  ProviderName: Microsoft Azure\n  PublisherName: Microsoft Corporation\n  InvoiceIssuerName: Microsoft Corporation\n  PricingCategory: Usage-Based\n  PricingUnit: instance-hour\n  BillingCurrency: USD\n  ChargeCategory: Usage\n  RegionId: varies (eastus, westeurope, ...)\nmeters:\n  - name:\
  \ vm_instance_hours\n    description: Pay-as-you-go VM compute hours by SKU and region.\n    unit: instance-hour\n    aggregation: sum\n    dimensions:\n      - vm_size\n      - region\n      - os_type\n      - resource_group\n  - name: vm_reserved_hours\n    description: VM-hours covered by Reserved Instance commitments.\n    unit: instance-hour\n    aggregation: sum\n    dimensions:\n      - vm_family\n      - term_years\n      - scope\n  - name: savings_plan_commitment\n    description: Azure Savings Plan for Compute hourly $-commitment.\n    unit: hour-commit\n    aggregation: sum\n    dimensions:\n      - term_years\n      - billing_account\n  - name: spot_instance_hours\n    description: Spot VM hours consumed.\n    unit: instance-hour\n    aggregation: sum\n    dimensions:\n      - vm_size\n      - region\n      - eviction_policy\n  - name: managed_disk_gb_month\n    description: Premium SSD / Standard SSD / Standard HDD storage attached to VMs.\n    unit: GB-month\n    aggregation:\
  \ max\n    dimensions:\n      - disk_type\n      - region\n  - name: data_egress\n    description: VM outbound data transfer billed under Azure bandwidth meter.\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - source_region\n      - destination_zone\n  - name: license_premium\n    description: Windows Server / SQL Server / RHEL / SUSE license premium per vCPU-hour\n      (excluded if using Azure Hybrid Benefit).\n    unit: vcpu-hour\n    aggregation: sum\n    dimensions:\n      - license_type\n      - bring_your_own_license\nprinciples:\n  - name: Visibility\n    description: Cost Management + Billing exposes per-resource VM-hour, per-disk, and per-license\n      line items. Azure Monitor metrics show CPU/memory/disk utilization to identify oversized\n      VMs. FOCUS-aligned billing exports v2 ingest into BI / FinOps platforms with consistent\n      column names (ResourceId, ServiceName, ChargeCategory).\n  - name: Allocation\n    description: Tag every VM with cost-center,\
  \ environment, application, owner. Enforce via\n      Azure Policy. Subscriptions / resource groups create natural chargeback boundaries.\n      Multi-tenant clusters can use container-level allocation if VMs run AKS workloads.\n  - name: Optimization\n    description: Right-size via Azure Advisor (idle / underutilized VMs). Stop dev/test VMs\n      off-hours via Auto-shutdown policies. Buy Reserved Instances or Savings Plans for steady\n      base load (target 60-80% of PAYG hours covered). Use Spot for batch / fault-tolerant\n      jobs (up to 90% off). Apply Azure Hybrid Benefit if you have Windows Server / SQL Server\n      Software Assurance. Migrate older v1/v2 sizes to current-gen v5/v6 for better $/perf.\n      Use AKS / Container Apps / Functions for workloads that don't need full VM.\n  - name: Accountability\n    description: Workload owners approve VM size changes. FinOps practitioner reviews monthly\n      Reserved/Savings coverage and recommends rebalances quarterly. Set\
  \ Cost Management\n      budgets per resource group / subscription with alerts at 50/80/100%. Anomaly detection\n      via Cost Management's Anomaly alerts catches unexpected spikes.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n    url: https://azure.microsoft.com/services/virtual-machines/\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/microsoft-azure-virtual-machines/refs/heads/main/finops/microsoft-azure-virtual-machines-finops.yml
sources:
- https://azure.microsoft.com/en-us/pricing/details/virtual-machines/linux/
- https://learn.microsoft.com/en-us/azure/cost-management-billing/
- https://learn.microsoft.com/en-us/azure/cost-management-billing/savings-plan/
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Cloud Computing
- Compute
- IaaS
- Infrastructure
- Virtual Machines
- FinOps
- FOCUS
---
