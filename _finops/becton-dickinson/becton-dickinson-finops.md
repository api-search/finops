---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  - Tax
  - Adjustment
  chargeFrequency: Recurring
  pricingCategory: Hospital Services Agreement
description: 'FOCUS-aligned FinOps shape for BD Incada and BD Pyxis: hospital-services agreement billed per platform license + connected-device scope, with API access bundled. Public rate-card data is not available.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Becton, Dickinson and Company
  PricingCategory: Hospital Services Agreement
  PricingUnit: device
  ProviderName: Becton Dickinson
  PublisherName: Becton, Dickinson and Company
  ServiceCategory: Healthcare / Medical Device Connectivity
  ServiceName: BD Connected Care
layout: finops
meters:
- aggregation: max
  description: BD devices integrated through Incada / Pyxis
  dimensions:
  - device_class
  - hospital_unit
  name: connected_devices
  unit: device
- aggregation: max
  description: BD Pyxis automated dispensing stations under management
  dimensions:
  - hospital_unit
  name: pyxis_stations
  unit: station
- aggregation: sum
  description: Medication dispense / administration events tracked through Pyxis / Incada
  dimensions:
  - hospital_unit
  - medication_class
  name: medication_events
  unit: event
- aggregation: sum
  description: AI-analytics seats / use-case licenses
  dimensions:
  - module
  - hospital_unit
  name: ai_analytics_seats
  unit: seat
name: Becton Dickinson Finops
provider_name: Becton Dickinson
provider_slug: becton-dickinson
publisher_name: Becton, Dickinson and Company
service_category: Healthcare / Medical Device Connectivity
slug: becton-dickinson-finops
source_filename: becton-dickinson-finops.yml
source_heading: FinOps Profile
source_url: https://www.bd.com/en-us/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Becton Dickinson\nproviderId: becton-dickinson\npublisherName: Becton, Dickinson and Company\nserviceCategory: Healthcare / Medical Device Connectivity\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Healthcare\n  - Medical Devices\n  - Medication Management\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps shape for BD Incada and BD Pyxis: hospital-services agreement billed\n  per platform license + connected-device scope, with API access bundled. Public rate-card data is not\n  available.'\nnotes: No public rate card. Replace meter values with the customer-negotiated BD agreement once available.\nsources:\n  - https://www.bd.com/en-us/\nprinciples:\n\
  \  - name: Visibility\n    description: Use BD Incada's natural-language analytics and Pyxis reporting to attribute medication\n      use, infusion volume, and inventory by hospital unit.\n  - name: Allocation\n    description: Allocate platform cost across nursing units (ICU, peri-op, oncology) and pharmacy by\n      connected-device count and medication-event volume.\n  - name: Optimization\n    description: Right-size connected-device scope each renewal; consolidate Pyxis station footprint where\n      utilization is low. Use AI inventory analytics to reduce stockouts and waste.\n  - name: Accountability\n    description: Joint biomed / pharmacy ownership of the BD engagement; review uptime, integration changes,\n      and medication-safety metrics quarterly.\nbillingModel:\n  pricingCategory: Hospital Services Agreement\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Tax\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n\
  \  ServiceName: BD Connected Care\n  ServiceCategory: Healthcare / Medical Device Connectivity\n  ProviderName: Becton Dickinson\n  PublisherName: Becton, Dickinson and Company\n  InvoiceIssuerName: Becton, Dickinson and Company\n  PricingCategory: Hospital Services Agreement\n  PricingUnit: device\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: connected_devices\n    description: BD devices integrated through Incada / Pyxis\n    unit: device\n    aggregation: max\n    dimensions:\n      - device_class\n      - hospital_unit\n  - name: pyxis_stations\n    description: BD Pyxis automated dispensing stations under management\n    unit: station\n    aggregation: max\n    dimensions:\n      - hospital_unit\n  - name: medication_events\n    description: Medication dispense / administration events tracked through Pyxis / Incada\n    unit: event\n    aggregation: sum\n    dimensions:\n      - hospital_unit\n      - medication_class\n  - name: ai_analytics_seats\n    description:\
  \ AI-analytics seats / use-case licenses\n    unit: seat\n    aggregation: sum\n    dimensions:\n      - module\n      - hospital_unit\napis:\n  - name: BD Incada Connected Care Platform\n    baseURL: ''\n    serviceName: BD Incada Connected Care Platform\n    serviceCategory: API\n  - name: BD Pyxis Medication Management System\n    baseURL: ''\n    serviceName: BD Pyxis Medication Management System\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per Connected Device\n    metric: platform_cost / connected_devices\n    target: align to per-device clinical / inventory savings\n  - name: Cost per Pyxis Station\n    metric: pyxis_cost / pyxis_stations\n    target: align to medication-safety + waste-reduction targets\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/becton-dickinson/refs/heads/main/finops/becton-dickinson-finops.yml
sources:
- https://www.bd.com/en-us/
specification: FinOps Framework
tags:
- Healthcare
- Medical Devices
- Medication Management
- FinOps
- FOCUS
---
