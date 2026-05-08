---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: coingecko-crypto-market-data-api-openapi.yml
  format: yaml
  label: CoinGecko Crypto Market Data API
  slug: crypto-market-data-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/coingecko/refs/heads/main/openapi/coingecko-crypto-market-data-api-openapi.yml
- filename: coingecko-pro-api-openapi.yml
  format: yaml
  label: CoinGecko Pro API
  slug: pro-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/coingecko/refs/heads/main/openapi/coingecko-pro-api-openapi.yml
- filename: coingecko-onchain-dex-api-openapi.yml
  format: yaml
  label: CoinGecko Onchain DEX API
  slug: onchain-dex-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/coingecko/refs/heads/main/openapi/coingecko-onchain-dex-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Purchase
  - Usage
  - Tax
  - Adjustment
  - Refund
  pricingCategory: Tiered Subscription + Overage
description: 'FOCUS-aligned FinOps for CoinGecko: subscription tiers with monthly call-credit allotments plus per-500K-call overage at $250.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Gecko Labs Pte. Ltd.
  ProviderName: CoinGecko
  PublisherName: Gecko Labs Pte. Ltd.
  ServiceCategory: Market Data
  ServiceName: CoinGecko API
layout: finops
meters:
- aggregation: sum
  dimensions:
  - plan
  - endpoint
  - status_code
  name: api_credits_consumed
  unit: request
- aggregation: sum
  dimensions:
  - plan
  - billing_cycle
  name: subscription_fee
  unit: month
- aggregation: sum
  dimensions:
  - plan
  name: overage_credits
  unit: request
name: Coingecko Finops
provider_name: CoinGecko
provider_slug: coingecko
publisher_name: Gecko Labs Pte. Ltd.
service_category: Market Data
slug: coingecko-finops
source_filename: coingecko-finops.yml
source_heading: FinOps Profile
source_url: https://www.coingecko.com/en/api/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: CoinGecko\nproviderId: coingecko\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Cryptocurrency\n  - Market Data\ndescription: 'FOCUS-aligned FinOps for CoinGecko: subscription tiers with monthly call-credit allotments\n  plus per-500K-call overage at $250.'\nsources:\n  - https://www.coingecko.com/en/api/pricing\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Gecko Labs Pte. Ltd.\nserviceCategory: Market Data\nbillingModel:\n  pricingCategory: Tiered Subscription + Overage\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\n    - Tax\n    - Adjustment\n    - Refund\nfocusColumns:\n\
  \  ServiceName: CoinGecko API\n  ServiceCategory: Market Data\n  ProviderName: CoinGecko\n  PublisherName: Gecko Labs Pte. Ltd.\n  InvoiceIssuerName: Gecko Labs Pte. Ltd.\n  BillingCurrency: USD\nmeters:\n  - name: api_credits_consumed\n    unit: request\n    aggregation: sum\n    dimensions:\n      - plan\n      - endpoint\n      - status_code\n  - name: subscription_fee\n    unit: month\n    aggregation: sum\n    dimensions:\n      - plan\n      - billing_cycle\n  - name: overage_credits\n    unit: request\n    aggregation: sum\n    dimensions:\n      - plan\nprinciples:\n  - name: Visibility\n    description: Track per-key consumption against monthly credits using the CoinGecko dashboard usage\n      tab; alert at 80% of monthly allotment to avoid overage charges.\n  - name: Allocation\n    description: Issue separate API keys per consuming application or environment so credits and overage\n      can be charged back.\n  - name: Optimization\n    description: Cache frequent endpoints\
  \ (coins/markets, simple/price); use webhook/WebSocket Pro features\n      to avoid polling; right-size plan annually given $250 / 500K-call overage versus next-tier subscription.\n  - name: Accountability\n    description: Engineering owns endpoint efficiency and caching; finance owns plan tier and renewal.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/coingecko/refs/heads/main/finops/coingecko-finops.yml
sources:
- https://www.coingecko.com/en/api/pricing
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Cryptocurrency
- Market Data
---
