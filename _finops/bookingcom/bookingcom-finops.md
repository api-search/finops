---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: bookingcom-booking-api-openapi.yml
  format: yaml
  label: Booking.com API
  slug: booking-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/bookingcom/refs/heads/main/openapi/bookingcom-booking-api-openapi.yml
billing_model:
  billingCurrency: USD/EUR/GBP
  billingFrequency: Monthly
  chargeCategories:
  - Adjustment
  - Credit
  - Tax
  pricingCategory: Commission / Partner Agreement
description: 'FOCUS-aligned FinOps for Booking.com partner APIs: an affiliate / connectivity model where approved partners pay no per-request fee but settle commercials on commission share from confirmed stays or contracted connectivity terms.'
focus_columns:
  BillingCurrency: EUR
  InvoiceIssuerName: Booking.com B.V.
  PricingCategory: Other
  PricingUnit: completed-stay
  ProviderName: Booking.com
  PublisherName: Booking.com B.V.
  ServiceCategory: Travel & Hospitality
  ServiceName: Booking.com
layout: finops
meters:
- aggregation: sum
  description: Number of completed bookings attributed to the affiliate / partner channel.
  dimensions:
  - partner
  - market
  - property_type
  name: completed_stays
  unit: stay
- aggregation: sum
  description: Gross booking value of completed stays, used as the commission base.
  dimensions:
  - partner
  - currency
  - market
  name: booking_value
  unit: currency
- aggregation: sum
  description: Demand / Connectivity API request volume; used for capacity and fair-use review rather than direct billing.
  dimensions:
  - api
  - endpoint
  - partner
  name: api_requests
  unit: request
name: Bookingcom Finops
provider_name: Booking.com
provider_slug: bookingcom
publisher_name: Booking.com B.V.
service_category: Travel & Hospitality
slug: bookingcom-finops
source_filename: bookingcom-finops.yml
source_heading: FinOps Profile
source_url: https://developers.booking.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Booking.com\nproviderId: bookingcom\npublisherName: Booking.com B.V.\nserviceCategory: Travel & Hospitality\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Accommodations\n  - Affiliates\n  - Connectivity\n  - Hospitality\n  - Hotels\n  - Reservations\n  - Travel\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps for Booking.com partner APIs: an affiliate / connectivity model where\n  approved partners pay no per-request fee but settle commercials on commission share from confirmed stays\n  or contracted connectivity terms.'\nsources:\n  - https://developers.booking.com/\n  - https://legacy.developers.booking.com/api\n\
  notes: No public pricing; commercial model is partner agreement and commission share, not metered API\n  spend. Reconcile once partner agreement terms are in scope.\nbillingModel:\n  pricingCategory: Commission / Partner Agreement\n  billingFrequency: Monthly\n  billingCurrency: USD/EUR/GBP\n  chargeCategories:\n    - Adjustment\n    - Credit\n    - Tax\nfocusColumns:\n  ServiceName: Booking.com\n  ServiceCategory: Travel & Hospitality\n  ProviderName: Booking.com\n  PublisherName: Booking.com B.V.\n  InvoiceIssuerName: Booking.com B.V.\n  BillingCurrency: EUR\n  PricingCategory: Other\n  PricingUnit: completed-stay\nmeters:\n  - name: completed_stays\n    description: Number of completed bookings attributed to the affiliate / partner channel.\n    unit: stay\n    aggregation: sum\n    dimensions:\n      - partner\n      - market\n      - property_type\n  - name: booking_value\n    description: Gross booking value of completed stays, used as the commission base.\n    unit: currency\n \
  \   aggregation: sum\n    dimensions:\n      - partner\n      - currency\n      - market\n  - name: api_requests\n    description: Demand / Connectivity API request volume; used for capacity and fair-use review rather\n      than direct billing.\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - partner\nprinciples:\n  - name: Visibility\n    description: Reconcile completed-stay reports and commission statements from the Booking.com Partner\n      Hub against your internal booking and traffic data.\n  - name: Allocation\n    description: Tag affiliate traffic with campaign / property / market so commission revenue and any\n      contracted connectivity costs allocate cleanly to product lines.\n  - name: Optimization\n    description: Tune affiliate placements toward higher-converting markets and property types; cache search\n      results within partner-allowed TTLs to reduce Demand API load.\n  - name: Accountability\n    description: Assign\
  \ a partner-relationship owner; review monthly statements, dispute discrepancies\n      against booking and stay data, and track commission share against renewal targets.\nmaintainers:\n  - FN: Kin Lane\n    email: kinlane@gmail.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/bookingcom/refs/heads/main/finops/bookingcom-finops.yml
sources:
- https://developers.booking.com/
- https://legacy.developers.booking.com/api
specification: FinOps Framework
tags:
- Accommodations
- Affiliates
- Connectivity
- Hospitality
- Hotels
- Reservations
- Travel
- FinOps
- FOCUS
---
