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
  pricingCategory: Subscription + Commission
description: FinOps view of Tradier billing. Customers fund a brokerage account; revenue is per-contract options commissions, monthly subscription on the Stocks + Options plan, and market-data fees. API access is bundled with the brokerage relationship.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Subscription
  InvoiceIssuerName: Tradier
  ProviderName: Tradier
  PublisherName: Tradier Brokerage Inc.
  ServiceCategory: Fintech
  ServiceName: Tradier Brokerage and Streaming API
layout: finops
meters:
- aggregation: sum
  description: Per-contract option commission.
  dimensions:
  - account
  name: option_contract
  unit: contract
- aggregation: sum
  description: Stocks + Options plan monthly fee.
  dimensions:
  - account
  name: monthly_subscription
  unit: month
- aggregation: sum
  description: Optional real-time market data subscription.
  dimensions:
  - account
  name: market_data
  unit: month
name: Tradier Finops
provider_name: Tradier
provider_slug: tradier
publisher_name: Tradier Brokerage Inc.
service_category: Fintech
slug: tradier-finops
source_filename: tradier-finops.yml
source_heading: FinOps Profile
source_url: https://tradier.com/individuals/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Tradier\nproviderId: tradier\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: true\ntags:\n  - Fintech\n  - Trading\n  - Brokerage\n  - FinOps\n  - FOCUS\ndescription: >-\n  FinOps view of Tradier billing. Customers fund a brokerage account; revenue is per-contract\n  options commissions, monthly subscription on the Stocks + Options plan, and market-data fees.\n  API access is bundled with the brokerage relationship.\nsources:\n  - https://tradier.com/individuals/pricing\n  - https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Tradier Brokerage Inc.\nserviceCategory: Fintech\nbillingModel:\n  pricingCategory: Subscription\
  \ + Commission\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Subscription\n    - Usage\n    - Adjustment\nfocusColumns:\n  ServiceName: Tradier Brokerage and Streaming API\n  ServiceCategory: Fintech\n  ProviderName: Tradier\n  PublisherName: Tradier Brokerage Inc.\n  InvoiceIssuerName: Tradier\n  BillingCurrency: USD\n  ChargeCategory: Subscription\nmeters:\n  - name: option_contract\n    description: Per-contract option commission.\n    unit: contract\n    aggregation: sum\n    dimensions:\n      - account\n  - name: monthly_subscription\n    description: Stocks + Options plan monthly fee.\n    unit: month\n    aggregation: sum\n    dimensions:\n      - account\n  - name: market_data\n    description: Optional real-time market data subscription.\n    unit: month\n    aggregation: sum\n    dimensions:\n      - account\nprinciples:\n  - name: Visibility\n    description: Pull monthly brokerage statements and treat them as the cost-of-API-usage feed.\n\
  \  - name: Allocation\n    description: Allocate commissions and subscription fees to the desk consuming the API.\n  - name: Optimization\n    description: Compare per-contract cost vs trading volume; consider TradierPRO if option flow is heavy.\n  - name: Accountability\n    description: Assign a billing owner for the brokerage relationship and review at renewal.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/tradier/refs/heads/main/finops/tradier-finops.yml
sources:
- https://tradier.com/individuals/pricing
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Fintech
- Trading
- Brokerage
- FinOps
- FOCUS
---
