---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: shell-b2b-mobility-openapi.yml
  format: yaml
  label: Shell B2B Mobility Card Management API
  slug: b2b-mobility-card-management
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/shell/refs/heads/main/openapi/shell-b2b-mobility-openapi.yml
- filename: shell-b2b-mobility-openapi.yml
  format: yaml
  label: Shell B2B Mobility Card Transaction Data API
  slug: b2b-mobility-card-transaction-data
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/shell/refs/heads/main/openapi/shell-b2b-mobility-openapi.yml
- filename: shell-b2b-mobility-openapi.yml
  format: yaml
  label: Shell B2B Mobility Invoice API
  slug: b2b-mobility-invoice
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/shell/refs/heads/main/openapi/shell-b2b-mobility-openapi.yml
- filename: shell-loyalty-openapi.yml
  format: yaml
  label: Shell Loyalty Catalogue API
  slug: loyalty-catalogue
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/shell/refs/heads/main/openapi/shell-loyalty-openapi.yml
- filename: shell-loyalty-openapi.yml
  format: yaml
  label: Shell Loyalty Account Management API
  slug: loyalty-account-management
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/shell/refs/heads/main/openapi/shell-loyalty-openapi.yml
- filename: shell-loyalty-openapi.yml
  format: yaml
  label: Shell Loyalty Points Balance API
  slug: loyalty-points-balance
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/shell/refs/heads/main/openapi/shell-loyalty-openapi.yml
- filename: shell-loyalty-openapi.yml
  format: yaml
  label: Shell Loyalty Points Redemption API
  slug: loyalty-points-redemption
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/shell/refs/heads/main/openapi/shell-loyalty-openapi.yml
- filename: shell-lubricants-openapi.yml
  format: yaml
  label: Shell Lubricants Order Management API
  slug: lubricants-order-management
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/shell/refs/heads/main/openapi/shell-lubricants-openapi.yml
- filename: shell-b2b-mobility-openapi.yml
  format: yaml
  label: Shell B2B Mobility Sites API
  slug: b2b-mobility-sites
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/shell/refs/heads/main/openapi/shell-b2b-mobility-openapi.yml
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
description: FinOps framework definition for the Shell API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Shell
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Shell
  PublisherName: Shell
  ServiceCategory: Developer Tools / API
  ServiceName: Shell
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
name: Shell Finops
provider_name: Shell
provider_slug: shell
publisher_name: Shell
service_category: API
slug: shell-finops
source_filename: shell-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Shell\nproviderId: shell\npublisherName: Shell\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Aviation\n  - Electric Vehicle Charging\n  - Energy\n  - Fleet Management\n  - Fuel\n  - Gas\n  - Loyalty\n  - Lubricants\n  - Mobility\n  - Oil and Gas\n  - Renewable Energy\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Shell API surface. Provides a FOCUS-aligned mapping for\n  cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n\
  \  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and\
  \ SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Shell\n  ServiceCategory: Developer Tools / API\n  ProviderName: Shell\n  PublisherName: Shell\n  InvoiceIssuerName: Shell\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over\
  \ the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Shell B2B Mobility Card Management API\n    baseURL: ''\n    tags:\n      - B2B\n      - Cards\n      - Fleet\n      - Mobility\n    serviceName: Shell B2B Mobility Card Management API\n    serviceCategory: API\n  - name: Shell B2B Mobility Card Transaction Data API\n    baseURL: ''\n    tags:\n      - B2B\n      - Fleet\n      - Mobility\n      - Transactions\n    serviceName: Shell B2B Mobility Card Transaction Data API\n    serviceCategory: API\n  - name: Shell B2B Mobility Invoice API\n    baseURL: ''\n    tags:\n      - B2B\n      - Finance\n      - Fleet\n      - Invoices\n    serviceName: Shell B2B Mobility Invoice API\n    serviceCategory:\
  \ API\n  - name: Shell Loyalty Catalogue API\n    baseURL: ''\n    tags:\n      - Loyalty\n      - Rewards\n      - Retail\n    serviceName: Shell Loyalty Catalogue API\n    serviceCategory: API\n  - name: Shell Loyalty Account Management API\n    baseURL: ''\n    tags:\n      - Loyalty\n      - Rewards\n      - Accounts\n    serviceName: Shell Loyalty Account Management API\n    serviceCategory: API\n  - name: Shell Loyalty Points Balance API\n    baseURL: ''\n    tags:\n      - Loyalty\n      - Points\n      - Rewards\n    serviceName: Shell Loyalty Points Balance API\n    serviceCategory: API\n  - name: Shell Loyalty Points Redemption API\n    baseURL: ''\n    tags:\n      - Loyalty\n      - Points\n      - Redemption\n    serviceName: Shell Loyalty Points Redemption API\n    serviceCategory: API\n  - name: Shell Lubricants Order Management API\n    baseURL: ''\n    tags:\n      - Lubricants\n      - Oil\n      - Orders\n      - B2B\n    serviceName: Shell Lubricants Order Management\
  \ API\n    serviceCategory: API\n  - name: Shell Aviation Fuel Reseller API\n    baseURL: ''\n    tags:\n      - Aviation\n      - Fuel\n      - B2B\n    serviceName: Shell Aviation Fuel Reseller API\n    serviceCategory: API\n  - name: Shell B2B Mobility Sites API\n    baseURL: ''\n    tags:\n      - B2B\n      - Fleet\n      - Locations\n      - Mobility\n    serviceName: Shell B2B Mobility Sites API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n  - FN: Shell Digital Services\n    email: api-maintainers@shell.com\n    X-twitter: shell\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/shell/refs/heads/main/finops/shell-finops.yml
sources: []
specification: FinOps Framework
tags:
- Aviation
- Electric Vehicle Charging
- Energy
- Fleet Management
- Fuel
- Gas
- Loyalty
- Lubricants
- Mobility
- Oil and Gas
- Renewable Energy
- FinOps
- Cost Management
- FOCUS
---
