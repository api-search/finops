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
  pricingCategory: Subscription
description: FinOps view of Polygon.io. Subscription-based per asset class with multiple tiers; Business contracts add redistribution and OPRA/CME exchange fees passed through. Customers should budget per-asset-class subscriptions plus exchange data fees on Business plans.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Subscription
  InvoiceIssuerName: Polygon.io
  ProviderName: Polygon.io
  PublisherName: Polygon.io
  ServiceCategory: Fintech
  ServiceName: Polygon.io Market Data API
layout: finops
meters:
- aggregation: sum
  description: Stocks plan monthly subscription.
  dimensions:
  - api_key
  name: stocks_subscription
  unit: month
- aggregation: sum
  description: Options plan monthly subscription (includes OPRA exchange fee on Business).
  dimensions:
  - api_key
  name: options_subscription
  unit: month
- aggregation: sum
  description: Futures plan monthly subscription (CME exchange fees on Business).
  dimensions:
  - api_key
  name: futures_subscription
  unit: month
name: Polygon Io Finops
provider_name: Polygon.io
provider_slug: polygon-io
publisher_name: Polygon.io / Massive
service_category: Fintech
slug: polygon-io-finops
source_filename: polygon-io-finops.yml
source_heading: FinOps Profile
source_url: https://polygon.io/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Polygon.io\nproviderId: polygon-io\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: true\ntags:\n  - Fintech\n  - Market Data\n  - FinOps\n  - FOCUS\ndescription: >-\n  FinOps view of Polygon.io. Subscription-based per asset class with multiple tiers; Business\n  contracts add redistribution and OPRA/CME exchange fees passed through. Customers should\n  budget per-asset-class subscriptions plus exchange data fees on Business plans.\nsources:\n  - https://polygon.io/pricing\n  - https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Polygon.io / Massive\nserviceCategory: Fintech\nbillingModel:\n  pricingCategory: Subscription\n\
  \  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Subscription\n    - Usage\n    - Adjustment\nfocusColumns:\n  ServiceName: Polygon.io Market Data API\n  ServiceCategory: Fintech\n  ProviderName: Polygon.io\n  PublisherName: Polygon.io\n  InvoiceIssuerName: Polygon.io\n  BillingCurrency: USD\n  ChargeCategory: Subscription\nmeters:\n  - name: stocks_subscription\n    description: Stocks plan monthly subscription.\n    unit: month\n    aggregation: sum\n    dimensions:\n      - api_key\n  - name: options_subscription\n    description: Options plan monthly subscription (includes OPRA exchange fee on Business).\n    unit: month\n    aggregation: sum\n    dimensions:\n      - api_key\n  - name: futures_subscription\n    description: Futures plan monthly subscription (CME exchange fees on Business).\n    unit: month\n    aggregation: sum\n    dimensions:\n      - api_key\nprinciples:\n  - name: Visibility\n    description: Tag each Polygon API key to a single\
  \ owning workload to enable accurate allocation.\n  - name: Allocation\n    description: Allocate subscription cost across consuming products; redistribution requires Business plan.\n  - name: Optimization\n    description: Right-size between Starter / Developer / Advanced based on actual rpm and SIP requirements.\n  - name: Accountability\n    description: Assign a billing owner per asset-class subscription; review at renewal.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/polygon-io/refs/heads/main/finops/polygon-io-finops.yml
sources:
- https://polygon.io/pricing
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Fintech
- Market Data
- FinOps
- FOCUS
---
