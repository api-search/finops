---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
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
description: FinOps framework definition for the Epic Games API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Epic Games
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Epic Games
  PublisherName: Epic Games
  ServiceCategory: Developer Tools / API
  ServiceName: Epic Games
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
name: Epic Finops
provider_name: Epic Games
provider_slug: epic
publisher_name: Epic Games
service_category: API
slug: epic-finops
source_filename: epic-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Epic Games\nproviderId: epic\npublisherName: Epic Games\nserviceCategory: API\ncreated: '2026-05-04'\nmodified: '2026-05-04'\ntags:\n  - Game Services\n  - Gaming\n  - Cross-Platform\n  - Achievements\n  - Leaderboards\n  - Matchmaking\n  - Anti-Cheat\n  - OAuth2\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Epic Games API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n \
  \   description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage\
  \ the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Epic Games\n  ServiceCategory: Developer Tools / API\n  ProviderName: Epic Games\n  PublisherName: Epic Games\n  InvoiceIssuerName: Epic Games\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the\
  \ network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Epic Account Services API\n    baseURL: https://api.epicgames.dev\n    tags:\n      - Authentication\n      - OAuth2\n      - Identity\n      - Single Sign-On\n    serviceName: Epic Account Services API\n    serviceCategory: API\n  - name: Epic Online Services Achievements API\n    baseURL: https://api.epicgames.dev\n    tags:\n      - Achievements\n      - Game Services\n      - Progression\n    serviceName: Epic Online Services Achievements API\n    serviceCategory: API\n  - name: Epic Online Services Leaderboards API\n    baseURL: https://api.epicgames.dev\n    tags:\n      - Leaderboards\n      - Game Services\n      - Stats\n    serviceName:\
  \ Epic Online Services Leaderboards API\n    serviceCategory: API\n  - name: Epic Online Services Stats API\n    baseURL: https://api.epicgames.dev\n    tags:\n      - Stats\n      - Game Services\n      - Telemetry\n    serviceName: Epic Online Services Stats API\n    serviceCategory: API\n  - name: Epic Online Services Friends API\n    baseURL: https://api.epicgames.dev\n    tags:\n      - Friends\n      - Social\n      - Game Services\n    serviceName: Epic Online Services Friends API\n    serviceCategory: API\n  - name: Epic Online Services Ecom API\n    baseURL: https://api.epicgames.dev\n    tags:\n      - Ecommerce\n      - Entitlements\n      - Catalog\n      - Epic Games Store\n    serviceName: Epic Online Services Ecom API\n    serviceCategory: API\n  - name: Epic Online Services Lobby and Sessions API\n    baseURL: https://api.epicgames.dev\n    tags:\n      - Matchmaking\n      - Lobbies\n      - Sessions\n      - Multiplayer\n    serviceName: Epic Online Services Lobby and\
  \ Sessions API\n    serviceCategory: API\n  - name: Epic Online Services Player Data Storage API\n    baseURL: https://api.epicgames.dev\n    tags:\n      - Storage\n      - Cloud Saves\n      - Game Services\n    serviceName: Epic Online Services Player Data Storage API\n    serviceCategory: API\n  - name: Epic Online Services Anti-Cheat API\n    baseURL: https://api.epicgames.dev\n    tags:\n      - Anti-Cheat\n      - Security\n      - Multiplayer\n    serviceName: Epic Online Services Anti-Cheat API\n    serviceCategory: API\n  - name: Epic Online Services Voice API\n    baseURL: https://api.epicgames.dev\n    tags:\n      - Voice\n      - Chat\n      - Communications\n      - Vivox\n    serviceName: Epic Online Services Voice API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  -\
  \ FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/epic/refs/heads/main/finops/epic-finops.yml
sources: []
specification: FinOps Framework
tags:
- Game Services
- Gaming
- Cross-Platform
- Achievements
- Leaderboards
- Matchmaking
- Anti-Cheat
- OAuth2
- FinOps
- Cost Management
- FOCUS
---
