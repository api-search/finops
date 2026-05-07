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
  billingFrequency: None
  chargeCategories:
  - Adjustment
  pricingCategory: Free
description: The Riot Games Developer API is free; there is no Riot-issued invoice for API consumption. FinOps treatment for consumers therefore focuses on the indirect cost of consuming and storing Riot data (compute, storage, egress on the consumer's own cloud) and the policy cost of staying compliant with Riot's developer terms.
focus_columns:
  BillingCurrency: USD
  ProviderName: Riot Games
  PublisherName: Riot Games, Inc.
  ServiceCategory: Gaming Developer Platform
  ServiceName: Riot Games Developer API
layout: finops
meters:
- aggregation: sum
  description: Requests consumed against Riot's developer API; not billed by Riot but useful for forecasting consumer-side infrastructure cost.
  dimensions:
  - region
  - api
  - key_tier
  name: api_requests
  unit: request
- aggregation: count
  description: Count of 429 responses; an operational signal that limits or method-call patterns need tuning, not a billable line.
  dimensions:
  - region
  - rate_limit_type
  name: rate_limit_breaches
  unit: response
name: Riot Games Finops
provider_name: Riot Games
provider_slug: riot-games
publisher_name: Riot Games, Inc.
service_category: Gaming Developer Platform
slug: riot-games-finops
source_filename: riot-games-finops.yml
source_heading: FinOps Profile
source_url: https://developer.riotgames.com/docs/portal
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Riot Games\nproviderId: riot-games\npublisherName: Riot Games, Inc.\nserviceCategory: Gaming Developer Platform\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - Riot Games\n  - Gaming\n  - Developer API\n  - FinOps\n  - FOCUS\ndescription: >-\n  The Riot Games Developer API is free; there is no Riot-issued invoice for API consumption.\n  FinOps treatment for consumers therefore focuses on the indirect cost of consuming and\n  storing Riot data (compute, storage, egress on the consumer's own cloud) and the policy\n  cost of staying compliant with Riot's developer terms.\nsources:\n  - https://developer.riotgames.com/docs/portal\n\
  \  - https://developer.riotgames.com/policies.html\nbillingModel:\n  pricingCategory: Free\n  billingFrequency: None\n  billingCurrency: USD\n  chargeCategories:\n    - Adjustment\nfocusColumns:\n  ServiceName: Riot Games Developer API\n  ServiceCategory: Gaming Developer Platform\n  ProviderName: Riot Games\n  PublisherName: Riot Games, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: api_requests\n    description: >-\n      Requests consumed against Riot's developer API; not billed by Riot but useful for\n      forecasting consumer-side infrastructure cost.\n    unit: request\n    aggregation: sum\n    dimensions:\n      - region\n      - api\n      - key_tier\n  - name: rate_limit_breaches\n    description: >-\n      Count of 429 responses; an operational signal that limits or method-call patterns need\n      tuning, not a billable line.\n    unit: response\n    aggregation: count\n    dimensions:\n      - region\n      - rate_limit_type\nprinciples:\n  - name: Visibility\n    description:\
  \ >-\n      Track Riot API consumption from the client side (request log, 429 rate, retry queue\n      depth); Riot does not publish a usage or billing API.\n  - name: Allocation\n    description: >-\n      Allocate the consumer-side infrastructure cost of running Riot integrations\n      (compute/storage/egress) to the product team that owns the integration, not to\n      undifferentiated platform cost.\n  - name: Optimization\n    description: >-\n      Cache match and account data to stay under per-region method limits; coalesce repeated\n      summoner/match lookups; request a production-key raise before scaling the request rate\n      itself.\n  - name: Accountability\n    description: >-\n      The product owner of the consumer application owns adherence to Riot's developer\n      terms; budget concerns are limited to consumer-side infra and staff cost.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/riot-games/refs/heads/main/finops/riot-games-finops.yml
sources:
- https://developer.riotgames.com/docs/portal
- https://developer.riotgames.com/policies.html
specification: FinOps Framework
tags:
- Riot Games
- Gaming
- Developer API
- FinOps
- FOCUS
---
