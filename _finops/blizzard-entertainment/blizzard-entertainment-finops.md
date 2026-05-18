---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: blizzard-world-of-warcraft-openapi.yml
  format: yaml
  label: World of Warcraft Game Data API
  slug: world-of-warcraft-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/blizzard-entertainment/refs/heads/main/openapi/blizzard-world-of-warcraft-openapi.yml
- filename: blizzard-diablo-iii-openapi.yml
  format: yaml
  label: Diablo III Community API
  slug: diablo-iii-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/blizzard-entertainment/refs/heads/main/openapi/blizzard-diablo-iii-openapi.yml
- filename: blizzard-starcraft-ii-openapi.yml
  format: yaml
  label: StarCraft II Community API
  slug: starcraft-ii-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/blizzard-entertainment/refs/heads/main/openapi/blizzard-starcraft-ii-openapi.yml
- filename: blizzard-hearthstone-openapi.yml
  format: yaml
  label: Hearthstone Game Data API
  slug: hearthstone-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/blizzard-entertainment/refs/heads/main/openapi/blizzard-hearthstone-openapi.yml
- filename: blizzard-oauth-openapi.yml
  format: yaml
  label: Battle.net OAuth API
  slug: oauth-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/blizzard-entertainment/refs/heads/main/openapi/blizzard-oauth-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: None
  chargeCategories:
  - Usage
  chargeFrequency: None
  pricingCategory: No-Charge
description: FinOps framework definition for the Battle.net Developer API surface. Battle.net Game Data and Community APIs are offered at no charge to developers under the Battle.net Developer API Terms of Use, so the primary cost lever for consumers is engineering effort and infrastructure to honor the per-second and per-hour limits, not invoiced API cost.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Blizzard Entertainment
  PricingCategory: No-Charge
  PricingUnit: request
  ProviderName: Blizzard Entertainment
  PublisherName: Blizzard Entertainment
  ServiceCategory: Developer Tools / API
  ServiceName: Battle.net Developer API
layout: finops
meters:
- aggregation: sum
  description: Count of Battle.net API requests
  dimensions:
  - api
  - endpoint
  - region
  - game
  - client_id
  name: api_requests
  unit: request
- aggregation: sum
  description: Count of 429 / throttled responses
  dimensions:
  - api
  - region
  - client_id
  name: throttled_requests
  unit: request
- aggregation: sum
  description: Count of OAuth token issuance calls
  dimensions:
  - client_id
  - grant_type
  name: oauth_token_issuance
  unit: request
name: Blizzard Entertainment Finops
provider_name: Blizzard Entertainment
provider_slug: blizzard-entertainment
publisher_name: Blizzard Entertainment
service_category: API
slug: blizzard-entertainment-finops
source_filename: blizzard-entertainment-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Blizzard Entertainment\nproviderId: blizzard-entertainment\npublisherName: Blizzard Entertainment\nserviceCategory: API\ncreated: '2026-05-16'\nmodified: '2026-05-16'\nreconciled: false\ntags:\n  - Games\n  - Battle.net\n  - Game Data\n  - FinOps\n  - FOCUS\ndescription: >-\n  FinOps framework definition for the Battle.net Developer API surface.\n  Battle.net Game Data and Community APIs are offered at no charge to\n  developers under the Battle.net Developer API Terms of Use, so the primary\n  cost lever for consumers is engineering effort and infrastructure to honor\n  the per-second and per-hour limits, not invoiced API cost.\nprinciples:\n  - name: Visibility\n    description: Make API\
  \ call volume per Battle.net client visible to engineering and product.\n  - name: Allocation\n    description: Tag every Battle.net request with consuming feature, environment, region, and game so cost (effort, infrastructure, partner risk) can be allocated.\n  - name: Optimization\n    description: Cache static-namespace data, debounce profile lookups, and batch metadata fetches to stay well within Battle.net's per-second and per-hour ceilings.\n  - name: Accountability\n    description: Designate an owner for each Battle.net client id and review usage and 429 rates monthly.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n\
  \      - Workload Optimization\nbillingModel:\n  pricingCategory: No-Charge\n  billingFrequency: None\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n  chargeFrequency: None\nfocusColumns:\n  ServiceName: Battle.net Developer API\n  ServiceCategory: Developer Tools / API\n  ProviderName: Blizzard Entertainment\n  PublisherName: Blizzard Entertainment\n  InvoiceIssuerName: Blizzard Entertainment\n  PricingCategory: No-Charge\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of Battle.net API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - region\n      - game\n      - client_id\n  - name: throttled_requests\n    description: Count of 429 / throttled responses\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - client_id\n  - name: oauth_token_issuance\n    description: Count of OAuth token issuance\
  \ calls\n    unit: request\n    aggregation: sum\n    dimensions:\n      - client_id\n      - grant_type\napis:\n  - name: World of Warcraft Game Data API\n    baseURL: https://us.api.blizzard.com\n    tags:\n      - World of Warcraft\n      - Game Data\n    serviceName: World of Warcraft Game Data API\n    serviceCategory: API\n  - name: Diablo III Community API\n    baseURL: https://us.api.blizzard.com\n    tags:\n      - Diablo III\n      - Game Data\n    serviceName: Diablo III Community API\n    serviceCategory: API\n  - name: StarCraft II Community API\n    baseURL: https://us.api.blizzard.com\n    tags:\n      - StarCraft II\n      - Game Data\n    serviceName: StarCraft II Community API\n    serviceCategory: API\n  - name: Hearthstone Game Data API\n    baseURL: https://us.api.blizzard.com\n    tags:\n      - Hearthstone\n      - Game Data\n    serviceName: Hearthstone Game Data API\n    serviceCategory: API\n  - name: Battle.net OAuth API\n    baseURL: https://oauth.battle.net\n\
  \    tags:\n      - OAuth\n      - Authentication\n    serviceName: Battle.net OAuth API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: infrastructure_cost / (api_requests / 1000)\n    target: TBD\n  - name: 429 Rate\n    metric: throttled_requests / api_requests\n    target: '< 0.001'\nmaintainers: []\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/blizzard-entertainment/refs/heads/main/finops/blizzard-entertainment-finops.yml
sources: []
specification: FinOps Framework
tags:
- Games
- Battle.net
- Game Data
- FinOps
- FOCUS
---
