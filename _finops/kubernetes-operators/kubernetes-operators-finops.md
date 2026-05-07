---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: kubernetes-operators-watch-asyncapi.yml
  format: yaml
  label: Kubernetes Operators
  slug: kubernetes-operators
  spec_type: AsyncAPI
  url: https://raw.githubusercontent.com/api-evangelist/kubernetes-operators/refs/heads/main/asyncapi/kubernetes-operators-watch-asyncapi.yml
- filename: kubernetes-crd-openapi.yml
  format: yaml
  label: Kubernetes Custom Resource Definitions
  slug: custom-resource-definitions
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/kubernetes-operators/refs/heads/main/openapi/kubernetes-crd-openapi.yml
- filename: kubernetes-olm-openapi.yml
  format: yaml
  label: Operator Lifecycle Manager
  slug: operator-lifecycle-manager
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/kubernetes-operators/refs/heads/main/openapi/kubernetes-olm-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: N/A
  chargeCategories:
  - Usage
  pricingCategory: Open Source (no license fee)
description: 'FOCUS-aligned FinOps for the Kubernetes Operators pattern: there is no software license fee, so all FinOps signal flows from the underlying compute (cluster nodes) and from any commercial operators consumed from third-party vendors. Cost is allocated through the workload (operator pods, CRD-managed resources) rather than a Kubernetes-Operators line item.'
focus_columns:
  BillingCurrency: USD
  ProviderName: Kubernetes Operators (CNCF pattern)
  PublisherName: Cloud Native Computing Foundation
  ServiceCategory: Container Orchestration / Pattern
  ServiceName: Kubernetes Operators
layout: finops
meters:
- aggregation: sum
  dimensions:
  - cluster
  - namespace
  - operator_name
  name: operator_pod_compute
  unit: vCPU-hour
- aggregation: sum
  dimensions:
  - cluster
  - namespace
  - operator_name
  name: operator_pod_memory
  unit: GiB-hour
- aggregation: max
  dimensions:
  - crd
  - cluster
  name: managed_resource_count
  unit: resource
- aggregation: sum
  dimensions:
  - operator_name
  - verb
  name: api_server_calls
  unit: request
name: Kubernetes Operators Finops
provider_name: Kubernetes Operators
provider_slug: kubernetes-operators
publisher_name: Cloud Native Computing Foundation (CNCF)
service_category: Open Source / Kubernetes Pattern
slug: kubernetes-operators-finops
source_filename: kubernetes-operators-finops.yml
source_heading: FinOps Profile
source_url: https://kubernetes.io/docs/concepts/extend-kubernetes/operator/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Kubernetes Operators\nproviderId: kubernetes-operators\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Kubernetes\n  - Operators\n  - Open Source\ndescription: 'FOCUS-aligned FinOps for the Kubernetes Operators pattern: there is no software license\n  fee, so all FinOps signal flows from the underlying compute (cluster nodes) and from any commercial\n  operators consumed from third-party vendors. Cost is allocated through the workload (operator pods,\n  CRD-managed resources) rather than a Kubernetes-Operators line item.'\nsources:\n  - https://kubernetes.io/docs/concepts/extend-kubernetes/operator/\n  - https://operatorhub.io/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\n\
  publisherName: Cloud Native Computing Foundation (CNCF)\nserviceCategory: Open Source / Kubernetes Pattern\nbillingModel:\n  pricingCategory: Open Source (no license fee)\n  billingFrequency: N/A\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\nfocusColumns:\n  ServiceName: Kubernetes Operators\n  ServiceCategory: Container Orchestration / Pattern\n  ProviderName: Kubernetes Operators (CNCF pattern)\n  PublisherName: Cloud Native Computing Foundation\n  BillingCurrency: USD\nmeters:\n  - name: operator_pod_compute\n    unit: vCPU-hour\n    aggregation: sum\n    dimensions:\n      - cluster\n      - namespace\n      - operator_name\n  - name: operator_pod_memory\n    unit: GiB-hour\n    aggregation: sum\n    dimensions:\n      - cluster\n      - namespace\n      - operator_name\n  - name: managed_resource_count\n    unit: resource\n    aggregation: max\n    dimensions:\n      - crd\n      - cluster\n  - name: api_server_calls\n    unit: request\n    aggregation: sum\n    dimensions:\n\
  \      - operator_name\n      - verb\nprinciples:\n  - name: Visibility\n    description: Use Kubecost / OpenCost to attribute compute cost to operator workloads by namespace\n      and label; surface CRD-managed resources as first-class allocation dimensions.\n  - name: Allocation\n    description: Label every operator deployment and the resources it manages with team, product, and\n      environment so allocation flows through to the underlying cloud bill.\n  - name: Optimization\n    description: Right-size operator pods (most are leader-elected and idle); deduplicate operators across\n      namespaces; prefer cluster-scoped operators when fan-out is wide; tune controller-runtime workqueue\n      and resync periods to reduce API server pressure.\n  - name: Accountability\n    description: Platform team owns the cluster-shared operators (cert-manager, ingress controllers);\n      product teams own application-scoped operators they install. Cost reports should split these owners.\nmaintainers:\n\
  \  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/kubernetes-operators/refs/heads/main/finops/kubernetes-operators-finops.yml
sources:
- https://kubernetes.io/docs/concepts/extend-kubernetes/operator/
- https://operatorhub.io/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Kubernetes
- Operators
- Open Source
---
