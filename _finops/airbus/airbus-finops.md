---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: EUR
  billingFrequency: Per-Invoice
  chargeCategories:
  - Purchase
  - Usage
  pricingCategory: Hybrid
description: Airbus OneAtlas combines fixed-fee subscriptions (Living Library) with consumption-based pay-per-order pricing on archive and tasking imagery, and enterprise / defense contracts. The metered units are area (square kilometres) for archive / Living Library and acquisitions for tasking. Public pricing is gated, so the FinOps mapping is structural.
focus_columns:
  BillingCurrency: EUR
  InvoiceIssuerName: Airbus Defence and Space SAS
  ProviderName: Airbus
  PublisherName: Airbus Defence and Space SAS
  ServiceCategory: Earth Observation / Satellite Imagery
  ServiceName: Airbus OneAtlas
layout: finops
meters:
- aggregation: sum
  description: Square kilometres of AOI streamed or downloaded from the Living Library under subscription.
  dimensions:
  - product
  - constellation
  name: living_library_sqkm
  unit: sqkm
- aggregation: sum
  description: Square kilometres of imagery purchased on a pay-per-order basis from the archive.
  dimensions:
  - product
  - constellation
  - acquisition_date
  name: archive_order_sqkm
  unit: sqkm
- aggregation: sum
  description: Tasking acquisitions ordered on a pay-per-order basis, priced per acquisition and per priority tier.
  dimensions:
  - constellation
  - priority
  name: tasking_acquisition
  unit: acquisition
- aggregation: sum
  description: Tile / API calls against the OneAtlas Basemap service under the relevant plan.
  dimensions:
  - region
  name: basemap_tiles
  unit: tile
name: Airbus Finops
provider_name: Airbus
provider_slug: airbus
publisher_name: Airbus Defence and Space SAS
service_category: Earth Observation / Satellite Imagery
slug: airbus-finops
source_filename: airbus-finops.yml
source_heading: FinOps Profile
source_url: https://api.oneatlas.airbus.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Airbus\nproviderId: airbus\ncreated: '2026-05-16'\nmodified: '2026-05-16'\nreconciled: false\ntags:\n  - Aerospace\n  - Earth Observation\n  - FinOps\n  - FOCUS\ndescription: Airbus OneAtlas combines fixed-fee subscriptions (Living Library) with consumption-based pay-per-order pricing on archive and tasking imagery, and enterprise / defense contracts. The metered units are area (square kilometres) for archive / Living Library and acquisitions for tasking. Public pricing is gated, so the FinOps mapping is structural.\nnotes: Unit prices are gated behind sales; FinOps mapping documents the billing surface but cannot be reconciled to a public rate card.\nsources:\n  - https://api.oneatlas.airbus.com/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl:\
  \ https://focus.finops.org/focus-specification/v1-3/\npublisherName: Airbus Defence and Space SAS\nserviceCategory: Earth Observation / Satellite Imagery\nbillingModel:\n  pricingCategory: Hybrid\n  billingFrequency: Per-Invoice\n  billingCurrency: EUR\n  chargeCategories:\n    - Purchase\n    - Usage\nfocusColumns:\n  ServiceName: Airbus OneAtlas\n  ServiceCategory: Earth Observation / Satellite Imagery\n  ProviderName: Airbus\n  PublisherName: Airbus Defence and Space SAS\n  InvoiceIssuerName: Airbus Defence and Space SAS\n  BillingCurrency: EUR\nmeters:\n  - name: living_library_sqkm\n    description: Square kilometres of AOI streamed or downloaded from the Living Library under subscription.\n    unit: sqkm\n    aggregation: sum\n    dimensions:\n      - product\n      - constellation\n  - name: archive_order_sqkm\n    description: Square kilometres of imagery purchased on a pay-per-order basis from the archive.\n    unit: sqkm\n    aggregation: sum\n    dimensions:\n      - product\n\
  \      - constellation\n      - acquisition_date\n  - name: tasking_acquisition\n    description: Tasking acquisitions ordered on a pay-per-order basis, priced per acquisition and per priority tier.\n    unit: acquisition\n    aggregation: sum\n    dimensions:\n      - constellation\n      - priority\n  - name: basemap_tiles\n    description: Tile / API calls against the OneAtlas Basemap service under the relevant plan.\n    unit: tile\n    aggregation: sum\n    dimensions:\n      - region\nprinciples:\n  - name: Visibility\n    description: Track OneAtlas spend by product (Living Library / Pay-Per-Order Archives / Tasking / Basemap / Radar & Elevation) and by AOI.\n  - name: Allocation\n    description: Allocate OneAtlas cost to the analyst team / project consuming the AOI; tag orders with project codes during ordering.\n  - name: Optimization\n    description: Optimize by preferring Living Library streaming for repeat AOIs, batching archive orders, and aligning tasking priority with\
  \ operational SLAs.\n  - name: Accountability\n    description: GIS / geospatial leadership owns the OneAtlas subscription; project owners are accountable for pay-per-order spend within their AOI envelope.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/airbus/refs/heads/main/finops/airbus-finops.yml
sources:
- https://api.oneatlas.airbus.com/
specification: FinOps Framework
tags:
- Aerospace
- Earth Observation
- FinOps
- FOCUS
---
