---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: betsolutions-wallet-api.yaml
  format: yaml
  label: BetSolutions Wallet API
  slug: wallet-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/betsolutions/refs/heads/main/openapi/betsolutions-wallet-api.yaml
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
description: FinOps framework definition for the BetSolutions API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: BetSolutions
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: BetSolutions
  PublisherName: BetSolutions
  ServiceCategory: Developer Tools / API
  ServiceName: BetSolutions
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
name: Betsolutions Finops
provider_name: BetSolutions
provider_slug: betsolutions
publisher_name: BetSolutions
service_category: API
slug: betsolutions-finops
source_filename: betsolutions-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: BetSolutions\nproviderId: betsolutions\npublisherName: BetSolutions\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Betting\n  - Casinos\n  - Gaming\n  - Gambling\n  - Slots\n  - Sports Betting\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the BetSolutions API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable\
  \ API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n\
  \      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: BetSolutions\n  ServiceCategory: Developer Tools / API\n  ProviderName: BetSolutions\n  PublisherName: BetSolutions\n  InvoiceIssuerName: BetSolutions\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit:\
  \ GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: BetSolutions Wallet API\n    baseURL: ''\n    tags:\n      - Wallet\n      - Payments\n      - Transfer\n      - Seamless\n    serviceName: BetSolutions Wallet API\n    serviceCategory: API\n  - name: BetSolutions Player API\n    baseURL: ''\n    tags:\n      - Players\n      - Accounts\n      - Information\n    serviceName: BetSolutions Player API\n    serviceCategory: API\n  - name: BetSolutions Slots API\n    baseURL: ''\n    tags:\n      - Slots\n      - Campaigns\n      - Freespins\n      - Gaming\n    serviceName: BetSolutions Slots API\n    serviceCategory: API\n  - name: BetSolutions Table Games API\n    baseURL: ''\n    tags:\n      - Table Games\n      - Multiplayer\n\
  \      - Tournaments\n      - Gaming\n    serviceName: BetSolutions Table Games API\n    serviceCategory: API\n  - name: BetSolutions Provably Fair Games API\n    baseURL: ''\n    tags:\n      - Provably Fair\n      - Zeppelin\n      - Gaming\n    serviceName: BetSolutions Provably Fair Games API\n    serviceCategory: API\n  - name: BetSolutions Third-Party Integration API\n    baseURL: ''\n    tags:\n      - Sportsbook\n      - BCBetting\n      - Integration\n    serviceName: BetSolutions Third-Party Integration API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/betsolutions/refs/heads/main/finops/betsolutions-finops.yml
sources: []
specification: FinOps Framework
tags:
- Betting
- Casinos
- Gaming
- Gambling
- Slots
- Sports Betting
- FinOps
- Cost Management
- FOCUS
---
