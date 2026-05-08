---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: deel-platform-endpoints-openapi.json
  format: json
  label: Deel People API
  slug: deel-people-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/deel/refs/heads/main/openapi/deel-platform-endpoints-openapi.json
- filename: deel-platform-endpoints-openapi.json
  format: json
  label: Deel Organizations API
  slug: deel-organizations-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/deel/refs/heads/main/openapi/deel-platform-endpoints-openapi.json
- filename: deel-platform-endpoints-openapi.json
  format: json
  label: Deel Contracts API
  slug: deel-contracts-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/deel/refs/heads/main/openapi/deel-platform-endpoints-openapi.json
- filename: deel-platform-endpoints-openapi.json
  format: json
  label: Deel Time Off API
  slug: deel-time-off-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/deel/refs/heads/main/openapi/deel-platform-endpoints-openapi.json
- filename: deel-platform-endpoints-openapi.json
  format: json
  label: Deel Time Tracking API
  slug: deel-time-tracking-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/deel/refs/heads/main/openapi/deel-platform-endpoints-openapi.json
- filename: deel-platform-endpoints-openapi.json
  format: json
  label: Deel Payroll API
  slug: deel-payroll-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/deel/refs/heads/main/openapi/deel-platform-endpoints-openapi.json
- filename: deel-platform-endpoints-openapi.json
  format: json
  label: Deel Invoices API
  slug: deel-invoices-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/deel/refs/heads/main/openapi/deel-platform-endpoints-openapi.json
- filename: deel-platform-endpoints-openapi.json
  format: json
  label: Deel Expenses API
  slug: deel-expenses-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/deel/refs/heads/main/openapi/deel-platform-endpoints-openapi.json
- filename: deel-platform-endpoints-openapi.json
  format: json
  label: Deel EOR API
  slug: deel-eor-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/deel/refs/heads/main/openapi/deel-platform-endpoints-openapi.json
- filename: deel-platform-endpoints-openapi.json
  format: json
  label: Deel Background Checks API
  slug: deel-background-checks-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/deel/refs/heads/main/openapi/deel-platform-endpoints-openapi.json
- filename: deel-platform-endpoints-openapi.json
  format: json
  label: Deel Immigration API
  slug: deel-immigration-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/deel/refs/heads/main/openapi/deel-platform-endpoints-openapi.json
- filename: deel-platform-endpoints-openapi.json
  format: json
  label: Deel IT API
  slug: deel-it-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/deel/refs/heads/main/openapi/deel-platform-endpoints-openapi.json
- filename: deel-platform-endpoints-openapi.json
  format: json
  label: Deel SCIM API
  slug: deel-scim-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/deel/refs/heads/main/openapi/deel-platform-endpoints-openapi.json
- filename: deel-platform-endpoints-openapi.json
  format: json
  label: Deel ATS API
  slug: deel-ats-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/deel/refs/heads/main/openapi/deel-platform-endpoints-openapi.json
- filename: deel-platform-endpoints-openapi.json
  format: json
  label: Deel Accounting API
  slug: deel-accounting-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/deel/refs/heads/main/openapi/deel-platform-endpoints-openapi.json
- filename: deel-platform-endpoints-openapi.json
  format: json
  label: Deel Lookups API
  slug: deel-lookups-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/deel/refs/heads/main/openapi/deel-platform-endpoints-openapi.json
- filename: deel-platform-endpoints-openapi.json
  format: json
  label: Deel Webhooks API
  slug: deel-webhooks-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/deel/refs/heads/main/openapi/deel-platform-endpoints-openapi.json
- filename: deel-platform-endpoints-openapi.json
  format: json
  label: Deel OAuth & Apps API
  slug: deel-oauth-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/deel/refs/heads/main/openapi/deel-platform-endpoints-openapi.json
- filename: deel-platform-endpoints-openapi.json
  format: json
  label: Deel MCP Server
  slug: deel-mcp-server
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/deel/refs/heads/main/openapi/deel-platform-endpoints-openapi.json
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
description: FinOps framework definition for the Deel API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Deel
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Deel
  PublisherName: Deel
  ServiceCategory: Developer Tools / API
  ServiceName: Deel
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
name: Deel Finops
provider_name: Deel
provider_slug: deel
publisher_name: Deel
service_category: API
slug: deel-finops
source_filename: deel-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Deel\nproviderId: deel\npublisherName: Deel\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - HR\n  - Payroll\n  - Global Hiring\n  - EOR\n  - Contractors\n  - Compliance\n  - SCIM\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Deel API surface. Provides a FOCUS-aligned mapping for\n  cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming\
  \ team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice\
  \ Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Deel\n  ServiceCategory: Developer Tools / API\n  ProviderName: Deel\n  PublisherName: Deel\n  InvoiceIssuerName: Deel\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      -\
  \ api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Deel People API\n    baseURL: ''\n    tags:\n      - People\n      - Workers\n      - Employees\n    serviceName: Deel People API\n    serviceCategory: API\n  - name: Deel Organizations API\n    baseURL: ''\n    tags:\n      - Organizations\n      - Teams\n      - Departments\n      - Locations\n    serviceName: Deel Organizations API\n    serviceCategory: API\n  - name: Deel Contracts API\n    baseURL: ''\n    tags:\n      - Contracts\n      - Agreements\n      - Documents\n    serviceName: Deel Contracts API\n    serviceCategory: API\n  - name: Deel Time Off API\n    baseURL: ''\n    tags:\n      - Time Off\n      - Leave\n      - PTO\n      - Holidays\n    serviceName: Deel Time Off API\n    serviceCategory: API\n  - name:\
  \ Deel Time Tracking API\n    baseURL: ''\n    tags:\n      - Time Tracking\n      - Timesheets\n      - Shifts\n    serviceName: Deel Time Tracking API\n    serviceCategory: API\n  - name: Deel Payroll API\n    baseURL: ''\n    tags:\n      - Payroll\n      - Payslips\n      - Adjustments\n    serviceName: Deel Payroll API\n    serviceCategory: API\n  - name: Deel Invoices API\n    baseURL: ''\n    tags:\n      - Invoices\n      - Adjustments\n      - Milestones\n      - Tasks\n    serviceName: Deel Invoices API\n    serviceCategory: API\n  - name: Deel Expenses API\n    baseURL: ''\n    tags:\n      - Expenses\n      - Reimbursements\n    serviceName: Deel Expenses API\n    serviceCategory: API\n  - name: Deel EOR API\n    baseURL: ''\n    tags:\n      - EOR\n      - Global Hiring\n      - Benefits\n      - Onboarding\n    serviceName: Deel EOR API\n    serviceCategory: API\n  - name: Deel Background Checks API\n    baseURL: ''\n    tags:\n      - Background Checks\n      - KYC\n   \
  \   - Verification\n    serviceName: Deel Background Checks API\n    serviceCategory: API\n  - name: Deel Immigration API\n    baseURL: ''\n    tags:\n      - Immigration\n      - Mobility\n      - Visas\n    serviceName: Deel Immigration API\n    serviceCategory: API\n  - name: Deel IT API\n    baseURL: ''\n    tags:\n      - IT\n      - Devices\n      - Equipment\n      - MDM\n    serviceName: Deel IT API\n    serviceCategory: API\n  - name: Deel SCIM API\n    baseURL: ''\n    tags:\n      - SCIM\n      - Identity\n      - Provisioning\n    serviceName: Deel SCIM API\n    serviceCategory: API\n  - name: Deel ATS API\n    baseURL: ''\n    tags:\n      - ATS\n      - Recruiting\n      - Candidates\n    serviceName: Deel ATS API\n    serviceCategory: API\n  - name: Deel Accounting API\n    baseURL: ''\n    tags:\n      - Accounting\n      - GL\n      - Invoices\n    serviceName: Deel Accounting API\n    serviceCategory: API\n  - name: Deel Lookups API\n    baseURL: ''\n    tags:\n     \
  \ - Lookups\n      - Reference Data\n      - Countries\n      - Currencies\n    serviceName: Deel Lookups API\n    serviceCategory: API\n  - name: Deel Webhooks API\n    baseURL: ''\n    tags:\n      - Webhooks\n      - Events\n    serviceName: Deel Webhooks API\n    serviceCategory: API\n  - name: Deel OAuth & Apps API\n    baseURL: ''\n    tags:\n      - OAuth\n      - Apps\n      - Marketplace\n    serviceName: Deel OAuth & Apps API\n    serviceCategory: API\n  - name: Deel MCP Server\n    baseURL: ''\n    tags:\n      - MCP\n      - AI Agents\n    serviceName: Deel MCP Server\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/deel/refs/heads/main/finops/deel-finops.yml
sources: []
specification: FinOps Framework
tags:
- HR
- Payroll
- Global Hiring
- EOR
- Contractors
- Compliance
- SCIM
- FinOps
- Cost Management
- FOCUS
---
