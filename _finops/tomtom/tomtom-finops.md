---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: tomtom-maps-openapi.yml
  format: yaml
  label: TomTom Maps API
  slug: tomtom-maps-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/tomtom/refs/heads/main/openapi/tomtom-maps-openapi.yml
- filename: tomtom-search-openapi.yml
  format: yaml
  label: TomTom Search API
  slug: tomtom-search-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/tomtom/refs/heads/main/openapi/tomtom-search-openapi.yml
- filename: tomtom-routing-openapi.yml
  format: yaml
  label: TomTom Routing API
  slug: tomtom-routing-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/tomtom/refs/heads/main/openapi/tomtom-routing-openapi.yml
- filename: tomtom-traffic-openapi.yml
  format: yaml
  label: TomTom Traffic API
  slug: tomtom-traffic-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/tomtom/refs/heads/main/openapi/tomtom-traffic-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  pricingCategory: Freemium + Pay-Per-1000 + Enterprise
description: FOCUS-aligned FinOps for TomTom.
focus_columns:
  BillingCurrency: USD
  ProviderName: TomTom
  PublisherName: TomTom
  ServiceCategory: Maps
  ServiceName: TomTom
layout: finops
meters:
- aggregation: sum
  name: tile_requests
  unit: request
- aggregation: sum
  name: non_tile_requests
  unit: request
- aggregation: sum
  name: search_requests
  unit: request
- aggregation: sum
  name: routing_requests
  unit: request
name: Tomtom Finops
provider_name: TomTom
provider_slug: tomtom
publisher_name: TomTom
service_category: Maps
slug: tomtom-finops
source_filename: tomtom-finops.yml
source_heading: FinOps Profile
source_url: https://developer.tomtom.com/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: TomTom\nproviderId: tomtom\ncreated: '2026-05-04'\nmodified: '2026-05-04'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Maps\ndescription: FOCUS-aligned FinOps for TomTom.\nsources:\n  - https://developer.tomtom.com/pricing\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: TomTom\nserviceCategory: Maps\nbillingModel:\n  pricingCategory: Freemium + Pay-Per-1000 + Enterprise\n  billingFrequency: Monthly\n  billingCurrency: USD\nfocusColumns:\n  ServiceName: TomTom\n  ServiceCategory: Maps\n  ProviderName: TomTom\n  PublisherName: TomTom\n  BillingCurrency: USD\nmeters:\n  - name: tile_requests\n    unit: request\n    aggregation: sum\n  - name: non_tile_requests\n    unit: request\n\
  \    aggregation: sum\n  - name: search_requests\n    unit: request\n    aggregation: sum\n  - name: routing_requests\n    unit: request\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Track TomTom consumption monthly.\n  - name: Allocation\n    description: Tag usage to teams/cost centers.\n  - name: Optimization\n    description: Right-size; reclaim unused entitlements.\n  - name: Accountability\n    description: Set spend alerts; quarterly review.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/tomtom/refs/heads/main/finops/tomtom-finops.yml
sources:
- https://developer.tomtom.com/pricing
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Maps
---
