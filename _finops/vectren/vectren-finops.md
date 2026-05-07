---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  pricingCategory: Tariff
description: 'FOCUS-aligned FinOps stub for Vectren / CenterPoint Energy: a regulated utility, not an API vendor. Costs are tariff-based energy delivery, not SaaS or API consumption.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: CenterPoint Energy, Inc.
  ProviderName: CenterPoint Energy
  PublisherName: CenterPoint Energy, Inc.
  ServiceCategory: Utility
  ServiceName: Vectren / CenterPoint Energy Service
layout: finops
meters:
- aggregation: sum
  description: Metered energy delivery (kWh / therms) per customer account; not an API meter.
  name: energy_consumption
  unit: varies
name: Vectren Finops
provider_name: Vectren (CenterPoint Energy)
provider_slug: vectren
publisher_name: CenterPoint Energy, Inc.
service_category: Utility
slug: vectren-finops
source_filename: vectren-finops.yml
source_heading: FinOps Profile
source_url: https://www.centerpointenergy.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Vectren (CenterPoint Energy)\nproviderId: vectren\npublisherName: CenterPoint Energy, Inc.\nserviceCategory: Utility\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Utility\n  - Energy\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps stub for Vectren / CenterPoint Energy: a regulated utility, not an API\n  vendor. Costs are tariff-based energy delivery, not SaaS or API consumption.'\nsources:\n  - https://www.centerpointenergy.com/\nnotes: Regulated-utility billing falls outside the API FinOps scope. No public usage/billing API. Stub\n  retained for catalog completeness only.\nbillingModel:\n  pricingCategory:\
  \ Tariff\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\nfocusColumns:\n  ServiceName: Vectren / CenterPoint Energy Service\n  ServiceCategory: Utility\n  ProviderName: CenterPoint Energy\n  PublisherName: CenterPoint Energy, Inc.\n  InvoiceIssuerName: CenterPoint Energy, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: energy_consumption\n    description: Metered energy delivery (kWh / therms) per customer account; not an API meter.\n    unit: varies\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Customers view consumption via the CenterPoint Energy customer portal and monthly bill;\n      no developer-facing telemetry is exposed.\n  - name: Allocation\n    description: Allocation is per service address / account number, governed by the utility tariff.\n  - name: Optimization\n    description: Optimization is consumption-side (energy efficiency programs, demand response) rather\n      than rate-card optimization; the\
  \ rate is regulated.\n  - name: Accountability\n    description: Accountability sits with the customer of record on the utility account; CenterPoint Energy\n      bills monthly per regulated tariff.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n    url: https://apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/vectren/refs/heads/main/finops/vectren-finops.yml
sources:
- https://www.centerpointenergy.com/
specification: FinOps Framework
tags:
- Utility
- Energy
- FinOps
- FOCUS
---
