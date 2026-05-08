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
  - Subscription
  - Usage
  - Adjustment
  pricingCategory: Subscription with Metered Credit Allowance
description: FinOps view of CoinMarketCap. Subscription tiers each gate a monthly credit allowance and a per-minute rate limit. Per-call credit cost varies by endpoint and by the number of items in the response. Annual billing offers up to 20% discount.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Subscription
  InvoiceIssuerName: CoinMarketCap
  ProviderName: CoinMarketCap
  PublisherName: CoinMarketCap
  ServiceCategory: Crypto Market Data
  ServiceName: CoinMarketCap Pro API
layout: finops
meters:
- aggregation: sum
  description: Monthly subscription per tier.
  dimensions:
  - api_key
  name: subscription
  unit: month
- aggregation: sum
  description: Per-call credit consumption against monthly allowance.
  dimensions:
  - api_key
  - endpoint
  name: credits
  unit: credit
name: Coinmarketcap Finops
provider_name: CoinMarketCap
provider_slug: coinmarketcap
publisher_name: CoinMarketCap
service_category: Crypto Market Data
slug: coinmarketcap-finops
source_filename: coinmarketcap-finops.yml
source_heading: FinOps Profile
source_url: https://coinmarketcap.com/api/pricing/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: CoinMarketCap\nproviderId: coinmarketcap\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: true\ntags:\n  - Crypto\n  - Market Data\n  - FinOps\n  - FOCUS\ndescription: >-\n  FinOps view of CoinMarketCap. Subscription tiers each gate a monthly credit allowance and a\n  per-minute rate limit. Per-call credit cost varies by endpoint and by the number of items in\n  the response. Annual billing offers up to 20% discount.\nsources:\n  - https://coinmarketcap.com/api/pricing/\n  - https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: CoinMarketCap\nserviceCategory: Crypto Market Data\nbillingModel:\n  pricingCategory: Subscription\
  \ with Metered Credit Allowance\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Subscription\n    - Usage\n    - Adjustment\nfocusColumns:\n  ServiceName: CoinMarketCap Pro API\n  ServiceCategory: Crypto Market Data\n  ProviderName: CoinMarketCap\n  PublisherName: CoinMarketCap\n  InvoiceIssuerName: CoinMarketCap\n  BillingCurrency: USD\n  ChargeCategory: Subscription\nmeters:\n  - name: subscription\n    description: Monthly subscription per tier.\n    unit: month\n    aggregation: sum\n    dimensions:\n      - api_key\n  - name: credits\n    description: Per-call credit consumption against monthly allowance.\n    unit: credit\n    aggregation: sum\n    dimensions:\n      - api_key\n      - endpoint\nprinciples:\n  - name: Visibility\n    description: Track per-endpoint credit consumption to forecast tier sufficiency.\n  - name: Allocation\n    description: Allocate subscription to consuming product; tag API keys per workload.\n  - name: Optimization\n\
  \    description: Cache responses and use bundled symbol calls to reduce credit consumption.\n  - name: Accountability\n    description: Assign a billing owner per API key; review monthly credits-vs-allowance.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/coinmarketcap/refs/heads/main/finops/coinmarketcap-finops.yml
sources:
- https://coinmarketcap.com/api/pricing/
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Crypto
- Market Data
- FinOps
- FOCUS
---
