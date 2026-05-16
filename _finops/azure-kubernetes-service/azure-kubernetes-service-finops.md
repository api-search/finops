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
  slug: azure-kubernetes-service-rest-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/azure-kubernetes-service/refs/heads/main/openapi/azure-kubernetes-service-openapi.yml
- filename: azure-kubernetes-service-openapi.yml
  format: yaml
  label: Azure Kubernetes Service Managed Clusters API
  slug: azure-kubernetes-service-managed-clusters-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/azure-kubernetes-service/refs/heads/main/openapi/azure-kubernetes-service-openapi.yml
- filename: azure-kubernetes-service-openapi.yml
  format: yaml
  label: Azure Kubernetes Service Agent Pools API
  slug: azure-kubernetes-service-agent-pools-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/azure-kubernetes-service/refs/heads/main/openapi/azure-kubernetes-service-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  - Tax
  - Adjustment
  pricingCategory: Pay-As-You-Go + Committed Use
description: 'FOCUS-aligned FinOps for Azure Kubernetes Service: free cluster management on the Free tier (no SLA), pay-per-cluster-hour on Standard / Premium for control-plane SLA, plus pay-as-you-go for the underlying VMs, disks, load balancers, and egress. Tier choice and node-pool right-sizing dominate total cost.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Microsoft Corporation
  PricingCategory: Pay-As-You-Go
  ProviderName: Microsoft
  PublisherName: Microsoft Corporation
  ServiceCategory: Container Platform
  ServiceName: Azure Kubernetes Service
layout: finops
meters:
- aggregation: sum
  description: Per-cluster-hour management charge on Standard / Premium tiers
  dimensions:
  - tier
  - region
  - cluster
  name: control_plane_hours
  unit: cluster-hour
- aggregation: sum
  description: Agent node compute time
  dimensions:
  - vm_sku
  - region
  - node_pool
  - cluster
  name: node_vm_hours
  unit: instance-hour
- aggregation: avg
  description: OS disks and persistent volumes
  dimensions:
  - disk_tier
  - region
  name: managed_disks
  unit: GB-month
- aggregation: sum
  description: Standard Load Balancer rules and data processed
  dimensions:
  - region
  name: load_balancer
  unit: rule-hour
- aggregation: sum
  description: Internet / cross-region traffic from cluster
  dimensions:
  - region
  - destination
  name: egress_bandwidth
  unit: GB
name: Azure Kubernetes Service Finops
provider_name: Azure Kubernetes Service
provider_slug: azure-kubernetes-service
publisher_name: Microsoft Corporation
service_category: Container Platform
slug: azure-kubernetes-service-finops
source_filename: azure-kubernetes-service-finops.yml
source_heading: FinOps Profile
source_url: https://azure.microsoft.com/en-us/pricing/details/kubernetes-service/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Azure Kubernetes Service\nproviderId: azure-kubernetes-service\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - Containers\n  - Kubernetes\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps for Azure Kubernetes Service: free cluster management on the Free\n  tier (no SLA), pay-per-cluster-hour on Standard / Premium for control-plane SLA, plus pay-as-you-go\n  for the underlying VMs, disks, load balancers, and egress. Tier choice and node-pool right-sizing dominate\n  total cost.'\nsources:\n  - https://azure.microsoft.com/en-us/pricing/details/kubernetes-service/\n  - https://learn.microsoft.com/en-us/azure/aks/free-standard-pricing-tiers\n  - https://learn.microsoft.com/en-us/azure/aks/quotas-skus-regions\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n\
  \  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Microsoft Corporation\nserviceCategory: Container Platform\nbillingModel:\n  pricingCategory: Pay-As-You-Go + Committed Use\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Adjustment\nfocusColumns:\n  ServiceName: Azure Kubernetes Service\n  ServiceCategory: Container Platform\n  ProviderName: Microsoft\n  PublisherName: Microsoft Corporation\n  InvoiceIssuerName: Microsoft Corporation\n  PricingCategory: Pay-As-You-Go\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: control_plane_hours\n    description: Per-cluster-hour management charge on Standard / Premium tiers\n    unit: cluster-hour\n    aggregation: sum\n    dimensions:\n      - tier\n      - region\n      - cluster\n  - name: node_vm_hours\n    description: Agent node compute time\n    unit: instance-hour\n    aggregation: sum\n\
  \    dimensions:\n      - vm_sku\n      - region\n      - node_pool\n      - cluster\n  - name: managed_disks\n    description: OS disks and persistent volumes\n    unit: GB-month\n    aggregation: avg\n    dimensions:\n      - disk_tier\n      - region\n  - name: load_balancer\n    description: Standard Load Balancer rules and data processed\n    unit: rule-hour\n    aggregation: sum\n    dimensions:\n      - region\n  - name: egress_bandwidth\n    description: Internet / cross-region traffic from cluster\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - region\n      - destination\nprinciples:\n  - name: Visibility\n    description: Use AKS Cost Analysis (preview) which integrates with OpenCost; layer Azure Cost Management\n      tag-based filters by namespace, deployment, and pod label propagated from cluster tags.\n  - name: Allocation\n    description: Tag clusters and node pools; map Kubernetes namespaces to teams via cost allocation\n      labels; use OpenCost or Microsoft\
  \ Cost Analysis to break down by workload.\n  - name: Optimization\n    description: Use Free tier for non-production; pick Standard over Premium unless LTS is required;\n      enable cluster autoscaler and Karpenter-style pod-driven scaling; right-size VM SKUs; use Spot\n      node pools for fault-tolerant workloads; commit to Azure Reservations or Savings Plans for steady\n      node pools.\n  - name: Accountability\n    description: Assign cluster admins as cost owners; review monthly per-namespace cost trends; alert\n      on unattended node-pool growth or Spot eviction-driven cost spikes.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/azure-kubernetes-service/refs/heads/main/finops/azure-kubernetes-service-finops.yml
sources:
- https://azure.microsoft.com/en-us/pricing/details/kubernetes-service/
- https://learn.microsoft.com/en-us/azure/aks/free-standard-pricing-tiers
- https://learn.microsoft.com/en-us/azure/aks/quotas-skus-regions
specification: FinOps Framework
tags:
- Containers
- Kubernetes
- FinOps
- FOCUS
---
