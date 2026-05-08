---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: pitney-bowes-openapi.yml
  format: yaml
  label: Pitney Bowes APIs
  slug: pitney-bowes
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/pitney-bowes/refs/heads/main/openapi/pitney-bowes-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Per-Shipment / Monthly
  chargeCategories:
  - Usage
  - Purchase
  - Tax
  - Adjustment
  pricingCategory: Pass-Through Postage + Contract
description: FOCUS-aligned FinOps placeholder for Pitney Bowes. The cost surface is dominated by pass-through carrier postage and parcel rates plus any negotiated platform fees. APIs are an entitlement of the merchant contract rather than a separately metered SKU.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Pitney Bowes Inc.
  ProviderName: Pitney Bowes
  PublisherName: Pitney Bowes Inc.
  ServiceCategory: Shipping and Mailing
  ServiceName: Pitney Bowes Shipping API
  ServiceSubcategory: Parcel and Postage
layout: finops
meters:
- aggregation: count
  description: Each label generated / parcel shipped through the Shipping API. Drives the pass-through carrier postage charge.
  dimensions:
  - carrier
  - service_class
  - origin
  - destination
  name: shipment
  unit: shipment
- aggregation: sum
  description: Pass-through postage / parcel cost charged by the carrier (USPS / UPS / FedEx etc.) on each shipment.
  dimensions:
  - carrier
  - service_class
  name: postage_amount
  unit: USD
- aggregation: count
  description: Tracking webhook events / poll responses; typically not separately billed.
  dimensions:
  - carrier
  name: tracking_event
  unit: event
- aggregation: sum
  description: Negotiated monthly platform fee for the Shipping API merchant contract.
  dimensions:
  - merchant
  name: platform_subscription
  unit: month
name: Pitney Bowes Finops
provider_name: Pitney Bowes
provider_slug: pitney-bowes
publisher_name: Pitney Bowes Inc.
service_category: Shipping and Mailing
slug: pitney-bowes-finops
source_filename: pitney-bowes-finops.yml
source_heading: FinOps Profile
source_url: https://www.pitneybowes.com/us/developer.html
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Pitney Bowes\nproviderId: pitney-bowes\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Shipping\n  - Logistics\n  - Mailing\nnotes: Pitney Bowes does not publish a self-service price book for its Shipping APIs. Cost is\n  driven by negotiated merchant contracts plus pass-through postage / parcel rates. This artifact\n  models the FinOps shape at the contract / shipment level; per-call API price is not publicly\n  documented.\ndescription: FOCUS-aligned FinOps placeholder for Pitney Bowes. The cost surface is dominated by\n  pass-through carrier postage and parcel rates plus any negotiated platform fees. APIs are an\n  entitlement of the merchant contract rather than a separately metered SKU.\nsources:\n  - https://www.pitneybowes.com/us/developer.html\n  - https://docs.shippingapi.pitneybowes.com/api\nalignedWith:\n\
  \  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Pitney Bowes Inc.\nserviceCategory: Shipping and Mailing\nbillingModel:\n  pricingCategory: Pass-Through Postage + Contract\n  billingFrequency: Per-Shipment / Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Adjustment\nfocusColumns:\n  ServiceName: Pitney Bowes Shipping API\n  ServiceCategory: Shipping and Mailing\n  ServiceSubcategory: Parcel and Postage\n  ProviderName: Pitney Bowes\n  PublisherName: Pitney Bowes Inc.\n  InvoiceIssuerName: Pitney Bowes Inc.\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: shipment\n    description: Each label generated / parcel shipped through the Shipping API. Drives the\n      pass-through carrier postage charge.\n    unit: shipment\n    aggregation: count\n \
  \   dimensions:\n      - carrier\n      - service_class\n      - origin\n      - destination\n  - name: postage_amount\n    description: Pass-through postage / parcel cost charged by the carrier (USPS / UPS / FedEx\n      etc.) on each shipment.\n    unit: USD\n    aggregation: sum\n    dimensions:\n      - carrier\n      - service_class\n  - name: tracking_event\n    description: Tracking webhook events / poll responses; typically not separately billed.\n    unit: event\n    aggregation: count\n    dimensions:\n      - carrier\n  - name: platform_subscription\n    description: Negotiated monthly platform fee for the Shipping API merchant contract.\n    unit: month\n    aggregation: sum\n    dimensions:\n      - merchant\nprinciples:\n  - name: Visibility\n    description: Track per-shipment cost via the Shipping API response (rate quote) and reconcile\n      monthly against the Pitney Bowes invoice; pass-through postage dominates the line item.\n  - name: Allocation\n    description:\
  \ Tag shipments with the originating store / fulfillment center / SKU so postage\n      cost rolls up to the correct business unit.\n  - name: Optimization\n    description: Use rate-shopping to pick the cheapest carrier / service class per shipment;\n      consolidate to negotiated zones; use Pitney Bowes presort / cubic discounts where they\n      apply.\n  - name: Accountability\n    description: Logistics / fulfillment team owns shipment cost; finance reviews aggregate\n      postage spend monthly versus volume.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/pitney-bowes/refs/heads/main/finops/pitney-bowes-finops.yml
sources:
- https://www.pitneybowes.com/us/developer.html
- https://docs.shippingapi.pitneybowes.com/api
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Shipping
- Logistics
- Mailing
---
