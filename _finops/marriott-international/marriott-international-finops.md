---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: marriott-international-developer-api-openapi.yml
  format: yaml
  label: Marriott Developer API
  slug: developer-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/marriott-international/refs/heads/main/openapi/marriott-international-developer-api-openapi.yml
billing_model:
  billingCurrency: USD (settlement varies)
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Adjustment
  - Credit
  chargeFrequency: Recurring
  pricingCategory: Partner Commission (Per-Booking / Per-Stayed-Night)
description: 'FOCUS-aligned FinOps shape for Marriott International: distribution / connectivity API consumed under partner agreements. Cost is realized at the booking level (commission per stay) rather than at the per-API-call level, so meters track look-to-book efficiency alongside booking volume.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Marriott International, Inc.
  ProviderName: Marriott International
  PublisherName: Marriott International, Inc.
  ServiceCategory: Hospitality Distribution
  ServiceName: Marriott Developer API
layout: finops
meters:
- aggregation: sum
  description: Availability / shopping requests submitted by the partner.
  dimensions:
  - partner
  - brand
  - market
  - channel
  name: shopping_requests
  unit: request
- aggregation: sum
  description: Reservations successfully created via the API.
  dimensions:
  - partner
  - brand
  - property
  - channel
  name: bookings_created
  unit: booking
- aggregation: sum
  description: Nights actually stayed (post-arrival), the unit on which most distribution commission is settled.
  dimensions:
  - partner
  - brand
  - property
  - rate_plan
  name: stayed_nights
  unit: room-night
- aggregation: sum
  description: Commission paid by Marriott to the distribution partner (or vice versa, per contract).
  dimensions:
  - partner
  - brand
  - market
  name: commission_settled
  unit: USD
name: Marriott International Finops
provider_name: Marriott International
provider_slug: marriott-international
publisher_name: Marriott International, Inc.
service_category: Hospitality Distribution API
slug: marriott-international-finops
source_filename: marriott-international-finops.yml
source_heading: FinOps Profile
source_url: https://developer.marriott.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Marriott International\nproviderId: marriott-international\npublisherName: Marriott International, Inc.\nserviceCategory: Hospitality Distribution API\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Hospitality\n  - Hotels\n  - Travel\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps shape for Marriott International: distribution / connectivity API\n  consumed under partner agreements. Cost is realized at the booking level (commission per stay) rather\n  than at the per-API-call level, so meters track look-to-book efficiency alongside booking volume.'\nnotes: |\n  No public per-API-call pricing exists. The economic\
  \ unit for Marriott distribution is the booked / stayed\n  reservation; API call volume is governed by partner contract rather than directly billed.\nsources:\n  - https://developer.marriott.com/\n  - https://www.marriott.com/marriott/aboutmarriott.mi\nprinciples:\n  - name: Visibility\n    description: Reconcile partner production metrics (shopping calls, bookings created, stayed nights)\n      against the partner's monthly / quarterly distribution invoice. Monitor the look-to-book ratio\n      surfaced in the developer portal.\n  - name: Allocation\n    description: Allocate distribution cost by channel (leisure OTA, corporate, GDS, loyalty), brand,\n      and geographic market. Tag external transaction IDs with internal channel / campaign identifiers\n      at booking time to support chargeback to product or marketing teams.\n  - name: Optimization\n    description: Reduce wasted shopping traffic via cache and short-TTL availability storage, defer\n      non-revenue-impacting modify\
  \ calls, and consolidate connections through a single distribution\n      gateway where commercially viable.\n  - name: Accountability\n    description: Assign a connectivity owner who reviews look-to-book ratios, dispute volume, and commission\n      reconciliation each month with Marriott's distribution team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Rate Optimization\n      - Workload Optimization\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - Invoicing and Chargeback\n      - Onboarding Workloads\nbillingModel:\n  pricingCategory: Partner Commission (Per-Booking / Per-Stayed-Night)\n  billingFrequency:\
  \ Monthly\n  billingCurrency: USD (settlement varies)\n  chargeCategories:\n    - Usage\n    - Adjustment\n    - Credit\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Marriott Developer API\n  ServiceCategory: Hospitality Distribution\n  ProviderName: Marriott International\n  PublisherName: Marriott International, Inc.\n  InvoiceIssuerName: Marriott International, Inc.\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: shopping_requests\n    description: Availability / shopping requests submitted by the partner.\n    unit: request\n    aggregation: sum\n    dimensions:\n      - partner\n      - brand\n      - market\n      - channel\n  - name: bookings_created\n    description: Reservations successfully created via the API.\n    unit: booking\n    aggregation: sum\n    dimensions:\n      - partner\n      - brand\n      - property\n      - channel\n  - name: stayed_nights\n    description: Nights actually stayed (post-arrival), the unit on which most distribution\
  \ commission\n      is settled.\n    unit: room-night\n    aggregation: sum\n    dimensions:\n      - partner\n      - brand\n      - property\n      - rate_plan\n  - name: commission_settled\n    description: Commission paid by Marriott to the distribution partner (or vice versa, per contract).\n    unit: USD\n    aggregation: sum\n    dimensions:\n      - partner\n      - brand\n      - market\napis:\n  - name: Marriott Developer API\n    baseURL: https://devportalprod.marriott.com\n    tags:\n      - Hospitality\n      - Hotels\n      - Reservations\n      - Travel\n    serviceName: Marriott Developer API\n    serviceCategory: API\nunitEconomics:\n  - name: Look-to-Book Ratio\n    metric: shopping_requests / bookings_created\n    target: contractual ceiling\n  - name: Commission per Stayed Night\n    metric: commission_settled / stayed_nights\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/marriott-international/refs/heads/main/finops/marriott-international-finops.yml
sources:
- https://developer.marriott.com/
- https://www.marriott.com/marriott/aboutmarriott.mi
specification: FinOps Framework
tags:
- Hospitality
- Hotels
- Travel
- FinOps
- FOCUS
---
