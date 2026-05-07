---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: lufthansa-openapi.yml
  format: yaml
  label: Lufthansa Public API
  slug: public-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/lufthansa/refs/heads/main/openapi/lufthansa-openapi.yml
billing_model:
  billingCurrency: EUR
  billingFrequency: Per-Contract
  chargeCategories:
  - Usage
  - Purchase
  - Adjustment
  pricingCategory: Free Registration + Partner Contract
description: 'FOCUS-aligned FinOps for Lufthansa Open API: Open Data plan is free / registration-based, Fares plan is partner-contracted with commercial terms in the NDC Partner Program. Cost shape is partner-contract-driven rather than per-call usage billing.'
focus_columns:
  BillingCurrency: EUR
  InvoiceIssuerName: Deutsche Lufthansa AG
  ProviderName: Lufthansa
  PublisherName: Deutsche Lufthansa AG
  ServiceCategory: Travel
  ServiceName: Lufthansa Open API
layout: finops
meters:
- aggregation: sum
  dimensions:
  - endpoint
  name: api_requests_open_data
  unit: request
- aggregation: sum
  dimensions:
  - origin
  - destination
  name: fare_offer_requests
  unit: request
- aggregation: sum
  name: bookings_completed
  unit: booking
- aggregation: sum
  name: ndc_offer_calls
  unit: request
name: Lufthansa Finops
provider_name: Lufthansa
provider_slug: lufthansa
publisher_name: Deutsche Lufthansa AG
service_category: Travel
slug: lufthansa-finops
source_filename: lufthansa-finops.yml
source_heading: FinOps Profile
source_url: https://developer.lufthansa.com
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Lufthansa\nproviderId: lufthansa\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Airlines\n  - Travel\ndescription: 'FOCUS-aligned FinOps for Lufthansa Open API: Open Data plan is free / registration-based,\n  Fares plan is partner-contracted with commercial terms in the NDC Partner Program. Cost shape is\n  partner-contract-driven rather than per-call usage billing.'\nsources:\n  - https://developer.lufthansa.com\nnotes: No public pricing/billing surface; cost meters reflect typical airline NDC partner billing lines.\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Deutsche Lufthansa AG\nserviceCategory: Travel\nbillingModel:\n\
  \  pricingCategory: Free Registration + Partner Contract\n  billingFrequency: Per-Contract\n  billingCurrency: EUR\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Adjustment\nfocusColumns:\n  ServiceName: Lufthansa Open API\n  ServiceCategory: Travel\n  ProviderName: Lufthansa\n  PublisherName: Deutsche Lufthansa AG\n  InvoiceIssuerName: Deutsche Lufthansa AG\n  BillingCurrency: EUR\nmeters:\n  - name: api_requests_open_data\n    unit: request\n    aggregation: sum\n    dimensions:\n      - endpoint\n  - name: fare_offer_requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - origin\n      - destination\n  - name: bookings_completed\n    unit: booking\n    aggregation: sum\n  - name: ndc_offer_calls\n    unit: request\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Track Open Data API consumption against developer-portal counters; for Fares, reconcile\n      offer/booking traffic against the NDC partner statement.\n  - name: Allocation\n\
  \    description: Tag requests by integration (booking, ops, cargo, notifications) and by partner consumer\n      app for chargeback.\n  - name: Optimization\n    description: Cache reference data (airports, schedules) and reduce repeat fare-offer calls; consolidate\n      polling on the Notifications API to lower call volume.\n  - name: Accountability\n    description: Partner-side owners review NDC contract economics quarterly; renegotiate via the Lufthansa\n      partner team as volume grows.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/lufthansa/refs/heads/main/finops/lufthansa-finops.yml
sources:
- https://developer.lufthansa.com
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Airlines
- Travel
---
