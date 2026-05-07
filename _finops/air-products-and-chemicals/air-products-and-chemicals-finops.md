---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD/EUR/GBP
  billingFrequency: Monthly
  chargeCategories:
  - Purchase
  - Usage
  - Tax
  - Adjustment
  pricingCategory: Take-or-Pay / Long-Term Supply
description: FOCUS-aligned shape for Air Products. Cost surface is industrial-gas product, on-site equipment, and services under long-term supply contracts — not API consumption. APIs and telemetry are integration plumbing covered by the supply agreement.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Air Products and Chemicals, Inc.
  ProviderName: Air Products and Chemicals
  PublisherName: Air Products and Chemicals, Inc.
  ServiceCategory: Industrial Gases / Chemicals
  ServiceName: Industrial Gas Supply
layout: finops
meters:
- aggregation: sum
  description: Industrial-gas product delivered (hydrogen, oxygen, nitrogen, helium, argon, etc.)
  dimensions:
  - product
  - delivery_mode
  - site
  - region
  name: gas_volume
  unit: varies
- aggregation: sum
  description: On-site tank, vaporizer, and equipment rental
  dimensions:
  - equipment_type
  - site
  name: equipment_rental
  unit: equipment-month
- aggregation: sum
  description: Delivery, fuel surcharge, hazmat, and transport fees
  dimensions:
  - mode
  - region
  name: delivery_charges
  unit: delivery
- aggregation: sum
  description: API requests against Air Products portal / telemetry endpoints (customer-side telemetry)
  dimensions:
  - integration
  - site
  name: api_requests
  unit: request
name: Air Products And Chemicals Finops
provider_name: Air Products and Chemicals
provider_slug: air-products-and-chemicals
publisher_name: Air Products and Chemicals, Inc.
service_category: Industrial Gases / Chemicals
slug: air-products-and-chemicals-finops
source_filename: air-products-and-chemicals-finops.yml
source_heading: FinOps Profile
source_url: https://www.airproducts.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Air Products and Chemicals\nproviderId: air-products-and-chemicals\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Air Products and Chemicals, Inc.\nserviceCategory: Industrial Gases / Chemicals\ntags:\n  - Industrial Gases\n  - Chemicals\n  - Energy\n  - Manufacturing\n  - Hydrogen\n  - FinOps\n  - FOCUS\ndescription: FOCUS-aligned shape for Air Products. Cost surface is industrial-gas product, on-site\n  equipment, and services under long-term supply contracts — not API consumption. APIs and telemetry\n  are integration plumbing covered by the supply agreement.\nnotes: No API rate card; meters reflect the industrial-gas\
  \ billing surface (product volume, equipment,\n  delivery) plus customer-side API request telemetry.\nsources:\n  - https://www.airproducts.com/\nbillingModel:\n  pricingCategory: Take-or-Pay / Long-Term Supply\n  billingFrequency: Monthly\n  billingCurrency: USD/EUR/GBP\n  chargeCategories:\n    - Purchase\n    - Usage\n    - Tax\n    - Adjustment\nfocusColumns:\n  ServiceName: Industrial Gas Supply\n  ServiceCategory: Industrial Gases / Chemicals\n  ProviderName: Air Products and Chemicals\n  PublisherName: Air Products and Chemicals, Inc.\n  InvoiceIssuerName: Air Products and Chemicals, Inc.\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: gas_volume\n    description: Industrial-gas product delivered (hydrogen, oxygen, nitrogen, helium, argon, etc.)\n    unit: varies\n    aggregation: sum\n    dimensions:\n      - product\n      - delivery_mode\n      - site\n      - region\n  - name: equipment_rental\n    description: On-site tank, vaporizer, and equipment rental\n\
  \    unit: equipment-month\n    aggregation: sum\n    dimensions:\n      - equipment_type\n      - site\n  - name: delivery_charges\n    description: Delivery, fuel surcharge, hazmat, and transport fees\n    unit: delivery\n    aggregation: sum\n    dimensions:\n      - mode\n      - region\n  - name: api_requests\n    description: API requests against Air Products portal / telemetry endpoints (customer-side telemetry)\n    unit: request\n    aggregation: sum\n    dimensions:\n      - integration\n      - site\nprinciples:\n  - name: Visibility\n    description: Track Air Products spend at the site / product level via the MyAirProducts portal and\n      monthly invoices; correlate with on-site tank telemetry to see consumption vs delivery cadence.\n  - name: Allocation\n    description: Allocate by site, business unit, and gas product; tank-level telemetry is the natural\n      allocation key.\n  - name: Optimization\n    description: Optimize through right-sizing tank capacity, scheduling\
  \ deliveries to avoid emergency\n      runs, consolidating gas products where feasible, and re-negotiating take-or-pay tiers at renewal.\n  - name: Accountability\n    description: Plant operations and procurement jointly own the Air Products contract; align reviews\n      with the gas-supply renewal cycle and major capex (on-site plant) decisions.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/air-products-and-chemicals/refs/heads/main/finops/air-products-and-chemicals-finops.yml
sources:
- https://www.airproducts.com/
specification: FinOps Framework
tags:
- Industrial Gases
- Chemicals
- Energy
- Manufacturing
- Hydrogen
- FinOps
- FOCUS
---
