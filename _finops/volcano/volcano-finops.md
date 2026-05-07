---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: volcano-job-openapi.yml
  format: yaml
  label: Volcano Batch Scheduling API
  slug: volcano-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/volcano/refs/heads/main/openapi/volcano-job-openapi.yml
- filename: volcano-queue-openapi.yml
  format: yaml
  label: Volcano Queue API
  slug: volcano-queue-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/volcano/refs/heads/main/openapi/volcano-queue-openapi.yml
- filename: volcano-podgroup-openapi.yml
  format: yaml
  label: Volcano PodGroup API
  slug: volcano-podgroup-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/volcano/refs/heads/main/openapi/volcano-podgroup-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Continuous Settlement
  chargeCategories:
  - Usage
  pricingCategory: Open Source
description: FinOps view of Volcano - the project itself has no licensing or invoice surface (Apache 2.0, CNCF incubating). Costs of running Volcano- scheduled workloads accrue at the underlying compute, GPU, network, and storage layers of the host Kubernetes cluster (cloud or on-prem). The FinOps levers are queue capacity, gang-schedule efficiency, and bin-packing of batch workloads onto the underlying infrastructure.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: (none - open source)
  ProviderName: Volcano
  PublisherName: Cloud Native Computing Foundation
  ServiceCategory: Open Source / Kubernetes Scheduler
  ServiceName: Volcano
layout: finops
meters:
- aggregation: sum
  description: Compute consumed by Volcano-scheduled pods on the underlying cluster, attributed via Volcano Queue and Job labels.
  dimensions:
  - queue
  - job
  - namespace
  - node_pool
  name: scheduled_compute_seconds
  unit: second
- aggregation: sum
  description: GPU time consumed by Volcano-scheduled batch / HPC / ML training workloads.
  dimensions:
  - queue
  - gpu_type
  - job
  name: gpu_seconds
  unit: second
- aggregation: avg
  description: Ratio of allocated to declared Queue capability across CPU, memory, and GPU.
  dimensions:
  - queue
  - resource
  name: queue_capacity_utilization
  unit: ratio
name: Volcano Finops
provider_name: Volcano
provider_slug: volcano
publisher_name: Cloud Native Computing Foundation
service_category: Open Source / Kubernetes Scheduler
slug: volcano-finops
source_filename: volcano-finops.yml
source_heading: FinOps Profile
source_url: https://volcano.sh
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Volcano\nproviderId: volcano\npublisherName: Cloud Native Computing Foundation\nserviceCategory: Open Source / Kubernetes Scheduler\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - Open Source\n  - Kubernetes\n  - Batch Scheduling\n  - HPC\n  - FinOps\n  - FOCUS\ndescription: FinOps view of Volcano - the project itself has no licensing or\n  invoice surface (Apache 2.0, CNCF incubating). Costs of running Volcano-\n  scheduled workloads accrue at the underlying compute, GPU, network, and\n  storage layers of the host Kubernetes cluster (cloud or on-prem). The\n  FinOps levers are queue capacity, gang-schedule efficiency, and\n  bin-packing of batch workloads onto\
  \ the underlying infrastructure.\nsources:\n  - https://volcano.sh\n  - https://volcano.sh/en/docs/\n  - https://github.com/volcano-sh/volcano\nnotes: No publisher invoice. FOCUS records for Volcano workloads are produced\n  by the underlying cloud / Kubernetes-platform billing pipeline and tagged by\n  Volcano Queue / Job metadata; there is no Volcano-issued line item.\nbillingModel:\n  pricingCategory: Open Source\n  billingFrequency: Continuous Settlement\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\nfocusColumns:\n  ServiceName: Volcano\n  ServiceCategory: Open Source / Kubernetes Scheduler\n  ProviderName: Volcano\n  PublisherName: Cloud Native Computing Foundation\n  InvoiceIssuerName: '(none - open source)'\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: scheduled_compute_seconds\n    description: Compute consumed by Volcano-scheduled pods on the underlying\n      cluster, attributed via Volcano Queue and Job labels.\n    unit: second\n    aggregation:\
  \ sum\n    dimensions:\n      - queue\n      - job\n      - namespace\n      - node_pool\n  - name: gpu_seconds\n    description: GPU time consumed by Volcano-scheduled batch / HPC / ML\n      training workloads.\n    unit: second\n    aggregation: sum\n    dimensions:\n      - queue\n      - gpu_type\n      - job\n  - name: queue_capacity_utilization\n    description: Ratio of allocated to declared Queue capability across CPU,\n      memory, and GPU.\n    unit: ratio\n    aggregation: avg\n    dimensions:\n      - queue\n      - resource\nprinciples:\n  - name: Visibility\n    description: Volcano emits Prometheus metrics for queue allocation,\n      pending pods, and job state; pair with kube-state-metrics and the\n      cluster's cost-allocation tool (OpenCost, Kubecost) to attribute spend\n      to Queues / Jobs.\n  - name: Allocation\n    description: Allocate underlying compute spend by Volcano Queue and\n      Job labels - typical breakdown is per training run, team, or\n      research\
  \ project mapped to a Queue weight.\n  - name: Optimization\n    description: Tune Queue weight and capability to bin-pack batch workloads,\n      use gang scheduling to avoid stranded GPU reservations, and right-size\n      PodGroup minMember to reduce idle waiting.\n  - name: Accountability\n    description: Platform / SRE owns the Volcano scheduler configuration;\n      individual Queue owners are accountable for staying within the\n      declared capability and for tagging Jobs for chargeback.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n    url: https://apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/volcano/refs/heads/main/finops/volcano-finops.yml
sources:
- https://volcano.sh
- https://volcano.sh/en/docs/
- https://github.com/volcano-sh/volcano
specification: FinOps Framework
tags:
- Open Source
- Kubernetes
- Batch Scheduling
- HPC
- FinOps
- FOCUS
---
