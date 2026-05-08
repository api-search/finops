---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: etcd-http-gateway-openapi.yml
  format: yaml
  label: etcd HTTP Gateway API
  slug: etcd-http-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/etcd/refs/heads/main/openapi/etcd-http-gateway-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: N/A
  chargeCategories:
  - Usage
  pricingCategory: Open Source (no direct cost)
description: 'FinOps view of etcd: no vendor invoice. Direct cost is the underlying compute, storage (low-latency SSD), and networking required to run a quorum-typically-3 cluster. When etcd is consumed via managed Kubernetes (EKS, GKE, AKS), its cost is bundled into the control-plane fee on the cloud bill.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: N/A (open source)
  ProviderName: etcd
  PublisherName: Cloud Native Computing Foundation
  ServiceCategory: Distributed Systems / Key-Value Store
  ServiceName: etcd
layout: finops
meters:
- aggregation: sum
  dimensions:
  - cluster
  - region
  - instance_type
  name: compute_hours
  unit: instance-hour
- aggregation: max
  dimensions:
  - cluster
  - region
  name: ssd_storage
  unit: GB-month
- aggregation: max
  dimensions:
  - cluster
  name: backup_storage
  unit: GB-month
- aggregation: sum
  dimensions:
  - cluster
  - region
  name: network_egress
  unit: GB
name: Etcd Finops
provider_name: Etcd
provider_slug: etcd
publisher_name: Cloud Native Computing Foundation
service_category: Distributed Systems / Key-Value Store
slug: etcd-finops
source_filename: etcd-finops.yml
source_heading: FinOps Profile
source_url: https://etcd.io/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Etcd\nproviderId: etcd\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Open Source\n  - Distributed Systems\n  - Kubernetes\ndescription: 'FinOps view of etcd: no vendor invoice. Direct cost is the underlying compute, storage\n  (low-latency SSD), and networking required to run a quorum-typically-3 cluster. When etcd is consumed\n  via managed Kubernetes (EKS, GKE, AKS), its cost is bundled into the control-plane fee on the cloud\n  bill.'\nsources:\n  - https://etcd.io/\n  - https://www.cncf.io/projects/etcd/\nnotes: No vendor invoice from the etcd project. FinOps surface is infrastructure cost (self-hosted) or\n  a portion of managed-Kubernetes control-plane spend.\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion:\
  \ '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Cloud Native Computing Foundation\nserviceCategory: Distributed Systems / Key-Value Store\nbillingModel:\n  pricingCategory: Open Source (no direct cost)\n  billingFrequency: N/A\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\nfocusColumns:\n  ServiceName: etcd\n  ServiceCategory: Distributed Systems / Key-Value Store\n  ProviderName: etcd\n  PublisherName: Cloud Native Computing Foundation\n  InvoiceIssuerName: N/A (open source)\n  BillingCurrency: USD\nmeters:\n  - name: compute_hours\n    unit: instance-hour\n    aggregation: sum\n    dimensions:\n      - cluster\n      - region\n      - instance_type\n  - name: ssd_storage\n    unit: GB-month\n    aggregation: max\n    dimensions:\n      - cluster\n      - region\n  - name: backup_storage\n    unit: GB-month\n    aggregation: max\n    dimensions:\n      - cluster\n  - name: network_egress\n    unit: GB\n    aggregation: sum\n    dimensions:\n\
  \      - cluster\n      - region\nprinciples:\n  - name: Visibility\n    description: Scrape etcd's Prometheus metrics (mvcc_db_total_size_in_bytes, disk fsync latency, leader\n      changes) and join with cloud cost data per cluster.\n  - name: Allocation\n    description: Tag etcd nodes/disks per cluster and per environment so platform-team cost is attributable\n      to consuming Kubernetes/control-plane workloads.\n  - name: Optimization\n    description: Co-locate etcd peers on low-latency NVMe SSD; right-size CPU/memory; use defrag and\n      compaction to keep DB small; consolidate small clusters where multi-tenant model permits.\n  - name: Accountability\n    description: Platform team owns etcd cluster cost; charge back to consuming Kubernetes control-plane\n      tenants on a per-cluster or per-namespace basis.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/etcd/refs/heads/main/finops/etcd-finops.yml
sources:
- https://etcd.io/
- https://www.cncf.io/projects/etcd/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Open Source
- Distributed Systems
- Kubernetes
---
