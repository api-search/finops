---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: coinbase-advanced-trade-openapi.yml
  format: yaml
  label: Coinbase Advanced Trade API
  slug: advanced-trade-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/coinbase/refs/heads/main/openapi/coinbase-advanced-trade-openapi.yml
- filename: coinbase-exchange-openapi.yml
  format: yaml
  label: Coinbase Exchange API
  slug: exchange-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/coinbase/refs/heads/main/openapi/coinbase-exchange-openapi.yml
- filename: coinbase-prime-openapi.yml
  format: yaml
  label: Coinbase Prime API
  slug: prime-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/coinbase/refs/heads/main/openapi/coinbase-prime-openapi.yml
- filename: coinbase-onramp-openapi.yml
  format: yaml
  label: Coinbase Onramp API
  slug: onramp-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/coinbase/refs/heads/main/openapi/coinbase-onramp-openapi.yml
- filename: coinbase-commerce-openapi.yml
  format: yaml
  label: Coinbase Commerce API
  slug: commerce-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/coinbase/refs/heads/main/openapi/coinbase-commerce-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Continuous Settlement
  chargeCategories:
  - Usage
  - Adjustment
  - Refund
  pricingCategory: Take Rate
description: 'FOCUS-aligned FinOps for Coinbase: per-trade maker/taker take rates that scale by 30-day USD volume. API access itself is free; cost is realized at trade execution.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Coinbase, Inc.
  ProviderName: Coinbase
  PublisherName: Coinbase, Inc.
  ServiceCategory: Financial Services
  ServiceName: Coinbase Advanced Trade
layout: finops
meters:
- aggregation: sum
  dimensions:
  - product_id
  - fee_tier
  - stable_pair_flag
  name: maker_volume
  unit: USD
- aggregation: sum
  dimensions:
  - product_id
  - fee_tier
  name: taker_volume
  unit: USD
- aggregation: sum
  dimensions:
  - product_id
  - fee_tier
  name: maker_fees
  unit: USD
- aggregation: sum
  dimensions:
  - product_id
  - fee_tier
  name: taker_fees
  unit: USD
- aggregation: max
  dimensions:
  - account
  name: rolling_30d_volume
  unit: USD
name: Coinbase Finops
provider_name: Coinbase
provider_slug: coinbase
publisher_name: Coinbase, Inc.
service_category: Financial Services
slug: coinbase-finops
source_filename: coinbase-finops.yml
source_heading: FinOps Profile
source_url: https://help.coinbase.com/en/coinbase/trading-and-funding/advanced-trade/advanced-trade-fees
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Coinbase\nproviderId: coinbase\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Cryptocurrency\n  - Trading\ndescription: 'FOCUS-aligned FinOps for Coinbase: per-trade maker/taker take rates that scale by 30-day\n  USD volume. API access itself is free; cost is realized at trade execution.'\nsources:\n  - https://help.coinbase.com/en/coinbase/trading-and-funding/advanced-trade/advanced-trade-fees\n  - https://docs.cdp.coinbase.com/advanced-trade/docs/welcome\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Coinbase, Inc.\nserviceCategory: Financial Services\nbillingModel:\n  pricingCategory: Take Rate\n  billingFrequency: Continuous\
  \ Settlement\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Adjustment\n    - Refund\nfocusColumns:\n  ServiceName: Coinbase Advanced Trade\n  ServiceCategory: Financial Services\n  ProviderName: Coinbase\n  PublisherName: Coinbase, Inc.\n  InvoiceIssuerName: Coinbase, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: maker_volume\n    unit: USD\n    aggregation: sum\n    dimensions:\n      - product_id\n      - fee_tier\n      - stable_pair_flag\n  - name: taker_volume\n    unit: USD\n    aggregation: sum\n    dimensions:\n      - product_id\n      - fee_tier\n  - name: maker_fees\n    unit: USD\n    aggregation: sum\n    dimensions:\n      - product_id\n      - fee_tier\n  - name: taker_fees\n    unit: USD\n    aggregation: sum\n    dimensions:\n      - product_id\n      - fee_tier\n  - name: rolling_30d_volume\n    unit: USD\n    aggregation: max\n    dimensions:\n      - account\nprinciples:\n  - name: Visibility\n    description: Pull executed-trade fee data from\
  \ the Advanced Trade /orders/historical/fills endpoint;\n      track 30-day rolling USD volume to anticipate tier transitions.\n  - name: Allocation\n    description: Tag orders with client_order_id metadata to attribute trading PnL and fees to strategy,\n      desk, or product.\n  - name: Optimization\n    description: Use limit orders to qualify for maker pricing; route through 22 stable pairs (0.00% maker)\n      where possible; consolidate volume across one entity to reach higher Advanced tiers; apply for fee\n      upgrade program above $100M monthly volume.\n  - name: Accountability\n    description: Trading desk owns fee tier; finance reconciles maker/taker fees against fills nightly.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/coinbase/refs/heads/main/finops/coinbase-finops.yml
sources:
- https://help.coinbase.com/en/coinbase/trading-and-funding/advanced-trade/advanced-trade-fees
- https://docs.cdp.coinbase.com/advanced-trade/docs/welcome
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Cryptocurrency
- Trading
---
