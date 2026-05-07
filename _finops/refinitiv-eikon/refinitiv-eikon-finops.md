---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: swagger.yaml
  format: yaml
  label: Refinitiv Data Platform APIs
  slug: ''
  spec_type: OpenAPI
  url: https://api.refinitiv.com/streaming-pricing/docs/swagger.yaml
billing_model:
  billingCurrency: USD (settlement varies)
  billingFrequency: Monthly
  chargeCategories:
  - Purchase
  pricingCategory: Subscription
description: FinOps shape for Refinitiv Eikon, retired June 30, 2025 and superseded by LSEG Workspace. Spend is per-seat subscription via the LSEG contract; there is no usage-based meter to reconcile.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: London Stock Exchange Group plc
  ProviderName: LSEG
  PublisherName: London Stock Exchange Group plc
  ServiceCategory: Market Data
  ServiceName: Refinitiv Eikon
layout: finops
meters:
- aggregation: sum
  dimensions:
  - entitlement
  name: licensed_users
  unit: seat
name: Refinitiv Eikon Finops
provider_name: Refinitiv Eikon
provider_slug: refinitiv-eikon
publisher_name: London Stock Exchange Group plc
service_category: Market Data
slug: refinitiv-eikon-finops
source_filename: refinitiv-eikon-finops.yml
source_heading: FinOps Profile
source_url: https://www.lseg.com/en/data-analytics/products/eikon-trading-software
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Refinitiv Eikon\nproviderId: refinitiv-eikon\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Financial Data\n  - Market Data\ndescription: FinOps shape for Refinitiv Eikon, retired June 30, 2025 and superseded by LSEG Workspace.\n  Spend is per-seat subscription via the LSEG contract; there is no usage-based meter to reconcile.\nsources:\n  - https://www.lseg.com/en/data-analytics/products/eikon-trading-software\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: London Stock Exchange Group plc\nserviceCategory: Market Data\nbillingModel:\n  pricingCategory: Subscription\n  billingFrequency: Monthly\n  billingCurrency: USD (settlement\
  \ varies)\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: Refinitiv Eikon\n  ServiceCategory: Market Data\n  ProviderName: LSEG\n  PublisherName: London Stock Exchange Group plc\n  InvoiceIssuerName: London Stock Exchange Group plc\n  BillingCurrency: USD\nmeters:\n  - name: licensed_users\n    unit: seat\n    aggregation: sum\n    dimensions:\n      - entitlement\nprinciples:\n  - name: Visibility\n    description: Visibility comes from the LSEG monthly invoice and the entitlement report listing active\n      Eikon/Workspace seats; no API-level usage meter is exposed.\n  - name: Allocation\n    description: Allocate per licensed user (trader, analyst, RM); map each seat to a cost center in\n      the entitlement system.\n  - name: Optimization\n    description: Optimization is seat hygiene — reclaim seats from inactive users, migrate from Eikon\n      to LSEG Workspace before contract renewal, and right-size data-set entitlements.\n  - name: Accountability\n    description:\
  \ Owner is the market-data licensing administrator who manages LSEG entitlements; renewals\n      and seat changes flow through that role.\nnotes: Per-seat subscription only; no API request meter exists. Generic FOCUS request meters and per-call\n  dimensions removed.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/refinitiv-eikon/refs/heads/main/finops/refinitiv-eikon-finops.yml
sources:
- https://www.lseg.com/en/data-analytics/products/eikon-trading-software
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Financial Data
- Market Data
---
