---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: dtn-weather-conditions-openapi.yml
  format: yaml
  label: DTN Weather Conditions API
  slug: dtn-weather-conditions-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/dtn/refs/heads/main/openapi/dtn-weather-conditions-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Per-Invoice
  chargeCategories:
  - Purchase
  - Usage
  - Tax
  pricingCategory: Subscription (or AWS Marketplace PAYG)
description: FOCUS-aligned FinOps shape for DTN. Billing is custom subscription per industry vertical (Weather, Marine, Agribusiness, Aviation, Refined Fuels). A subset is also available pay-as-you-go via AWS Marketplace.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: DTN, LLC (or AWS Marketplace)
  ProviderName: DTN
  PublisherName: DTN, LLC
  ServiceCategory: Weather & Industry Data
  ServiceName: DTN APIs
layout: finops
meters:
- aggregation: sum
  description: Internal observability of calls against DTN endpoints
  dimensions:
  - api
  - endpoint
  - subscription_tier
  name: api_requests
  unit: request
- aggregation: count
  description: Active DTN subscriptions
  dimensions:
  - vertical
  name: subscription_seats
  unit: seat
- aggregation: sum
  description: Metered units when consumed via AWS Marketplace
  dimensions:
  - product
  name: aws_marketplace_units
  unit: varies
name: Dtn Finops
provider_name: dtn
provider_slug: dtn
publisher_name: DTN, LLC
service_category: Weather & Industry Data
slug: dtn-finops
source_filename: dtn-finops.yml
source_heading: FinOps Profile
source_url: https://devportal.dtn.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: DTN\nproviderId: dtn\npublisherName: DTN, LLC\nserviceCategory: Weather & Industry Data\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Weather\n  - Agriculture\n  - Aviation\n  - Marine\n  - FinOps\n  - FOCUS\ndescription: FOCUS-aligned FinOps shape for DTN. Billing is custom subscription per industry vertical\n  (Weather, Marine, Agribusiness, Aviation, Refined Fuels). A subset is also available pay-as-you-go via\n  AWS Marketplace.\nnotes: No public per-call meter; reconciled=false.\nsources:\n  - https://devportal.dtn.com/\n  - https://www.dtn.com/resources/api-data-integrations/\n  - https://aws.amazon.com/marketplace/pp/prodview-yohehde7bckaq\n\
  billingModel:\n  pricingCategory: Subscription (or AWS Marketplace PAYG)\n  billingFrequency: Per-Invoice\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\n    - Tax\nfocusColumns:\n  ServiceName: DTN APIs\n  ServiceCategory: Weather & Industry Data\n  ProviderName: DTN\n  PublisherName: DTN, LLC\n  InvoiceIssuerName: DTN, LLC (or AWS Marketplace)\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: api_requests\n    description: Internal observability of calls against DTN endpoints\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - subscription_tier\n  - name: subscription_seats\n    description: Active DTN subscriptions\n    unit: seat\n    aggregation: count\n    dimensions:\n      - vertical\n  - name: aws_marketplace_units\n    description: Metered units when consumed via AWS Marketplace\n    unit: varies\n    aggregation: sum\n    dimensions:\n      - product\nprinciples:\n  - name: Visibility\n\
  \    description: Reconcile DTN invoices (or AWS Marketplace charges) against subscription scope; cache\n      forecast and observation responses at the subscription's update cadence.\n  - name: Allocation\n    description: Allocate DTN cost to the line of business consuming the data (agronomy, fleet ops, refined-fuels\n      ops, aviation safety).\n  - name: Optimization\n    description: Right-size the forecast horizon to the lowest tier that meets the use case; cache observation\n      pulls; coalesce duplicate point forecasts at the geofence level.\n  - name: Accountability\n    description: Subscription owner per vertical is accountable for renewal terms and adherence to subscription\n      scope.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/dtn/refs/heads/main/finops/dtn-finops.yml
sources:
- https://devportal.dtn.com/
- https://www.dtn.com/resources/api-data-integrations/
- https://aws.amazon.com/marketplace/pp/prodview-yohehde7bckaq
specification: FinOps Framework
tags:
- Weather
- Agriculture
- Aviation
- Marine
- FinOps
- FOCUS
---
