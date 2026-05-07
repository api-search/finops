---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: booking-com-demand-api-openapi.yml
  format: yaml
  label: Booking.com Demand API
  slug: demand-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/booking-com/refs/heads/main/openapi/booking-com-demand-api-openapi.yml
- filename: booking-com-car-rentals-api-openapi.yml
  format: yaml
  label: Booking.com Car Rentals API
  slug: car-rentals-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/booking-com/refs/heads/main/openapi/booking-com-car-rentals-api-openapi.yml
- filename: booking-com-connectivity-content-api-openapi.yml
  format: yaml
  label: Booking.com Connectivity Content API
  slug: connectivity-content-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/booking-com/refs/heads/main/openapi/booking-com-connectivity-content-api-openapi.yml
- filename: booking-com-connectivity-reservations-api-openapi.yml
  format: yaml
  label: Booking.com Connectivity Reservations API
  slug: connectivity-reservations-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/booking-com/refs/heads/main/openapi/booking-com-connectivity-reservations-api-openapi.yml
- filename: booking-com-connectivity-rates-availability-api-openapi.yml
  format: yaml
  label: Booking.com Connectivity Rates and Availability API
  slug: connectivity-rates-availability-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/booking-com/refs/heads/main/openapi/booking-com-connectivity-rates-availability-api-openapi.yml
- filename: booking-com-connectivity-promotions-api-openapi.yml
  format: yaml
  label: Booking.com Connectivity Promotions API
  slug: connectivity-promotions-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/booking-com/refs/heads/main/openapi/booking-com-connectivity-promotions-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  pricingCategory: Custom B2B Contract
description: FOCUS-aligned FinOps for Booking.com.
focus_columns:
  BillingCurrency: USD
  ProviderName: Booking.com
  PublisherName: Booking.com
  ServiceCategory: Travel / Hospitality
  ServiceName: Booking.com
layout: finops
meters:
- aggregation: sum
  dimensions:
  - product
  name: transactions
  unit: transaction
- aggregation: sum
  name: api_calls
  unit: call
- aggregation: max
  name: annual_contract
  unit: year
name: Booking Com Finops
provider_name: booking-com
provider_slug: booking-com
publisher_name: Booking.com
service_category: Travel / Hospitality
slug: booking-com-finops
source_filename: booking-com-finops.yml
source_heading: FinOps Profile
source_url: https://connect.booking.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Booking.com\nproviderId: booking-com\ncreated: '2026-05-04'\nmodified: '2026-05-04'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Travel / Hospitality\ndescription: FOCUS-aligned FinOps for Booking.com.\nsources:\n  - https://connect.booking.com/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Booking.com\nserviceCategory: Travel / Hospitality\nbillingModel:\n  pricingCategory: Custom B2B Contract\n  billingFrequency: Monthly\n  billingCurrency: USD\nfocusColumns:\n  ServiceName: Booking.com\n  ServiceCategory: Travel / Hospitality\n  ProviderName: Booking.com\n  PublisherName: Booking.com\n  BillingCurrency: USD\nmeters:\n  - name: transactions\n    unit: transaction\n\
  \    aggregation: sum\n    dimensions:\n      - product\n  - name: api_calls\n    unit: call\n    aggregation: sum\n  - name: annual_contract\n    unit: year\n    aggregation: max\nprinciples:\n  - name: Visibility\n    description: Track Booking.com consumption monthly.\n  - name: Allocation\n    description: Tag usage to teams/cost centers for chargeback.\n  - name: Optimization\n    description: Right-size; reclaim unused entitlements.\n  - name: Accountability\n    description: Set spend alerts; quarterly review.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/booking-com/refs/heads/main/finops/booking-com-finops.yml
sources:
- https://connect.booking.com/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Travel / Hospitality
---
