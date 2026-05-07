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
  pricingCategory: Usage-Based
description: 'FOCUS-aligned FinOps for Mapbox: per-product metered usage with free allocations.'
focus_columns:
  BillingCurrency: USD
  ProviderName: Mapbox
  PublisherName: Mapbox Inc.
  ServiceCategory: Location Services
  ServiceName: Mapbox
layout: finops
meters:
- aggregation: sum
  name: map_loads_web
  unit: load
- aggregation: max
  name: mau_mobile
  unit: MAU
- aggregation: sum
  name: static_image_requests
  unit: request
- aggregation: sum
  name: directions_requests
  unit: request
- aggregation: sum
  name: geocoding_requests
  unit: request
- aggregation: sum
  name: search_box_sessions
  unit: session
- aggregation: sum
  name: navigation_trips
  unit: trip
name: Mapbox Finops
provider_name: Mapbox
provider_slug: mapbox
publisher_name: Mapbox Inc.
service_category: Location Services
slug: mapbox-finops
source_filename: mapbox-finops.yml
source_heading: FinOps Profile
source_url: https://www.mapbox.com/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Mapbox\nproviderId: mapbox\ncreated: '2026-05-04'\nmodified: '2026-05-04'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Maps\ndescription: 'FOCUS-aligned FinOps for Mapbox: per-product metered usage with free allocations.'\nsources:\n  - https://www.mapbox.com/pricing\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Mapbox Inc.\nserviceCategory: Location Services\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\nfocusColumns:\n  ServiceName: Mapbox\n  ServiceCategory: Location Services\n  ProviderName: Mapbox\n  PublisherName: Mapbox Inc.\n  BillingCurrency: USD\nmeters:\n  - name: map_loads_web\n    unit: load\n    aggregation:\
  \ sum\n  - name: mau_mobile\n    unit: MAU\n    aggregation: max\n  - name: static_image_requests\n    unit: request\n    aggregation: sum\n  - name: directions_requests\n    unit: request\n    aggregation: sum\n  - name: geocoding_requests\n    unit: request\n    aggregation: sum\n  - name: search_box_sessions\n    unit: session\n    aggregation: sum\n  - name: navigation_trips\n    unit: trip\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Use Statistics API for per-token per-product usage daily.\n  - name: Allocation\n    description: Use distinct access tokens per app/feature for chargeback.\n  - name: Optimization\n    description: Cache tile responses where licenses permit; pick metered vs unlimited Navigation by trip-volume\n      crossover.\n  - name: Accountability\n    description: Set spend alerts at $X per token; revoke unused tokens.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/mapbox/refs/heads/main/finops/mapbox-finops.yml
sources:
- https://www.mapbox.com/pricing
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Maps
---
