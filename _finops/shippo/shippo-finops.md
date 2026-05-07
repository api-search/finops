---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: shippo-openapi.yml
  format: yaml
  label: Shippo API
  slug: shippo-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/shippo/refs/heads/main/openapi/shippo-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  pricingCategory: Per-Label + Add-On API Calls
description: FOCUS-aligned FinOps for Shippo.
focus_columns:
  BillingCurrency: USD
  ProviderName: Shippo
  PublisherName: Shippo
  ServiceCategory: Shipping API
  ServiceName: Shippo
layout: finops
meters:
- aggregation: sum
  dimensions:
  - carrier
  - service_level
  name: labels_purchased
  unit: label
- aggregation: sum
  name: address_validations
  unit: validation
- aggregation: sum
  name: tracking_subscriptions
  unit: tracking
- aggregation: sum
  name: rating_calls
  unit: call
name: Shippo Finops
provider_name: Shippo
provider_slug: shippo
publisher_name: Shippo
service_category: Shipping API
slug: shippo-finops
source_filename: shippo-finops.yml
source_heading: FinOps Profile
source_url: https://goshippo.com/pricing/api
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Shippo\nproviderId: shippo\ncreated: '2026-05-04'\nmodified: '2026-05-04'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Shipping API\ndescription: FOCUS-aligned FinOps for Shippo.\nsources:\n  - https://goshippo.com/pricing/api\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Shippo\nserviceCategory: Shipping API\nbillingModel:\n  pricingCategory: Per-Label + Add-On API Calls\n  billingFrequency: Monthly\n  billingCurrency: USD\nfocusColumns:\n  ServiceName: Shippo\n  ServiceCategory: Shipping API\n  ProviderName: Shippo\n  PublisherName: Shippo\n  BillingCurrency: USD\nmeters:\n  - name: labels_purchased\n    unit: label\n    aggregation: sum\n    dimensions:\n      - carrier\n\
  \      - service_level\n  - name: address_validations\n    unit: validation\n    aggregation: sum\n  - name: tracking_subscriptions\n    unit: tracking\n    aggregation: sum\n  - name: rating_calls\n    unit: call\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Track Shippo consumption monthly.\n  - name: Allocation\n    description: Tag usage to teams/cost centers.\n  - name: Optimization\n    description: Right-size; reclaim unused entitlements.\n  - name: Accountability\n    description: Set spend alerts; quarterly review.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/shippo/refs/heads/main/finops/shippo-finops.yml
sources:
- https://goshippo.com/pricing/api
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Shipping API
---
