---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: swagger.json
  format: json
  label: OpenShift REST API
  slug: openshift-rest-api
  spec_type: OpenAPI
  url: https://api.openshift.com/api/swagger.json
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  - Adjustment
  - Credit
  pricingCategory: Subscription + Pay-As-You-Go + Committed Use
description: 'FOCUS-aligned FinOps for Red Hat OpenShift: subscription per-core for self-managed editions and per-vCPU hourly + optional 1/3-year reserved for cloud-services editions (ROSA, ARO, Dedicated, IBM Cloud). Underlying cloud-provider compute, storage, and network costs are billed separately by the hyperscaler.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Red Hat / AWS / Microsoft / Google / IBM (depending on edition)
  ProviderName: Red Hat
  PublisherName: Red Hat, Inc.
  ServiceCategory: Application Platform / Containers
  ServiceName: Red Hat OpenShift
layout: finops
meters:
- aggregation: sum
  dimensions:
  - cluster
  - region
  - node_type
  - edition
  name: worker_vcpu_hours
  unit: vCPU-hour
- aggregation: sum
  dimensions:
  - cluster
  - edition
  - region
  name: control_plane_hours
  unit: cluster-hour
- aggregation: sum
  dimensions:
  - term
  - region
  name: reserved_instances
  unit: 4-vCPU-year
- aggregation: sum
  dimensions:
  - edition
  - environment
  name: self_managed_subscription_cores
  unit: core-year
- aggregation: sum
  dimensions:
  - storage_class
  - cluster
  name: persistent_storage
  unit: GB-month
- aggregation: sum
  dimensions:
  - cluster
  - region
  name: data_egress
  unit: GB
name: Openshift Finops
provider_name: OpenShift
provider_slug: openshift
publisher_name: Red Hat, Inc. (IBM)
service_category: Application Platform / Containers
slug: openshift-finops
source_filename: openshift-finops.yml
source_heading: FinOps Profile
source_url: https://www.redhat.com/en/technologies/cloud-computing/openshift/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: OpenShift\nproviderId: openshift\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - Containers\n  - Kubernetes\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps for Red Hat OpenShift: subscription per-core for self-managed editions\n  and per-vCPU hourly + optional 1/3-year reserved for cloud-services editions (ROSA, ARO, Dedicated,\n  IBM Cloud). Underlying cloud-provider compute, storage, and network costs are billed separately by the\n  hyperscaler.'\nsources:\n  - https://www.redhat.com/en/technologies/cloud-computing/openshift/pricing\n  - https://aws.amazon.com/rosa/pricing/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName:\
  \ Red Hat, Inc. (IBM)\nserviceCategory: Application Platform / Containers\nbillingModel:\n  pricingCategory: Subscription + Pay-As-You-Go + Committed Use\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Adjustment\n    - Credit\nfocusColumns:\n  ServiceName: Red Hat OpenShift\n  ServiceCategory: Application Platform / Containers\n  ProviderName: Red Hat\n  PublisherName: Red Hat, Inc.\n  InvoiceIssuerName: Red Hat / AWS / Microsoft / Google / IBM (depending on edition)\n  BillingCurrency: USD\nmeters:\n  - name: worker_vcpu_hours\n    unit: vCPU-hour\n    aggregation: sum\n    dimensions:\n      - cluster\n      - region\n      - node_type\n      - edition\n  - name: control_plane_hours\n    unit: cluster-hour\n    aggregation: sum\n    dimensions:\n      - cluster\n      - edition\n      - region\n  - name: reserved_instances\n    unit: 4-vCPU-year\n    aggregation: sum\n    dimensions:\n      - term\n      - region\n  - name:\
  \ self_managed_subscription_cores\n    unit: core-year\n    aggregation: sum\n    dimensions:\n      - edition\n      - environment\n  - name: persistent_storage\n    unit: GB-month\n    aggregation: sum\n    dimensions:\n      - storage_class\n      - cluster\n  - name: data_egress\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - cluster\n      - region\nprinciples:\n  - name: Visibility\n    description: Use the OpenShift Cost Management operator (Koku/Cost-mgmt) plus the underlying cloud\n      bill (AWS Cost Explorer, Azure Cost Management) to attribute spend by namespace, label, and cluster.\n  - name: Allocation\n    description: Tag all namespaces and workloads with team / app / environment labels; the Cost Management\n      operator allocates cluster cost to namespaces based on CPU/memory usage.\n  - name: Optimization\n    description: Convert sustained on-demand ROSA workloads to 1- or 3-year reserved (33%/55% discounts);\n      right-size requests/limits, enable\
  \ cluster autoscaler, use spot worker pools for non-critical workloads,\n      and consolidate clusters where possible.\n  - name: Accountability\n    description: Platform team owns cluster-level subscription cost; application teams own namespace-level\n      consumption. Set namespace ResourceQuota and budget alerts in the cloud provider's cost tool.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/openshift/refs/heads/main/finops/openshift-finops.yml
sources:
- https://www.redhat.com/en/technologies/cloud-computing/openshift/pricing
- https://aws.amazon.com/rosa/pricing/
specification: FinOps Framework
tags:
- Containers
- Kubernetes
- FinOps
- Cost Management
- FOCUS
---
