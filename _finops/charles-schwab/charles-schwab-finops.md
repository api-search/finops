---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: charles-schwab-trader-api-openapi.yml
  format: yaml
  label: Charles Schwab Trader API
  slug: trader-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/charles-schwab/refs/heads/main/openapi/charles-schwab-trader-api-openapi.yml
- filename: charles-schwab-market-data-api-openapi.yml
  format: yaml
  label: Charles Schwab Market Data API
  slug: market-data-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/charles-schwab/refs/heads/main/openapi/charles-schwab-market-data-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Continuous Settlement
  chargeCategories:
  - Usage
  - Purchase
  - Tax
  - Adjustment
  - Refund
  pricingCategory: Brokerage Fees + Exchange Data Pass-Through
description: 'FOCUS-aligned FinOps framing for Charles Schwab developer APIs: API access itself is free for account holders, while underlying brokerage activity (commissions, margin, asset fees) and exchange market-data fees produce the billing surface.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Charles Schwab & Co., Inc.
  ProviderName: Charles Schwab
  PublisherName: Charles Schwab & Co., Inc.
  ServiceCategory: Financial Services
  ServiceName: Schwab Developer APIs
layout: finops
meters:
- aggregation: sum
  dimensions:
  - account
  - venue
  name: equity_trades
  unit: trade
- aggregation: sum
  dimensions:
  - account
  name: option_contracts
  unit: contract
- aggregation: max
  name: margin_balance
  unit: USD
- aggregation: avg
  dimensions:
  - product
  name: asset_under_management
  unit: USD
- aggregation: sum
  dimensions:
  - exchange
  - feed
  name: exchange_market_data_fees
  unit: USD
name: Charles Schwab Finops
provider_name: Charles Schwab
provider_slug: charles-schwab
publisher_name: Charles Schwab & Co., Inc.
service_category: Financial Services / Brokerage
slug: charles-schwab-finops
source_filename: charles-schwab-finops.yml
source_heading: FinOps Profile
source_url: https://developer.schwab.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Charles Schwab\nproviderId: charles-schwab\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Brokerage\n  - Trading\ndescription: 'FOCUS-aligned FinOps framing for Charles Schwab developer APIs: API access itself is free\n  for account holders, while underlying brokerage activity (commissions, margin, asset fees) and exchange\n  market-data fees produce the billing surface.'\nnotes: APIs are not separately priced; meters reflect brokerage and exchange-data billing lines.\nsources:\n  - https://developer.schwab.com/\n  - https://www.schwab.com/pricing\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Charles Schwab & Co., Inc.\nserviceCategory:\
  \ Financial Services / Brokerage\nbillingModel:\n  pricingCategory: Brokerage Fees + Exchange Data Pass-Through\n  billingFrequency: Continuous Settlement\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Adjustment\n    - Refund\nfocusColumns:\n  ServiceName: Schwab Developer APIs\n  ServiceCategory: Financial Services\n  ProviderName: Charles Schwab\n  PublisherName: Charles Schwab & Co., Inc.\n  InvoiceIssuerName: Charles Schwab & Co., Inc.\n  BillingCurrency: USD\nmeters:\n  - name: equity_trades\n    unit: trade\n    aggregation: sum\n    dimensions:\n      - account\n      - venue\n  - name: option_contracts\n    unit: contract\n    aggregation: sum\n    dimensions:\n      - account\n  - name: margin_balance\n    unit: USD\n    aggregation: max\n  - name: asset_under_management\n    unit: USD\n    aggregation: avg\n    dimensions:\n      - product\n  - name: exchange_market_data_fees\n    unit: USD\n    aggregation: sum\n    dimensions:\n\
  \      - exchange\n      - feed\nprinciples:\n  - name: Visibility\n    description: Use the Trader API transactions endpoints and Schwab statements to attribute fees to\n      accounts, strategies, and exchanges.\n  - name: Allocation\n    description: Tag orders with strategy/account metadata so fees and PnL roll up to the right business\n      unit.\n  - name: Optimization\n    description: Manage margin usage, route orders thoughtfully, and minimize redundant streaming subscriptions\n      to control exchange-data fees.\n  - name: Accountability\n    description: Trading desk / treasury owns Schwab fees and exchange data licenses; review monthly\n      against trading volume.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/charles-schwab/refs/heads/main/finops/charles-schwab-finops.yml
sources:
- https://developer.schwab.com/
- https://www.schwab.com/pricing
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Brokerage
- Trading
---
