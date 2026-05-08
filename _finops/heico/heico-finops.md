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
  - Purchase
  - Tax
  - Adjustment
  pricingCategory: Purchase Order (Goods)
description: FOCUS-aligned FinOps stub for HEICO. HEICO does not bill for API access; spend is component purchase-order based.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: HEICO Corporation (operating subsidiary)
  PricingCategory: Purchase
  PricingUnit: part
  ProviderName: HEICO Corporation
  PublisherName: HEICO Corporation
  ServiceCategory: Aerospace / Defense
  ServiceName: HEICO Corporation
layout: finops
meters:
- aggregation: sum
  description: Component / part purchase-order line items
  dimensions:
  - subsidiary
  - part_number
  - aircraft_program
  name: component_purchases
  unit: part
name: Heico Finops
provider_name: HEICO Corporation
provider_slug: heico
publisher_name: HEICO Corporation
service_category: Aerospace / Defense
slug: heico-finops
source_filename: heico-finops.yml
source_heading: FinOps Profile
source_url: https://www.heico.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: HEICO Corporation\nproviderId: heico\npublisherName: HEICO Corporation\nserviceCategory: Aerospace / Defense\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Aerospace\n  - Aviation\n  - Defense\n  - FinOps\n  - FOCUS\nnotes: HEICO is a hardware / aerospace component conglomerate, not a SaaS / API vendor. There is no\n  invoice surface for API consumption to track in FinOps; spend with HEICO is purchase-order-based against\n  components and parts. Meters here are stubs documenting that shape.\ndescription: 'FOCUS-aligned FinOps stub for HEICO. HEICO does not bill for API access; spend is component\n  purchase-order based.'\nsources:\n  - https://www.heico.com/\n\
  billingModel:\n  pricingCategory: Purchase Order (Goods)\n  billingFrequency: Per-Invoice\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Tax\n    - Adjustment\nfocusColumns:\n  ServiceName: HEICO Corporation\n  ServiceCategory: Aerospace / Defense\n  ProviderName: HEICO Corporation\n  PublisherName: HEICO Corporation\n  InvoiceIssuerName: HEICO Corporation (operating subsidiary)\n  PricingCategory: Purchase\n  PricingUnit: part\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nprinciples:\n  - name: Visibility\n    description: Track spend through procurement / ERP systems against HEICO PO numbers and component part\n      numbers. There is no public usage API to call.\n  - name: Allocation\n    description: Allocate component spend to fleet, aircraft tail, or program through ERP cost-center tags.\n  - name: Optimization\n    description: Levers are procurement-side - alternative-source qualification, overhaul-versus-replace\n      decisions, and volume agreements.\n\
  \  - name: Accountability\n    description: Procurement / supply-chain owns the relationship and PO lifecycle; engineering owns\n      part-substitution decisions.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Allocation\n      - Reporting and Analytics\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Rate Optimization\n      - Workload Optimization\n  - name: Manage the FinOps Practice\n    capabilities:\n      - Invoicing and Chargeback\n      - Intersecting Disciplines\nmeters:\n  - name: component_purchases\n    description: Component / part purchase-order line items\n    unit: part\n    aggregation: sum\n    dimensions:\n      - subsidiary\n      - part_number\n      - aircraft_program\napis:\n  - name: HEICO Corporation API\n    baseURL: https://api.heico.com\n    tags:\n      - Aerospace\n      - Aviation\n    \
  \  - Defense\n    serviceName: HEICO Corporation API\n    serviceCategory: Aerospace / Defense\nunitEconomics:\n  - name: Cost per Component\n    metric: po_total / parts_received\n    target: per procurement agreement\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/heico/refs/heads/main/finops/heico-finops.yml
sources:
- https://www.heico.com/
specification: FinOps Framework
tags:
- Aerospace
- Aviation
- Defense
- FinOps
- FOCUS
---
