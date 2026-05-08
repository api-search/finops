---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: openapi.yaml
  format: yaml
  label: Cilium API
  slug: cilium-api
  spec_type: OpenAPI
  url: https://github.com/cilium/cilium/blob/main/api/v1/openapi.yaml
- filename: cilium-hubble-asyncapi.yml
  format: yaml
  label: Hubble API
  slug: hubble-api
  spec_type: AsyncAPI
  url: https://raw.githubusercontent.com/api-evangelist/cilium/refs/heads/main/asyncapi/cilium-hubble-asyncapi.yml
- filename: openapi.yaml
  format: yaml
  label: Cilium Operator API
  slug: cilium-operator-api
  spec_type: OpenAPI
  url: https://github.com/cilium/cilium/blob/main/api/v1/operator/openapi.yaml
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
description: FinOps framework definition for the Cilium API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Cilium
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Cilium
  PublisherName: Cilium
  ServiceCategory: Developer Tools / API
  ServiceName: Cilium
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
name: Cilium Finops
provider_name: Cilium
provider_slug: cilium
publisher_name: Cilium
service_category: API
slug: cilium-finops
source_filename: cilium-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Cilium\nproviderId: cilium\npublisherName: Cilium\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Cloud Native\n  - eBPF\n  - Kubernetes\n  - Networking\n  - Security\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Cilium API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team,\
  \ environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n\
  \      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Cilium\n  ServiceCategory: Developer Tools / API\n  ProviderName: Cilium\n  PublisherName: Cilium\n  InvoiceIssuerName: Cilium\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n\
  \      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Cilium API\n    baseURL: https://localhost/v1\n    tags:\n      - eBPF\n      - Kubernetes\n      - Networking\n      - Security\n    serviceName: Cilium API\n    serviceCategory: API\n  - name: Hubble API\n    baseURL: ''\n    tags:\n      - eBPF\n      - Kubernetes\n      - Networking\n      - Observability\n    serviceName: Hubble API\n    serviceCategory: API\n  - name: Tetragon API\n    baseURL: ''\n    tags:\n      - eBPF\n      - Kubernetes\n      - Observability\n      - Security\n    serviceName: Tetragon API\n    serviceCategory: API\n  - name: Cilium Operator API\n    baseURL: https://localhost/v1\n    tags:\n      - eBPF\n      - Kubernetes\n      - Networking\n      - Operations\n    serviceName: Cilium Operator API\n\
  \    serviceCategory: API\n  - name: Hubble Relay API\n    baseURL: ''\n    tags:\n      - gRPC\n      - Kubernetes\n      - Networking\n      - Observability\n    serviceName: Hubble Relay API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/cilium/refs/heads/main/finops/cilium-finops.yml
sources: []
specification: FinOps Framework
tags:
- Cloud Native
- eBPF
- Kubernetes
- Networking
- Security
- FinOps
- Cost Management
- FOCUS
---
