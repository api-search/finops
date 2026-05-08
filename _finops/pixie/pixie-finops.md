---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: pixie-openapi.yml
  format: yaml
  label: Pixie API
  slug: pixie
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/pixie/refs/heads/main/openapi/pixie-openapi.yml
billing_model:
  billingCurrency: N/A
  billingFrequency: None
  chargeCategories: []
  pricingCategory: Open Source
description: FOCUS-aligned FinOps for Pixie - Pixie is open source under Apache 2.0; there are no vendor invoices for the project itself. The cost surface is the user's own Kubernetes cluster resources (CPU, memory, storage) consumed by the Pixie Cloud control plane and Vizier data plane. Commercial managed offerings that bundle Pixie (e.g. New Relic) are billed by those vendors and outside the scope of this artifact.
focus_columns:
  BillingCurrency: N/A
  ChargeCategory: N/A
  PricingCategory: Open Source
  ProviderName: Pixie (CNCF)
  PublisherName: Pixie Authors / CNCF
  ServiceCategory: Observability
  ServiceName: Pixie
  ServiceSubcategory: Kubernetes Observability
layout: finops
meters:
- aggregation: sum
  description: CPU consumed by Pixie Vizier agents (PEMs / Cloud Connector / Kelvin) on the monitored cluster. Cost shows up in your cloud provider bill, not from Pixie.
  dimensions:
  - cluster
  - component
  - node
  name: cluster_cpu_pixie
  unit: vCPU-hour
- aggregation: sum
  description: Memory consumed by Pixie components on the cluster.
  dimensions:
  - cluster
  - component
  name: cluster_memory_pixie
  unit: GB-hour
- aggregation: sum
  description: CPU / memory consumed by the self-hosted Pixie Cloud control plane (only if self-hosting; otherwise the community-hosted instance bears this).
  dimensions:
  - service
  name: pixie_cloud_compute
  unit: vCPU-hour
- aggregation: sum
  description: Pixie API / PxL script invocations. Not billed by Pixie; useful for capacity planning of the Cloud control plane.
  dimensions:
  - api
  - script
  name: api_calls
  unit: request
name: Pixie Finops
provider_name: Pixie
provider_slug: pixie
publisher_name: Pixie Authors (CNCF Sandbox project, originally contributed by New Relic, Inc.)
service_category: Observability
slug: pixie-finops
source_filename: pixie-finops.yml
source_heading: FinOps Profile
source_url: https://docs.px.dev/about-pixie/faq/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Pixie\nproviderId: pixie\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Observability\n  - Kubernetes\n  - Open Source\ndescription: FOCUS-aligned FinOps for Pixie - Pixie is open source under Apache 2.0; there are no\n  vendor invoices for the project itself. The cost surface is the user's own Kubernetes cluster\n  resources (CPU, memory, storage) consumed by the Pixie Cloud control plane and Vizier data\n  plane. Commercial managed offerings that bundle Pixie (e.g. New Relic) are billed by those\n  vendors and outside the scope of this artifact.\nsources:\n  - https://docs.px.dev/about-pixie/faq/\n  - https://github.com/pixie-io/pixie/blob/main/LICENSE\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl:\
  \ https://focus.finops.org/focus-specification/v1-3/\npublisherName: Pixie Authors (CNCF Sandbox project, originally contributed by New Relic, Inc.)\nserviceCategory: Observability\nbillingModel:\n  pricingCategory: Open Source\n  billingFrequency: None\n  billingCurrency: N/A\n  chargeCategories: []\nfocusColumns:\n  ServiceName: Pixie\n  ServiceCategory: Observability\n  ServiceSubcategory: Kubernetes Observability\n  ProviderName: Pixie (CNCF)\n  PublisherName: Pixie Authors / CNCF\n  BillingCurrency: N/A\n  ChargeCategory: N/A\n  PricingCategory: Open Source\nmeters:\n  - name: cluster_cpu_pixie\n    description: CPU consumed by Pixie Vizier agents (PEMs / Cloud Connector / Kelvin) on the\n      monitored cluster. Cost shows up in your cloud provider bill, not from Pixie.\n    unit: vCPU-hour\n    aggregation: sum\n    dimensions:\n      - cluster\n      - component\n      - node\n  - name: cluster_memory_pixie\n    description: Memory consumed by Pixie components on the cluster.\n\
  \    unit: GB-hour\n    aggregation: sum\n    dimensions:\n      - cluster\n      - component\n  - name: pixie_cloud_compute\n    description: CPU / memory consumed by the self-hosted Pixie Cloud control plane (only if\n      self-hosting; otherwise the community-hosted instance bears this).\n    unit: vCPU-hour\n    aggregation: sum\n    dimensions:\n      - service\n  - name: api_calls\n    description: Pixie API / PxL script invocations. Not billed by Pixie; useful for capacity\n      planning of the Cloud control plane.\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - script\nprinciples:\n  - name: Visibility\n    description: Pixie itself is free; cost visibility comes from your Kubernetes cost-allocation\n      tooling (OpenCost, Kubecost, cloud-provider bill) measuring the CPU / memory / storage\n      footprint of the Pixie components.\n  - name: Allocation\n    description: Tag the Pixie namespace and components with cost-allocation labels (team,\n\
  \      environment) so the cluster cost system attributes Pixie's footprint to the observability\n      function.\n  - name: Optimization\n    description: Tune PEM agent CPU / memory limits to fit your cluster's traffic profile; reduce\n      data-table retention windows to lower memory; self-host Pixie Cloud only when the community-\n      hosted offering becomes a bottleneck.\n  - name: Accountability\n    description: Platform / observability team owns Pixie's footprint as part of the cluster's\n      observability budget; review CPU / memory of the px-operator namespace each quarter.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/pixie/refs/heads/main/finops/pixie-finops.yml
sources:
- https://docs.px.dev/about-pixie/faq/
- https://github.com/pixie-io/pixie/blob/main/LICENSE
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Observability
- Kubernetes
- Open Source
---
