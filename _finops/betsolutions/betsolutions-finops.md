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
  billingCurrency: USD (settlement varies)
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  - Tax
  - Adjustment
  - Refund
  - Credit
  chargeFrequency: Recurring
  pricingCategory: Revenue Share + Integration Fees
description: 'FOCUS-aligned FinOps shape for BetSolutions: B2B iGaming platform with revenue-share commercial structure on Gross Gaming Revenue plus integration fees. Costs are not API-call denominated; they scale with player wager volume and operator GGR.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: BetSolutions
  PricingCategory: Revenue Share
  PricingUnit: GGR
  ProviderName: BetSolutions
  PublisherName: BetSolutions
  ServiceCategory: iGaming Platform / Casino APIs
  ServiceName: BetSolutions Casino Platform
layout: finops
meters:
- aggregation: sum
  description: Operator GGR (wagers minus payouts) used as the revenue-share base
  dimensions:
  - operator
  - game_module
  - currency
  name: gross_gaming_revenue
  unit: USD
- aggregation: sum
  description: Total wager volume across modules
  dimensions:
  - operator
  - game_module
  - player_segment
  name: wager_volume
  unit: USD
- aggregation: sum
  description: Game round count
  dimensions:
  - game_module
  - game_studio
  name: rounds
  unit: round
- aggregation: sum
  description: Freespin campaign cost (player liability incurred via promotional rounds)
  dimensions:
  - campaign
  - operator
  name: freespin_campaigns
  unit: USD
- aggregation: sum
  description: Setup / module / annual integration fees
  dimensions:
  - operator
  - module
  name: integration_fees
  unit: month
name: Betsolutions Finops
provider_name: BetSolutions
provider_slug: betsolutions
publisher_name: BetSolutions
service_category: iGaming Platform / Casino APIs
slug: betsolutions-finops
source_filename: betsolutions-finops.yml
source_heading: FinOps Profile
source_url: https://docs.betsolutions.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: BetSolutions\nproviderId: betsolutions\npublisherName: BetSolutions\nserviceCategory: iGaming Platform / Casino APIs\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Betting\n  - Casinos\n  - Gaming\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps shape for BetSolutions: B2B iGaming platform with revenue-share commercial\n  structure on Gross Gaming Revenue plus integration fees. Costs are not API-call denominated; they\n  scale with player wager volume and operator GGR.'\nnotes: No public revenue-share rate or integration fee schedule. Replace meter values with the operator's\n  executed BetSolutions agreement once available.\nsources:\n  - https://docs.betsolutions.com/\n\
  \  - https://www.betsolutions.com/\nprinciples:\n  - name: Visibility\n    description: Use the Player and Slots APIs (rake / freespin / round data) to attribute platform cost\n      to player segments, game studios, and campaigns.\n  - name: Allocation\n    description: Allocate revenue share by game module (slots vs table vs sportsbook) and by player segment\n      so marketing / acquisition spend can be weighed against per-segment GGR.\n  - name: Optimization\n    description: Optimize game-mix and freespin-campaign economics — high-margin games and well-targeted\n      campaigns reduce platform cost as a percentage of net revenue.\n  - name: Accountability\n    description: Operator's compliance + finance teams jointly own the BetSolutions relationship; review\n      monthly GGR statements and revenue-share reconciliation.\nbillingModel:\n  pricingCategory: Revenue Share + Integration Fees\n  billingFrequency: Monthly\n  billingCurrency: USD (settlement varies)\n  chargeCategories:\n\
  \    - Usage\n    - Purchase\n    - Tax\n    - Adjustment\n    - Refund\n    - Credit\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: BetSolutions Casino Platform\n  ServiceCategory: iGaming Platform / Casino APIs\n  ProviderName: BetSolutions\n  PublisherName: BetSolutions\n  InvoiceIssuerName: BetSolutions\n  PricingCategory: Revenue Share\n  PricingUnit: GGR\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: gross_gaming_revenue\n    description: Operator GGR (wagers minus payouts) used as the revenue-share base\n    unit: USD\n    aggregation: sum\n    dimensions:\n      - operator\n      - game_module\n      - currency\n  - name: wager_volume\n    description: Total wager volume across modules\n    unit: USD\n    aggregation: sum\n    dimensions:\n      - operator\n      - game_module\n      - player_segment\n  - name: rounds\n    description: Game round count\n    unit: round\n    aggregation: sum\n    dimensions:\n      - game_module\n      - game_studio\n\
  \  - name: freespin_campaigns\n    description: Freespin campaign cost (player liability incurred via promotional rounds)\n    unit: USD\n    aggregation: sum\n    dimensions:\n      - campaign\n      - operator\n  - name: integration_fees\n    description: Setup / module / annual integration fees\n    unit: month\n    aggregation: sum\n    dimensions:\n      - operator\n      - module\napis:\n  - name: BetSolutions Wallet API\n    baseURL: ''\n    serviceName: BetSolutions Wallet API\n    serviceCategory: API\n  - name: BetSolutions Player API\n    baseURL: ''\n    serviceName: BetSolutions Player API\n    serviceCategory: API\n  - name: BetSolutions Slots API\n    baseURL: ''\n    serviceName: BetSolutions Slots API\n    serviceCategory: API\n  - name: BetSolutions Table Games API\n    baseURL: ''\n    serviceName: BetSolutions Table Games API\n    serviceCategory: API\n  - name: BetSolutions Provably Fair Games API\n    baseURL: ''\n    serviceName: BetSolutions Provably Fair Games\
  \ API\n    serviceCategory: API\n  - name: BetSolutions Third-Party Integration API\n    baseURL: ''\n    serviceName: BetSolutions Third-Party Integration API\n    serviceCategory: API\nunitEconomics:\n  - name: Platform Take Rate\n    metric: revenue_share / gross_gaming_revenue\n    target: per executed agreement\n  - name: Cost per Round\n    metric: (revenue_share + integration_fees) / rounds\n    target: minimize via game-mix\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/betsolutions/refs/heads/main/finops/betsolutions-finops.yml
sources:
- https://docs.betsolutions.com/
- https://www.betsolutions.com/
specification: FinOps Framework
tags:
- Betting
- Casinos
- Gaming
- FinOps
- FOCUS
---
