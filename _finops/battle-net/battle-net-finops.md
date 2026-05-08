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
  billingFrequency: Not Billed
  chargeCategories:
  - Usage
  chargeFrequency: One-Time
  pricingCategory: No Direct Charge
description: 'FOCUS-aligned FinOps for the Battle.net Developer APIs: zero direct cost (free, rate-limited developer access), so FinOps focuses on attribution, rate-limit utilization, and partner-access decisions rather than billed spend.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Blizzard Entertainment, Inc.
  PricingCategory: No Direct Charge
  PricingUnit: request
  ProviderName: Battle.net
  PublisherName: Blizzard Entertainment, Inc.
  ServiceCategory: Gaming / Developer APIs
  ServiceName: Battle.net Developer APIs
layout: finops
meters:
- aggregation: sum
  description: Count of API requests per OAuth Client ID; for utilization tracking against the free-tier ceilings, not for billing
  dimensions:
  - oauth_client_id
  - region
  - game
  - endpoint
  name: api_requests
  unit: request
- aggregation: max
  description: Percent of per-second / per-hour ceiling consumed; used to forecast when partner access becomes necessary
  dimensions:
  - oauth_client_id
  - window
  name: rate_limit_utilization
  unit: percent
- aggregation: count
  description: Cached responses that did not consume Blizzard quota
  dimensions:
  - oauth_client_id
  - endpoint
  name: cache_hits
  unit: request
name: Battle Net Finops
provider_name: Battle.net
provider_slug: battle-net
publisher_name: Blizzard Entertainment, Inc.
service_category: Gaming / Developer APIs
slug: battle-net-finops
source_filename: battle-net-finops.yml
source_heading: FinOps Profile
source_url: https://develop.battle.net/access/clients
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Battle.net\nproviderId: battle-net\npublisherName: Blizzard Entertainment, Inc.\nserviceCategory: Gaming / Developer APIs\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - Games\n  - Gaming\n  - Blizzard\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps for the Battle.net Developer APIs: zero direct cost (free, rate-limited\n  developer access), so FinOps focuses on attribution, rate-limit utilization, and partner-access decisions\n  rather than billed spend.'\nsources:\n  - https://develop.battle.net/access/clients\n  - https://community.developer.battle.net/documentation\nprinciples:\n  - name: Visibility\n    description: Track requests per OAuth Client\
  \ ID against the 100 req/s and 36,000 req/hr ceilings using\n      your own observability stack — Blizzard does not expose a usage API.\n  - name: Allocation\n    description: Issue a separate OAuth Client ID per consuming application or team to attribute usage\n      and avoid one team starving another against the shared per-client ceiling.\n  - name: Optimization\n    description: Cache static game-data responses (realms, classes, items) aggressively. The hourly ceiling\n      is the binding constraint; cached responses do not consume quota.\n  - name: Accountability\n    description: Designate an owner of the partner relationship with Blizzard Developer Relations who\n      can request elevated limits when an application's growth justifies it.\nbillingModel:\n  pricingCategory: No Direct Charge\n  billingFrequency: Not Billed\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n  chargeFrequency: One-Time\nfocusColumns:\n  ServiceName: Battle.net Developer APIs\n  ServiceCategory:\
  \ Gaming / Developer APIs\n  ProviderName: Battle.net\n  PublisherName: Blizzard Entertainment, Inc.\n  InvoiceIssuerName: Blizzard Entertainment, Inc.\n  PricingCategory: No Direct Charge\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of API requests per OAuth Client ID; for utilization tracking against the free-tier\n      ceilings, not for billing\n    unit: request\n    aggregation: sum\n    dimensions:\n      - oauth_client_id\n      - region\n      - game\n      - endpoint\n  - name: rate_limit_utilization\n    description: Percent of per-second / per-hour ceiling consumed; used to forecast when partner access\n      becomes necessary\n    unit: percent\n    aggregation: max\n    dimensions:\n      - oauth_client_id\n      - window\n  - name: cache_hits\n    description: Cached responses that did not consume Blizzard quota\n    unit: request\n    aggregation: count\n    dimensions:\n      - oauth_client_id\n\
  \      - endpoint\napis:\n  - name: World of Warcraft Game Data API\n    baseURL: https://us.api.blizzard.com\n    serviceName: World of Warcraft Game Data API\n    serviceCategory: API\n  - name: World of Warcraft Profile API\n    baseURL: https://us.api.blizzard.com\n    serviceName: World of Warcraft Profile API\n    serviceCategory: API\n  - name: Diablo III API\n    baseURL: https://us.api.blizzard.com\n    serviceName: Diablo III API\n    serviceCategory: API\n  - name: Hearthstone Game Data API\n    baseURL: https://us.api.blizzard.com\n    serviceName: Hearthstone Game Data API\n    serviceCategory: API\n  - name: StarCraft II API\n    baseURL: https://us.api.blizzard.com\n    serviceName: StarCraft II API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per Active Consumer\n    metric: '0 / active_consumers (no direct cost; opportunity cost = engineering time + partner relationship)'\n    target: track engineering hours instead\n  - name: Headroom Against Ceiling\n  \
  \  metric: peak_requests_per_hour / 36000\n    target: '< 0.7 to trigger partner-access conversation'\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/battle-net/refs/heads/main/finops/battle-net-finops.yml
sources:
- https://develop.battle.net/access/clients
- https://community.developer.battle.net/documentation
specification: FinOps Framework
tags:
- Games
- Gaming
- Blizzard
- FinOps
- FOCUS
---
