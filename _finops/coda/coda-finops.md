---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: coda-openapi.json
  format: json
  label: Coda Docs API
  slug: coda-docs-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/coda/refs/heads/main/openapi/coda-openapi.json
- filename: coda-openapi.json
  format: json
  label: Coda Folders API
  slug: coda-folders-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/coda/refs/heads/main/openapi/coda-openapi.json
- filename: coda-openapi.json
  format: json
  label: Coda Pages API
  slug: coda-pages-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/coda/refs/heads/main/openapi/coda-openapi.json
- filename: coda-openapi.json
  format: json
  label: Coda Tables API
  slug: coda-tables-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/coda/refs/heads/main/openapi/coda-openapi.json
- filename: coda-openapi.json
  format: json
  label: Coda Columns API
  slug: coda-columns-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/coda/refs/heads/main/openapi/coda-openapi.json
- filename: coda-openapi.json
  format: json
  label: Coda Rows API
  slug: coda-rows-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/coda/refs/heads/main/openapi/coda-openapi.json
- filename: coda-openapi.json
  format: json
  label: Coda Formulas API
  slug: coda-formulas-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/coda/refs/heads/main/openapi/coda-openapi.json
- filename: coda-openapi.json
  format: json
  label: Coda Controls API
  slug: coda-controls-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/coda/refs/heads/main/openapi/coda-openapi.json
- filename: coda-openapi.json
  format: json
  label: Coda Automations API
  slug: coda-automations-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/coda/refs/heads/main/openapi/coda-openapi.json
- filename: coda-openapi.json
  format: json
  label: Coda Permissions API
  slug: coda-permissions-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/coda/refs/heads/main/openapi/coda-openapi.json
- filename: coda-openapi.json
  format: json
  label: Coda Publishing API
  slug: coda-publishing-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/coda/refs/heads/main/openapi/coda-openapi.json
- filename: coda-openapi.json
  format: json
  label: Coda Account API
  slug: coda-account-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/coda/refs/heads/main/openapi/coda-openapi.json
- filename: coda-openapi.json
  format: json
  label: Coda Analytics API
  slug: coda-analytics-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/coda/refs/heads/main/openapi/coda-openapi.json
- filename: coda-openapi.json
  format: json
  label: Coda Packs SDK
  slug: coda-packs-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/coda/refs/heads/main/openapi/coda-openapi.json
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
description: FinOps framework definition for the Coda API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Coda
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Coda
  PublisherName: Coda
  ServiceCategory: Developer Tools / API
  ServiceName: Coda
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
name: Coda Finops
provider_name: Coda
provider_slug: coda
publisher_name: Coda
service_category: API
slug: coda-finops
source_filename: coda-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Coda\nproviderId: coda\npublisherName: Coda\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Productivity\n  - Docs\n  - No-Code\n  - Collaboration\n  - Database\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Coda API surface. Provides a FOCUS-aligned mapping for\n  cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment,\
  \ application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      -\
  \ FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Coda\n  ServiceCategory: Developer Tools / API\n  ProviderName: Coda\n  PublisherName: Coda\n  InvoiceIssuerName: Coda\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n\
  \      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Coda Docs API\n    baseURL: https://coda.io/apis/v1\n    tags:\n      - Docs\n      - Documents\n    serviceName: Coda Docs API\n    serviceCategory: API\n  - name: Coda Folders API\n    baseURL: https://coda.io/apis/v1\n    tags:\n      - Folders\n      - Workspaces\n    serviceName: Coda Folders API\n    serviceCategory: API\n  - name: Coda Pages API\n    baseURL: https://coda.io/apis/v1\n    tags:\n      - Pages\n      - Content\n    serviceName: Coda Pages API\n    serviceCategory: API\n  - name: Coda Tables API\n    baseURL: https://coda.io/apis/v1\n    tags:\n      - Tables\n      - Database\n    serviceName: Coda Tables API\n    serviceCategory: API\n  - name: Coda Columns API\n    baseURL: https://coda.io/apis/v1\n    tags:\n      - Columns\n\
  \      - Schema\n    serviceName: Coda Columns API\n    serviceCategory: API\n  - name: Coda Rows API\n    baseURL: https://coda.io/apis/v1\n    tags:\n      - Rows\n      - Records\n      - CRUD\n    serviceName: Coda Rows API\n    serviceCategory: API\n  - name: Coda Formulas API\n    baseURL: https://coda.io/apis/v1\n    tags:\n      - Formulas\n      - Compute\n    serviceName: Coda Formulas API\n    serviceCategory: API\n  - name: Coda Controls API\n    baseURL: https://coda.io/apis/v1\n    tags:\n      - Controls\n      - UI\n    serviceName: Coda Controls API\n    serviceCategory: API\n  - name: Coda Automations API\n    baseURL: https://coda.io/apis/v1\n    tags:\n      - Automations\n      - Webhooks\n      - Triggers\n    serviceName: Coda Automations API\n    serviceCategory: API\n  - name: Coda Permissions API\n    baseURL: https://coda.io/apis/v1\n    tags:\n      - Permissions\n      - Sharing\n      - ACL\n    serviceName: Coda Permissions API\n    serviceCategory: API\n\
  \  - name: Coda Publishing API\n    baseURL: https://coda.io/apis/v1\n    tags:\n      - Publishing\n      - Public Docs\n    serviceName: Coda Publishing API\n    serviceCategory: API\n  - name: Coda Account API\n    baseURL: https://coda.io/apis/v1\n    tags:\n      - Account\n      - User\n    serviceName: Coda Account API\n    serviceCategory: API\n  - name: Coda Analytics API\n    baseURL: https://coda.io/apis/v1\n    tags:\n      - Analytics\n      - Usage\n    serviceName: Coda Analytics API\n    serviceCategory: API\n  - name: Coda Packs SDK\n    baseURL: https://coda.io/apis/v1\n    tags:\n      - Packs\n      - Extensions\n      - SDK\n    serviceName: Coda Packs SDK\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/coda/refs/heads/main/finops/coda-finops.yml
sources: []
specification: FinOps Framework
tags:
- Productivity
- Docs
- No-Code
- Collaboration
- Database
- FinOps
- Cost Management
- FOCUS
---
