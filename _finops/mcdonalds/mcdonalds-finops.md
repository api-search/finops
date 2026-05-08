---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD (settlement varies by market)
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  - Adjustment
  - Credit
  pricingCategory: Partner Commission + Per-Store Technology Fees
description: 'FOCUS-aligned FinOps shape for McDonald''s: bilateral partner integrations (delivery marketplaces, POS, loyalty). Costs flow through partnership economics (per-order commission, per-store technology fees) rather than per-API-call billing.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: McDonald's Corporation
  ProviderName: McDonald's
  PublisherName: McDonald's Corporation
  ServiceCategory: Restaurant Marketplace
  ServiceName: McDonald's Partner / Marketplace Integration
layout: finops
meters:
- aggregation: sum
  description: Orders processed through a given channel (mobile, drive-thru, kiosk, marketplace).
  dimensions:
  - channel
  - market
  - store
  name: orders_processed
  unit: order
- aggregation: sum
  description: Commission paid to delivery marketplaces per fulfilled order.
  dimensions:
  - marketplace
  - market
  - store
  name: marketplace_commission
  unit: USD
- aggregation: avg
  description: Active stores integrated with the relevant partner system.
  dimensions:
  - market
  - ownership
  - partner
  name: stores_active
  unit: store-month
- aggregation: avg
  description: Active MyMcDonald's loyalty members in the period.
  dimensions:
  - market
  name: loyalty_members_active
  unit: member-month
name: Mcdonalds Finops
provider_name: McDonald's
provider_slug: mcdonalds
publisher_name: McDonald's Corporation
service_category: Restaurant / Marketplace Integration
slug: mcdonalds-finops
source_filename: mcdonalds-finops.yml
source_heading: FinOps Profile
source_url: https://corporate.mcdonalds.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: McDonald's\nproviderId: mcdonalds\npublisherName: McDonald's Corporation\nserviceCategory: Restaurant / Marketplace Integration\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Delivery\n  - Fast Food\n  - Ordering\n  - Restaurants\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps shape for McDonald''s: bilateral partner integrations (delivery\n  marketplaces, POS, loyalty). Costs flow through partnership economics (per-order commission, per-store\n  technology fees) rather than per-API-call billing.'\nnotes: |\n  No public per-API pricing. Meters represent partnership economic units (orders, stores, marketplace\n\
  \  commission) rather than API requests.\nsources:\n  - https://corporate.mcdonalds.com/\nprinciples:\n  - name: Visibility\n    description: Track per-channel order volume (drive-thru, mobile order, marketplace delivery, kiosk)\n      via the McDonald's Global Mobile App and POS analytics; reconcile marketplace orders against\n      DoorDash / Uber Eats / Grubhub partner statements.\n  - name: Allocation\n    description: Allocate by ownership (corporate-owned vs franchisee), market, and channel. For franchisees,\n      allocate technology and integration costs to the operating company; for marketplace orders, allocate\n      commission to the order's source channel.\n  - name: Optimization\n    description: Optimize per-order commission via direct-to-consumer (Mobile Order & Pay, MyMcDonald's\n      loyalty) where margin is higher than marketplace, negotiate marketplace rates at volume, and\n      consolidate POS / kiosk vendor count to reduce per-store technology spend.\n  - name: Accountability\n\
  \    description: Assign owners per channel (mobile, delivery, in-store) who track contribution margin\n      and review partnership terms with marketplaces annually.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Budgeting\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Workload Optimization\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - Invoicing and Chargeback\n      - Onboarding Workloads\nbillingModel:\n  pricingCategory: Partner Commission + Per-Store Technology Fees\n  billingFrequency: Monthly\n  billingCurrency: USD (settlement varies by market)\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Adjustment\n    - Credit\nfocusColumns:\n  ServiceName: McDonald's Partner / Marketplace Integration\n\
  \  ServiceCategory: Restaurant Marketplace\n  ProviderName: McDonald's\n  PublisherName: McDonald's Corporation\n  InvoiceIssuerName: McDonald's Corporation\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: orders_processed\n    description: Orders processed through a given channel (mobile, drive-thru, kiosk, marketplace).\n    unit: order\n    aggregation: sum\n    dimensions:\n      - channel\n      - market\n      - store\n  - name: marketplace_commission\n    description: Commission paid to delivery marketplaces per fulfilled order.\n    unit: USD\n    aggregation: sum\n    dimensions:\n      - marketplace\n      - market\n      - store\n  - name: stores_active\n    description: Active stores integrated with the relevant partner system.\n    unit: store-month\n    aggregation: avg\n    dimensions:\n      - market\n      - ownership\n      - partner\n  - name: loyalty_members_active\n    description: Active MyMcDonald's loyalty members in the period.\n    unit: member-month\n\
  \    aggregation: avg\n    dimensions:\n      - market\napis:\n  - name: McDonald's API\n    baseURL: https://api.mcdonalds.com\n    tags:\n      - Delivery\n      - Fast Food\n      - Ordering\n      - Restaurants\n    serviceName: McDonald's API\n    serviceCategory: API\nunitEconomics:\n  - name: Marketplace Commission per Order\n    metric: marketplace_commission / orders_processed\n    target: TBD\n  - name: Cost per Active Loyalty Member\n    metric: program_cost / loyalty_members_active\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/mcdonalds/refs/heads/main/finops/mcdonalds-finops.yml
sources:
- https://corporate.mcdonalds.com/
specification: FinOps Framework
tags:
- Delivery
- Fast Food
- Ordering
- Restaurants
- FinOps
- FOCUS
---
