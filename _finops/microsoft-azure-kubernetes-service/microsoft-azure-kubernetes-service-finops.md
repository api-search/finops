---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: azure-kubernetes-service-openapi.yml
  format: yaml
  label: Azure Kubernetes Service REST API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-azure-kubernetes-service/refs/heads/main/openapi/azure-kubernetes-service-openapi.yml
- filename: azure-kubernetes-service-openapi.yml
  format: yaml
  label: Azure Kubernetes Service Managed Clusters API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-azure-kubernetes-service/refs/heads/main/openapi/azure-kubernetes-service-openapi.yml
- filename: azure-kubernetes-service-openapi.yml
  format: yaml
  label: Azure Kubernetes Service Agent Pools API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-azure-kubernetes-service/refs/heads/main/openapi/azure-kubernetes-service-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  - Tax
  - Adjustment
  - Credit
  pricingCategory: Pay-As-You-Go + Committed Use
description: 'FOCUS-aligned FinOps for Azure Kubernetes Service: tier-priced cluster-management hourly fee (Free 0, Standard $0.10, Premium $0.60 per cluster-hour) plus pass-through Azure VM, disk, and network costs for worker nodes.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Microsoft Corporation
  ProviderName: Microsoft
  PublisherName: Microsoft Corporation
  ServiceCategory: Compute
  ServiceName: Azure Kubernetes Service
layout: finops
meters:
- aggregation: sum
  dimensions:
  - tier
  - region
  - cluster
  name: cluster_management_hours
  unit: cluster-hour
- aggregation: sum
  dimensions:
  - vm_sku
  - region
  - nodepool
  - cluster
  name: worker_node_vm_hours
  unit: instance-hour
- aggregation: avg
  dimensions:
  - disk_sku
  - region
  - cluster
  name: managed_disk_gb_month
  unit: GB-month
- aggregation: sum
  dimensions:
  - region
  - cluster
  name: load_balancer_hours
  unit: instance-hour
- aggregation: sum
  dimensions:
  - region
  - cluster
  name: data_egress
  unit: GB
- aggregation: avg
  dimensions:
  - cluster
  name: container_storage_gb_month
  unit: GB-month
name: Microsoft Azure Kubernetes Service Finops
provider_name: Azure Kubernetes Service
provider_slug: microsoft-azure-kubernetes-service
publisher_name: Microsoft Corporation
service_category: Compute / Container Orchestration
slug: microsoft-azure-kubernetes-service-finops
source_filename: microsoft-azure-kubernetes-service-finops.yml
source_heading: FinOps Profile
source_url: https://azure.microsoft.com/en-us/pricing/details/kubernetes-service/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Azure Kubernetes Service\nproviderId: microsoft-azure-kubernetes-service\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Kubernetes\n  - Containers\n  - Microsoft Azure\ndescription: 'FOCUS-aligned FinOps for Azure Kubernetes Service: tier-priced cluster-management hourly\n  fee (Free 0, Standard $0.10, Premium $0.60 per cluster-hour) plus pass-through Azure VM, disk, and\n  network costs for worker nodes.'\nsources:\n  - https://azure.microsoft.com/en-us/pricing/details/kubernetes-service/\n  - https://learn.microsoft.com/en-us/azure/aks/cost-analysis\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Microsoft Corporation\nserviceCategory:\
  \ Compute / Container Orchestration\nbillingModel:\n  pricingCategory: Pay-As-You-Go + Committed Use\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Adjustment\n    - Credit\nfocusColumns:\n  ServiceName: Azure Kubernetes Service\n  ServiceCategory: Compute\n  ProviderName: Microsoft\n  PublisherName: Microsoft Corporation\n  InvoiceIssuerName: Microsoft Corporation\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: cluster_management_hours\n    unit: cluster-hour\n    aggregation: sum\n    dimensions:\n      - tier\n      - region\n      - cluster\n  - name: worker_node_vm_hours\n    unit: instance-hour\n    aggregation: sum\n    dimensions:\n      - vm_sku\n      - region\n      - nodepool\n      - cluster\n  - name: managed_disk_gb_month\n    unit: GB-month\n    aggregation: avg\n    dimensions:\n      - disk_sku\n      - region\n      - cluster\n  - name: load_balancer_hours\n    unit: instance-hour\n\
  \    aggregation: sum\n    dimensions:\n      - region\n      - cluster\n  - name: data_egress\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - region\n      - cluster\n  - name: container_storage_gb_month\n    unit: GB-month\n    aggregation: avg\n    dimensions:\n      - cluster\nprinciples:\n  - name: Visibility\n    description: Use AKS Cost Analysis (built-in cost view powered by OpenCost) to break down spend\n      by namespace, deployment, and label; export Azure Cost Management to a Log Analytics workspace\n      for deeper analysis.\n  - name: Allocation\n    description: Use Kubernetes namespaces and labels (team, cost-center, environment) propagated\n      to AKS Cost Analysis tags; place per-team workloads in isolated node pools where chargeback\n      requires hard separation.\n  - name: Optimization\n    description: Right-size requests/limits with VPA recommendations; use Cluster Autoscaler / Karpenter;\n      mix Reserved Instances and Spot node pools; consolidate\
  \ dev/test on Free tier; pick Standard\n      over Premium when LTS is not required.\n  - name: Accountability\n    description: Assign cluster owners; alert on cost-per-namespace anomalies; review node-pool\n      sizing monthly; periodically delete idle clusters and orphaned PVCs.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/microsoft-azure-kubernetes-service/refs/heads/main/finops/microsoft-azure-kubernetes-service-finops.yml
sources:
- https://azure.microsoft.com/en-us/pricing/details/kubernetes-service/
- https://learn.microsoft.com/en-us/azure/aks/cost-analysis
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Kubernetes
- Containers
- Microsoft Azure
---
