---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: activision-blizzard-battle-net.json
  format: json
  label: Battle.net API
  slug: battle-net
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/activision-blizzard/refs/heads/main/openapi/activision-blizzard-battle-net.json
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  pricingCategory: Free (Non-Commercial) / Negotiated Commercial Licence
description: FOCUS-aligned FinOps scaffold for Activision Blizzard's Battle.net API. There is no Blizzard invoice for non-commercial use; FinOps relevance is restricted to compute/egress costs incurred by the integrating application when polling Battle.net data and to any commercial-licence fee negotiated directly with Blizzard.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Blizzard Entertainment, Inc.
  ProviderName: Blizzard Entertainment
  PublisherName: Blizzard Entertainment, Inc.
  ServiceCategory: Gaming / Game Data
  ServiceName: Battle.net API
layout: finops
meters:
- aggregation: sum
  description: Battle.net API request consumed against per-OAuth-client limits. Not directly billed under the free developer tier, but the unit consumers track for cost-of-integration analysis.
  dimensions:
  - region
  - game
  - endpoint
  name: api_request
  unit: request
- aggregation: sum
  description: Annual commercial-licence fee for Battle.net API use, where contracted.
  dimensions:
  - tier
  name: commercial_licence
  unit: year
name: Activision Blizzard Finops
provider_name: activision-blizzard
provider_slug: activision-blizzard
publisher_name: Blizzard Entertainment, Inc.
service_category: Gaming / Game Data
slug: activision-blizzard-finops
source_filename: activision-blizzard-finops.yml
source_heading: FinOps Profile
source_url: https://develop.battle.net/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Activision Blizzard\nproviderId: activision-blizzard\npublisherName: Blizzard Entertainment, Inc.\nserviceCategory: Gaming / Game Data\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Gaming\n  - Battle.net\n  - FinOps\n  - FOCUS\ndescription: FOCUS-aligned FinOps scaffold for Activision Blizzard's Battle.net API. There is no Blizzard\n  invoice for non-commercial use; FinOps relevance is restricted to compute/egress costs incurred by\n  the integrating application when polling Battle.net data and to any commercial-licence fee negotiated\n  directly with Blizzard.\nsources:\n  - https://develop.battle.net/\n  - https://community.developer.battle.net/\n\
  notes: No published commercial billing model. Reconciled flag is false because there is no provider\n  invoice to map to FOCUS columns.\nbillingModel:\n  pricingCategory: Free (Non-Commercial) / Negotiated Commercial Licence\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: Battle.net API\n  ServiceCategory: Gaming / Game Data\n  ProviderName: Blizzard Entertainment\n  PublisherName: Blizzard Entertainment, Inc.\n  InvoiceIssuerName: Blizzard Entertainment, Inc.\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: api_request\n    description: Battle.net API request consumed against per-OAuth-client limits. Not directly billed\n      under the free developer tier, but the unit consumers track for cost-of-integration analysis.\n    unit: request\n    aggregation: sum\n    dimensions:\n      - region\n      - game\n      - endpoint\n  - name: commercial_licence\n    description: Annual commercial-licence\
  \ fee for Battle.net API use, where contracted.\n    unit: year\n    aggregation: sum\n    dimensions:\n      - tier\nprinciples:\n  - name: Visibility\n    description: There is no Blizzard usage API. Track outbound calls by OAuth2 client at the consumer's\n      egress / API gateway and watch for 429 responses as the practical \"approaching budget\" signal.\n  - name: Allocation\n    description: Allocate compute and egress costs of polling Battle.net data to the consuming product\n      (e.g. guild website, leaderboard service, esports backend) rather than to Blizzard.\n  - name: Optimization\n    description: Cache aggressively, prefer scheduled batch refreshes over on-demand calls, share OAuth\n      clients only when limits permit, and use change-aware patterns where exposed.\n  - name: Accountability\n    description: The integrator's engineering team owns rate-limit headroom and any commercial-licence\n      renewal.\nmaintainers:\n  - FN: Kin Lane\n    email: info@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/activision-blizzard/refs/heads/main/finops/activision-blizzard-finops.yml
sources:
- https://develop.battle.net/
- https://community.developer.battle.net/
specification: FinOps Framework
tags:
- Gaming
- Battle.net
- FinOps
- FOCUS
---
