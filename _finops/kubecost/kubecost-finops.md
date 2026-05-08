---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: kubecost-allocation-openapi.yml
  format: yaml
  label: Kubecost Allocation API
  slug: allocation-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/kubecost/refs/heads/main/openapi/kubecost-allocation-openapi.yml
- filename: kubecost-assets-openapi.yml
  format: yaml
  label: Kubecost Assets API
  slug: assets-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/kubecost/refs/heads/main/openapi/kubecost-assets-openapi.yml
- filename: kubecost-cloud-cost-openapi.yml
  format: yaml
  label: Kubecost Cloud Cost API
  slug: cloud-cost-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/kubecost/refs/heads/main/openapi/kubecost-cloud-cost-openapi.yml
- filename: kubecost-budget-openapi.yml
  format: yaml
  label: Kubecost Budget API
  slug: budget-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/kubecost/refs/heads/main/openapi/kubecost-budget-openapi.yml
- filename: kubecost-forecast-openapi.yml
  format: yaml
  label: Kubecost Forecast API
  slug: forecast-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/kubecost/refs/heads/main/openapi/kubecost-forecast-openapi.yml
- filename: kubecost-savings-openapi.yml
  format: yaml
  label: Kubecost Savings API
  slug: savings-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/kubecost/refs/heads/main/openapi/kubecost-savings-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Usage
  - Purchase
  - Adjustment
  - Credit
  pricingCategory: Freemium + Subscription
description: 'FOCUS-aligned FinOps for Kubecost: Apptio-licensed Kubernetes cost-allocation and optimization tooling. Foundations is free; Enterprise tiers are subscription contracts. The product itself emits the FinOps signal — its Allocation, Assets, Cloud Cost, Budget, Forecast, and Savings APIs are the data plane that downstream FinOps tooling consumes.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Apptio, Inc.
  ProviderName: Kubecost
  PublisherName: International Business Machines Corporation (Apptio)
  ServiceCategory: Cloud Cost Management
  ServiceName: Kubecost
layout: finops
meters:
- aggregation: max
  dimensions:
  - cluster
  - cloud_provider
  - region
  name: cluster_cores
  unit: core
- aggregation: count
  name: monitored_clusters
  unit: cluster
- aggregation: max
  name: metric_retention_days
  unit: day
- aggregation: sum
  dimensions:
  - api
  - window
  - aggregation
  name: allocation_queries
  unit: request
- aggregation: count
  name: gpu_optimization_enabled
  unit: cluster
name: Kubecost Finops
provider_name: Kubecost
provider_slug: kubecost
publisher_name: International Business Machines Corporation (Apptio)
service_category: Cloud Cost Management
slug: kubecost-finops
source_filename: kubecost-finops.yml
source_heading: FinOps Profile
source_url: https://www.apptio.com/pricing?src=kc-com
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Kubecost\nproviderId: kubecost\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Cloud Cost\n  - Kubernetes\n  - Cost Management\ndescription: 'FOCUS-aligned FinOps for Kubecost: Apptio-licensed Kubernetes cost-allocation and optimization\n  tooling. Foundations is free; Enterprise tiers are subscription contracts. The product itself emits\n  the FinOps signal — its Allocation, Assets, Cloud Cost, Budget, Forecast, and Savings APIs are the\n  data plane that downstream FinOps tooling consumes.'\nsources:\n  - https://www.apptio.com/pricing?src=kc-com\n  - https://docs.kubecost.com/apis/monitoring-apis/api-allocation\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\n\
  publisherName: International Business Machines Corporation (Apptio)\nserviceCategory: Cloud Cost Management\nbillingModel:\n  pricingCategory: Freemium + Subscription\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Adjustment\n    - Credit\nfocusColumns:\n  ServiceName: Kubecost\n  ServiceCategory: Cloud Cost Management\n  ProviderName: Kubecost\n  PublisherName: International Business Machines Corporation (Apptio)\n  InvoiceIssuerName: Apptio, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: cluster_cores\n    unit: core\n    aggregation: max\n    dimensions:\n      - cluster\n      - cloud_provider\n      - region\n  - name: monitored_clusters\n    unit: cluster\n    aggregation: count\n  - name: metric_retention_days\n    unit: day\n    aggregation: max\n  - name: allocation_queries\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - window\n      - aggregation\n  - name: gpu_optimization_enabled\n\
  \    unit: cluster\n    aggregation: count\nprinciples:\n  - name: Visibility\n    description: Use the Allocation, Assets, and Cloud Cost APIs to expose Kubernetes spend by namespace,\n      label, deployment, controller, and cloud asset; reconcile against AWS/Azure/GCP bills via the bill-reconciliation\n      pipeline.\n  - name: Allocation\n    description: Drive cost allocation off Kubernetes labels and annotations; align label keys with the\n      organization's chargeback dimensions (team, product, environment).\n  - name: Optimization\n    description: Use the Savings API to surface right-sizing, abandoned workload, and request/limit recommendations;\n      drive Forecast API into the FinOps planning loop.\n  - name: Accountability\n    description: Set Budget API alerts per namespace owner; review weekly Allocation deltas in the FinOps\n      practice cadence; tie Foundations vs Enterprise feature differences (RBAC, retention) to the maturity\n      stage of the consuming team.\n\
  maintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/kubecost/refs/heads/main/finops/kubecost-finops.yml
sources:
- https://www.apptio.com/pricing?src=kc-com
- https://docs.kubecost.com/apis/monitoring-apis/api-allocation
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Cloud Cost
- Kubernetes
- Cost Management
---
