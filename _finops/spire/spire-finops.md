---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: spire-workload-asyncapi.yml
  format: yaml
  label: SPIRE Workload API
  slug: spire-workload-api
  spec_type: AsyncAPI
  url: https://raw.githubusercontent.com/api-evangelist/spire/refs/heads/main/asyncapi/spire-workload-asyncapi.yml
- filename: spire-health-openapi.yml
  format: yaml
  label: SPIRE Agent API
  slug: spire-agent-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/spire/refs/heads/main/openapi/spire-health-openapi.yml
- filename: spire-oidc-discovery-openapi.yml
  format: yaml
  label: SPIRE OIDC Discovery API
  slug: spire-oidc-discovery-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/spire/refs/heads/main/openapi/spire-oidc-discovery-openapi.yml
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
description: FinOps framework definition for the SPIRE API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: SPIRE
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: SPIRE
  PublisherName: SPIRE
  ServiceCategory: Developer Tools / API
  ServiceName: SPIRE
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
name: Spire Finops
provider_name: SPIRE
provider_slug: spire
publisher_name: SPIRE
service_category: API
slug: spire-finops
source_filename: spire-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: SPIRE\nproviderId: spire\npublisherName: SPIRE\nserviceCategory: API\ncreated: '2026-05-04'\nmodified: '2026-05-04'\ntags:\n  - Authentication\n  - Cloud Native\n  - Graduated\n  - Identity\n  - Security\n  - Zero Trust\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the SPIRE API surface. Provides a FOCUS-aligned mapping for\n  cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with\
  \ the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps\
  \ Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: SPIRE\n  ServiceCategory: Developer Tools / API\n  ProviderName: SPIRE\n  PublisherName: SPIRE\n  InvoiceIssuerName: SPIRE\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n\
  \      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: SPIRE Workload API\n    baseURL: ''\n    tags:\n      - gRPC\n      - Identity\n      - JWT\n      - Workload\n      - X.509\n    serviceName: SPIRE Workload API\n    serviceCategory: API\n  - name: SPIRE Server API\n    baseURL: ''\n    tags:\n      - Administration\n      - Attestation\n      - gRPC\n      - Registration\n      - Server\n    serviceName: SPIRE Server API\n    serviceCategory: API\n  - name: SPIRE Agent API\n    baseURL: ''\n    tags:\n      - Agent\n      - Attestation\n      - Identity\n      - Node\n      - Security\n    serviceName: SPIRE Agent API\n    serviceCategory: API\n  - name: SPIRE OIDC Discovery API\n    baseURL: ''\n    tags:\n      - Cloud\n      - Federation\n      - Identity\n    \
  \  - JWT\n      - OIDC\n    serviceName: SPIRE OIDC Discovery API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/spire/refs/heads/main/finops/spire-finops.yml
sources: []
specification: FinOps Framework
tags:
- Authentication
- Cloud Native
- Graduated
- Identity
- Security
- Zero Trust
- FinOps
- Cost Management
- FOCUS
---
