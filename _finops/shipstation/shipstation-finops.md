---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: shipstation-v1-openapi.yml
  format: yaml
  label: ShipStation V1 API
  slug: shipstation-v1-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/shipstation/refs/heads/main/openapi/shipstation-v1-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  pricingCategory: Subscription with Shipment Quota
description: FOCUS-aligned FinOps for ShipStation.
focus_columns:
  BillingCurrency: USD
  ProviderName: ShipStation
  PublisherName: ShipStation
  ServiceCategory: Shipping / Order Management
  ServiceName: ShipStation
layout: finops
meters:
- aggregation: sum
  name: shipments_processed
  unit: shipment
- aggregation: max
  name: user_seats
  unit: seat-month
- aggregation: max
  name: active_stores
  unit: store-month
name: Shipstation Finops
provider_name: ShipStation
provider_slug: shipstation
publisher_name: ShipStation
service_category: Shipping / Order Management
slug: shipstation-finops
source_filename: shipstation-finops.yml
source_heading: FinOps Profile
source_url: https://www.shipstation.com/pricing/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: ShipStation\nproviderId: shipstation\ncreated: '2026-05-04'\nmodified: '2026-05-04'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Shipping / Order Management\ndescription: FOCUS-aligned FinOps for ShipStation.\nsources:\n  - https://www.shipstation.com/pricing/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: ShipStation\nserviceCategory: Shipping / Order Management\nbillingModel:\n  pricingCategory: Subscription with Shipment Quota\n  billingFrequency: Monthly\n  billingCurrency: USD\nfocusColumns:\n  ServiceName: ShipStation\n  ServiceCategory: Shipping / Order Management\n  ProviderName: ShipStation\n  PublisherName: ShipStation\n  BillingCurrency: USD\nmeters:\n  - name:\
  \ shipments_processed\n    unit: shipment\n    aggregation: sum\n  - name: user_seats\n    unit: seat-month\n    aggregation: max\n  - name: active_stores\n    unit: store-month\n    aggregation: max\nprinciples:\n  - name: Visibility\n    description: Track ShipStation consumption monthly.\n  - name: Allocation\n    description: Tag usage to teams/cost centers.\n  - name: Optimization\n    description: Right-size; reclaim unused entitlements.\n  - name: Accountability\n    description: Set spend alerts; quarterly review.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/shipstation/refs/heads/main/finops/shipstation-finops.yml
sources:
- https://www.shipstation.com/pricing/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Shipping / Order Management
---
