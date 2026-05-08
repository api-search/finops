---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: kuma-api-openapi.yml
  format: yaml
  label: Kuma API
  slug: kuma-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/kuma/refs/heads/main/openapi/kuma-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Usage
  - Purchase
  - Adjustment
  pricingCategory: Open Source + Enterprise Subscription
description: 'FOCUS-aligned FinOps for Kuma: open-source service mesh with no license fee for the OSS build; Kong Mesh (the commercial distribution by Kong, Inc.) is a contact-sales subscription. FinOps signal at the OSS level comes entirely from the underlying compute and network spend (control-plane pods, sidecar proxies, mesh-internal traffic).'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Kong, Inc.
  ProviderName: Kuma (CNCF) / Kong Mesh (Kong, Inc.)
  PublisherName: Kong, Inc.
  ServiceCategory: Service Mesh
  ServiceName: Kuma
layout: finops
meters:
- aggregation: sum
  dimensions:
  - zone
  - cluster
  name: control_plane_compute
  unit: vCPU-hour
- aggregation: max
  dimensions:
  - mesh
  - zone
  - service
  name: dataplane_proxies
  unit: proxy
- aggregation: sum
  dimensions:
  - source_service
  - destination_service
  - zone
  name: mesh_traffic
  unit: GB
- aggregation: max
  name: kong_mesh_subscription_seats
  unit: seat
- aggregation: max
  name: managed_meshes
  unit: mesh
name: Kuma Finops
provider_name: Kuma
provider_slug: kuma
publisher_name: Kong, Inc.
service_category: Service Mesh / Networking
slug: kuma-finops
source_filename: kuma-finops.yml
source_heading: FinOps Profile
source_url: https://kuma.io/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Kuma\nproviderId: kuma\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Service Mesh\n  - Open Source\ndescription: 'FOCUS-aligned FinOps for Kuma: open-source service mesh with no license fee for the OSS\n  build; Kong Mesh (the commercial distribution by Kong, Inc.) is a contact-sales subscription. FinOps\n  signal at the OSS level comes entirely from the underlying compute and network spend (control-plane\n  pods, sidecar proxies, mesh-internal traffic).'\nsources:\n  - https://kuma.io/\n  - https://konghq.com/products/kong-mesh\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Kong, Inc.\nserviceCategory: Service Mesh / Networking\n\
  billingModel:\n  pricingCategory: Open Source + Enterprise Subscription\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Adjustment\nfocusColumns:\n  ServiceName: Kuma\n  ServiceCategory: Service Mesh\n  ProviderName: Kuma (CNCF) / Kong Mesh (Kong, Inc.)\n  PublisherName: Kong, Inc.\n  InvoiceIssuerName: Kong, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: control_plane_compute\n    unit: vCPU-hour\n    aggregation: sum\n    dimensions:\n      - zone\n      - cluster\n  - name: dataplane_proxies\n    unit: proxy\n    aggregation: max\n    dimensions:\n      - mesh\n      - zone\n      - service\n  - name: mesh_traffic\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - source_service\n      - destination_service\n      - zone\n  - name: kong_mesh_subscription_seats\n    unit: seat\n    aggregation: max\n  - name: managed_meshes\n    unit: mesh\n    aggregation: max\nprinciples:\n  - name: Visibility\n    description:\
  \ Use Kuma's built-in Prometheus metrics and traffic permissions API plus the data-plane\n      Envoy stats to attribute traffic and proxy compute to source/destination services.\n  - name: Allocation\n    description: Map each Kuma 'service' tag and 'mesh' to a team/product label; carry those labels onto\n      the underlying pod and node bill via Kubernetes labels.\n  - name: Optimization\n    description: Right-size sidecar resource requests; co-locate heavy mesh-internal traffic in the same\n      zone to avoid cross-AZ egress; consolidate meshes only where isolation is required (each mesh has\n      its own control-plane footprint); turn off optional features (tracing exporters, access logs to\n      object storage) when not in active use.\n  - name: Accountability\n    description: Platform team owns the Kuma control plane and Kong Mesh subscription (if any); product\n      teams own the sidecar overhead of the services they ship. Review proxy count and mesh traffic monthly;\n  \
  \    escalate Kong Mesh seat / cluster overages before renewal.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/kuma/refs/heads/main/finops/kuma-finops.yml
sources:
- https://kuma.io/
- https://konghq.com/products/kong-mesh
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Service Mesh
- Open Source
---
