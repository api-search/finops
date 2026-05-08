---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: openapi.yaml
  format: yaml
  label: Cilium API
  slug: cilium-api
  spec_type: OpenAPI
  url: https://github.com/cilium/cilium/blob/main/api/v1/openapi.yaml
- filename: cilium-hubble-asyncapi.yml
  format: yaml
  label: Hubble API
  slug: hubble-api
  spec_type: AsyncAPI
  url: https://raw.githubusercontent.com/api-evangelist/cilium/refs/heads/main/asyncapi/cilium-hubble-asyncapi.yml
- filename: openapi.yaml
  format: yaml
  label: Cilium Operator API
  slug: cilium-operator-api
  spec_type: OpenAPI
  url: https://github.com/cilium/cilium/blob/main/api/v1/operator/openapi.yaml
billing_model:
  billingCurrency: USD
  billingFrequency: N/A (upstream) / Annual (Isovalent Enterprise)
  chargeCategories:
  - Adjustment
  - Purchase
  pricingCategory: Open Source (Optional Commercial Subscription)
description: 'FOCUS-aligned FinOps for Cilium: the upstream project itself is free (Apache 2.0). The cost surface is internal — compute / memory consumed by cilium-agent, Hubble, Hubble Relay, and Tetragon DaemonSets in customer clusters, plus the optional Isovalent Enterprise subscription (Cisco) for organizations that want a supported distribution. There is no metered billing surface exposed by Cilium itself.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Adjustment
  InvoiceIssuerName: N/A (upstream); Cisco / Isovalent for Enterprise
  PricingCategory: Open Source
  ProviderName: Cilium / CNCF
  PublisherName: Cilium Authors / CNCF
  ServiceCategory: Cloud Native Networking & Security
  ServiceName: Cilium
layout: finops
meters:
- aggregation: sum
  description: vCPU and RAM consumed by cilium-agent DaemonSets across cluster nodes
  dimensions:
  - cluster
  - node_pool
  name: agent_overhead
  unit: vCPU-hour
- aggregation: sum
  description: Resources consumed by Hubble and Hubble Relay (observability stack)
  dimensions:
  - cluster
  name: hubble_overhead
  unit: vCPU-hour
- aggregation: sum
  description: Resources consumed by Tetragon DaemonSets (runtime security)
  dimensions:
  - cluster
  name: tetragon_overhead
  unit: vCPU-hour
- aggregation: sum
  description: Optional Isovalent Enterprise / Cisco subscription line (when purchased)
  dimensions:
  - tier
  name: enterprise_subscription
  unit: month
name: Cilium Finops
provider_name: Cilium
provider_slug: cilium
publisher_name: Cilium Authors / CNCF
service_category: Cloud Native Networking & Security
slug: cilium-finops
source_filename: cilium-finops.yml
source_heading: FinOps Profile
source_url: https://cilium.io/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Cilium\nproviderId: cilium\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Cloud Native\n  - eBPF\n  - Kubernetes\n  - Networking\n  - Open Source\n  - Security\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps for Cilium: the upstream project itself is free (Apache 2.0). The\n  cost surface is internal — compute / memory consumed by cilium-agent, Hubble, Hubble Relay, and\n  Tetragon DaemonSets in customer clusters, plus the optional Isovalent Enterprise subscription\n  (Cisco) for organizations that want a supported distribution. There is no metered billing surface\n  exposed by Cilium itself.'\nnotes: Cilium is free and open source. Cost surfaces below describe internal infrastructure cost\n  (cluster overhead) and optional commercial subscription cost.\nsources:\n  - https://cilium.io/\n  - https://docs.cilium.io/\n  -\
  \ https://isovalent.com/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Cilium Authors / CNCF\nserviceCategory: Cloud Native Networking & Security\nbillingModel:\n  pricingCategory: Open Source (Optional Commercial Subscription)\n  billingFrequency: N/A (upstream) / Annual (Isovalent Enterprise)\n  billingCurrency: USD\n  chargeCategories:\n    - Adjustment\n    - Purchase\nfocusColumns:\n  ServiceName: Cilium\n  ServiceCategory: Cloud Native Networking & Security\n  ProviderName: Cilium / CNCF\n  PublisherName: Cilium Authors / CNCF\n  InvoiceIssuerName: N/A (upstream); Cisco / Isovalent for Enterprise\n  BillingCurrency: USD\n  ChargeCategory: Adjustment\n  PricingCategory: Open Source\nmeters:\n  - name: agent_overhead\n    description: vCPU and RAM consumed by cilium-agent DaemonSets across cluster\
  \ nodes\n    unit: vCPU-hour\n    aggregation: sum\n    dimensions:\n      - cluster\n      - node_pool\n  - name: hubble_overhead\n    description: Resources consumed by Hubble and Hubble Relay (observability stack)\n    unit: vCPU-hour\n    aggregation: sum\n    dimensions:\n      - cluster\n  - name: tetragon_overhead\n    description: Resources consumed by Tetragon DaemonSets (runtime security)\n    unit: vCPU-hour\n    aggregation: sum\n    dimensions:\n      - cluster\n  - name: enterprise_subscription\n    description: Optional Isovalent Enterprise / Cisco subscription line (when purchased)\n    unit: month\n    aggregation: sum\n    dimensions:\n      - tier\nprinciples:\n  - name: Visibility\n    description: Track Cilium's cluster overhead through Kubernetes resource usage (cAdvisor,\n      kube-state-metrics, Prometheus) and tag DaemonSet cost back to platform engineering.\n  - name: Allocation\n    description: Allocate Cilium overhead to the platform / networking cost center;\
  \ allocate\n      Hubble / Tetragon overhead to the security observability team if separately funded.\n  - name: Optimization\n    description: Tune Hubble flow retention, Tetragon policy footprint, and cilium-agent memory\n      limits to reduce per-node overhead; only enable Cluster Mesh and advanced features where they\n      pay back in security or operational simplification.\n  - name: Accountability\n    description: Platform engineering owns Cilium runtime cost and version cadence; security owns\n      Tetragon policy; finance reviews any Isovalent Enterprise subscription against the value\n      delivered (support, hardening, certified releases).\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/cilium/refs/heads/main/finops/cilium-finops.yml
sources:
- https://cilium.io/
- https://docs.cilium.io/
- https://isovalent.com/
specification: FinOps Framework
tags:
- Cloud Native
- eBPF
- Kubernetes
- Networking
- Open Source
- Security
- FinOps
- FOCUS
---
