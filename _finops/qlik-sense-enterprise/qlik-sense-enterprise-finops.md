---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: qlik-sense-enterprise-repository-service-openapi.yml
  format: yaml
  label: Qlik Sense Repository Service
  slug: qlik-sense-repository-service
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/qlik-sense-enterprise/refs/heads/main/openapi/qlik-sense-enterprise-repository-service-openapi.yml
- filename: qlik-sense-enterprise-proxy-service-openapi.yml
  format: yaml
  label: Qlik Sense Proxy Service
  slug: qlik-sense-proxy-service
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/qlik-sense-enterprise/refs/heads/main/openapi/qlik-sense-enterprise-proxy-service-openapi.yml
- filename: qlik-sense-enterprise-about-service-openapi.yml
  format: yaml
  label: Qlik Sense About Service
  slug: qlik-sense-about-service
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/qlik-sense-enterprise/refs/heads/main/openapi/qlik-sense-enterprise-about-service-openapi.yml
- filename: qlik-sense-enterprise-data-connection-openapi.yml
  format: yaml
  label: Qlik Sense Data Connection
  slug: qlik-sense-data-connection
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/qlik-sense-enterprise/refs/heads/main/openapi/qlik-sense-enterprise-data-connection-openapi.yml
- filename: qlik-sense-enterprise-licenses-openapi.yml
  format: yaml
  label: Qlik Sense Licenses
  slug: qlik-sense-licenses
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/qlik-sense-enterprise/refs/heads/main/openapi/qlik-sense-enterprise-licenses-openapi.yml
- filename: qlik-sense-enterprise-odag-service-openapi.yml
  format: yaml
  label: Qlik Sense ODAG
  slug: qlik-sense-odag
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/qlik-sense-enterprise/refs/heads/main/openapi/qlik-sense-enterprise-odag-service-openapi.yml
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
description: FinOps framework definition for the Qlik Sense Enterprise API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Qlik Sense Enterprise
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Qlik Sense Enterprise
  PublisherName: Qlik Sense Enterprise
  ServiceCategory: Developer Tools / API
  ServiceName: Qlik Sense Enterprise
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
name: Qlik Sense Enterprise Finops
provider_name: Qlik Sense Enterprise
provider_slug: qlik-sense-enterprise
publisher_name: Qlik Sense Enterprise
service_category: API
slug: qlik-sense-enterprise-finops
source_filename: qlik-sense-enterprise-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Qlik Sense Enterprise\nproviderId: qlik-sense-enterprise\npublisherName: Qlik Sense Enterprise\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Analytics\n  - Business Intelligence\n  - Data Visualization\n  - Enterprise\n  - REST API\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Qlik Sense Enterprise API surface. Provides a FOCUS-aligned\n  mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name:\
  \ Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  -\
  \ name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Qlik Sense Enterprise\n  ServiceCategory: Developer Tools / API\n  ProviderName: Qlik Sense Enterprise\n  PublisherName: Qlik Sense Enterprise\n  InvoiceIssuerName: Qlik Sense Enterprise\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name:\
  \ data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Qlik Sense Repository Service\n    baseURL: ''\n    tags:\n      - Management\n      - Repository\n      - Security\n    serviceName: Qlik Sense Repository Service\n    serviceCategory: API\n  - name: Qlik Sense Engine JSON API\n    baseURL: ''\n    tags:\n      - Engine\n      - JSON-RPC\n      - WebSocket\n    serviceName: Qlik Sense Engine JSON API\n    serviceCategory: API\n  - name: Qlik Sense Proxy Service\n    baseURL: ''\n    tags:\n      - Proxy\n      - Authentication\n      - Sessions\n    serviceName: Qlik Sense Proxy Service\n    serviceCategory: API\n  - name: Qlik Sense\
  \ About Service\n    baseURL: ''\n    tags:\n      - Metadata\n      - Service\n    serviceName: Qlik Sense About Service\n    serviceCategory: API\n  - name: Qlik Sense Data Connection\n    baseURL: ''\n    tags:\n      - Data Connections\n      - Integration\n    serviceName: Qlik Sense Data Connection\n    serviceCategory: API\n  - name: Qlik Sense Licenses\n    baseURL: ''\n    tags:\n      - Licensing\n      - Allocation\n    serviceName: Qlik Sense Licenses\n    serviceCategory: API\n  - name: Qlik Sense ODAG\n    baseURL: ''\n    tags:\n      - ODAG\n      - On-Demand\n      - Apps\n    serviceName: Qlik Sense ODAG\n    serviceCategory: API\n  - name: Qlik Sense Capabilities\n    baseURL: ''\n    tags:\n      - Visualization\n      - Mashup\n      - Embedding\n    serviceName: Qlik Sense Capabilities\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n   \
  \ metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/qlik-sense-enterprise/refs/heads/main/finops/qlik-sense-enterprise-finops.yml
sources: []
specification: FinOps Framework
tags:
- Analytics
- Business Intelligence
- Data Visualization
- Enterprise
- REST API
- FinOps
- Cost Management
- FOCUS
---
