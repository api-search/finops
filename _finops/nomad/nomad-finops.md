---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: nomad-http-api-openapi.yml
  format: yaml
  label: HashiCorp Nomad HTTP API
  slug: http-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/nomad/refs/heads/main/openapi/nomad-http-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Purchase
  - Usage
  - Tax
  - Adjustment
  pricingCategory: Subscription + Pay-As-You-Go
description: 'FOCUS-aligned FinOps for HashiCorp Nomad: Community Edition is free; Enterprise is contracted per-resource / per-cluster; HCP Nomad bills via IBM PAYG or HashiCorp Flex multi-year plans.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: HashiCorp, Inc. (IBM)
  PricingCategory: Subscription
  ProviderName: HashiCorp
  PublisherName: HashiCorp, Inc. (IBM)
  ServiceCategory: Workload Orchestration
  ServiceName: HashiCorp Nomad
  ServiceSubcategory: Container / Workload Scheduler
layout: finops
meters:
- aggregation: avg
  description: Licensed Nomad Enterprise clusters under contract.
  dimensions:
  - environment
  - region
  name: nomad_enterprise_clusters
  unit: cluster-month
- aggregation: avg
  description: Nomad Enterprise client/server nodes counted against license.
  dimensions:
  - region
  - tier
  name: nomad_enterprise_nodes
  unit: node-month
- aggregation: sum
  description: HCP Nomad managed-service consumption via IBM PAYG.
  dimensions:
  - region
  - sku
  name: hcp_nomad_payg
  unit: hour
- aggregation: sum
  description: HashiCorp / IBM enterprise support tier subscription.
  dimensions:
  - tier
  name: support_subscription
  unit: month
name: Nomad Finops
provider_name: HashiCorp Nomad
provider_slug: nomad
publisher_name: HashiCorp, Inc. (IBM)
service_category: Workload Orchestration
slug: nomad-finops
source_filename: nomad-finops.yml
source_heading: FinOps Profile
source_url: https://www.hashicorp.com/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: HashiCorp Nomad\nproviderId: nomad\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Workload Orchestration\n  - DevOps\n  - Cost Management\nnotes: HashiCorp / IBM does not publish public Nomad-specific PAYG rates; FinOps shape captured here\n  follows the documented HashiCorp pricing patterns (Community free, Enterprise contracted, HCP PAYG/Flex).\n  Reconcile against the IBM HashiCorp Cloud Platform pricing table or customer ELA quote.\ndescription: 'FOCUS-aligned FinOps for HashiCorp Nomad: Community Edition is free; Enterprise is contracted\n  per-resource / per-cluster; HCP Nomad bills via IBM PAYG or HashiCorp Flex multi-year plans.'\nsources:\n  - https://www.hashicorp.com/pricing\n  - https://developer.hashicorp.com/nomad\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n\
  \  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: HashiCorp, Inc. (IBM)\nserviceCategory: Workload Orchestration\nbillingModel:\n  pricingCategory: Subscription + Pay-As-You-Go\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\n    - Tax\n    - Adjustment\nfocusColumns:\n  ServiceName: HashiCorp Nomad\n  ServiceCategory: Workload Orchestration\n  ServiceSubcategory: Container / Workload Scheduler\n  ProviderName: HashiCorp\n  PublisherName: HashiCorp, Inc. (IBM)\n  InvoiceIssuerName: HashiCorp, Inc. (IBM)\n  BillingCurrency: USD\n  PricingCategory: Subscription\nmeters:\n  - name: nomad_enterprise_clusters\n    description: Licensed Nomad Enterprise clusters under contract.\n    unit: cluster-month\n    aggregation: avg\n    dimensions:\n      - environment\n      - region\n  - name: nomad_enterprise_nodes\n    description: Nomad Enterprise client/server nodes\
  \ counted against license.\n    unit: node-month\n    aggregation: avg\n    dimensions:\n      - region\n      - tier\n  - name: hcp_nomad_payg\n    description: HCP Nomad managed-service consumption via IBM PAYG.\n    unit: hour\n    aggregation: sum\n    dimensions:\n      - region\n      - sku\n  - name: support_subscription\n    description: HashiCorp / IBM enterprise support tier subscription.\n    unit: month\n    aggregation: sum\n    dimensions:\n      - tier\nprinciples:\n  - name: Visibility\n    description: Use Nomad's metrics API (Prometheus exposition) for scheduler and allocation utilization;\n      use HashiCorp Cloud Platform billing dashboard or IBM PAYG console for managed billing.\n  - name: Allocation\n    description: Use namespaces (Enterprise) to attribute scheduler and node consumption per team; tag\n      jobs with cost-center metadata; map clusters to business units.\n  - name: Optimization\n    description: Use bin-packing scheduler placement constraints to\
  \ maximize node utilization; set resource\n      `cpu` / `memory` requests accurately; consolidate Community workloads where governance allows;\n      retire idle Enterprise nodes before renewal.\n  - name: Accountability\n    description: Assign per-namespace owners for spend; review quarterly cluster headcount vs. node license\n      utilization; reconcile HCP Nomad PAYG charges against capacity-planning forecasts.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/nomad/refs/heads/main/finops/nomad-finops.yml
sources:
- https://www.hashicorp.com/pricing
- https://developer.hashicorp.com/nomad
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Workload Orchestration
- DevOps
- Cost Management
---
