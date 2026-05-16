---
aligned_with: {}
api_specs:
- filename: frostbyte-ip-geolocation-openapi.yml
  format: yaml
  label: Frostbyte IP Geolocation API
  slug: ip-geolocation
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/frostbyte/refs/heads/main/openapi/frostbyte-ip-geolocation-openapi.yml
- filename: frostbyte-crypto-prices-openapi.yml
  format: yaml
  label: Frostbyte Crypto Prices API
  slug: crypto-prices
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/frostbyte/refs/heads/main/openapi/frostbyte-crypto-prices-openapi.yml
- filename: frostbyte-screenshot-openapi.yml
  format: yaml
  label: Frostbyte Screenshot API
  slug: screenshot
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/frostbyte/refs/heads/main/openapi/frostbyte-screenshot-openapi.yml
- filename: frostbyte-dns-lookup-openapi.yml
  format: yaml
  label: Frostbyte DNS Lookup API
  slug: dns-lookup
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/frostbyte/refs/heads/main/openapi/frostbyte-dns-lookup-openapi.yml
- filename: frostbyte-web-scraper-openapi.yml
  format: yaml
  label: Frostbyte Web Scraper API
  slug: web-scraper
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/frostbyte/refs/heads/main/openapi/frostbyte-web-scraper-openapi.yml
- filename: frostbyte-code-execution-openapi.yml
  format: yaml
  label: Frostbyte Code Execution API
  slug: code-execution
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/frostbyte/refs/heads/main/openapi/frostbyte-code-execution-openapi.yml
- filename: frostbyte-agent-gateway-openapi.yml
  format: yaml
  label: Frostbyte Agent Gateway (Full API)
  slug: agent-gateway
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/frostbyte/refs/heads/main/openapi/frostbyte-agent-gateway-openapi.yml
billing_model: {}
description: 'Frostbyte''s billing surface is a credit-based, pay-as-you-go model

  with USDC-on-Base settlement via the x402 protocol. There are no

  recurring subscriptions, no invoices, and no traditional billing

  relationship; cost data is observable on-chain and through the

  gateway''s analytics and balance endpoints.

  '
focus_columns: {}
layout: finops
meters: []
name: Frostbyte Finops
provider_name: Frostbyte
provider_slug: frostbyte
publisher_name: ''
service_category: ''
slug: frostbyte-finops
source_filename: frostbyte-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "finopsFrameworkVersion: 'FOCUS-1.0'\nproviderId: frostbyte\nprovider:\n  name: Frostbyte\n  url: https://api-catalog-three.vercel.app/\nmodified: '2026-05-16'\nreconciled: false\ndescription: |\n  Frostbyte's billing surface is a credit-based, pay-as-you-go model\n  with USDC-on-Base settlement via the x402 protocol. There are no\n  recurring subscriptions, no invoices, and no traditional billing\n  relationship; cost data is observable on-chain and through the\n  gateway's analytics and balance endpoints.\n\nbilling_model:\n  type: usage-based\n  unit: credit\n  rate: 1 credit per request (default)\n  currency:\n    name: USDC\n    chain: base\n    protocol: x402\n  invoicing: none\n  contract: none\n\nfocus:\n  BillingCurrency: USDC\n  PricingUnit: credit\n  ChargeCategory: Usage\n  ChargeFrequency: One-Time\n  ChargeSubcategory: Pay-As-You-Go\n  CommitmentDiscountType: None\n  ServiceCategory:\n    - Developer Tools\n    - AI & ML\n  SubAccount:\n    description: Per-API-key\
  \ balance scoping; each key holds an independent credit balance.\n  ResourceType: api-call\n\ncost_observability:\n  - endpoint: GET /api/keys/balance\n    description: Returns remaining credit balance and key expiry.\n  - endpoint: GET /api/analytics\n    description: Gateway-level usage analytics.\n  - endpoint: 'GET /api/payments/*'\n    description: Payment lookup / receipt endpoints for x402 USDC top-ups.\n  - on_chain: 'Base network — USDC transfers to provider address (x402 settlement)'\n\ncost_optimization:\n  - Use the free 200-credit allowance for evaluation before topping up.\n  - Top up to extend key validity from 30 to 90 days.\n  - Batch endpoints where supported (e.g. IP geolocation batch, DNS batch).\n\nunpublished:\n  - bulk-discounts\n  - committed-use-discounts\n  - enterprise-pricing\n  - SLA-credits\n\nnotes: |\n  No subscriptions, invoices, or enterprise plans are published as of the\n  profile date. All cost attribution is per-API-key, settled in USDC on\n  Base\
  \ via x402.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/frostbyte/refs/heads/main/finops/frostbyte-finops.yml
sources: []
specification: ''
tags:
- Developer Tools
- Utility APIs
- Geolocation
- Cryptocurrency
- Screenshots
- DNS
- Scraping
- AI Agents
---
