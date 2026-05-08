---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: cri-o-status-openapi.yml
  format: yaml
  label: CRI-O Status API
  slug: cri-o-status-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/cri-o/refs/heads/main/openapi/cri-o-status-openapi.yml
- filename: cri-o-metrics-openapi.yml
  format: yaml
  label: CRI-O Metrics API
  slug: cri-o-metrics-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/cri-o/refs/heads/main/openapi/cri-o-metrics-openapi.yml
billing_model:
  billingCurrency: N/A
  billingFrequency: N/A
  chargeCategories: []
  chargeFrequency: N/A
  pricingCategory: Open Source (No Charge)
description: FinOps shape for CRI-O - an Apache 2.0 / CNCF Graduated open-source container runtime. There is no upstream invoice. Operator cost is borne by the underlying compute (node-hours), image storage, and image-pull egress on the hosting cluster.
focus_columns:
  BillingCurrency: N/A
  ChargeCategory: N/A
  PricingCategory: Free
  ProviderName: CRI-O Project
  PublisherName: CRI-O Authors / CNCF
  ServiceCategory: Open Source Container Runtime
  ServiceName: CRI-O
layout: finops
meters:
- aggregation: sum
  description: Node-hours of CRI-O runtime time (proxied via underlying node billing on the cloud provider)
  dimensions:
  - cluster
  - node_pool
  name: container_runtime_hours
  unit: node-hour
- aggregation: sum
  description: Container image pull operations (drives upstream registry egress and any registry bandwidth charges)
  dimensions:
  - registry
  - image
  - cluster
  name: image_pulls
  unit: pull
- aggregation: avg
  description: Container image / layer storage on the node disk (drives node-disk capacity sizing)
  dimensions:
  - node_pool
  - cluster
  name: image_storage
  unit: GB
- aggregation: sum
  description: Container start events (operational metric from CRI-O Prometheus metrics)
  dimensions:
  - cluster
  - namespace
  name: container_starts
  unit: event
name: Cri O Finops
provider_name: CRI-O
provider_slug: cri-o
publisher_name: CRI-O Authors / CNCF
service_category: Open Source Container Runtime
slug: cri-o-finops
source_filename: cri-o-finops.yml
source_heading: FinOps Profile
source_url: https://cri-o.io/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: CRI-O\nproviderId: cri-o\npublisherName: CRI-O Authors / CNCF\nserviceCategory: Open Source Container Runtime\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - CNCF\n  - Container Runtime\n  - Containers\n  - CRI\n  - Kubernetes\n  - OCI\n  - Open Source\n  - FinOps\n  - FOCUS\ndescription: FinOps shape for CRI-O - an Apache 2.0 / CNCF Graduated open-source container runtime.\n  There is no upstream invoice. Operator cost is borne by the underlying compute (node-hours), image\n  storage, and image-pull egress on the hosting cluster.\nsources:\n  - https://cri-o.io/\n  - https://github.com/cri-o/cri-o\n  - https://www.cncf.io/projects/cri-o/\n\
  billingModel:\n  pricingCategory: Open Source (No Charge)\n  billingFrequency: N/A\n  billingCurrency: N/A\n  chargeCategories: []\n  chargeFrequency: N/A\nfocusColumns:\n  ServiceName: CRI-O\n  ServiceCategory: Open Source Container Runtime\n  ProviderName: CRI-O Project\n  PublisherName: CRI-O Authors / CNCF\n  PricingCategory: Free\n  BillingCurrency: N/A\n  ChargeCategory: N/A\nmeters:\n  - name: container_runtime_hours\n    description: Node-hours of CRI-O runtime time (proxied via underlying node billing on the cloud\n      provider)\n    unit: node-hour\n    aggregation: sum\n    dimensions:\n      - cluster\n      - node_pool\n  - name: image_pulls\n    description: Container image pull operations (drives upstream registry egress and any registry\n      bandwidth charges)\n    unit: pull\n    aggregation: sum\n    dimensions:\n      - registry\n      - image\n      - cluster\n  - name: image_storage\n    description: Container image / layer storage on the node disk (drives node-disk\
  \ capacity sizing)\n    unit: GB\n    aggregation: avg\n    dimensions:\n      - node_pool\n      - cluster\n  - name: container_starts\n    description: Container start events (operational metric from CRI-O Prometheus metrics)\n    unit: event\n    aggregation: sum\n    dimensions:\n      - cluster\n      - namespace\nprinciples:\n  - name: Visibility\n    description: CRI-O itself is free; observe cost via the Prometheus /metrics endpoint (image pulls,\n      operations, errors) joined to FOCUS-aligned node-hour billing.\n  - name: Allocation\n    description: Allocate node-hour cost to namespaces / workloads via Kubernetes labels; image-pull\n      egress can be attributed to the namespace whose pod triggered the pull.\n  - name: Optimization\n    description: Use a registry mirror or pull-through cache to cut registry egress; configure\n      drop_infra_ctr and small-pause images to reduce per-pod overhead; right-size node-pool to actual\n      pod density; prune unused images on a\
  \ schedule via crictl rmi to control disk consumption.\n  - name: Accountability\n    description: Assign a platform-team owner for the container-runtime layer; alert on image-pull\n      error rate and inode pressure; review CRI-O / Kubernetes upgrade cadence to keep the runtime\n      patched without extra paid support.\nnotes: CRI-O is open-source with no upstream commercial billing. FinOps for CRI-O is FinOps for the\n  underlying node compute, image storage, and image-pull egress. Reconciled is false because there\n  is no provider rate card or invoice to reconcile against.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/cri-o/refs/heads/main/finops/cri-o-finops.yml
sources:
- https://cri-o.io/
- https://github.com/cri-o/cri-o
- https://www.cncf.io/projects/cri-o/
specification: FinOps Framework
tags:
- CNCF
- Container Runtime
- Containers
- CRI
- Kubernetes
- OCI
- Open Source
- FinOps
- FOCUS
---
