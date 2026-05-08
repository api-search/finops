---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: red-hat-openshift-api-openapi.yml
  format: yaml
  label: Red Hat OpenShift Container Platform API
  slug: openshift-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/red-hat-openshift/refs/heads/main/openapi/red-hat-openshift-api-openapi.yml
- filename: openapi
  format: yaml
  label: Red Hat OpenShift Cluster Manager API
  slug: openshift-cluster-manager-api
  spec_type: OpenAPI
  url: https://api.openshift.com/openapi
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  - Tax
  - Credit
  - Adjustment
  chargeFrequency: Recurring
  pricingCategory: Usage-Based
description: FinOps framework definition for the Red Hat OpenShift API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Red Hat OpenShift
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Red Hat OpenShift
  PublisherName: Red Hat OpenShift
  ServiceCategory: Developer Tools / API
  ServiceName: Red Hat OpenShift
layout: finops
meters:
- aggregation: sum
  description: Count of billable API requests
  dimensions:
  - api
  - endpoint
  - tier
  - region
  - consumer
  name: api_requests
  unit: request
- aggregation: sum
  description: Bytes returned over the network in API responses
  dimensions:
  - api
  - region
  - consumer
  name: data_egress
  unit: GB
- aggregation: sum
  description: Server-side compute consumed by the request, where applicable
  dimensions:
  - api
  - endpoint
  - tier
  name: compute_seconds
  unit: second
name: Red Hat Openshift Finops
provider_name: Red Hat OpenShift
provider_slug: red-hat-openshift
publisher_name: Red Hat OpenShift
service_category: API
slug: red-hat-openshift-finops
source_filename: red-hat-openshift-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Red Hat OpenShift\nproviderId: red-hat-openshift\npublisherName: Red Hat OpenShift\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Containers\n  - Enterprise\n  - Hybrid Cloud\n  - Kubernetes\n  - PaaS\n  - Red Hat\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Red Hat OpenShift API surface. Provides a FOCUS-aligned\n  mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description:\
  \ Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n\
  \    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Red Hat OpenShift\n  ServiceCategory: Developer Tools / API\n  ProviderName: Red Hat OpenShift\n  PublisherName: Red Hat OpenShift\n  InvoiceIssuerName: Red Hat OpenShift\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over\
  \ the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Red Hat OpenShift Container Platform API\n    baseURL: https://api.cluster.example.com:6443\n    tags:\n      - Builds\n      - Cluster Management\n      - Containers\n      - Kubernetes\n      - Networking\n      - Workloads\n    serviceName: Red Hat OpenShift Container Platform API\n    serviceCategory: API\n  - name: Red Hat OpenShift Cluster Manager API\n    baseURL: https://api.openshift.com\n    tags:\n      - Cluster Management\n      - Cloud\n      - Hybrid Cloud\n      - Multi-Cluster\n      - Subscriptions\n    serviceName: Red Hat OpenShift Cluster Manager API\n    serviceCategory: API\n  - name: Red Hat OpenShift Pipelines\
  \ (Tekton) API\n    baseURL: https://api.cluster.example.com:6443/apis/tekton.dev/v1\n    tags:\n      - CI/CD\n      - Kubernetes\n      - Pipelines\n      - Tekton\n    serviceName: Red Hat OpenShift Pipelines (Tekton) API\n    serviceCategory: API\n  - name: Red Hat OpenShift GitOps (ArgoCD) API\n    baseURL: https://api.cluster.example.com:6443/apis/argoproj.io/v1alpha1\n    tags:\n      - ArgoCD\n      - CI/CD\n      - GitOps\n      - Kubernetes\n    serviceName: Red Hat OpenShift GitOps (ArgoCD) API\n    serviceCategory: API\n  - name: Red Hat OpenShift Service Mesh API\n    baseURL: https://api.cluster.example.com:6443/apis/networking.istio.io/v1beta1\n    tags:\n      - Istio\n      - Kubernetes\n      - Service Mesh\n      - Traffic Management\n    serviceName: Red Hat OpenShift Service Mesh API\n    serviceCategory: API\n  - name: Red Hat OpenShift Serverless (Knative) API\n    baseURL: https://api.cluster.example.com:6443/apis/serving.knative.dev/v1\n    tags:\n      - Event-Driven\n\
  \      - Knative\n      - Kubernetes\n      - Serverless\n    serviceName: Red Hat OpenShift Serverless (Knative) API\n    serviceCategory: API\n  - name: Red Hat OpenShift Service on AWS (ROSA) API\n    baseURL: https://api.openshift.com/api/clusters_mgmt/v1\n    tags:\n      - AWS\n      - Cloud\n      - Managed Service\n      - OpenShift\n    serviceName: Red Hat OpenShift Service on AWS (ROSA) API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/red-hat-openshift/refs/heads/main/finops/red-hat-openshift-finops.yml
sources: []
specification: FinOps Framework
tags:
- Containers
- Enterprise
- Hybrid Cloud
- Kubernetes
- PaaS
- Red Hat
- FinOps
- Cost Management
- FOCUS
---
