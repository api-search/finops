---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  - Tax
  - Adjustment
  chargeFrequency: Recurring
  pricingCategory: Subscription
description: 'FOCUS-aligned FinOps placeholder for Hallmark Cards: no public commercial API. The shape below treats partner integration as a contract-bundled subscription with allocation meters for retail / supply-chain integration.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Hallmark Cards, Inc.
  PricingCategory: Subscription
  PricingUnit: partner-agreement
  ProviderName: Hallmark Cards
  PublisherName: Hallmark Cards, Inc.
  ServiceCategory: Retail / Consumer Goods Partner API
  ServiceName: Hallmark Cards API
layout: finops
meters:
- aggregation: sum
  description: Partner-integration request volume (allocation meter)
  dimensions:
  - partner
  - channel
  - endpoint
  name: api_requests
  unit: request
- aggregation: sum
  description: Order / fulfillment events synced via the API
  dimensions:
  - partner
  - channel
  name: orders_synced
  unit: order
name: Hallmark Cards Finops
provider_name: Hallmark Cards
provider_slug: hallmark-cards
publisher_name: Hallmark Cards, Inc.
service_category: Retail / Consumer Goods Partner API
slug: hallmark-cards-finops
source_filename: hallmark-cards-finops.yml
source_heading: FinOps Profile
source_url: https://www.hallmark.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Hallmark Cards\nproviderId: hallmark-cards\npublisherName: Hallmark Cards, Inc.\nserviceCategory: Retail / Consumer Goods Partner API\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Greeting Cards\n  - Gift\n  - Retail\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps placeholder for Hallmark Cards: no public commercial API. The\n  shape below treats partner integration as a contract-bundled subscription with allocation meters\n  for retail / supply-chain integration.'\nnotes: No public commercial model is published. Reconcile against an actual partner agreement.\nsources:\n  - https://www.hallmark.com/\n\
  principles:\n  - name: Visibility\n    description: Track partner-integration request volume via the Hallmark partner gateway logs.\n  - name: Allocation\n    description: Allocate integration cost across retail channels (own-brand stores, big-box,\n      e-commerce) using the calling system identifier.\n  - name: Optimization\n    description: Cache catalog and inventory lookups; batch order updates; consolidate retailer\n      integrations through a single channel.\n  - name: Accountability\n    description: Designate a partner-program owner; review API utilization quarterly.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting\
  \ for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Subscription\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Tax\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Hallmark Cards API\n  ServiceCategory: Retail / Consumer Goods Partner API\n  ProviderName: Hallmark Cards\n  PublisherName: Hallmark Cards, Inc.\n  InvoiceIssuerName: Hallmark Cards, Inc.\n  PricingCategory: Subscription\n  PricingUnit: partner-agreement\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: api_requests\n    description: Partner-integration request volume (allocation meter)\n\
  \    unit: request\n    aggregation: sum\n    dimensions:\n      - partner\n      - channel\n      - endpoint\n  - name: orders_synced\n    description: Order / fulfillment events synced via the API\n    unit: order\n    aggregation: sum\n    dimensions:\n      - partner\n      - channel\napis:\n  - name: Hallmark Cards API\n    baseURL: https://api.hallmark.com\n    tags:\n      - Greeting Cards\n      - Gift\n      - Retail\n    serviceName: Hallmark Cards API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per Partner Integration\n    metric: billed_cost / active_partners\n    target: TBD\n  - name: Cost per Order Synced\n    metric: billed_cost / orders_synced\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/hallmark-cards/refs/heads/main/finops/hallmark-cards-finops.yml
sources:
- https://www.hallmark.com/
specification: FinOps Framework
tags:
- Greeting Cards
- Gift
- Retail
- FinOps
- Cost Management
- FOCUS
---
