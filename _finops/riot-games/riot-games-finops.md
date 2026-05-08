---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: riot-games-league-of-legends-openapi.yml
  format: yaml
  label: League of Legends API
  slug: league-of-legends-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/riot-games/refs/heads/main/openapi/riot-games-league-of-legends-openapi.yml
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
description: FinOps framework definition for the Riot Games API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Riot Games
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Riot Games
  PublisherName: Riot Games
  ServiceCategory: Developer Tools / API
  ServiceName: Riot Games
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
name: Riot Games Finops
provider_name: Riot Games
provider_slug: riot-games
publisher_name: Riot Games
service_category: API
slug: riot-games-finops
source_filename: riot-games-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Riot Games\nproviderId: riot-games\npublisherName: Riot Games\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Esports\n  - Gaming\n  - League of Legends\n  - Legends of Runeterra\n  - Teamfight Tactics\n  - VALORANT\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Riot Games API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description:\
  \ Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n\
  \    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Riot Games\n  ServiceCategory: Developer Tools / API\n  ProviderName: Riot Games\n  PublisherName: Riot Games\n  InvoiceIssuerName: Riot Games\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n\
  \    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: League of Legends API\n    baseURL: https://na1.api.riotgames.com\n    tags:\n      - Champion Mastery\n      - Clash\n      - League of Legends\n      - Match History\n      - Ranked\n      - Summoner\n      - Tournaments\n    serviceName: League of Legends API\n    serviceCategory: API\n  - name: VALORANT API\n    baseURL: https://na.api.riotgames.com\n    tags:\n      - Console\n      - Match History\n      - Ranked\n      - VALORANT\n    serviceName: VALORANT API\n    serviceCategory: API\n  - name: Teamfight Tactics API\n    baseURL: https://na1.api.riotgames.com\n    tags:\n      - Match History\n      - Ranked\n      - Summoner\n      - Teamfight Tactics\n \
  \   serviceName: Teamfight Tactics API\n    serviceCategory: API\n  - name: Legends of Runeterra API\n    baseURL: https://americas.api.riotgames.com\n    tags:\n      - Decks\n      - Legends of Runeterra\n      - Match History\n      - Ranked\n    serviceName: Legends of Runeterra API\n    serviceCategory: API\n  - name: Riot Account API\n    baseURL: https://americas.api.riotgames.com\n    tags:\n      - Account\n      - Authentication\n      - Identity\n      - PUUID\n    serviceName: Riot Account API\n    serviceCategory: API\n  - name: Riot Data Dragon\n    baseURL: https://ddragon.leagueoflegends.com/cdn\n    tags:\n      - Champions\n      - Data Dragon\n      - Items\n      - Static Data\n    serviceName: Riot Data Dragon\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN:\
  \ Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/riot-games/refs/heads/main/finops/riot-games-finops.yml
sources: []
specification: FinOps Framework
tags:
- Esports
- Gaming
- League of Legends
- Legends of Runeterra
- Teamfight Tactics
- VALORANT
- FinOps
- Cost Management
- FOCUS
---
