---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: alpaca-trading-api-openapi.yml
  format: yaml
  label: Alpaca Trading API
  slug: trading-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/alpaca/refs/heads/main/openapi/alpaca-trading-api-openapi.yml
- filename: alpaca-data-api-openapi.yml
  format: yaml
  label: Alpaca Market Data API
  slug: market-data-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/alpaca/refs/heads/main/openapi/alpaca-data-api-openapi.yml
- filename: alpaca-broker-api-openapi.yml
  format: yaml
  label: Alpaca Broker API
  slug: broker-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/alpaca/refs/heads/main/openapi/alpaca-broker-api-openapi.yml
- filename: alpaca-oauth-api-openapi.yml
  format: yaml
  label: Alpaca OAuth API
  slug: oauth-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/alpaca/refs/heads/main/openapi/alpaca-oauth-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Subscription
  - Usage
  - Adjustment
  pricingCategory: Subscription + Custom Contract
description: FinOps view of Alpaca billing. Trading is commission-free; revenue comes from PFOR, margin, Algo Trader Plus subscription ($99/month), and Broker API contracts. Customers should treat market-data subscriptions and Broker API minimums as the primary cost lines.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Subscription
  InvoiceIssuerName: Alpaca
  ProviderName: Alpaca
  PublisherName: Alpaca Securities LLC
  ServiceCategory: Fintech
  ServiceName: Alpaca Market Data and Trading
layout: finops
meters:
- aggregation: sum
  description: Algo Trader Plus market data subscription.
  dimensions:
  - account
  name: market_data_subscription
  unit: month
- aggregation: sum
  description: Broker API minimums and per-account fees per partner contract.
  dimensions:
  - partner
  name: broker_api_contract
  unit: contract
name: Alpaca Finops
provider_name: Alpaca
provider_slug: alpaca
publisher_name: Alpaca Securities LLC / Alpaca Crypto LLC
service_category: Fintech
slug: alpaca-finops
source_filename: alpaca-finops.yml
source_heading: FinOps Profile
source_url: https://alpaca.markets/data
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Alpaca\nproviderId: alpaca\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: true\ntags:\n  - Fintech\n  - Trading\n  - Brokerage\n  - FinOps\n  - FOCUS\ndescription: >-\n  FinOps view of Alpaca billing. Trading is commission-free; revenue comes from PFOR, margin,\n  Algo Trader Plus subscription ($99/month), and Broker API contracts. Customers should treat\n  market-data subscriptions and Broker API minimums as the primary cost lines.\nsources:\n  - https://alpaca.markets/data\n  - https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Alpaca Securities LLC / Alpaca Crypto LLC\nserviceCategory: Fintech\nbillingModel:\n  pricingCategory:\
  \ Subscription + Custom Contract\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Subscription\n    - Usage\n    - Adjustment\nfocusColumns:\n  ServiceName: Alpaca Market Data and Trading\n  ServiceCategory: Fintech\n  ProviderName: Alpaca\n  PublisherName: Alpaca Securities LLC\n  InvoiceIssuerName: Alpaca\n  BillingCurrency: USD\n  ChargeCategory: Subscription\nmeters:\n  - name: market_data_subscription\n    description: Algo Trader Plus market data subscription.\n    unit: month\n    aggregation: sum\n    dimensions:\n      - account\n  - name: broker_api_contract\n    description: Broker API minimums and per-account fees per partner contract.\n    unit: contract\n    aggregation: sum\n    dimensions:\n      - partner\nprinciples:\n  - name: Visibility\n    description: Pull subscription invoices and broker partner monthly billing into FinOps store.\n  - name: Allocation\n    description: Allocate market data subscription to consuming trading desk or\
  \ product line.\n  - name: Optimization\n    description: Right-size between Free and Algo Trader Plus by audit of actual rpm and symbol counts.\n  - name: Accountability\n    description: Assign a billing owner for the brokerage relationship and review at renewal.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/alpaca/refs/heads/main/finops/alpaca-finops.yml
sources:
- https://alpaca.markets/data
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Fintech
- Trading
- Brokerage
- FinOps
- FOCUS
---
