---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: maps-js.yaml
  format: yaml
  label: Maps JavaScript API
  slug: ''
  spec_type: OpenAPI
  url: https://api.example.com/openapi/maps-js.yaml
- filename: google-maps-geocoding-api.yml
  format: yaml
  label: Geocoding API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/google-maps/refs/heads/main/openapi/google-maps-geocoding-api.yml
- filename: google-maps-places-api.yml
  format: yaml
  label: Places API (New)
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/google-maps/refs/heads/main/openapi/google-maps-places-api.yml
- filename: google-maps-directions-api.yml
  format: yaml
  label: Directions API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/google-maps/refs/heads/main/openapi/google-maps-directions-api.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  pricingCategory: Pay-As-You-Go + Committed Use
description: FOCUS-aligned FinOps for Google Maps Platform.
focus_columns:
  BillingCurrency: USD
  ProviderName: Google Maps Platform
  PublisherName: Google Maps Platform
  ServiceCategory: Maps and Location
  ServiceName: Google Maps Platform
layout: finops
meters:
- aggregation: sum
  dimensions:
  - service
  - region
  - instance_type
  - tenant
  name: compute_hours
  unit: instance-hour
- aggregation: max
  dimensions:
  - service
  - tier
  name: storage
  unit: GB-month
- aggregation: sum
  dimensions:
  - egress_type
  - region_pair
  name: data_transfer
  unit: GB
- aggregation: sum
  dimensions:
  - service
  - operation
  name: api_requests
  unit: request
- aggregation: sum
  dimensions:
  - service
  name: managed_services
  unit: varies
name: Google Maps Finops
provider_name: Google Maps Platform
provider_slug: google-maps
publisher_name: Google Maps Platform
service_category: Maps and Location
slug: google-maps-finops
source_filename: google-maps-finops.yml
source_heading: FinOps Profile
source_url: https://mapsplatform.google.com/pricing/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Google Maps Platform\nproviderId: google-maps\ncreated: '2026-05-04'\nmodified: '2026-05-04'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Maps and Location\ndescription: FOCUS-aligned FinOps for Google Maps Platform.\nsources:\n  - https://mapsplatform.google.com/pricing/\n  - https://focus.finops.org/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Google Maps Platform\nserviceCategory: Maps and Location\nbillingModel:\n  pricingCategory: Pay-As-You-Go + Committed Use\n  billingFrequency: Monthly\n  billingCurrency: USD\nfocusColumns:\n  ServiceName: Google Maps Platform\n  ServiceCategory: Maps and Location\n  ProviderName: Google Maps Platform\n  PublisherName: Google\
  \ Maps Platform\n  BillingCurrency: USD\nmeters:\n  - name: compute_hours\n    unit: instance-hour\n    aggregation: sum\n    dimensions:\n      - service\n      - region\n      - instance_type\n      - tenant\n  - name: storage\n    unit: GB-month\n    aggregation: max\n    dimensions:\n      - service\n      - tier\n  - name: data_transfer\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - egress_type\n      - region_pair\n  - name: api_requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - service\n      - operation\n  - name: managed_services\n    unit: varies\n    aggregation: sum\n    dimensions:\n      - service\nprinciples:\n  - name: Visibility\n    description: Track Google Maps Platform consumption monthly.\n  - name: Allocation\n    description: Tag usage to teams/cost centers for chargeback.\n  - name: Optimization\n    description: Right-size; reclaim unused entitlements.\n  - name: Accountability\n    description: Set spend alerts; quarterly\
  \ review.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/google-maps/refs/heads/main/finops/google-maps-finops.yml
sources:
- https://mapsplatform.google.com/pricing/
- https://focus.finops.org/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Maps and Location
---
