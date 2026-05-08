---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: wise-platform-openapi.yml
  format: yaml
  label: Wise Profiles API
  slug: profiles
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/wise/refs/heads/main/openapi/wise-platform-openapi.yml
- filename: wise-platform-openapi.yml
  format: yaml
  label: Wise Recipients API
  slug: recipients
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/wise/refs/heads/main/openapi/wise-platform-openapi.yml
- filename: wise-platform-openapi.yml
  format: yaml
  label: Wise Quotes API
  slug: quotes
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/wise/refs/heads/main/openapi/wise-platform-openapi.yml
- filename: wise-platform-openapi.yml
  format: yaml
  label: Wise Transfers API
  slug: transfers
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/wise/refs/heads/main/openapi/wise-platform-openapi.yml
- filename: wise-platform-openapi.yml
  format: yaml
  label: Wise Balances API
  slug: balances
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/wise/refs/heads/main/openapi/wise-platform-openapi.yml
- filename: wise-platform-openapi.yml
  format: yaml
  label: Wise Multi-Currency Account API
  slug: multi-currency-account
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/wise/refs/heads/main/openapi/wise-platform-openapi.yml
- filename: wise-platform-openapi.yml
  format: yaml
  label: Wise Statements API
  slug: statements
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/wise/refs/heads/main/openapi/wise-platform-openapi.yml
- filename: wise-platform-openapi.yml
  format: yaml
  label: Wise Cards API
  slug: cards
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/wise/refs/heads/main/openapi/wise-platform-openapi.yml
- filename: wise-platform-openapi.yml
  format: yaml
  label: Wise Webhooks API
  slug: webhooks
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/wise/refs/heads/main/openapi/wise-platform-openapi.yml
- filename: wise-platform-openapi.yml
  format: yaml
  label: Wise Simulation API
  slug: simulation
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/wise/refs/heads/main/openapi/wise-platform-openapi.yml
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
description: FinOps framework definition for the Wise API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Wise
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Wise
  PublisherName: Wise
  ServiceCategory: Developer Tools / API
  ServiceName: Wise
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
name: Wise Finops
provider_name: Wise
provider_slug: wise
publisher_name: Wise
service_category: API
slug: wise-finops
source_filename: wise-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Wise\nproviderId: wise\npublisherName: Wise\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Payments\n  - FX\n  - Cross-Border\n  - Banking\n  - Multi-Currency\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Wise API surface. Provides a FOCUS-aligned mapping for\n  cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment,\
  \ application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      -\
  \ FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Wise\n  ServiceCategory: Developer Tools / API\n  ProviderName: Wise\n  PublisherName: Wise\n  InvoiceIssuerName: Wise\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n\
  \      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Wise Profiles API\n    baseURL: https://api.wise.com/v2\n    tags:\n      - Profiles\n      - Identity\n      - KYC\n    serviceName: Wise Profiles API\n    serviceCategory: API\n  - name: Wise Recipients API\n    baseURL: https://api.wise.com/v1\n    tags:\n      - Recipients\n      - Beneficiaries\n      - Bank Accounts\n    serviceName: Wise Recipients API\n    serviceCategory: API\n  - name: Wise Quotes API\n    baseURL: https://api.wise.com/v3\n    tags:\n      - Quotes\n      - FX\n      - Pricing\n    serviceName: Wise Quotes API\n    serviceCategory: API\n  - name: Wise Transfers API\n    baseURL: https://api.wise.com/v1\n    tags:\n      - Transfers\n      - Payments\n      - Cross-Border\n    serviceName: Wise Transfers API\n    serviceCategory:\
  \ API\n  - name: Wise Balances API\n    baseURL: https://api.wise.com/v4\n    tags:\n      - Balances\n      - Multi-Currency\n      - Wallets\n    serviceName: Wise Balances API\n    serviceCategory: API\n  - name: Wise Multi-Currency Account API\n    baseURL: https://api.wise.com/v1\n    tags:\n      - Multi-Currency Account\n      - Receive Money\n      - Local Bank Details\n    serviceName: Wise Multi-Currency Account API\n    serviceCategory: API\n  - name: Wise Statements API\n    baseURL: https://api.wise.com/v1\n    tags:\n      - Statements\n      - Reporting\n      - Accounting\n    serviceName: Wise Statements API\n    serviceCategory: API\n  - name: Wise Cards API\n    baseURL: https://api.wise.com/v3\n    tags:\n      - Cards\n      - Issuing\n      - Spending Controls\n    serviceName: Wise Cards API\n    serviceCategory: API\n  - name: Wise Webhooks API\n    baseURL: https://api.wise.com/v3\n    tags:\n      - Webhooks\n      - Events\n      - Notifications\n    serviceName:\
  \ Wise Webhooks API\n    serviceCategory: API\n  - name: Wise Simulation API\n    baseURL: https://api.sandbox.transferwise.tech\n    tags:\n      - Simulation\n      - Sandbox\n      - Testing\n    serviceName: Wise Simulation API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/wise/refs/heads/main/finops/wise-finops.yml
sources: []
specification: FinOps Framework
tags:
- Payments
- FX
- Cross-Border
- Banking
- Multi-Currency
- FinOps
- Cost Management
- FOCUS
---
