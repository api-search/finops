---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: rook-ceph-object-storage-openapi.yml
  format: yaml
  label: Rook Ceph Object Storage API
  slug: rook-ceph-object-storage-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/rook/refs/heads/main/openapi/rook-ceph-object-storage-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: None
  chargeCategories:
  - Adjustment
  pricingCategory: Open Source
description: Rook is Apache 2.0 open-source software hosted by the CNCF; it does not issue invoices. The relevant FinOps surface is the underlying compute, storage, and network capacity the operator consumes on the host Kubernetes cluster, plus any optional commercial-support contract with a vendor such as Clyso or Red Hat (OpenShift Data Foundation).
focus_columns:
  BillingCurrency: USD
  ProviderName: Rook (CNCF)
  PublisherName: Cloud Native Computing Foundation
  ServiceCategory: Cloud Native Storage Orchestration
  ServiceName: Rook
layout: finops
meters:
- aggregation: max
  description: Provisioned Ceph storage capacity managed by Rook (block, file, object); cost is incurred on the host cloud / on-prem hardware, not by Rook.
  dimensions:
  - storage_class
  - cluster
  name: storage_capacity
  unit: GB-month
- aggregation: sum
  description: CPU and memory consumed by Rook operator pods, OSDs, MONs, MGRs, and RGWs on the host Kubernetes cluster.
  dimensions:
  - component
  - node
  name: compute_resources
  unit: cpu-hour
- aggregation: sum
  description: Annual subscription with a third-party support vendor (Clyso, Red Hat ODF). Optional.
  dimensions:
  - vendor
  name: vendor_support_contract
  unit: month
name: Rook Finops
provider_name: Rook
provider_slug: rook
publisher_name: Cloud Native Computing Foundation
service_category: Cloud Native Storage Orchestration
slug: rook-finops
source_filename: rook-finops.yml
source_heading: FinOps Profile
source_url: https://rook.io/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Rook\nproviderId: rook\npublisherName: Cloud Native Computing Foundation\nserviceCategory: Cloud Native Storage Orchestration\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - Rook\n  - Ceph\n  - Kubernetes\n  - Open Source\n  - FinOps\n  - FOCUS\ndescription: >-\n  Rook is Apache 2.0 open-source software hosted by the CNCF; it does not issue invoices.\n  The relevant FinOps surface is the underlying compute, storage, and network capacity the\n  operator consumes on the host Kubernetes cluster, plus any optional commercial-support\n  contract with a vendor such as Clyso or Red Hat (OpenShift Data Foundation).\nsources:\n\
  \  - https://rook.io/\n  - https://github.com/rook/rook\nbillingModel:\n  pricingCategory: Open Source\n  billingFrequency: None\n  billingCurrency: USD\n  chargeCategories:\n    - Adjustment\nfocusColumns:\n  ServiceName: Rook\n  ServiceCategory: Cloud Native Storage Orchestration\n  ProviderName: Rook (CNCF)\n  PublisherName: Cloud Native Computing Foundation\n  BillingCurrency: USD\nmeters:\n  - name: storage_capacity\n    description: >-\n      Provisioned Ceph storage capacity managed by Rook (block, file, object); cost is\n      incurred on the host cloud / on-prem hardware, not by Rook.\n    unit: GB-month\n    aggregation: max\n    dimensions:\n      - storage_class\n      - cluster\n  - name: compute_resources\n    description: >-\n      CPU and memory consumed by Rook operator pods, OSDs, MONs, MGRs, and RGWs on the host\n      Kubernetes cluster.\n    unit: cpu-hour\n    aggregation: sum\n    dimensions:\n      - component\n      - node\n  - name: vendor_support_contract\n \
  \   description: >-\n      Annual subscription with a third-party support vendor (Clyso, Red Hat ODF). Optional.\n    unit: month\n    aggregation: sum\n    dimensions:\n      - vendor\nprinciples:\n  - name: Visibility\n    description: >-\n      Track Rook-managed storage usage with Ceph dashboards, Prometheus exports from the\n      Rook operator, and the host cloud/cluster cost surface; there is no Rook-issued usage\n      API.\n  - name: Allocation\n    description: >-\n      Tag Rook namespaces, storage classes, and CephBlockPools to the consuming workload so\n      that capacity and IO can be attributed back to the team that owns the data.\n  - name: Optimization\n    description: >-\n      Right-size OSD count, choose appropriate replication vs erasure-coding, set per-pool\n      quotas, and tier rarely accessed data to lower-cost storage classes; consolidate small\n      Ceph clusters to amortize MON/MGR overhead.\n  - name: Accountability\n    description: >-\n      Platform\
  \ engineering owns the Rook/Ceph cluster; consuming teams own per-namespace and\n      per-pool quotas. Treat any vendor-support contract as a normal SaaS line item under\n      platform budget.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/rook/refs/heads/main/finops/rook-finops.yml
sources:
- https://rook.io/
- https://github.com/rook/rook
specification: FinOps Framework
tags:
- Rook
- Ceph
- Kubernetes
- Open Source
- FinOps
- FOCUS
---
