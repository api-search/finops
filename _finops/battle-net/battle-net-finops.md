---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: battle-net-hearthstone-game-data.yaml
  format: yaml
  label: Hearthstone Game Data API
  slug: hearthstone-game-data
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/battle-net/refs/heads/main/openapi/battle-net-hearthstone-game-data.yaml
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
description: FinOps framework definition for the Battle.net API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Battle.net
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Battle.net
  PublisherName: Battle.net
  ServiceCategory: Developer Tools / API
  ServiceName: Battle.net
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
name: Battle Net Finops
provider_name: Battle.net
provider_slug: battle-net
publisher_name: Battle.net
service_category: API
slug: battle-net-finops
source_filename: battle-net-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Battle.net\nproviderId: battle-net\npublisherName: Battle.net\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Games\n  - Gaming\n  - Blizzard\n  - World Of Warcraft\n  - Diablo\n  - Hearthstone\n  - Starcraft\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Battle.net API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every\
  \ chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n   \
  \ capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Battle.net\n  ServiceCategory: Developer Tools / API\n  ProviderName: Battle.net\n  PublisherName: Battle.net\n  InvoiceIssuerName: Battle.net\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n\
  \    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: World of Warcraft Game Data API\n    baseURL: ''\n    tags:\n      - Games\n      - Gaming\n      - World Of Warcraft\n    serviceName: World of Warcraft Game Data API\n    serviceCategory: API\n  - name: World of Warcraft Profile API\n    baseURL: ''\n    tags:\n      - Games\n      - Gaming\n      - World Of Warcraft\n      - Player Profile\n    serviceName: World of Warcraft Profile API\n    serviceCategory: API\n  - name: World of Warcraft Classic Game Data API\n    baseURL: ''\n    tags:\n      - Games\n      - Gaming\n      - World Of Warcraft Classic\n    serviceName: World of Warcraft Classic Game Data API\n    serviceCategory: API\n  - name: Diablo III Game\
  \ Data API\n    baseURL: ''\n    tags:\n      - Games\n      - Gaming\n      - Diablo\n    serviceName: Diablo III Game Data API\n    serviceCategory: API\n  - name: Diablo III Community API\n    baseURL: ''\n    tags:\n      - Games\n      - Gaming\n      - Diablo\n    serviceName: Diablo III Community API\n    serviceCategory: API\n  - name: Hearthstone Game Data API\n    baseURL: ''\n    tags:\n      - Games\n      - Gaming\n      - Hearthstone\n    serviceName: Hearthstone Game Data API\n    serviceCategory: API\n  - name: StarCraft II Game Data API\n    baseURL: ''\n    tags:\n      - Games\n      - Gaming\n      - Starcraft\n    serviceName: StarCraft II Game Data API\n    serviceCategory: API\n  - name: StarCraft II Community API\n    baseURL: ''\n    tags:\n      - Games\n      - Gaming\n      - Starcraft\n    serviceName: StarCraft II Community API\n    serviceCategory: API\n  - name: Battle.net OAuth API\n    baseURL: ''\n    tags:\n      - Authentication\n      - Gaming\n  \
  \    - OAuth\n    serviceName: Battle.net OAuth API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/battle-net/refs/heads/main/finops/battle-net-finops.yml
sources: []
specification: FinOps Framework
tags:
- Games
- Gaming
- Blizzard
- World Of Warcraft
- Diablo
- Hearthstone
- Starcraft
- FinOps
- Cost Management
- FOCUS
---
