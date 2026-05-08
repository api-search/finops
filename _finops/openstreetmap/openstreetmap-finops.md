---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: openstreetmap-main-openapi.yml
  format: yaml
  label: OpenStreetMap Main Editing API v0.6
  slug: main-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/openstreetmap/refs/heads/main/openapi/openstreetmap-main-openapi.yml
- filename: openstreetmap-nominatim-openapi.yml
  format: yaml
  label: OpenStreetMap Nominatim Geocoding API
  slug: nominatim-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/openstreetmap/refs/heads/main/openapi/openstreetmap-nominatim-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  pricingCategory: Free (Donation-Funded) / Self-Host / 3rd-Party Provider
description: FOCUS-aligned FinOps for OpenStreetMap.
focus_columns:
  BillingCurrency: USD
  ProviderName: OpenStreetMap
  PublisherName: OpenStreetMap
  ServiceCategory: Open Geospatial Data
  ServiceName: OpenStreetMap
layout: finops
meters:
- aggregation: sum
  name: tile_requests
  unit: request
- aggregation: sum
  name: geocoding_requests
  unit: request
- aggregation: sum
  name: data_downloads
  unit: GB
name: Openstreetmap Finops
provider_name: OpenStreetMap
provider_slug: openstreetmap
publisher_name: OpenStreetMap
service_category: Open Geospatial Data
slug: openstreetmap-finops
source_filename: openstreetmap-finops.yml
source_heading: FinOps Profile
source_url: https://www.openstreetmap.org/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: OpenStreetMap\nproviderId: openstreetmap\ncreated: '2026-05-04'\nmodified: '2026-05-04'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Open Geospatial Data\ndescription: FOCUS-aligned FinOps for OpenStreetMap.\nsources:\n  - https://www.openstreetmap.org/\n  - https://operations.osmfoundation.org/policies/api/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: OpenStreetMap\nserviceCategory: Open Geospatial Data\nbillingModel:\n  pricingCategory: Free (Donation-Funded) / Self-Host / 3rd-Party Provider\n  billingFrequency: Monthly\n  billingCurrency: USD\nfocusColumns:\n  ServiceName: OpenStreetMap\n  ServiceCategory: Open Geospatial Data\n  ProviderName: OpenStreetMap\n  PublisherName:\
  \ OpenStreetMap\n  BillingCurrency: USD\nmeters:\n  - name: tile_requests\n    unit: request\n    aggregation: sum\n  - name: geocoding_requests\n    unit: request\n    aggregation: sum\n  - name: data_downloads\n    unit: GB\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Track OpenStreetMap consumption monthly.\n  - name: Allocation\n    description: Tag usage to teams/cost centers.\n  - name: Optimization\n    description: Right-size; reclaim unused entitlements.\n  - name: Accountability\n    description: Set spend alerts; quarterly review.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/openstreetmap/refs/heads/main/finops/openstreetmap-finops.yml
sources:
- https://www.openstreetmap.org/
- https://operations.osmfoundation.org/policies/api/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Open Geospatial Data
---
