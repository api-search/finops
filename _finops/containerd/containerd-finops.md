---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: containerd-metrics-openapi.yml
  format: yaml
  label: Containerd Metrics API
  slug: containerd-metrics-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/containerd/refs/heads/main/openapi/containerd-metrics-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Not Applicable
  chargeCategories:
  - Usage
  pricingCategory: Open Source / Free
description: 'FOCUS-aligned FinOps for Containerd: CNCF-graduated OSS runtime with no per-call or license cost. FinOps focuses on the underlying compute / storage / network it consumes (Kubernetes node hours, registry-pull egress) rather than a vendor invoice from containerd itself.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Not Applicable
  ProviderName: Containerd Project
  PublisherName: Cloud Native Computing Foundation (CNCF)
  ServiceCategory: Container Runtime
  ServiceName: Containerd
layout: finops
meters:
- aggregation: sum
  description: Compute hours of nodes running containerd (proxy meter — billed by the underlying cloud provider, not by containerd)
  dimensions:
  - cloud_provider
  - instance_type
  - cluster
  name: node_hours
  unit: instance-hour
- aggregation: sum
  description: Egress from container registries during image pulls
  dimensions:
  - registry
  - region
  name: image_pull_egress
  unit: GB
- aggregation: count
  description: Containers / pods executed via the containerd CRI surface (operational meter, no charge)
  dimensions:
  - namespace
  - cluster
  name: container_runtime_count
  unit: container
name: Containerd Finops
provider_name: Containerd
provider_slug: containerd
publisher_name: Cloud Native Computing Foundation (CNCF)
service_category: Container Runtime / Open Source
slug: containerd-finops
source_filename: containerd-finops.yml
source_heading: FinOps Profile
source_url: https://containerd.io
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Containerd\nproviderId: containerd\npublisherName: Cloud Native Computing Foundation (CNCF)\nserviceCategory: Container Runtime / Open Source\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - Cloud Native\n  - Container Runtime\n  - Kubernetes\n  - OSS\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps for Containerd: CNCF-graduated OSS runtime with no per-call or license\n  cost. FinOps focuses on the underlying compute / storage / network it consumes (Kubernetes node hours,\n  registry-pull egress) rather than a vendor invoice from containerd itself.'\nsources:\n  - https://containerd.io\n  - https://github.com/containerd/containerd\n\
  billingModel:\n  pricingCategory: Open Source / Free\n  billingFrequency: Not Applicable\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\nfocusColumns:\n  ServiceName: Containerd\n  ServiceCategory: Container Runtime\n  ProviderName: Containerd Project\n  PublisherName: Cloud Native Computing Foundation (CNCF)\n  InvoiceIssuerName: Not Applicable\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: node_hours\n    description: Compute hours of nodes running containerd (proxy meter — billed by the underlying cloud\n      provider, not by containerd)\n    unit: instance-hour\n    aggregation: sum\n    dimensions:\n      - cloud_provider\n      - instance_type\n      - cluster\n  - name: image_pull_egress\n    description: Egress from container registries during image pulls\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - registry\n      - region\n  - name: container_runtime_count\n    description: Containers / pods executed via the containerd CRI surface\
  \ (operational meter, no charge)\n    unit: container\n    aggregation: count\n    dimensions:\n      - namespace\n      - cluster\nprinciples:\n  - name: Visibility\n    description: Containerd does not produce invoices; surface infrastructure cost via the underlying\n      cloud provider's billing exports and via Prometheus metrics scraped from the kubelet / containerd.\n  - name: Allocation\n    description: Allocate via cluster / namespace / pod labels and cloud-provider node tags; align with\n      Kubecost or OpenCost for per-workload mapping.\n  - name: Optimization\n    description: Reduce image-pull egress with registry mirrors / pull-through caches; tune `max_concurrent_downloads`;\n      consider lazy-loading snapshotters (stargz) for large images; right-size node pools.\n  - name: Accountability\n    description: Platform / SRE teams own cluster-level spend; product teams own per-namespace footprint\n      and image hygiene that drives storage and pull egress.\nmaintainers:\n\
  \  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/containerd/refs/heads/main/finops/containerd-finops.yml
sources:
- https://containerd.io
- https://github.com/containerd/containerd
specification: FinOps Framework
tags:
- Cloud Native
- Container Runtime
- Kubernetes
- OSS
- FinOps
- FOCUS
---
