---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: virtual_service.proto
  format: yaml
  label: Istio API
  slug: istio-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/istio/api/master/networking/v1alpha3/virtual_service.proto
- filename: swagger.json
  format: json
  label: Consul Connect / Service Mesh API
  slug: consul-api
  spec_type: OpenAPI
  url: https://github.com/hashicorp/consul/blob/main/api/openapi-spec/swagger.json
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
description: FinOps framework definition for the Service Mesh API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Service Mesh
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Service Mesh
  PublisherName: Service Mesh
  ServiceCategory: Developer Tools / API
  ServiceName: Service Mesh
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
name: Service Mesh Finops
provider_name: Service Mesh
provider_slug: service-mesh
publisher_name: Service Mesh
service_category: API
slug: service-mesh-finops
source_filename: service-mesh-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Service Mesh\nproviderId: service-mesh\npublisherName: Service Mesh\nserviceCategory: API\ncreated: '2026-05-04'\nmodified: '2026-05-04'\ntags:\n  - Service Mesh\n  - Microservices\n  - Cloud Native\n  - Kubernetes\n  - Networking\n  - Observability\n  - Zero Trust\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Service Mesh API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n\
  \    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage\
  \ the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Service Mesh\n  ServiceCategory: Developer Tools / API\n  ProviderName: Service Mesh\n  PublisherName: Service Mesh\n  InvoiceIssuerName: Service Mesh\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned\
  \ over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Istio API\n    baseURL: ''\n    tags:\n      - Service Mesh\n      - Istio\n      - Traffic Management\n      - Kubernetes\n      - mTLS\n    serviceName: Istio API\n    serviceCategory: API\n  - name: Linkerd Admin API\n    baseURL: ''\n    tags:\n      - Service Mesh\n      - Linkerd\n      - CNCF\n      - Observability\n      - mTLS\n    serviceName: Linkerd Admin API\n    serviceCategory: API\n  - name: Consul Connect / Service Mesh API\n    baseURL: ''\n    tags:\n      - Service Mesh\n      - Consul\n      - HashiCorp\n      - Service Discovery\n      - Zero Trust\n    serviceName: Consul Connect / Service Mesh API\n    serviceCategory:\
  \ API\n  - name: AWS App Mesh API\n    baseURL: ''\n    tags:\n      - Service Mesh\n      - AWS\n      - Cloud\n      - EKS\n      - ECS\n    serviceName: AWS App Mesh API\n    serviceCategory: API\n  - name: Service Mesh Interface (SMI)\n    baseURL: ''\n    tags:\n      - Service Mesh\n      - SMI\n      - Standard\n      - Kubernetes\n      - CNCF\n    serviceName: Service Mesh Interface (SMI)\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/service-mesh/refs/heads/main/finops/service-mesh-finops.yml
sources: []
specification: FinOps Framework
tags:
- Service Mesh
- Microservices
- Cloud Native
- Kubernetes
- Networking
- Observability
- Zero Trust
- FinOps
- Cost Management
- FOCUS
---
