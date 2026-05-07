---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: nutanix-prism-central-v3-openapi.yml
  format: yaml
  label: Nutanix Prism Central API V3
  slug: prism-central-v3
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/nutanix/refs/heads/main/openapi/nutanix-prism-central-v3-openapi.yml
- filename: nutanix-prism-element-v2-openapi.yml
  format: yaml
  label: Nutanix Prism Element API V2
  slug: prism-element-v2
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/nutanix/refs/heads/main/openapi/nutanix-prism-element-v2-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Annual (subscription) or Hourly (NC2 via cloud)
  chargeCategories:
  - Purchase
  - Usage
  - Tax
  - Adjustment
  - Credit
  chargeFrequency: Recurring
  pricingCategory: Subscription (Per-Node) + Marketplace Hourly
description: 'FOCUS-aligned FinOps for Nutanix: per-node / per-core software subscription bundled with on-prem hardware, plus hourly metered NC2 in AWS/Azure cloud marketplaces. APIs are included with the license. Cost governance is provided by Nutanix Cloud Manager (NCM) Cost Governance.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Nutanix, Inc. (or AWS/Azure for NC2 marketplace)
  PricingCategory: Subscription
  PricingUnit: node
  ProviderName: Nutanix
  PublisherName: Nutanix, Inc.
  ServiceCategory: Hybrid Cloud Infrastructure
  ServiceName: Nutanix
layout: finops
meters:
- aggregation: sum
  description: Per-node Nutanix Cloud Infrastructure subscription
  dimensions:
  - edition
  - cluster
  - region
  name: nci_node_subscription
  unit: node
- aggregation: sum
  description: Per-core Nutanix Cloud Infrastructure subscription (capacity-based licensing)
  dimensions:
  - edition
  - cluster
  name: nci_core_subscription
  unit: core
- aggregation: sum
  description: Per-VM or per-core NCM (Cloud Manager) subscription
  dimensions:
  - product
  - cluster
  name: ncm_vm_subscription
  unit: vm
- aggregation: sum
  description: Per-database Nutanix Database Service subscription
  dimensions:
  - engine
  - cluster
  name: ndb_db_subscription
  unit: database
- aggregation: sum
  description: Hourly Nutanix software meter on NC2 (AWS/Azure)
  dimensions:
  - cloud
  - region
  - instance_type
  name: nc2_software_hours
  unit: instance-hour
- aggregation: sum
  description: Underlying cloud-provider infrastructure consumed by NC2
  dimensions:
  - cloud
  - region
  - instance_type
  name: nc2_cloud_infra
  unit: instance-hour
name: Nutanix Finops
provider_name: Nutanix
provider_slug: nutanix
publisher_name: Nutanix, Inc.
service_category: Hybrid Cloud Infrastructure
slug: nutanix-finops
source_filename: nutanix-finops.yml
source_heading: FinOps Profile
source_url: https://www.nutanix.com/products/cloud-platform
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Nutanix\nproviderId: nutanix\npublisherName: Nutanix, Inc.\nserviceCategory: Hybrid Cloud Infrastructure\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - Cloud Management\n  - Hyperconverged\n  - Infrastructure\n  - Virtualization\n  - Kubernetes\n  - Database\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps for Nutanix: per-node / per-core software subscription bundled with\n  on-prem hardware, plus hourly metered NC2 in AWS/Azure cloud marketplaces. APIs are included with the\n  license. Cost governance is provided by Nutanix Cloud Manager (NCM) Cost Governance.'\nsources:\n  - https://www.nutanix.com/products/cloud-platform\n\
  \  - https://www.nutanix.com/products/cloud-manager\n  - https://www.nutanix.com/products/cloud-clusters\nprinciples:\n  - name: Visibility\n    description: Use NCM Cost Governance (formerly Beam) to see consumption and chargeback across on-prem\n      Nutanix clusters and NC2 cloud spend. Pull NC2 billing from AWS Cost Explorer / Azure Cost Management\n      via FOCUS-aligned exports; pull on-prem usage from Prism Central.\n  - name: Allocation\n    description: Tag VMs and projects in Prism Central / NCM Self-Service for chargeback. Use NC2 cloud\n      tags to allocate AWS/Azure infrastructure spend back to consuming teams.\n  - name: Optimization\n    description: Use NCM Cost Governance recommendations to right-size VMs, identify idle resources, and\n      optimize NC2 footprint. Burst into NC2 only when on-prem capacity is exhausted; run baseline in\n      lower-cost on-prem.\n  - name: Accountability\n    description: 'Establish per-business-unit chargeback via NCM. Assign owners\
  \ for: on-prem cluster utilization,\n      NC2 cloud spend, and NDB database sprawl. Review monthly.'\nbillingModel:\n  pricingCategory: Subscription (Per-Node) + Marketplace Hourly\n  billingFrequency: Annual (subscription) or Hourly (NC2 via cloud)\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\n    - Tax\n    - Adjustment\n    - Credit\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Nutanix\n  ServiceCategory: Hybrid Cloud Infrastructure\n  ProviderName: Nutanix\n  PublisherName: Nutanix, Inc.\n  InvoiceIssuerName: Nutanix, Inc. (or AWS/Azure for NC2 marketplace)\n  PricingCategory: Subscription\n  PricingUnit: node\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: nci_node_subscription\n    description: Per-node Nutanix Cloud Infrastructure subscription\n    unit: node\n    aggregation: sum\n    dimensions:\n      - edition\n      - cluster\n      - region\n  - name: nci_core_subscription\n    description: Per-core Nutanix\
  \ Cloud Infrastructure subscription (capacity-based licensing)\n    unit: core\n    aggregation: sum\n    dimensions:\n      - edition\n      - cluster\n  - name: ncm_vm_subscription\n    description: Per-VM or per-core NCM (Cloud Manager) subscription\n    unit: vm\n    aggregation: sum\n    dimensions:\n      - product\n      - cluster\n  - name: ndb_db_subscription\n    description: Per-database Nutanix Database Service subscription\n    unit: database\n    aggregation: sum\n    dimensions:\n      - engine\n      - cluster\n  - name: nc2_software_hours\n    description: Hourly Nutanix software meter on NC2 (AWS/Azure)\n    unit: instance-hour\n    aggregation: sum\n    dimensions:\n      - cloud\n      - region\n      - instance_type\n  - name: nc2_cloud_infra\n    description: Underlying cloud-provider infrastructure consumed by NC2\n    unit: instance-hour\n    aggregation: sum\n    dimensions:\n      - cloud\n      - region\n      - instance_type\napis:\n  - name: Nutanix Prism Central\
  \ API V3\n    baseURL: https://{{prism-central-ip}}:9440/api/nutanix/v3\n    tags:\n      - Cloud Management\n      - Infrastructure\n      - Virtualization\n    serviceName: Nutanix Prism Central API V3\n    serviceCategory: Cloud Management\n  - name: Nutanix Prism Central API V4\n    baseURL: https://{{prism-central-ip}}:9440/api\n    tags:\n      - Cloud Management\n      - SDK\n    serviceName: Nutanix Prism Central API V4\n    serviceCategory: Cloud Management\n  - name: Nutanix Prism Element API V2\n    baseURL: https://{{cluster-ip}}:9440/PrismGateway/services/rest/v2.0\n    tags:\n      - Cluster Management\n      - Storage\n    serviceName: Nutanix Prism Element API V2\n    serviceCategory: Cluster Management\n  - name: Nutanix Karbon API\n    baseURL: ''\n    tags:\n      - Container Management\n      - Kubernetes\n    serviceName: Nutanix Karbon API\n    serviceCategory: Container Management\n  - name: Nutanix Database Service API\n    baseURL: ''\n    tags:\n      - Database\n\
  \      - DBaaS\n    serviceName: Nutanix Database Service API\n    serviceCategory: Database\n  - name: Nutanix Cloud Clusters API\n    baseURL: https://api.nutanix.com\n    tags:\n      - AWS\n      - Azure\n      - Hybrid Cloud\n    serviceName: Nutanix Cloud Clusters API\n    serviceCategory: Hybrid Cloud\n  - name: Nutanix NCM Self-Service API\n    baseURL: ''\n    tags:\n      - Automation\n      - Application Management\n    serviceName: Nutanix NCM Self-Service API\n    serviceCategory: Cloud Management\n  - name: Nutanix Foundation API\n    baseURL: ''\n    tags:\n      - Cluster Deployment\n      - Automation\n    serviceName: Nutanix Foundation API\n    serviceCategory: Cluster Management\nunitEconomics:\n  - name: Cost per VM-month (on-prem)\n    metric: nci_subscription_cost / running_vms\n    target: track against AWS/Azure equivalent for buy/burst decisions\n  - name: Cost per NC2 cluster-hour\n    metric: nc2_software_hours_cost + nc2_cloud_infra_cost / nc2_active_clusters\n\
  \    target: minimize via reserved instances on AWS/Azure for steady-state\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/nutanix/refs/heads/main/finops/nutanix-finops.yml
sources:
- https://www.nutanix.com/products/cloud-platform
- https://www.nutanix.com/products/cloud-manager
- https://www.nutanix.com/products/cloud-clusters
specification: FinOps Framework
tags:
- Cloud Management
- Hyperconverged
- Infrastructure
- Virtualization
- Kubernetes
- Database
- FinOps
- Cost Management
- FOCUS
---
