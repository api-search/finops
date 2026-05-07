---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: ice-consolidated-feed-api-openapi.yml
  format: yaml
  label: ICE Consolidated Feed API
  slug: consolidated-feed-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/intercontinental-exchange/refs/heads/main/openapi/ice-consolidated-feed-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Purchase
  - Usage
  - Tax
  - Adjustment
  pricingCategory: Subscription
description: 'FOCUS-aligned FinOps placeholder for Intercontinental Exchange: contract-based market data and mortgage technology APIs with negotiated subscription fees and per-feed entitlements.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Intercontinental Exchange, Inc.
  ProviderName: Intercontinental Exchange
  PublisherName: Intercontinental Exchange, Inc.
  ServiceCategory: Market Data
  ServiceName: Intercontinental Exchange
layout: finops
meters:
- aggregation: sum
  dimensions:
  - feed
  - exchange
  - market_data_tier
  name: data_feed_subscription
  unit: month
- aggregation: max
  dimensions:
  - exchange
  - asset_class
  name: symbols_entitled
  unit: symbol
- aggregation: max
  dimensions:
  - feed
  - user_class
  name: redistribution_users
  unit: seat
- aggregation: sum
  dimensions:
  - api
  - endpoint
  name: api_requests
  unit: request
name: Intercontinental Exchange Finops
provider_name: Intercontinental Exchange
provider_slug: intercontinental-exchange
publisher_name: Intercontinental Exchange, Inc.
service_category: Market Data
slug: intercontinental-exchange-finops
source_filename: intercontinental-exchange-finops.yml
source_heading: FinOps Profile
source_url: https://www.ice.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Intercontinental Exchange\nproviderId: intercontinental-exchange\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Market Data\n  - Financial Exchanges\ndescription: 'FOCUS-aligned FinOps placeholder for Intercontinental Exchange: contract-based market\n  data and mortgage technology APIs with negotiated subscription fees and per-feed entitlements.'\nnotes: ICE does not publish rate cards; meters and unit economics below describe the typical billable\n  surface for market data and mortgage technology APIs but cannot be reconciled without a customer contract.\nsources:\n  - https://www.ice.com/\n  - https://developer.theice.com/hc/en-us\n  - https://idsportal.icedataservices.com/marketdata\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n\
  \  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Intercontinental Exchange, Inc.\nserviceCategory: Market Data\nbillingModel:\n  pricingCategory: Subscription\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\n    - Tax\n    - Adjustment\nfocusColumns:\n  ServiceName: Intercontinental Exchange\n  ServiceCategory: Market Data\n  ProviderName: Intercontinental Exchange\n  PublisherName: Intercontinental Exchange, Inc.\n  InvoiceIssuerName: Intercontinental Exchange, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: data_feed_subscription\n    unit: month\n    aggregation: sum\n    dimensions:\n      - feed\n      - exchange\n      - market_data_tier\n  - name: symbols_entitled\n    unit: symbol\n    aggregation: max\n    dimensions:\n      - exchange\n      - asset_class\n  - name: redistribution_users\n    unit: seat\n    aggregation: max\n    dimensions:\n      - feed\n     \
  \ - user_class\n  - name: api_requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\nprinciples:\n  - name: Visibility\n    description: Reconcile monthly ICE invoices against entitled feeds and redistribution counts; use\n      ICE customer portal usage exports where available.\n  - name: Allocation\n    description: Tag downstream consumers (trading desks, research, retail clients) to attribute feed\n      and redistribution costs back to revenue-producing units.\n  - name: Optimization\n    description: Right-size feed entitlements (delayed vs real-time, full-depth vs top-of-book) and\n      consolidate redundant exchange feeds during contract renewal.\n  - name: Accountability\n    description: Establish a market-data manager role; review entitlements quarterly and exit unused\n      symbols/feeds before annual true-up.\nmaintainers:\n  - FN: API Evangelist\n    email: info@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/intercontinental-exchange/refs/heads/main/finops/intercontinental-exchange-finops.yml
sources:
- https://www.ice.com/
- https://developer.theice.com/hc/en-us
- https://idsportal.icedataservices.com/marketdata
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Market Data
- Financial Exchanges
---
