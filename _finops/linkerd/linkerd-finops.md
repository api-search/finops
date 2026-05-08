---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: linkerd-proxy-admin-openapi.yml
  format: yaml
  label: Linkerd Proxy Admin API
  slug: proxy-admin-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/linkerd/refs/heads/main/openapi/linkerd-proxy-admin-openapi.yml
- filename: linkerd-viz-metrics-openapi.yml
  format: yaml
  label: Linkerd Viz Metrics API
  slug: viz-metrics-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/linkerd/refs/heads/main/openapi/linkerd-viz-metrics-openapi.yml
- filename: linkerd-tap-openapi.yml
  format: yaml
  label: Linkerd Tap API
  slug: tap-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/linkerd/refs/heads/main/openapi/linkerd-tap-openapi.yml
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
description: FinOps framework definition for the Linkerd API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Linkerd
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Linkerd
  PublisherName: Linkerd
  ServiceCategory: Developer Tools / API
  ServiceName: Linkerd
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
name: Linkerd Finops
provider_name: Linkerd
provider_slug: linkerd
publisher_name: Linkerd
service_category: API
slug: linkerd-finops
source_filename: linkerd-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Linkerd\nproviderId: linkerd\npublisherName: Linkerd\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Kubernetes\n  - mTLS\n  - Observability\n  - Security\n  - Service Mesh\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Linkerd API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming\
  \ team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice\
  \ Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Linkerd\n  ServiceCategory: Developer Tools / API\n  ProviderName: Linkerd\n  PublisherName: Linkerd\n  InvoiceIssuerName: Linkerd\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n\
  \      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Linkerd Proxy Admin API\n    baseURL: http://localhost:4191\n    tags:\n      - Health Check\n      - Metrics\n      - Prometheus\n      - Proxy\n    serviceName: Linkerd Proxy Admin API\n    serviceCategory: API\n  - name: Linkerd Viz Metrics API\n    baseURL: ''\n    tags:\n      - Dashboard\n      - Metrics\n      - Observability\n      - Statistics\n    serviceName: Linkerd Viz Metrics API\n    serviceCategory: API\n  - name: Linkerd Tap API\n    baseURL: ''\n    tags:\n      - Debugging\n      - Real-Time\n      - Tap\n      - Traffic Inspection\n    serviceName: Linkerd Tap API\n    serviceCategory: API\n  - name: Linkerd Proxy Control Plane API\n    baseURL: ''\n    tags:\n      - Control Plane\n      - gRPC\n\
  \      - mTLS\n      - Policy\n    serviceName: Linkerd Proxy Control Plane API\n    serviceCategory: API\n  - name: Linkerd Multicluster API\n    baseURL: ''\n    tags:\n      - Federation\n      - Kubernetes\n      - mTLS\n      - Multicluster\n    serviceName: Linkerd Multicluster API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/linkerd/refs/heads/main/finops/linkerd-finops.yml
sources: []
specification: FinOps Framework
tags:
- Kubernetes
- mTLS
- Observability
- Security
- Service Mesh
- FinOps
- Cost Management
- FOCUS
---
