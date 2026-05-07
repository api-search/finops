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
  - Usage
  - Tax
  - Adjustment
  chargeFrequency: Recurring
  pricingCategory: Subscription + Per-Asset (per enterprise agreement)
description: FOCUS-aligned FinOps stub for Honeywell. Enterprise subscription plus per-connected-asset metering, with rates set in the Master Services Agreement.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Honeywell International Inc.
  PricingCategory: Subscription + Per-Asset
  PricingUnit: asset
  ProviderName: Honeywell International Inc.
  PublisherName: Honeywell International Inc.
  ServiceCategory: Industrial IoT / Building Automation / Aerospace
  ServiceName: Honeywell Forge / Connected Enterprise
layout: finops
meters:
- aggregation: max
  description: Number of connected industrial / building / aerospace assets under management
  dimensions:
  - tenant
  - site
  - asset_type
  name: connected_assets
  unit: asset
- aggregation: sum
  description: Volume of telemetry ingested into Forge
  dimensions:
  - tenant
  - site
  - asset_type
  name: ingested_telemetry
  unit: GB
- aggregation: sum
  description: Annual subscription fee for Forge / Connected Enterprise modules
  dimensions:
  - tenant
  - module
  name: subscription_fee
  unit: year
- aggregation: sum
  description: Honeywell Professional Services engagements
  dimensions:
  - tenant
  - engagement
  name: professional_services
  unit: hour
name: Honeywell Finops
provider_name: Honeywell
provider_slug: honeywell
publisher_name: Honeywell International Inc.
service_category: Industrial IoT / Building Automation / Aerospace
slug: honeywell-finops
source_filename: honeywell-finops.yml
source_heading: FinOps Profile
source_url: https://www.honeywell.com/us/en
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Honeywell\nproviderId: honeywell\npublisherName: Honeywell International Inc.\nserviceCategory: Industrial IoT / Building Automation / Aerospace\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Aerospace\n  - Building Automation\n  - Industrial IoT\n  - Manufacturing\n  - FinOps\n  - FOCUS\nnotes: Honeywell sells industrial / building / aerospace SaaS (Honeywell Forge, Connected Enterprise) on\n  enterprise contracts. The FinOps shape is annual subscription + per-connected-asset fees + optional\n  professional services. Meters below capture this shape; rates are bilateral and not publicly disclosed.\ndescription: 'FOCUS-aligned FinOps stub for Honeywell. Enterprise\
  \ subscription plus per-connected-asset\n  metering, with rates set in the Master Services Agreement.'\nsources:\n  - https://www.honeywell.com/us/en\nbillingModel:\n  pricingCategory: Subscription + Per-Asset (per enterprise agreement)\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\n    - Tax\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Honeywell Forge / Connected Enterprise\n  ServiceCategory: Industrial IoT / Building Automation / Aerospace\n  ProviderName: Honeywell International Inc.\n  PublisherName: Honeywell International Inc.\n  InvoiceIssuerName: Honeywell International Inc.\n  PricingCategory: Subscription + Per-Asset\n  PricingUnit: asset\n  BillingCurrency: USD\n  ChargeCategory: Usage\nprinciples:\n  - name: Visibility\n    description: Use Honeywell Forge dashboards, exports, and connected-asset inventory APIs to track\n      asset count, ingestion volume, and module utilization. Reconcile\
  \ against the annual entitlement.\n  - name: Allocation\n    description: Allocate Forge spend by site, building, plant, or tail number using the asset hierarchy\n      that drives the contract's per-asset billing line.\n  - name: Optimization\n    description: Levers are deactivating unused assets / sites at renewal, consolidating Forge modules\n      to bundle pricing, and tuning data ingestion intervals to stay within the entitlement tier.\n  - name: Accountability\n    description: Site / facility owners are accountable for their connected-asset footprint; central\n      IT / OT owns the master agreement and renewal calendar.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize\
  \ Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nmeters:\n  - name: connected_assets\n    description: Number of connected industrial / building / aerospace assets under management\n    unit: asset\n    aggregation: max\n    dimensions:\n      - tenant\n      - site\n      - asset_type\n  - name: ingested_telemetry\n    description: Volume of telemetry ingested into Forge\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - tenant\n      - site\n      - asset_type\n  - name: subscription_fee\n    description: Annual subscription fee for Forge / Connected Enterprise modules\n    unit: year\n    aggregation: sum\n    dimensions:\n      - tenant\n      - module\n  - name: professional_services\n\
  \    description: Honeywell Professional Services engagements\n    unit: hour\n    aggregation: sum\n    dimensions:\n      - tenant\n      - engagement\napis:\n  - name: Honeywell Forge\n    baseURL: ''\n    tags:\n      - Building Automation\n      - Industrial IoT\n      - Manufacturing\n    serviceName: Honeywell Forge\n    serviceCategory: Industrial IoT / Building Automation / Aerospace\nunitEconomics:\n  - name: Cost per Connected Asset\n    metric: subscription_fee / connected_assets\n    target: per enterprise agreement\n  - name: Cost per Site\n    metric: subscription_fee / sites\n    target: per enterprise agreement\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/honeywell/refs/heads/main/finops/honeywell-finops.yml
sources:
- https://www.honeywell.com/us/en
specification: FinOps Framework
tags:
- Aerospace
- Building Automation
- Industrial IoT
- Manufacturing
- FinOps
- FOCUS
---
