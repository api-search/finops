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
description: FinOps framework definition for the Steam API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Steam
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Steam
  PublisherName: Steam
  ServiceCategory: Developer Tools / API
  ServiceName: Steam
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
name: Steam Finops
provider_name: Steam
provider_slug: steam
publisher_name: Steam
service_category: API
slug: steam-finops
source_filename: steam-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Steam\nproviderId: steam\npublisherName: Steam\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Gaming\n  - Valve\n  - Distribution\n  - Steamworks\n  - Marketplace\n  - Web API\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Steam API surface. Provides a FOCUS-aligned mapping for\n  cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming\
  \ team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice\
  \ Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Steam\n  ServiceCategory: Developer Tools / API\n  ProviderName: Steam\n  PublisherName: Steam\n  InvoiceIssuerName: Steam\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n  \
  \    - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: ISteamNews\n    baseURL: ''\n    tags:\n      - News\n      - Feeds\n      - Public\n    serviceName: ISteamNews\n    serviceCategory: API\n  - name: ISteamUserStats\n    baseURL: ''\n    tags:\n      - Stats\n      - Achievements\n      - Global Stats\n      - Schema\n    serviceName: ISteamUserStats\n    serviceCategory: API\n  - name: ISteamUser\n    baseURL: ''\n    tags:\n      - Users\n      - Profiles\n      - Friends\n      - Bans\n    serviceName: ISteamUser\n    serviceCategory: API\n  - name: ISteamUserAuth\n    baseURL: ''\n    tags:\n      - Authentication\n      - Sessions\n      - Tickets\n    serviceName: ISteamUserAuth\n    serviceCategory: API\n  - name: ISteamApps\n    baseURL: ''\n    tags:\n      -\
  \ Apps\n      - Catalog\n      - Servers\n    serviceName: ISteamApps\n    serviceCategory: API\n  - name: ISteamCommunity\n    baseURL: ''\n    tags:\n      - Community\n      - Reports\n    serviceName: ISteamCommunity\n    serviceCategory: API\n  - name: ISteamEconomy\n    baseURL: ''\n    tags:\n      - Economy\n      - Trades\n      - Asset Class\n    serviceName: ISteamEconomy\n    serviceCategory: API\n  - name: IGameInventory\n    baseURL: ''\n    tags:\n      - Inventory\n      - Items\n      - Economy\n    serviceName: IGameInventory\n    serviceCategory: API\n  - name: IInventoryService\n    baseURL: ''\n    tags:\n      - Inventory\n      - Items\n      - Service\n    serviceName: IInventoryService\n    serviceCategory: API\n  - name: ISteamGameServer\n    baseURL: ''\n    tags:\n      - Game Servers\n      - Sessions\n      - Login Tokens\n    serviceName: ISteamGameServer\n    serviceCategory: API\n  - name: ISteamRemoteStorage\n    baseURL: ''\n    tags:\n      - Remote\
  \ Storage\n      - Cloud Saves\n      - UGC\n    serviceName: ISteamRemoteStorage\n    serviceCategory: API\n  - name: ISteamLeaderboards\n    baseURL: ''\n    tags:\n      - Leaderboards\n      - Scores\n    serviceName: ISteamLeaderboards\n    serviceCategory: API\n  - name: IPlayerService\n    baseURL: ''\n    tags:\n      - Players\n      - Owned Games\n      - Recently Played\n      - Badges\n    serviceName: IPlayerService\n    serviceCategory: API\n  - name: IGameNotificationsService\n    baseURL: ''\n    tags:\n      - Notifications\n      - In-Game\n    serviceName: IGameNotificationsService\n    serviceCategory: API\n  - name: ISteamWebAPIUtil\n    baseURL: ''\n    tags:\n      - Utility\n      - Server Info\n      - Schema\n    serviceName: ISteamWebAPIUtil\n    serviceCategory: API\n  - name: IPublishedFileService\n    baseURL: ''\n    tags:\n      - Workshop\n      - UGC\n      - Published Files\n    serviceName: IPublishedFileService\n    serviceCategory: API\n  - name: IBroadcastService\n\
  \    baseURL: ''\n    tags:\n      - Broadcast\n      - Streaming\n      - Game Live\n    serviceName: IBroadcastService\n    serviceCategory: API\n  - name: Steam Store API\n    baseURL: ''\n    tags:\n      - Store\n      - Pricing\n      - App Details\n    serviceName: Steam Store API\n    serviceCategory: API\n  - name: ISteamCheckout\n    baseURL: ''\n    tags:\n      - Checkout\n      - In-Game Purchases\n      - Microtransactions\n    serviceName: ISteamCheckout\n    serviceCategory: API\n  - name: ISteamMicroTxn\n    baseURL: ''\n    tags:\n      - Microtransactions\n      - Payments\n      - Refunds\n    serviceName: ISteamMicroTxn\n    serviceCategory: API\n  - name: ISteamDeepLinkService\n    baseURL: ''\n    tags:\n      - Deep Links\n      - Marketing\n    serviceName: ISteamDeepLinkService\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric:\
  \ billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/steam/refs/heads/main/finops/steam-finops.yml
sources: []
specification: FinOps Framework
tags:
- Gaming
- Valve
- Distribution
- Steamworks
- Marketplace
- Web API
- FinOps
- Cost Management
- FOCUS
---
