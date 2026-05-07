---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: helm-chart-repository-openapi.yml
  format: yaml
  label: Helm Chart Repository API
  slug: chart-repository-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/helm/refs/heads/main/openapi/helm-chart-repository-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Not Applicable
  chargeCategories:
  - Adjustment
  chargeFrequency: Not Applicable
  pricingCategory: Free / Open Source
description: FOCUS-aligned FinOps definition for Helm. Helm itself is zero-cost open-source software; cost is incurred downstream by the cluster operator, registry host, and image store. This artifact records the FinOps shape of a Helm-driven release pipeline rather than a Helm-billed product.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Adjustment
  InvoiceIssuerName: Not applicable (open source)
  PricingCategory: Free
  PricingUnit: install
  ProviderName: Helm
  PublisherName: The Helm Authors
  ServiceCategory: Open Source / DevOps
  ServiceName: Helm
layout: finops
meters:
- aggregation: count
  description: Number of Helm releases installed per cluster / namespace; surrogate for downstream cluster cost
  dimensions:
  - cluster
  - namespace
  - chart_name
  - chart_version
  name: chart_installs
  unit: install
- aggregation: sum
  description: Pulls of chart artifacts from the upstream chart repository or OCI registry
  dimensions:
  - registry
  - chart_name
  - chart_version
  name: chart_pulls
  unit: pull
- aggregation: sum
  description: Container image pulls triggered by Helm-installed workloads (registry-side meter, not Helm-side)
  dimensions:
  - registry
  - image
  name: image_pulls
  unit: pull
name: Helm Finops
provider_name: Helm
provider_slug: helm
publisher_name: The Helm Authors / Cloud Native Computing Foundation
service_category: Open Source / DevOps
slug: helm-finops
source_filename: helm-finops.yml
source_heading: FinOps Profile
source_url: https://helm.sh/docs/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Helm\nproviderId: helm\npublisherName: The Helm Authors / Cloud Native Computing Foundation\nserviceCategory: Open Source / DevOps\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Charts\n  - Cloud Native\n  - Container Orchestration\n  - DevOps\n  - Kubernetes\n  - Package Manager\n  - Open Source\n  - FinOps\n  - FOCUS\nnotes: Helm is a CNCF-graduated open-source project distributed under Apache 2.0; it has no invoice surface\n  of its own. FinOps for a Helm-based release pipeline is really FinOps over (a) the Kubernetes clusters Helm\n  installs into, (b) the chart repository / OCI registry the charts live in, and (c) the storage/egress costs\n  of upstream\
  \ image pulls referenced by chart values. Meters and unit-economics are therefore stubs that\n  point at the underlying cloud and registry providers.\ndescription: 'FOCUS-aligned FinOps definition for Helm. Helm itself is zero-cost open-source software;\n  cost is incurred downstream by the cluster operator, registry host, and image store. This artifact\n  records the FinOps shape of a Helm-driven release pipeline rather than a Helm-billed product.'\nsources:\n  - https://helm.sh/docs/\n  - https://github.com/helm/helm\n  - https://www.cncf.io/projects/helm/\nbillingModel:\n  pricingCategory: Free / Open Source\n  billingFrequency: Not Applicable\n  billingCurrency: USD\n  chargeCategories:\n    - Adjustment\n  chargeFrequency: Not Applicable\nfocusColumns:\n  ServiceName: Helm\n  ServiceCategory: Open Source / DevOps\n  ProviderName: Helm\n  PublisherName: The Helm Authors\n  InvoiceIssuerName: 'Not applicable (open source)'\n  PricingCategory: Free\n  PricingUnit: install\n  BillingCurrency:\
  \ USD\n  ChargeCategory: Adjustment\nprinciples:\n  - name: Visibility\n    description: Track Helm release activity through 'helm list', the Kubernetes audit log, and (when\n      using GitOps) ArgoCD or Flux dashboards. Tag releases with team / environment labels so cluster\n      cost attribution can flow through.\n  - name: Allocation\n    description: Allocate spend not against Helm itself but against the Kubernetes namespaces and label\n      sets that Helm installs into. Use cluster-cost tools (OpenCost, Kubecost) keyed on the labels Helm\n      sets via 'app.kubernetes.io/instance'.\n  - name: Optimization\n    description: Helm-specific levers - prefer OCI registries with authenticated pulls to avoid Docker Hub\n      anonymous limits, mirror frequently-pulled charts internally, pin chart versions to skip\n      unnecessary 'helm repo update' churn, and use 'helm template' in CI to fail fast before consuming\n      cluster resources.\n  - name: Accountability\n    description:\
  \ Owners of each Helm chart in your internal catalog are responsible for the resource\n      requests/limits in default values.yaml; FinOps reviews should look at chart defaults as a primary\n      lever for cluster cost.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Workload Optimization\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - Onboarding Workloads\n      - Intersecting Disciplines\nmeters:\n  - name: chart_installs\n    description: Number of Helm releases installed per cluster / namespace; surrogate for downstream\n      cluster cost\n    unit: install\n    aggregation: count\n\
  \    dimensions:\n      - cluster\n      - namespace\n      - chart_name\n      - chart_version\n  - name: chart_pulls\n    description: Pulls of chart artifacts from the upstream chart repository or OCI registry\n    unit: pull\n    aggregation: sum\n    dimensions:\n      - registry\n      - chart_name\n      - chart_version\n  - name: image_pulls\n    description: Container image pulls triggered by Helm-installed workloads (registry-side meter, not\n      Helm-side)\n    unit: pull\n    aggregation: sum\n    dimensions:\n      - registry\n      - image\napis:\n  - name: Helm Chart Repository API\n    baseURL: ''\n    tags:\n      - Charts\n      - Helm\n      - Kubernetes\n      - Package Manager\n    serviceName: Helm Chart Repository API\n    serviceCategory: Open Source / DevOps\nunitEconomics:\n  - name: Cost per Helm Release\n    metric: cluster_cost / chart_installs\n    target: TBD (depends on chart resource defaults)\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/helm/refs/heads/main/finops/helm-finops.yml
sources:
- https://helm.sh/docs/
- https://github.com/helm/helm
- https://www.cncf.io/projects/helm/
specification: FinOps Framework
tags:
- Charts
- Cloud Native
- Container Orchestration
- DevOps
- Kubernetes
- Package Manager
- Open Source
- FinOps
- FOCUS
---
