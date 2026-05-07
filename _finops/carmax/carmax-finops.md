---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: Per-Invoice
  chargeCategories:
  - Purchase
  - Adjustment
  pricingCategory: Bundled / Custom Partner Agreement
description: 'FOCUS-aligned FinOps for CarMax: APIs are consumed internally by CarMax clients and selectively exposed to syndication partners; no public API billing surface exists.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: CarMax, Inc.
  ProviderName: CarMax
  PublisherName: CarMax, Inc.
  ServiceCategory: Auto Retail / Vehicle Inventory
  ServiceName: CarMax Inventory and Locations
layout: finops
meters:
- aggregation: sum
  dimensions:
  - api
  - partner
  name: api_requests
  unit: request
- aggregation: sum
  dimensions:
  - partner
  name: vehicle_listings_synced
  unit: listing
- aggregation: sum
  name: store_location_lookups
  unit: lookup
name: Carmax Finops
provider_name: CarMax
provider_slug: carmax
publisher_name: CarMax, Inc.
service_category: Auto Retail / Vehicle Inventory
slug: carmax-finops
source_filename: carmax-finops.yml
source_heading: FinOps Profile
source_url: https://www.carmax.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: CarMax\nproviderId: carmax\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Automotive\n  - Used Cars\n  - Retail\ndescription: 'FOCUS-aligned FinOps for CarMax: APIs are consumed internally by CarMax clients and selectively\n  exposed to syndication partners; no public API billing surface exists.'\nnotes: CarMax does not bill API access as a metered external service. FinOps framing is informational\n  for partner/syndication relationships.\nsources:\n  - https://www.carmax.com/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: CarMax, Inc.\nserviceCategory: Auto Retail / Vehicle Inventory\nbillingModel:\n  pricingCategory: Bundled\
  \ / Custom Partner Agreement\n  billingFrequency: Per-Invoice\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Adjustment\nfocusColumns:\n  ServiceName: CarMax Inventory and Locations\n  ServiceCategory: Auto Retail / Vehicle Inventory\n  ProviderName: CarMax\n  PublisherName: CarMax, Inc.\n  InvoiceIssuerName: CarMax, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: api_requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - partner\n  - name: vehicle_listings_synced\n    unit: listing\n    aggregation: sum\n    dimensions:\n      - partner\n  - name: store_location_lookups\n    unit: lookup\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Visibility into syndication traffic comes from CarMax engineering reporting; no consumer-facing\n      usage API exists.\n  - name: Allocation\n    description: Allocate by syndication partner credential and by listing surface (web, mobile, partner site).\n  - name: Optimization\n\
  \    description: Cache Store Locations and Vehicle Inventory responses; honor freshness windows recommended\n      by CarMax to avoid redundant calls.\n  - name: Accountability\n    description: Syndication / partner-marketing owner holds the relationship; quarterly traffic and\n      conversion reviews with CarMax are typical.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/carmax/refs/heads/main/finops/carmax-finops.yml
sources:
- https://www.carmax.com/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Automotive
- Used Cars
- Retail
---
