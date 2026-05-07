---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: uber-riders-openapi.yml
  format: yaml
  label: Uber Riders API
  slug: uber-riders
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/uber/refs/heads/main/openapi/uber-riders-openapi.yml
- filename: uber-drivers-openapi.yml
  format: yaml
  label: Uber Drivers API
  slug: uber-drivers
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/uber/refs/heads/main/openapi/uber-drivers-openapi.yml
- filename: uber-eats-openapi.yml
  format: yaml
  label: Uber Eats API
  slug: uber-eats
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/uber/refs/heads/main/openapi/uber-eats-openapi.yml
- filename: uber-direct-openapi.yml
  format: yaml
  label: Uber Direct API
  slug: uber-direct
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/uber/refs/heads/main/openapi/uber-direct-openapi.yml
- filename: uber-vouchers-openapi.yml
  format: yaml
  label: Uber Vouchers API
  slug: uber-vouchers
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/uber/refs/heads/main/openapi/uber-vouchers-openapi.yml
- filename: uber-businesses-openapi.yml
  format: yaml
  label: Uber for Business API
  slug: uber-businesses
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/uber/refs/heads/main/openapi/uber-businesses-openapi.yml
billing_model:
  billingCurrency: USD (settlement varies)
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  - Tax
  - Refund
  - Adjustment
  pricingCategory: Custom Contract
description: 'FOCUS-aligned FinOps for Uber: enterprise / partner-gated developer APIs with no public pricing. Spend is contract-driven (per-trip, per-delivery, platform fees) and surfaced via Uber for Business reporting rather than a public usage-meter API.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Uber Technologies, Inc.
  ProviderName: Uber
  PublisherName: Uber Technologies, Inc.
  ServiceCategory: Mobility / Logistics
  ServiceName: Uber for Business / Uber Direct
layout: finops
meters:
- aggregation: sum
  description: Completed Uber for Business / Guest Rides trips
  dimensions:
  - city
  - product
  name: trips
  unit: trip
- aggregation: sum
  description: Completed Uber Eats / Uber Direct deliveries
  dimensions:
  - city
  - merchant
  name: deliveries
  unit: delivery
- aggregation: sum
  description: Vouchers issued via the Vouchers API
  name: vouchers_issued
  unit: voucher
name: Uber Finops
provider_name: Uber
provider_slug: uber
publisher_name: Uber Technologies, Inc.
service_category: Mobility / Logistics
slug: uber-finops
source_filename: uber-finops.yml
source_heading: FinOps Profile
source_url: https://developer.uber.com/docs/businesses
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Uber\nproviderId: uber\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Ride-Sharing\n  - Food Delivery\n  - Logistics\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps for Uber: enterprise / partner-gated developer APIs with no public\n  pricing. Spend is contract-driven (per-trip, per-delivery, platform fees) and surfaced via Uber for\n  Business reporting rather than a public usage-meter API.'\nnotes: Uber developer access is enterprise-only; FOCUS columns and meters are best-effort placeholders\n  pending reconciliation against an actual Uber for Business invoice.\nsources:\n  - https://developer.uber.com/docs/businesses\n  - https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion:\
  \ '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Uber Technologies, Inc.\nserviceCategory: Mobility / Logistics\nbillingModel:\n  pricingCategory: Custom Contract\n  billingFrequency: Monthly\n  billingCurrency: USD (settlement varies)\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Refund\n    - Adjustment\nfocusColumns:\n  ServiceName: Uber for Business / Uber Direct\n  ServiceCategory: Mobility / Logistics\n  ProviderName: Uber\n  PublisherName: Uber Technologies, Inc.\n  InvoiceIssuerName: Uber Technologies, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: trips\n    description: Completed Uber for Business / Guest Rides trips\n    unit: trip\n    aggregation: sum\n    dimensions:\n      - city\n      - product\n  - name: deliveries\n    description: Completed Uber Eats / Uber Direct deliveries\n    unit: delivery\n    aggregation: sum\n    dimensions:\n      - city\n      - merchant\n  - name: vouchers_issued\n    description:\
  \ Vouchers issued via the Vouchers API\n    unit: voucher\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Pull spend from the Uber for Business dashboard, the Receipts API, and SFTP data automation\n      drops; there is no public usage-API for self-service tracking.\n  - name: Allocation\n    description: Allocate trips and deliveries to internal cost centers using Uber for Business expense\n      groups, custom fields, and SAP Concur integration.\n  - name: Optimization\n    description: Use product mix (UberX vs UberXL vs Uber Direct service levels) and policy controls\n      to manage per-trip / per-delivery cost; consolidate vouchers under a single program where possible.\n  - name: Accountability\n    description: Travel managers and ops owners review Uber for Business reporting; finance reconciles\n      against the monthly enterprise invoice.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/uber/refs/heads/main/finops/uber-finops.yml
sources:
- https://developer.uber.com/docs/businesses
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Ride-Sharing
- Food Delivery
- Logistics
- FinOps
- FOCUS
---
