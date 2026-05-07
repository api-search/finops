---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: consul-connect-openapi.yml
  format: yaml
  label: Consul Connect HTTP API
  slug: consul-connect-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/consul-connect/refs/heads/main/openapi/consul-connect-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  - Tax
  - Credit
  pricingCategory: Subscription + Pay-As-You-Go
description: 'FOCUS-aligned FinOps for Consul Connect: open-source service mesh APIs are free; commercial cost lives in Consul Enterprise (self-managed license) and HCP Consul (managed, usage-based on the IBM HashiCorp Cloud Platform). Track infrastructure cost (compute, network) for self-hosted clusters alongside the HashiCorp / IBM line items.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: HashiCorp, Inc. (an IBM company)
  ProviderName: HashiCorp
  PublisherName: HashiCorp, Inc. (an IBM company)
  ServiceCategory: Service Mesh / Networking
  ServiceName: Consul Connect
layout: finops
meters:
- aggregation: sum
  description: Managed HCP Consul cluster runtime hours
  dimensions:
  - cluster_size
  - region
  - environment
  name: hcp_consul_runtime
  unit: instance-hour
- aggregation: max
  description: Self-managed Consul Enterprise license (annual / multi-year)
  dimensions:
  - cluster
  - tier
  name: consul_enterprise_license
  unit: month
- aggregation: sum
  description: Compute / storage / network cost of operating self-hosted Consul agents and gateways
  dimensions:
  - cloud_provider
  - region
  - cluster
  name: self_hosted_infrastructure
  unit: instance-hour
- aggregation: sum
  description: WAN / mesh-gateway egress between datacenters
  dimensions:
  - source_dc
  - dest_dc
  name: cross_dc_traffic
  unit: GB
name: Consul Connect Finops
provider_name: Consul Connect
provider_slug: consul-connect
publisher_name: HashiCorp, Inc. (an IBM company)
service_category: Service Mesh / Networking
slug: consul-connect-finops
source_filename: consul-connect-finops.yml
source_heading: FinOps Profile
source_url: https://www.hashicorp.com/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Consul Connect\nproviderId: consul-connect\npublisherName: HashiCorp, Inc. (an IBM company)\nserviceCategory: Service Mesh / Networking\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Consul\n  - HashiCorp\n  - Service Mesh\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps for Consul Connect: open-source service mesh APIs are free; commercial\n  cost lives in Consul Enterprise (self-managed license) and HCP Consul (managed, usage-based on the\n  IBM HashiCorp Cloud Platform). Track infrastructure cost (compute, network) for self-hosted clusters\n  alongside the HashiCorp / IBM line items.'\nnotes: HashiCorp\
  \ does not publish a single canonical per-resource price for HCP Consul publicly; reconcile\n  against the active HCP / Consul Enterprise contract or the HCP pricing calculator at runtime.\nsources:\n  - https://www.hashicorp.com/pricing\n  - https://developer.hashicorp.com/consul\nbillingModel:\n  pricingCategory: Subscription + Pay-As-You-Go\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\nfocusColumns:\n  ServiceName: Consul Connect\n  ServiceCategory: Service Mesh / Networking\n  ProviderName: HashiCorp\n  PublisherName: HashiCorp, Inc. (an IBM company)\n  InvoiceIssuerName: HashiCorp, Inc. (an IBM company)\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: hcp_consul_runtime\n    description: Managed HCP Consul cluster runtime hours\n    unit: instance-hour\n    aggregation: sum\n    dimensions:\n      - cluster_size\n      - region\n      - environment\n  - name: consul_enterprise_license\n\
  \    description: Self-managed Consul Enterprise license (annual / multi-year)\n    unit: month\n    aggregation: max\n    dimensions:\n      - cluster\n      - tier\n  - name: self_hosted_infrastructure\n    description: Compute / storage / network cost of operating self-hosted Consul agents and gateways\n    unit: instance-hour\n    aggregation: sum\n    dimensions:\n      - cloud_provider\n      - region\n      - cluster\n  - name: cross_dc_traffic\n    description: WAN / mesh-gateway egress between datacenters\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - source_dc\n      - dest_dc\nprinciples:\n  - name: Visibility\n    description: Use the HCP console (or Consul UI for self-hosted) plus Prometheus / OTel metrics from\n      `consul.*` for per-cluster cost-and-utilization views; stream HCP usage to FOCUS-aligned exports\n      through IBM HashiCorp Cloud Platform billing.\n  - name: Allocation\n    description: Tag clusters and admin partitions / namespaces (Enterprise)\
  \ per business unit; correlate\n      cloud-provider tags on the underlying VMs / Kubernetes nodes.\n  - name: Optimization\n    description: Right-size cluster sizes against Raft load; consolidate via admin partitions; prefer\n      mesh gateways over public LBs for cross-DC traffic; consider Flex Plans for predictable HCP discounts;\n      use the OSS edition where Enterprise features are not needed.\n  - name: Accountability\n    description: Platform / SRE teams typically own Consul cluster spend; product teams own per-service\n      mesh footprint and cross-DC traffic generated by their workloads.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/consul-connect/refs/heads/main/finops/consul-connect-finops.yml
sources:
- https://www.hashicorp.com/pricing
- https://developer.hashicorp.com/consul
specification: FinOps Framework
tags:
- Consul
- HashiCorp
- Service Mesh
- FinOps
- FOCUS
---
