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
  - Purchase
  - Usage
  - Tax
  - Adjustment
  pricingCategory: Tiered Subscription + Usage
description: 'FOCUS-aligned FinOps for CME Group market data and connectivity: monthly subscriber-based billing for market data (MDP 3.0), per-dataset purchases for CME DataMine, and per-session billing for iLink connectivity. Subscriber reporting and audit obligations apply to market-data licensees.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Chicago Mercantile Exchange Inc.
  PricingCategory: Tiered Subscription
  ProviderName: CME Group
  PublisherName: Chicago Mercantile Exchange Inc.
  ServiceCategory: Market Data / Exchange Connectivity
  ServiceName: CME Group Market Data
layout: finops
meters:
- aggregation: max
  description: Count of professional market-data subscribers for the period.
  dimensions:
  - product
  - distribution_model
  name: professional_subscribers
  unit: seat-month
- aggregation: max
  description: Count of non-professional market-data subscribers for the period.
  dimensions:
  - product
  - distribution_model
  name: non_professional_subscribers
  unit: seat-month
- aggregation: max
  description: Non-display / derived data licenses.
  dimensions:
  - product
  - business_unit
  name: non_display_licenses
  unit: license-month
- aggregation: max
  description: iLink order-entry sessions allocated.
  dimensions:
  - environment
  name: ilink_sessions
  unit: session-month
- aggregation: sum
  description: One-time CME DataMine dataset purchases.
  dimensions:
  - dataset
  - product
  name: datamine_purchases
  unit: dataset
name: Cme Group Finops
provider_name: CME Group
provider_slug: cme-group
publisher_name: Chicago Mercantile Exchange Inc.
service_category: Market Data / Exchange Connectivity
slug: cme-group-finops
source_filename: cme-group-finops.yml
source_heading: FinOps Profile
source_url: https://www.cmegroup.com/market-data/distributors-and-vendors.html
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: CME Group\nproviderId: cme-group\npublisherName: Chicago Mercantile Exchange Inc.\nserviceCategory: Market Data / Exchange Connectivity\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Capital Markets\n  - Market Data\n  - Derivatives\nnotes: CME Group invoices market-data customers under fee schedules tied to subscriber counts (professional\n  / non-professional), distribution model (display / non-display / derived), and session count for iLink.\n  Specific dollar amounts come from PDF fee schedules per program; the meters below capture the typical\n  billing surface but are not reconciled against\
  \ a particular invoice.\ndescription: 'FOCUS-aligned FinOps for CME Group market data and connectivity: monthly subscriber-based\n  billing for market data (MDP 3.0), per-dataset purchases for CME DataMine, and per-session billing for\n  iLink connectivity. Subscriber reporting and audit obligations apply to market-data licensees.'\nsources:\n  - https://www.cmegroup.com/market-data/distributors-and-vendors.html\nbillingModel:\n  pricingCategory: Tiered Subscription + Usage\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\n    - Tax\n    - Adjustment\nfocusColumns:\n  ServiceName: CME Group Market Data\n  ServiceCategory: Market Data / Exchange Connectivity\n  ProviderName: CME Group\n  PublisherName: Chicago Mercantile Exchange Inc.\n  InvoiceIssuerName: Chicago Mercantile Exchange Inc.\n  PricingCategory: Tiered Subscription\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: professional_subscribers\n    description:\
  \ Count of professional market-data subscribers for the period.\n    unit: seat-month\n    aggregation: max\n    dimensions:\n      - product\n      - distribution_model\n  - name: non_professional_subscribers\n    description: Count of non-professional market-data subscribers for the period.\n    unit: seat-month\n    aggregation: max\n    dimensions:\n      - product\n      - distribution_model\n  - name: non_display_licenses\n    description: Non-display / derived data licenses.\n    unit: license-month\n    aggregation: max\n    dimensions:\n      - product\n      - business_unit\n  - name: ilink_sessions\n    description: iLink order-entry sessions allocated.\n    unit: session-month\n    aggregation: max\n    dimensions:\n      - environment\n  - name: datamine_purchases\n    description: One-time CME DataMine dataset purchases.\n    unit: dataset\n    aggregation: sum\n    dimensions:\n      - dataset\n      - product\nprinciples:\n  - name: Visibility\n    description: CME requires\
  \ monthly subscriber reporting from vendors / distributors; reconcile internal\n      entitlement systems against the report submitted to CME.\n  - name: Allocation\n    description: Allocate market-data fees to the trading desk or research team consuming the feed; allocate\n      iLink session fees to the order-routing application.\n  - name: Optimization\n    description: Audit professional vs non-professional classifications, sunset orphan iLink sessions,\n      and consolidate distribution agreements to take advantage of enterprise-licensing terms.\n  - name: Accountability\n    description: Assign a market-data administrator accountable for monthly reporting accuracy; CME audits\n      can result in retroactive fees if subscriber counts are under-reported.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/cme-group/refs/heads/main/finops/cme-group-finops.yml
sources:
- https://www.cmegroup.com/market-data/distributors-and-vendors.html
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Capital Markets
- Market Data
- Derivatives
---
