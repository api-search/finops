---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: argocd-server-openapi.json
  format: json
  label: Argo CD Applications API
  slug: argocd-applications-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/argocd/refs/heads/main/openapi/argocd-server-openapi.json
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
description: FinOps framework definition for the Argo CD API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Argo CD
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Argo CD
  PublisherName: Argo CD
  ServiceCategory: Developer Tools / API
  ServiceName: Argo CD
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
name: Argocd Finops
provider_name: Argo CD
provider_slug: argocd
publisher_name: Argo CD
service_category: API
slug: argocd-finops
source_filename: argocd-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Argo CD\nproviderId: argocd\npublisherName: Argo CD\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - DevOps\n  - GitOps\n  - Kubernetes\n  - Continuous Delivery\n  - CNCF\n  - Open Source\n  - Operator\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Argo CD API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable\
  \ API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n\
  \      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Argo CD\n  ServiceCategory: Developer Tools / API\n  ProviderName: Argo CD\n  PublisherName: Argo CD\n  InvoiceIssuerName: Argo CD\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation:\
  \ sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Argo CD Applications API\n    baseURL: ''\n    tags:\n      - Applications\n      - Sync\n      - GitOps\n      - Lifecycle\n    serviceName: Argo CD Applications API\n    serviceCategory: API\n  - name: Argo CD ApplicationSets API\n    baseURL: ''\n    tags:\n      - ApplicationSets\n      - Generators\n      - GitOps\n    serviceName: Argo CD ApplicationSets API\n    serviceCategory: API\n  - name: Argo CD Projects API\n    baseURL: ''\n    tags:\n      - Projects\n      - AppProjects\n      - RBAC\n    serviceName: Argo CD Projects API\n    serviceCategory: API\n  - name: Argo CD Clusters API\n    baseURL: ''\n    tags:\n      - Clusters\n      - Targets\n      - Kubernetes\n    serviceName:\
  \ Argo CD Clusters API\n    serviceCategory: API\n  - name: Argo CD Repositories API\n    baseURL: ''\n    tags:\n      - Repositories\n      - Git\n      - Helm\n      - OCI\n    serviceName: Argo CD Repositories API\n    serviceCategory: API\n  - name: Argo CD Accounts API\n    baseURL: ''\n    tags:\n      - Accounts\n      - Authentication\n      - Tokens\n    serviceName: Argo CD Accounts API\n    serviceCategory: API\n  - name: Argo CD Sessions API\n    baseURL: ''\n    tags:\n      - Sessions\n      - Authentication\n      - JWT\n    serviceName: Argo CD Sessions API\n    serviceCategory: API\n  - name: Argo CD Settings API\n    baseURL: ''\n    tags:\n      - Settings\n      - Configuration\n      - Plugins\n    serviceName: Argo CD Settings API\n    serviceCategory: API\n  - name: Argo CD Certificates API\n    baseURL: ''\n    tags:\n      - Certificates\n      - TLS\n      - SSH\n    serviceName: Argo CD Certificates API\n    serviceCategory: API\n  - name: Argo CD GPG Keys API\n\
  \    baseURL: ''\n    tags:\n      - GPG\n      - Signed Commits\n      - Security\n    serviceName: Argo CD GPG Keys API\n    serviceCategory: API\n  - name: Argo CD Notifications API\n    baseURL: ''\n    tags:\n      - Notifications\n      - Webhooks\n      - Slack\n      - Email\n    serviceName: Argo CD Notifications API\n    serviceCategory: API\n  - name: Argo CD Version API\n    baseURL: ''\n    tags:\n      - Version\n      - Build Info\n    serviceName: Argo CD Version API\n    serviceCategory: API\n  - name: Argo CD Application CRD\n    baseURL: ''\n    tags:\n      - CRD\n      - Kubernetes\n      - Application\n      - GitOps\n    serviceName: Argo CD Application CRD\n    serviceCategory: API\n  - name: Argo CD ApplicationSet CRD\n    baseURL: ''\n    tags:\n      - CRD\n      - Kubernetes\n      - ApplicationSet\n      - Generators\n    serviceName: Argo CD ApplicationSet CRD\n    serviceCategory: API\n  - name: Argo CD AppProject CRD\n    baseURL: ''\n    tags:\n      -\
  \ CRD\n      - Kubernetes\n      - AppProject\n      - RBAC\n    serviceName: Argo CD AppProject CRD\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/argocd/refs/heads/main/finops/argocd-finops.yml
sources: []
specification: FinOps Framework
tags:
- DevOps
- GitOps
- Kubernetes
- Continuous Delivery
- CNCF
- Open Source
- Operator
- FinOps
- Cost Management
- FOCUS
---
