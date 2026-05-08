---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: istio-networking-api-openapi.yml
  format: yaml
  label: Istio Networking API
  slug: networking-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/istio/refs/heads/main/openapi/istio-networking-api-openapi.yml
- filename: istio-security-api-openapi.yml
  format: yaml
  label: Istio Security API
  slug: security-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/istio/refs/heads/main/openapi/istio-security-api-openapi.yml
- filename: istio-telemetry-api-openapi.yml
  format: yaml
  label: Istio Telemetry API
  slug: telemetry-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/istio/refs/heads/main/openapi/istio-telemetry-api-openapi.yml
- filename: istio-extensions-api-openapi.yml
  format: yaml
  label: Istio Extensions API
  slug: extensions-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/istio/refs/heads/main/openapi/istio-extensions-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: N/A
  chargeCategories:
  - Purchase
  - Usage
  pricingCategory: Open Source (no fee) + Optional Subscription
description: 'FOCUS-aligned FinOps for Istio: open-source software with no license fee. Cost is dominated by the Kubernetes / cloud infrastructure required to run the control plane, sidecars (Envoy proxies), and supporting observability backends, plus optional commercial-distribution subscriptions.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: N/A (open source)
  ProviderName: Istio (CNCF)
  PublisherName: Cloud Native Computing Foundation
  ServiceCategory: Service Mesh
  ServiceName: Istio
layout: finops
meters:
- aggregation: sum
  dimensions:
  - cloud_provider
  - region
  - cluster
  name: control_plane_compute
  unit: instance-hour
- aggregation: sum
  dimensions:
  - workload
  - namespace
  - cluster
  name: sidecar_proxy_compute
  unit: instance-hour
- aggregation: sum
  dimensions:
  - source
  - destination
  - protocol
  name: mesh_traffic
  unit: GB
- aggregation: sum
  dimensions:
  - backend
  name: telemetry_storage
  unit: GB-month
- aggregation: sum
  dimensions:
  - vendor
  name: commercial_subscription
  unit: month
name: Istio Finops
provider_name: Istio
provider_slug: istio
publisher_name: Cloud Native Computing Foundation
service_category: Service Mesh / Networking
slug: istio-finops
source_filename: istio-finops.yml
source_heading: FinOps Profile
source_url: https://istio.io/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Istio\nproviderId: istio\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Service Mesh\n  - Open Source\n  - Kubernetes\ndescription: 'FOCUS-aligned FinOps for Istio: open-source software with no license fee. Cost is dominated\n  by the Kubernetes / cloud infrastructure required to run the control plane, sidecars (Envoy proxies),\n  and supporting observability backends, plus optional commercial-distribution subscriptions.'\nsources:\n  - https://istio.io/\n  - https://istio.io/latest/about/faq/\n  - https://www.cncf.io/projects/istio/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Cloud Native Computing Foundation\nserviceCategory:\
  \ Service Mesh / Networking\nbillingModel:\n  pricingCategory: Open Source (no fee) + Optional Subscription\n  billingFrequency: N/A\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\nfocusColumns:\n  ServiceName: Istio\n  ServiceCategory: Service Mesh\n  ProviderName: Istio (CNCF)\n  PublisherName: Cloud Native Computing Foundation\n  InvoiceIssuerName: N/A (open source)\n  BillingCurrency: USD\nmeters:\n  - name: control_plane_compute\n    unit: instance-hour\n    aggregation: sum\n    dimensions:\n      - cloud_provider\n      - region\n      - cluster\n  - name: sidecar_proxy_compute\n    unit: instance-hour\n    aggregation: sum\n    dimensions:\n      - workload\n      - namespace\n      - cluster\n  - name: mesh_traffic\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - source\n      - destination\n      - protocol\n  - name: telemetry_storage\n    unit: GB-month\n    aggregation: sum\n    dimensions:\n      - backend\n  - name: commercial_subscription\n\
  \    unit: month\n    aggregation: sum\n    dimensions:\n      - vendor\nprinciples:\n  - name: Visibility\n    description: Use Prometheus / Kiali / Grafana dashboards already shipped with Istio to attribute\n      sidecar CPU and memory back to workloads; export Envoy access-log volume to align with FOCUS\n      meters.\n  - name: Allocation\n    description: Tag namespaces and workloads with team / product labels so sidecar CPU, memory, and\n      egress can be charged back via Kubecost or OpenCost.\n  - name: Optimization\n    description: Right-size sidecar resources, enable Ambient mode (sidecar-less) where appropriate,\n      tune telemetry sampling and access-log filters, and consolidate to a single mesh per organization\n      where governance allows.\n  - name: Accountability\n    description: Platform team owns control-plane cost; application teams own sidecar overhead in their\n      namespaces; quarterly mesh-cost review.\nmaintainers:\n  - FN: API Evangelist\n    email: info@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/istio/refs/heads/main/finops/istio-finops.yml
sources:
- https://istio.io/
- https://istio.io/latest/about/faq/
- https://www.cncf.io/projects/istio/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Service Mesh
- Open Source
- Kubernetes
---
