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
  - Adjustment
  pricingCategory: Subscription + Per-Asset
description: 'FOCUS-aligned FinOps for Carrier Global: per-asset and per-building digital subscriptions (Lynx Fleet, Abound, i-Vu) bundled with hardware and dealer-network commercial agreements.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Carrier Global Corporation
  ProviderName: Carrier Global
  PublisherName: Carrier Global Corporation
  ServiceCategory: HVAC / IoT Platform
  ServiceName: Carrier Digital Platforms
layout: finops
meters:
- aggregation: max
  dimensions:
  - asset_type
  - region
  name: lynx_assets
  unit: asset-month
- aggregation: max
  dimensions:
  - region
  name: abound_buildings
  unit: building-month
- aggregation: max
  name: ivu_sites
  unit: site-year
- aggregation: sum
  dimensions:
  - api
  - tenant
  name: api_requests
  unit: request
- aggregation: sum
  dimensions:
  - api
  name: telemetry_volume
  unit: GB
name: Carrier Global Finops
provider_name: Carrier Global
provider_slug: carrier-global
publisher_name: Carrier Global Corporation
service_category: HVAC / IoT Platform
slug: carrier-global-finops
source_filename: carrier-global-finops.yml
source_heading: FinOps Profile
source_url: https://www.corporate.carrier.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Carrier Global\nproviderId: carrier-global\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - HVAC\n  - IoT\n  - Telematics\n  - Building Automation\ndescription: 'FOCUS-aligned FinOps for Carrier Global: per-asset and per-building digital subscriptions\n  (Lynx Fleet, Abound, i-Vu) bundled with hardware and dealer-network commercial agreements.'\nnotes: Carrier does not bill API access as a separate SKU. FinOps mapping is provisional; reconcile against\n  the customer's Lynx / Abound / i-Vu commercial agreement.\nsources:\n  - https://www.corporate.carrier.com/\n  - https://doc-api.fleet.lynx.carrier.io/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\n\
  publisherName: Carrier Global Corporation\nserviceCategory: HVAC / IoT Platform\nbillingModel:\n  pricingCategory: Subscription + Per-Asset\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\n    - Adjustment\nfocusColumns:\n  ServiceName: Carrier Digital Platforms\n  ServiceCategory: HVAC / IoT Platform\n  ProviderName: Carrier Global\n  PublisherName: Carrier Global Corporation\n  InvoiceIssuerName: Carrier Global Corporation\n  BillingCurrency: USD\nmeters:\n  - name: lynx_assets\n    unit: asset-month\n    aggregation: max\n    dimensions:\n      - asset_type\n      - region\n  - name: abound_buildings\n    unit: building-month\n    aggregation: max\n    dimensions:\n      - region\n  - name: ivu_sites\n    unit: site-year\n    aggregation: max\n  - name: api_requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - tenant\n  - name: telemetry_volume\n    unit: GB\n    aggregation: sum\n    dimensions:\n\
  \      - api\nprinciples:\n  - name: Visibility\n    description: Visibility comes from the Lynx Fleet / Abound dashboards (asset count, alarms, telemetry\n      volume); no separate API billing dashboard.\n  - name: Allocation\n    description: Allocate by asset (TRU), building, or site; multi-fleet operators should configure separate\n      Lynx tenants per business unit.\n  - name: Optimization\n    description: Decommission inactive assets to reduce per-asset subscription burn; tune alarm and telemetry\n      cadence to avoid redundant data ingestion.\n  - name: Accountability\n    description: Fleet-operations / facilities-management owner holds the relationship; quarterly asset\n      and renewal reviews with the Carrier dealer network are typical.\nmaintainers:\n  - FN: Kin Lane\n    email: info@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/carrier-global/refs/heads/main/finops/carrier-global-finops.yml
sources:
- https://www.corporate.carrier.com/
- https://doc-api.fleet.lynx.carrier.io/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- HVAC
- IoT
- Telematics
- Building Automation
---
