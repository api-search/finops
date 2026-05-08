---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: geoapify-forward-geocoding-api-openapi.yml
  format: yaml
  label: Forward Geocoding API
  slug: forward-geocoding
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/geoapify/refs/heads/main/openapi/geoapify-forward-geocoding-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  pricingCategory: Subscription with Daily Credit Quota
description: FOCUS-aligned FinOps for Geoapify.
focus_columns:
  BillingCurrency: USD
  ProviderName: Geoapify
  PublisherName: Geoapify
  ServiceCategory: Maps
  ServiceName: Geoapify
layout: finops
meters:
- aggregation: sum
  dimensions:
  - api
  name: credits_used
  unit: credit
- aggregation: sum
  dimensions:
  - plan
  name: subscription
  unit: month
name: Geoapify Finops
provider_name: Geoapify
provider_slug: geoapify
publisher_name: Geoapify
service_category: Maps
slug: geoapify-finops
source_filename: geoapify-finops.yml
source_heading: FinOps Profile
source_url: https://www.geoapify.com/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Geoapify\nproviderId: geoapify\ncreated: '2026-05-04'\nmodified: '2026-05-04'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Maps\ndescription: FOCUS-aligned FinOps for Geoapify.\nsources:\n  - https://www.geoapify.com/pricing\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Geoapify\nserviceCategory: Maps\nbillingModel:\n  pricingCategory: Subscription with Daily Credit Quota\n  billingFrequency: Monthly\n  billingCurrency: USD\nfocusColumns:\n  ServiceName: Geoapify\n  ServiceCategory: Maps\n  ProviderName: Geoapify\n  PublisherName: Geoapify\n  BillingCurrency: USD\nmeters:\n  - name: credits_used\n    unit: credit\n    aggregation: sum\n    dimensions:\n      - api\n \
  \ - name: subscription\n    unit: month\n    aggregation: sum\n    dimensions:\n      - plan\nprinciples:\n  - name: Visibility\n    description: Track Geoapify consumption monthly.\n  - name: Allocation\n    description: Tag usage to teams/cost centers.\n  - name: Optimization\n    description: Right-size; reclaim unused entitlements.\n  - name: Accountability\n    description: Set spend alerts; quarterly review.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/geoapify/refs/heads/main/finops/geoapify-finops.yml
sources:
- https://www.geoapify.com/pricing
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Maps
---
