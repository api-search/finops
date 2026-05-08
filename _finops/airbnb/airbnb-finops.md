---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: airbnb-homes-api-openapi.yml
  format: yaml
  label: Airbnb Homes API
  slug: homes-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/airbnb/refs/heads/main/openapi/airbnb-homes-api-openapi.yml
- filename: airbnb-activities-api-openapi.yml
  format: yaml
  label: Airbnb Activities API
  slug: activities-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/airbnb/refs/heads/main/openapi/airbnb-activities-api-openapi.yml
- filename: airbnb-webhooks-asyncapi.yml
  format: yaml
  label: Airbnb Webhooks API
  slug: webhooks-api
  spec_type: AsyncAPI
  url: https://raw.githubusercontent.com/api-evangelist/airbnb/refs/heads/main/asyncapi/airbnb-webhooks-asyncapi.yml
billing_model:
  billingCurrency: USD (settlement varies)
  billingFrequency: Per-Booking / Continuous Settlement
  chargeCategories:
  - Usage
  - Adjustment
  - Refund
  - Tax
  pricingCategory: Take Rate (Marketplace)
description: FOCUS-aligned shape for Airbnb. Take-rate marketplace — Airbnb is paid as a percentage of the booking subtotal. FinOps for hosts and partners centers on host service fees (3% split or ~14-16% host-only), guest fees, and product-line take rates (Services 15%, Experiences 20%).
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Airbnb, Inc.
  ProviderName: Airbnb
  PublisherName: Airbnb, Inc.
  ServiceCategory: Hospitality Marketplace
  ServiceName: Airbnb Marketplace
layout: finops
meters:
- aggregation: sum
  description: Host-side take rate on Homes bookings (split or host-only structure)
  dimensions:
  - fee_structure
  - country
  - listing
  name: host_service_fee
  unit: USD
- aggregation: sum
  description: Guest-side take rate on Homes bookings (split structure only)
  dimensions:
  - currency
  - country
  name: guest_service_fee
  unit: USD
- aggregation: sum
  description: 15% take rate on Airbnb Services bookings ($6 USD minimum)
  dimensions:
  - service_type
  - country
  name: services_fee
  unit: USD
- aggregation: sum
  description: 20% take rate on Airbnb Experiences bookings
  dimensions:
  - experience_type
  - country
  name: experiences_fee
  unit: USD
- aggregation: count
  description: Booking volume across the marketplace
  dimensions:
  - product_line
  - country
  - listing
  name: bookings_count
  unit: booking
name: Airbnb Finops
provider_name: airbnb
provider_slug: airbnb
publisher_name: Airbnb, Inc.
service_category: Hospitality Marketplace
slug: airbnb-finops
source_filename: airbnb-finops.yml
source_heading: FinOps Profile
source_url: https://www.airbnb.com/help/article/1857
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Airbnb\nproviderId: airbnb\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Airbnb, Inc.\nserviceCategory: Hospitality Marketplace\ntags:\n  - Hospitality\n  - Travel\n  - Short-Term Rental\n  - Marketplace\n  - FinOps\n  - FOCUS\ndescription: FOCUS-aligned shape for Airbnb. Take-rate marketplace — Airbnb is paid as a percentage of\n  the booking subtotal. FinOps for hosts and partners centers on host service fees (3% split or\n  ~14-16% host-only), guest fees, and product-line take rates (Services 15%, Experiences 20%).\nsources:\n  - https://www.airbnb.com/help/article/1857\n  - https://partners.airbnb.com/\nbillingModel:\n\
  \  pricingCategory: Take Rate (Marketplace)\n  billingFrequency: Per-Booking / Continuous Settlement\n  billingCurrency: USD (settlement varies)\n  chargeCategories:\n    - Usage\n    - Adjustment\n    - Refund\n    - Tax\nfocusColumns:\n  ServiceName: Airbnb Marketplace\n  ServiceCategory: Hospitality Marketplace\n  ProviderName: Airbnb\n  PublisherName: Airbnb, Inc.\n  InvoiceIssuerName: Airbnb, Inc.\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: host_service_fee\n    description: Host-side take rate on Homes bookings (split or host-only structure)\n    unit: USD\n    aggregation: sum\n    dimensions:\n      - fee_structure\n      - country\n      - listing\n  - name: guest_service_fee\n    description: Guest-side take rate on Homes bookings (split structure only)\n    unit: USD\n    aggregation: sum\n    dimensions:\n      - currency\n      - country\n  - name: services_fee\n    description: 15% take rate on Airbnb Services bookings ($6 USD minimum)\n    unit:\
  \ USD\n    aggregation: sum\n    dimensions:\n      - service_type\n      - country\n  - name: experiences_fee\n    description: 20% take rate on Airbnb Experiences bookings\n    unit: USD\n    aggregation: sum\n    dimensions:\n      - experience_type\n      - country\n  - name: bookings_count\n    description: Booking volume across the marketplace\n    unit: booking\n    aggregation: count\n    dimensions:\n      - product_line\n      - country\n      - listing\nprinciples:\n  - name: Visibility\n    description: Hosts track payouts and fees in the Airbnb host dashboard transaction history;\n      Software Partners reconcile via Reservations API and webhook events.\n  - name: Allocation\n    description: Allocate fees by listing, market (country / city), and product line (Homes / Services\n      / Experiences). For multi-property hosts, listing ID is the canonical allocation key.\n  - name: Optimization\n    description: Optimize take-rate exposure by tuning pricing strategy, choosing\
  \ between split and\n      host-only fee structures where eligible, minimizing cancellations and refunds, and using Smart\n      Pricing or pricing tools to maintain occupancy.\n  - name: Accountability\n    description: Hosts and property managers own marketplace fees against revenue; Software Partners\n      pass-through to their hosts. Review monthly against booking subtotals and adjust pricing\n      strategy quarterly.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/airbnb/refs/heads/main/finops/airbnb-finops.yml
sources:
- https://www.airbnb.com/help/article/1857
- https://partners.airbnb.com/
specification: FinOps Framework
tags:
- Hospitality
- Travel
- Short-Term Rental
- Marketplace
- FinOps
- FOCUS
---
