---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: Per-Invoice
  chargeCategories:
  - Usage
  - Purchase
  - Tax
  - Adjustment
  - Credit
  pricingCategory: Per-Shipment + Contract
description: 'FOCUS-aligned FinOps framing for C.H. Robinson: freight brokerage and 3PL services billed per shipment / load / contract; Navisphere API access bundled with the underlying logistics service.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: C.H. Robinson Worldwide, Inc.
  ProviderName: C.H. Robinson
  PublisherName: C.H. Robinson Worldwide, Inc.
  ServiceCategory: Logistics
  ServiceName: C.H. Robinson Navisphere
layout: finops
meters:
- aggregation: sum
  dimensions:
  - mode
  - lane
  - service_level
  name: shipments
  unit: shipment
- aggregation: sum
  dimensions:
  - mode
  - region
  name: loads
  unit: load
- aggregation: sum
  dimensions:
  - mode
  - region
  name: managed_spend
  unit: USD
- aggregation: sum
  name: customs_entries
  unit: entry
name: Ch Robinson Worldwide Finops
provider_name: C.H. Robinson
provider_slug: ch-robinson-worldwide
publisher_name: C.H. Robinson Worldwide, Inc.
service_category: Logistics / Freight
slug: ch-robinson-worldwide-finops
source_filename: ch-robinson-worldwide-finops.yml
source_heading: FinOps Profile
source_url: https://developer.chrobinson.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: C.H. Robinson\nproviderId: ch-robinson-worldwide\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Logistics\n  - Freight\ndescription: 'FOCUS-aligned FinOps framing for C.H. Robinson: freight brokerage and 3PL services billed\n  per shipment / load / contract; Navisphere API access bundled with the underlying logistics service.'\nnotes: API consumption is not separately metered. Meters and FOCUS columns reflect the freight billing\n  surface.\nsources:\n  - https://developer.chrobinson.com/\n  - https://www.chrobinson.com/en-us/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: C.H. Robinson Worldwide, Inc.\nserviceCategory: Logistics\
  \ / Freight\nbillingModel:\n  pricingCategory: Per-Shipment + Contract\n  billingFrequency: Per-Invoice\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Adjustment\n    - Credit\nfocusColumns:\n  ServiceName: C.H. Robinson Navisphere\n  ServiceCategory: Logistics\n  ProviderName: C.H. Robinson\n  PublisherName: C.H. Robinson Worldwide, Inc.\n  InvoiceIssuerName: C.H. Robinson Worldwide, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: shipments\n    unit: shipment\n    aggregation: sum\n    dimensions:\n      - mode\n      - lane\n      - service_level\n  - name: loads\n    unit: load\n    aggregation: sum\n    dimensions:\n      - mode\n      - region\n  - name: managed_spend\n    unit: USD\n    aggregation: sum\n    dimensions:\n      - mode\n      - region\n  - name: customs_entries\n    unit: entry\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Use Navisphere reporting and the freight payment / settlement APIs for\
  \ shipment-level\n      cost; reconcile invoices against booked loads.\n  - name: Allocation\n    description: Allocate freight cost by mode, lane, and BU using PO / shipment metadata pushed through\n      the API.\n  - name: Optimization\n    description: Optimize mode mix, consolidate shipments, and exercise contract rate reviews; lean on\n      C.H. Robinson sourcing for spot-vs-contract decisions.\n  - name: Accountability\n    description: Logistics / supply chain function owns C.H. Robinson spend; audit accessorial charges\n      and review carrier performance.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/ch-robinson-worldwide/refs/heads/main/finops/ch-robinson-worldwide-finops.yml
sources:
- https://developer.chrobinson.com/
- https://www.chrobinson.com/en-us/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Logistics
- Freight
---
