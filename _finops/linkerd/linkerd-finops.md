---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: linkerd-proxy-admin-openapi.yml
  format: yaml
  label: Linkerd Proxy Admin API
  slug: proxy-admin-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/linkerd/refs/heads/main/openapi/linkerd-proxy-admin-openapi.yml
- filename: linkerd-viz-metrics-openapi.yml
  format: yaml
  label: Linkerd Viz Metrics API
  slug: viz-metrics-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/linkerd/refs/heads/main/openapi/linkerd-viz-metrics-openapi.yml
- filename: linkerd-tap-openapi.yml
  format: yaml
  label: Linkerd Tap API
  slug: tap-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/linkerd/refs/heads/main/openapi/linkerd-tap-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  - Adjustment
  - Credit
  pricingCategory: Open Source + Subscription Support
description: 'FOCUS-aligned FinOps for Linkerd: open-source service mesh with no per-call cost. Direct spend lives only with Buoyant Enterprise for Linkerd subscriptions (Basic / Premium / Strategic) when used. Indirect cost is the cluster compute / memory / network consumed by the Linkerd proxy sidecars and control plane — surfaced via your Kubernetes cost tooling (Kubecost, OpenCost, cloud provider cost APIs), not via Linkerd or Buoyant.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Buoyant, Inc.
  ProviderName: Linkerd / Buoyant
  PublisherName: Buoyant, Inc.
  ServiceCategory: Service Mesh
  ServiceName: Linkerd
layout: finops
meters:
- aggregation: count
  dimensions:
  - tier
  - cluster
  name: bel_subscription
  unit: contract
- aggregation: sum
  dimensions:
  - cluster
  - namespace
  - workload
  name: proxy_cpu
  unit: vCPU-hour
- aggregation: sum
  dimensions:
  - cluster
  - namespace
  - workload
  name: proxy_memory
  unit: GiB-hour
- aggregation: sum
  dimensions:
  - cluster
  - component
  name: control_plane_cpu
  unit: vCPU-hour
- aggregation: sum
  dimensions:
  - cluster
  - direction
  name: mesh_egress
  unit: GB
name: Linkerd Finops
provider_name: Linkerd
provider_slug: linkerd
publisher_name: Buoyant, Inc. (commercial); CNCF (open source project)
service_category: Service Mesh / Kubernetes Infrastructure
slug: linkerd-finops
source_filename: linkerd-finops.yml
source_heading: FinOps Profile
source_url: https://linkerd.io
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Linkerd\nproviderId: linkerd\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Service Mesh\n  - Kubernetes\n  - Open Source\ndescription: 'FOCUS-aligned FinOps for Linkerd: open-source service mesh with no per-call cost. Direct\n  spend lives only with Buoyant Enterprise for Linkerd subscriptions (Basic / Premium / Strategic) when\n  used. Indirect cost is the cluster compute / memory / network consumed by the Linkerd proxy sidecars\n  and control plane — surfaced via your Kubernetes cost tooling (Kubecost, OpenCost, cloud provider\n  cost APIs), not via Linkerd or Buoyant.'\nsources:\n  - https://linkerd.io\n  - https://buoyant.io/pricing\n  - https://buoyant.io/enterprise\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion:\
  \ '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Buoyant, Inc. (commercial); CNCF (open source project)\nserviceCategory: Service Mesh / Kubernetes Infrastructure\nbillingModel:\n  pricingCategory: Open Source + Subscription Support\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Adjustment\n    - Credit\nfocusColumns:\n  ServiceName: Linkerd\n  ServiceCategory: Service Mesh\n  ProviderName: Linkerd / Buoyant\n  PublisherName: Buoyant, Inc.\n  InvoiceIssuerName: Buoyant, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: bel_subscription\n    unit: contract\n    aggregation: count\n    dimensions:\n      - tier\n      - cluster\n  - name: proxy_cpu\n    unit: vCPU-hour\n    aggregation: sum\n    dimensions:\n      - cluster\n      - namespace\n      - workload\n  - name: proxy_memory\n    unit: GiB-hour\n    aggregation: sum\n    dimensions:\n      - cluster\n      - namespace\n      - workload\n  -\
  \ name: control_plane_cpu\n    unit: vCPU-hour\n    aggregation: sum\n    dimensions:\n      - cluster\n      - component\n  - name: mesh_egress\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - cluster\n      - direction\nprinciples:\n  - name: Visibility\n    description: Use Linkerd Viz / Prometheus metrics for proxy resource usage; Kubecost or OpenCost\n      to attribute mesh sidecar cost to namespaces, workloads, and teams; Buoyant invoice for BEL subscription\n      cost.\n  - name: Allocation\n    description: Tag namespaces and workloads with team / product labels so sidecar overhead (CPU / memory)\n      can be charged back. Allocate BEL subscription cost across the clusters it covers.\n  - name: Optimization\n    description: Right-size proxy resource requests; use Linkerd's smaller proxy image vs sidecar-heavier\n      meshes; consolidate clusters where BEL Strategic SLAs are not needed; reclaim BEL coverage from\n      decommissioned clusters at renewal.\n  - name:\
  \ Accountability\n    description: Assign a platform-team owner for the BEL contract; review proxy overhead and BEL tier\n      fit annually at renewal alongside SLO and incident history.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/linkerd/refs/heads/main/finops/linkerd-finops.yml
sources:
- https://linkerd.io
- https://buoyant.io/pricing
- https://buoyant.io/enterprise
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Service Mesh
- Kubernetes
- Open Source
---
