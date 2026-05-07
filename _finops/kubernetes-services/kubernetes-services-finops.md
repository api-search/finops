---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: kubernetes-services-openapi.yml
  format: yaml
  label: Kubernetes Services
  slug: kubernetes-services
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/kubernetes-services/refs/heads/main/openapi/kubernetes-services-openapi.yml
- filename: kubernetes-ingress-openapi.yml
  format: yaml
  label: Kubernetes Ingress
  slug: kubernetes-ingress
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/kubernetes-services/refs/heads/main/openapi/kubernetes-ingress-openapi.yml
- filename: kubernetes-gateway-api-openapi.yml
  format: yaml
  label: Kubernetes Gateway API
  slug: kubernetes-gateway-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/kubernetes-services/refs/heads/main/openapi/kubernetes-gateway-api-openapi.yml
- filename: kubernetes-endpoint-slices-openapi.yml
  format: yaml
  label: Kubernetes EndpointSlices
  slug: kubernetes-endpoint-slices
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/kubernetes-services/refs/heads/main/openapi/kubernetes-endpoint-slices-openapi.yml
- filename: kubernetes-network-policies-openapi.yml
  format: yaml
  label: Kubernetes Network Policies
  slug: kubernetes-network-policies
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/kubernetes-services/refs/heads/main/openapi/kubernetes-network-policies-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: N/A
  chargeCategories:
  - Usage
  pricingCategory: Open Source (no license fee)
description: 'FOCUS-aligned FinOps for the Kubernetes Services API: the abstraction itself is free open source, but real spend appears on the cloud-provider invoice when Services of type LoadBalancer provision cloud LBs, when NodePort/ClusterIP traffic crosses zones, or when external IPs and egress are billed. FinOps signal therefore comes from the underlying cloud bill, allocated back to Services via labels and CCM annotations.'
focus_columns:
  BillingCurrency: USD
  ProviderName: Kubernetes (CNCF)
  PublisherName: Cloud Native Computing Foundation
  ServiceCategory: Container Orchestration / Networking
  ServiceName: Kubernetes Services
layout: finops
meters:
- aggregation: sum
  dimensions:
  - cluster
  - cloud_provider
  - lb_type
  name: load_balancer_hours
  unit: instance-hour
- aggregation: max
  dimensions:
  - service
  - region
  name: public_ip_count
  unit: ip
- aggregation: sum
  dimensions:
  - service
  - source_zone
  - destination_zone
  name: cross_zone_egress
  unit: GB
- aggregation: sum
  dimensions:
  - service
  - lb_type
  name: data_processed
  unit: GB
- aggregation: max
  dimensions:
  - service
  name: endpoint_count
  unit: endpoint
name: Kubernetes Services Finops
provider_name: Kubernetes Services
provider_slug: kubernetes-services
publisher_name: Cloud Native Computing Foundation (CNCF)
service_category: Open Source / Container Networking
slug: kubernetes-services-finops
source_filename: kubernetes-services-finops.yml
source_heading: FinOps Profile
source_url: https://kubernetes.io/docs/concepts/services-networking/service/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Kubernetes Services\nproviderId: kubernetes-services\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Kubernetes\n  - Networking\n  - Open Source\ndescription: 'FOCUS-aligned FinOps for the Kubernetes Services API: the abstraction itself is free open\n  source, but real spend appears on the cloud-provider invoice when Services of type LoadBalancer provision\n  cloud LBs, when NodePort/ClusterIP traffic crosses zones, or when external IPs and egress are billed.\n  FinOps signal therefore comes from the underlying cloud bill, allocated back to Services via labels\n  and CCM annotations.'\nsources:\n  - https://kubernetes.io/docs/concepts/services-networking/service/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n\
  \  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Cloud Native Computing Foundation (CNCF)\nserviceCategory: Open Source / Container Networking\nbillingModel:\n  pricingCategory: Open Source (no license fee)\n  billingFrequency: N/A\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\nfocusColumns:\n  ServiceName: Kubernetes Services\n  ServiceCategory: Container Orchestration / Networking\n  ProviderName: Kubernetes (CNCF)\n  PublisherName: Cloud Native Computing Foundation\n  BillingCurrency: USD\nmeters:\n  - name: load_balancer_hours\n    unit: instance-hour\n    aggregation: sum\n    dimensions:\n      - cluster\n      - cloud_provider\n      - lb_type\n  - name: public_ip_count\n    unit: ip\n    aggregation: max\n    dimensions:\n      - service\n      - region\n  - name: cross_zone_egress\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - service\n      - source_zone\n      - destination_zone\n  - name: data_processed\n    unit:\
  \ GB\n    aggregation: sum\n    dimensions:\n      - service\n      - lb_type\n  - name: endpoint_count\n    unit: endpoint\n    aggregation: max\n    dimensions:\n      - service\nprinciples:\n  - name: Visibility\n    description: Use OpenCost / Kubecost network attribution and cloud-provider LB tags to surface per-Service\n      cloud spend; correlate Service annotations with FOCUS BilledCost from the cloud invoice.\n  - name: Allocation\n    description: Tag Services with team/product/environment labels; ensure cloud-provider Cloud Controller\n      Manager (CCM) propagates those labels to LB resources so the bill carries the same allocation dimensions.\n  - name: Optimization\n    description: Consolidate small per-app LBs behind shared Ingress / Gateway API; use ClusterIP + Ingress\n      instead of one LoadBalancer Service per app; enable topology-aware routing to keep traffic in-zone\n      and reduce egress; consider internal LBs where external exposure is unnecessary.\n  - name:\
  \ Accountability\n    description: Platform team owns the shared Ingress / Gateway and the CCM configuration; product teams\n      own the Services they create. Review LB sprawl monthly; deprecate Services without active endpoints.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/kubernetes-services/refs/heads/main/finops/kubernetes-services-finops.yml
sources:
- https://kubernetes.io/docs/concepts/services-networking/service/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Kubernetes
- Networking
- Open Source
---
