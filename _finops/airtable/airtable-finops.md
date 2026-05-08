---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: airtable-airtable-api-openapi.yml
  format: yaml
  label: Airtable API
  slug: airtable-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/airtable/refs/heads/main/openapi/airtable-airtable-api-openapi.yml
- filename: airtable-metadata-api-openapi.yml
  format: yaml
  label: Airtable Metadata API
  slug: airtable-metadata-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/airtable/refs/heads/main/openapi/airtable-metadata-api-openapi.yml
- filename: airtable-enterprise-api-openapi.yml
  format: yaml
  label: Airtable Enterprise API
  slug: airtable-enterprise-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/airtable/refs/heads/main/openapi/airtable-enterprise-api-openapi.yml
- filename: airtable-scim-api-openapi.yml
  format: yaml
  label: Airtable SCIM API
  slug: airtable-scim-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/airtable/refs/heads/main/openapi/airtable-scim-api-openapi.yml
- filename: airtable-audit-logs-api-openapi.yml
  format: yaml
  label: Airtable Audit Logs API
  slug: airtable-audit-logs-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/airtable/refs/heads/main/openapi/airtable-audit-logs-api-openapi.yml
- filename: airtable-shares-api-openapi.yml
  format: yaml
  label: Airtable Shares API
  slug: airtable-shares-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/airtable/refs/heads/main/openapi/airtable-shares-api-openapi.yml
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
description: FinOps framework definition for the Airtable API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Airtable
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Airtable
  PublisherName: Airtable
  ServiceCategory: Developer Tools / API
  ServiceName: Airtable
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
name: Airtable Finops
provider_name: Airtable
provider_slug: airtable
publisher_name: Airtable
service_category: API
slug: airtable-finops
source_filename: airtable-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Airtable\nproviderId: airtable\npublisherName: Airtable\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Applications\n  - Collaboration\n  - Data\n  - Databases\n  - Low-Code\n  - Productivity\n  - Spreadsheets\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Airtable API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every\
  \ chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n   \
  \ capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Airtable\n  ServiceCategory: Developer Tools / API\n  ProviderName: Airtable\n  PublisherName: Airtable\n  InvoiceIssuerName: Airtable\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit:\
  \ GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Airtable API\n    baseURL: https://api.airtable.com\n    tags:\n      - Bases\n      - Collaborators\n      - Comments\n      - Fields\n      - Records\n      - Tables\n      - Views\n      - Webhooks\n    serviceName: Airtable API\n    serviceCategory: API\n  - name: Airtable Metadata API\n    baseURL: https://api.airtable.com/v0/meta\n    tags:\n      - Bases\n      - Fields\n      - Metadata\n      - Schema\n      - Tables\n    serviceName: Airtable Metadata API\n    serviceCategory: API\n  - name: Airtable Enterprise API\n    baseURL: https://api.airtable.com/v0\n    tags:\n      - Admin\n      - Audit\n      - Enterprise\n      - Groups\n      - Users\n    serviceName:\
  \ Airtable Enterprise API\n    serviceCategory: API\n  - name: Airtable SCIM API\n    baseURL: https://airtable.com/scim/v2\n    tags:\n      - Groups\n      - Identity\n      - Provisioning\n      - SCIM\n      - Users\n    serviceName: Airtable SCIM API\n    serviceCategory: API\n  - name: Airtable Audit Logs API\n    baseURL: https://api.airtable.com/v0\n    tags:\n      - Audit\n      - Compliance\n      - Enterprise\n      - Logs\n      - Security\n    serviceName: Airtable Audit Logs API\n    serviceCategory: API\n  - name: Airtable Shares API\n    baseURL: https://api.airtable.com/v0\n    tags:\n      - Access\n      - Collaboration\n      - Enterprise\n      - Shares\n    serviceName: Airtable Shares API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    url:\
  \ http://apievangelist.com\n    email: kin@apievangelist.com\n  - FN: Airtable\n    email: support@airtable.com\n    url: https://airtable.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/airtable/refs/heads/main/finops/airtable-finops.yml
sources: []
specification: FinOps Framework
tags:
- Applications
- Collaboration
- Data
- Databases
- Low-Code
- Productivity
- Spreadsheets
- FinOps
- Cost Management
- FOCUS
---
