---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: treblle-api-openapi.yml
  format: yaml
  label: Treblle Platform API
  slug: treblle-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/treblle/refs/heads/main/openapi/treblle-api-openapi.yml
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
description: FinOps framework definition for the Treblle API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Treblle
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Treblle
  PublisherName: Treblle
  ServiceCategory: Developer Tools / API
  ServiceName: Treblle
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
name: Treblle Finops
provider_name: Treblle
provider_slug: treblle
publisher_name: Treblle
service_category: API
slug: treblle-finops
source_filename: treblle-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Treblle\nproviderId: treblle\npublisherName: Treblle\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Analytics\n  - Artificial Intelligence\n  - Developer Experience\n  - Documentation\n  - Governance\n  - Insights\n  - Observability\n  - Platform\n  - Security\n  - Testing\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Treblle API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n\
  \      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n   \
  \   - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Treblle\n  ServiceCategory: Developer Tools / API\n  ProviderName: Treblle\n  PublisherName: Treblle\n  InvoiceIssuerName: Treblle\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description:\
  \ Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Treblle\n    baseURL: ''\n    tags:\n      - API Intelligence\n      - Monitoring\n      - Observability\n      - Platform\n    serviceName: Treblle\n    serviceCategory: API\n  - name: Treblle Platform API\n    baseURL: https://app.treblle.com/api/v1\n    tags:\n      - Analytics\n      - API Intelligence\n      - Governance\n      - Monitoring\n    serviceName: Treblle Platform API\n    serviceCategory: API\n  - name: Treblle API Intelligence\n    baseURL: ''\n    tags:\n      - API Intelligence\n      - Monitoring\n      - Observability\n    serviceName: Treblle API Intelligence\n    serviceCategory: API\n  - name:\
  \ Treblle API Documentation\n    baseURL: ''\n    tags:\n      - Developer Experience\n      - Documentation\n      - OpenAPI\n    serviceName: Treblle API Documentation\n    serviceCategory: API\n  - name: Treblle API Governance\n    baseURL: ''\n    tags:\n      - Compliance\n      - Governance\n      - Standards\n    serviceName: Treblle API Governance\n    serviceCategory: API\n  - name: Treblle API Analytics\n    baseURL: ''\n    tags:\n      - Analytics\n      - Dashboards\n      - Metrics\n    serviceName: Treblle API Analytics\n    serviceCategory: API\n  - name: Treblle API Security\n    baseURL: ''\n    tags:\n      - Compliance\n      - Security\n      - Threat Detection\n    serviceName: Treblle API Security\n    serviceCategory: API\n  - name: Treblle API Insights\n    baseURL: ''\n    tags:\n      - Governance\n      - OpenAPI\n      - Scoring\n    serviceName: Treblle API Insights\n    serviceCategory: API\n  - name: Treblle Alfred AI\n    baseURL: ''\n    tags:\n      -\
  \ Artificial Intelligence\n      - Assistant\n      - Developer Experience\n    serviceName: Treblle Alfred AI\n    serviceCategory: API\n  - name: Treblle Aspen API Testing\n    baseURL: ''\n    tags:\n      - Developer Tools\n      - macOS\n      - Testing\n    serviceName: Treblle Aspen API Testing\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/treblle/refs/heads/main/finops/treblle-finops.yml
sources: []
specification: FinOps Framework
tags:
- Analytics
- Artificial Intelligence
- Developer Experience
- Documentation
- Governance
- Insights
- Observability
- Platform
- Security
- Testing
- FinOps
- Cost Management
- FOCUS
---
