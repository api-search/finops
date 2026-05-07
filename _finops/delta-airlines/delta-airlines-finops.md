---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: Per-Contract
  chargeCategories:
  - Usage
  - Purchase
  - Tax
  - Credit
  - Adjustment
  chargeFrequency: Recurring
  pricingCategory: Negotiated Partner Agreement
description: FOCUS-aligned FinOps for Delta Airlines APIs (scaffold). Distribution APIs typically follow per-shop and per-book transaction economics under negotiated NDC / partner agreements. No public per-call price exists.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Delta Air Lines, Inc.
  PricingCategory: Negotiated
  PricingUnit: transaction
  ProviderName: Delta Airlines
  PublisherName: Delta Air Lines, Inc.
  ServiceCategory: Travel / Airline Distribution
  ServiceName: Delta API Suite
layout: finops
meters:
- aggregation: sum
  description: NDC shopping / availability / fare-search calls
  dimensions:
  - partner
  - channel
  - market
  name: shop_requests
  unit: request
- aggregation: sum
  description: NDC orders / PNRs created
  dimensions:
  - partner
  - channel
  - market
  name: bookings
  unit: transaction
- aggregation: sum
  description: Ancillary services (seats, bags, upgrades) sold via API
  dimensions:
  - partner
  - product
  name: ancillaries_sold
  unit: transaction
name: Delta Airlines Finops
provider_name: Delta Airlines
provider_slug: delta-airlines
publisher_name: Delta Air Lines, Inc.
service_category: Travel / Airline Distribution
slug: delta-airlines-finops
source_filename: delta-airlines-finops.yml
source_heading: FinOps Profile
source_url: https://developer.delta.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Delta Airlines\nproviderId: delta-airlines\npublisherName: Delta Air Lines, Inc.\nserviceCategory: Travel / Airline Distribution\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\nnotes: Delta does not publish API pricing or usage telemetry; FinOps shape is inferred from NDC distribution\n  norms (per-shop / per-book transaction fees, GDS pass-throughs, partner agreements). Reconcile when\n  partner contract terms become available.\ntags:\n  - Air Travel\n  - Airlines\n  - NDC\n  - Travel\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps for Delta Airlines APIs (scaffold). Distribution APIs typically follow\n  per-shop and per-book transaction economics under negotiated\
  \ NDC / partner agreements. No public per-call\n  price exists.'\nsources:\n  - https://developer.delta.com/\nprinciples:\n  - name: Visibility\n    description: Track Delta NDC API consumption (shopping, pricing, booking, ticketing, ancillary) per\n      partner integration; reconcile shop-to-look ratios, look-to-book ratios, and per-PNR cost via partner\n      reporting feeds.\n  - name: Allocation\n    description: Allocate distribution costs by point-of-sale, channel, and brand; tag every API transaction\n      to the originating retailing platform or call center.\n  - name: Optimization\n    description: Apply NDC offer-management caching, repricing rules, and look-to-book guardrails; reduce\n      excess shopping volume that drives partner-fee ladders.\n  - name: Accountability\n    description: Distribution leaders own per-channel API economics; route NDC SLA breaches and shop-volume\n      anomalies to the contract owner.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n\
  \      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Rate Optimization\n      - Workload Optimization\n  - name: Manage the FinOps Practice\n    capabilities:\n      - Invoicing and Chargeback\n      - Onboarding Workloads\nbillingModel:\n  pricingCategory: Negotiated Partner Agreement\n  billingFrequency: Per-Contract\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Delta API Suite\n  ServiceCategory: Travel / Airline Distribution\n  ProviderName: Delta Airlines\n  PublisherName: Delta Air Lines, Inc.\n  InvoiceIssuerName: Delta Air Lines, Inc.\n  PricingCategory: Negotiated\n\
  \  PricingUnit: transaction\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: shop_requests\n    description: NDC shopping / availability / fare-search calls\n    unit: request\n    aggregation: sum\n    dimensions:\n      - partner\n      - channel\n      - market\n  - name: bookings\n    description: NDC orders / PNRs created\n    unit: transaction\n    aggregation: sum\n    dimensions:\n      - partner\n      - channel\n      - market\n  - name: ancillaries_sold\n    description: Ancillary services (seats, bags, upgrades) sold via API\n    unit: transaction\n    aggregation: sum\n    dimensions:\n      - partner\n      - product\napis:\n  - name: Delta API Suite\n    baseURL: https://developer.delta.com/\n    tags:\n      - Flights\n      - NDC\n      - Offers\n      - Orders\n      - Travel\n    serviceName: Delta API Suite\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per Booking\n    metric: distribution_cost / bookings\n    target: TBD\n  - name: Look-to-Book\
  \ Ratio\n    metric: shop_requests / bookings\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/delta-airlines/refs/heads/main/finops/delta-airlines-finops.yml
sources:
- https://developer.delta.com/
specification: FinOps Framework
tags:
- Air Travel
- Airlines
- NDC
- Travel
- FinOps
- FOCUS
---
