---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: hilton-hilton-api-openapi.yml
  format: yaml
  label: Hilton Developer API
  slug: hilton-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/hilton/refs/heads/main/openapi/hilton-hilton-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  - Adjustment
  - Refund
  pricingCategory: Commission / Take Rate (per partner agreement)
description: FOCUS-aligned FinOps stub for Hilton. Partner-gated; commission and per-booking economics govern the FinOps shape, with rates set in bilateral connectivity agreements.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Hilton Worldwide Holdings Inc.
  PricingCategory: Commission
  PricingUnit: booking
  ProviderName: Hilton
  PublisherName: Hilton Worldwide Holdings Inc.
  ServiceCategory: Hospitality / Travel
  ServiceName: Hilton
layout: finops
meters:
- aggregation: sum
  description: Reservations confirmed through the partner connectivity API
  dimensions:
  - partner_id
  - brand
  - property_id
  - market
  - rate_code
  name: bookings
  unit: booking
- aggregation: sum
  description: Room nights generated
  dimensions:
  - partner_id
  - brand
  - property_id
  name: room_nights
  unit: room-night
- aggregation: sum
  description: Gross dollar value of confirmed bookings
  dimensions:
  - partner_id
  - brand
  - property_id
  name: gross_booking_value
  unit: USD
- aggregation: sum
  description: Commission paid (or due) to the partner
  dimensions:
  - partner_id
  - brand
  name: commissions
  unit: USD
- aggregation: sum
  description: Hilton Honors points issued or accrued via the partner
  dimensions:
  - partner_id
  - brand
  name: loyalty_points_issued
  unit: point
name: Hilton Finops
provider_name: Hilton
provider_slug: hilton
publisher_name: Hilton Worldwide Holdings Inc.
service_category: Hospitality / Travel
slug: hilton-finops
source_filename: hilton-finops.yml
source_heading: FinOps Profile
source_url: https://www.hilton.com/en/corporate/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Hilton\nproviderId: hilton\npublisherName: Hilton Worldwide Holdings Inc.\nserviceCategory: Hospitality / Travel\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Hospitality\n  - Hotels\n  - Travel\n  - Reservations\n  - Loyalty\n  - FinOps\n  - FOCUS\nnotes: Hilton's API surface is partner-gated; FinOps for a Hilton integration is typically a take-rate /\n  commission shape (booking commission to OTAs, channel-management fees, loyalty-points reciprocity) plus\n  bilateral partner-program fees. No public price book exists; this stub captures the right meter shape.\ndescription: 'FOCUS-aligned FinOps stub for Hilton. Partner-gated; commission and per-booking economics\n\
  \  govern the FinOps shape, with rates set in bilateral connectivity agreements.'\nsources:\n  - https://www.hilton.com/en/corporate/\nbillingModel:\n  pricingCategory: Commission / Take Rate (per partner agreement)\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Adjustment\n    - Refund\nfocusColumns:\n  ServiceName: Hilton\n  ServiceCategory: Hospitality / Travel\n  ProviderName: Hilton\n  PublisherName: Hilton Worldwide Holdings Inc.\n  InvoiceIssuerName: Hilton Worldwide Holdings Inc.\n  PricingCategory: Commission\n  PricingUnit: booking\n  BillingCurrency: USD\n  ChargeCategory: Usage\nprinciples:\n  - name: Visibility\n    description: Reconcile booking activity through the partner portal's reporting feeds (booking,\n      cancellation, no-show, loyalty-event events) against Hilton statements.\n  - name: Allocation\n    description: Tag bookings by partner channel, brand, market, and corporate-rate code so commission\n\
  \      and revenue-share are attributable per business unit.\n  - name: Optimization\n    description: Cost levers are commission renegotiation, parity enforcement, and shifting traffic to\n      lower-commission direct or loyalty channels.\n  - name: Accountability\n    description: Distribution / commercial team owns commission accounts; technology team owns\n      connectivity uptime and 429 / error rates.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Rate Optimization\n      - Workload Optimization\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\n\
  meters:\n  - name: bookings\n    description: Reservations confirmed through the partner connectivity API\n    unit: booking\n    aggregation: sum\n    dimensions:\n      - partner_id\n      - brand\n      - property_id\n      - market\n      - rate_code\n  - name: room_nights\n    description: Room nights generated\n    unit: room-night\n    aggregation: sum\n    dimensions:\n      - partner_id\n      - brand\n      - property_id\n  - name: gross_booking_value\n    description: Gross dollar value of confirmed bookings\n    unit: USD\n    aggregation: sum\n    dimensions:\n      - partner_id\n      - brand\n      - property_id\n  - name: commissions\n    description: Commission paid (or due) to the partner\n    unit: USD\n    aggregation: sum\n    dimensions:\n      - partner_id\n      - brand\n  - name: loyalty_points_issued\n    description: Hilton Honors points issued or accrued via the partner\n    unit: point\n    aggregation: sum\n    dimensions:\n      - partner_id\n      - brand\n\
  apis:\n  - name: Hilton Developer API\n    baseURL: https://api.hilton.com\n    tags:\n      - Hospitality\n      - Hotels\n      - Reservations\n      - Loyalty\n    serviceName: Hilton Developer API\n    serviceCategory: Hospitality / Travel\nunitEconomics:\n  - name: Effective Commission Rate\n    metric: commissions / gross_booking_value\n    target: per partner agreement\n  - name: Cost per Booking\n    metric: commissions / bookings\n    target: per partner agreement\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/hilton/refs/heads/main/finops/hilton-finops.yml
sources:
- https://www.hilton.com/en/corporate/
specification: FinOps Framework
tags:
- Hospitality
- Hotels
- Travel
- Reservations
- Loyalty
- FinOps
- FOCUS
---
