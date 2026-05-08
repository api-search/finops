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
  - Purchase
  - Tax
  - Adjustment
  - Refund
  pricingCategory: Regulated Utility Tariff + Partner Contract
description: FOCUS-aligned FinOps for CenterPoint Energy's integration surfaces. The Smart Meter Texas TPSP and Green Button Connect My Data APIs are free under regulator / consortium policy; the only invoice surfaces visible to a partner are (a) the underlying utility bill driven by metered consumption and (b) any Centerpoint Connect partner contract for the contractor / field-service platform.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: CenterPoint Energy, Inc.
  ProviderName: CenterPoint Energy
  PublisherName: CenterPoint Energy, Inc.
  ServiceCategory: Utility Data
  ServiceName: CenterPoint Energy APIs
layout: finops
meters:
- aggregation: sum
  dimensions:
  - tpsp
  - account
  name: smt_usage_inquiries
  unit: request
- aggregation: count
  dimensions:
  - third_party
  name: green_button_authorizations
  unit: authorization
- aggregation: sum
  dimensions:
  - account
  - service_class
  name: interval_kwh_delivered
  unit: kWh
- aggregation: sum
  dimensions:
  - partner
  - operation
  name: cpc_api_requests
  unit: request
- aggregation: sum
  dimensions:
  - account
  - service_class
  - region
  name: utility_invoiced_amount
  unit: USD
name: Centerpoint Energy Finops
provider_name: CenterPoint Energy
provider_slug: centerpoint-energy
publisher_name: CenterPoint Energy, Inc.
service_category: Utility (Energy + Gas)
slug: centerpoint-energy-finops
source_filename: centerpoint-energy-finops.yml
source_heading: FinOps Profile
source_url: https://www.smartmetertexas.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: CenterPoint Energy\nproviderId: centerpoint-energy\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Energy\n  - Utility\n  - Smart Meter\n  - Green Button\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps for CenterPoint Energy''s integration surfaces. The Smart Meter Texas\n  TPSP and Green Button Connect My Data APIs are free under regulator / consortium policy; the only\n  invoice surfaces visible to a partner are (a) the underlying utility bill driven by metered consumption\n  and (b) any Centerpoint Connect partner contract for the contractor / field-service platform.'\nnotes: API access is free (SMT, Green Button) or partner-contracted (Centerpoint Connect). Meters track\n  usage and invoice signals rather than per-call charges.\nsources:\n  - https://www.smartmetertexas.com/\n  - https://www.energy.gov/data/green-button\n\
  \  - https://api-portal.centerpointconnect.io/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: CenterPoint Energy, Inc.\nserviceCategory: Utility (Energy + Gas)\nbillingModel:\n  pricingCategory: Regulated Utility Tariff + Partner Contract\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Adjustment\n    - Refund\nfocusColumns:\n  ServiceName: CenterPoint Energy APIs\n  ServiceCategory: Utility Data\n  ProviderName: CenterPoint Energy\n  PublisherName: CenterPoint Energy, Inc.\n  InvoiceIssuerName: CenterPoint Energy, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: smt_usage_inquiries\n    unit: request\n    aggregation: sum\n    dimensions:\n      - tpsp\n      - account\n  - name: green_button_authorizations\n    unit: authorization\n\
  \    aggregation: count\n    dimensions:\n      - third_party\n  - name: interval_kwh_delivered\n    unit: kWh\n    aggregation: sum\n    dimensions:\n      - account\n      - service_class\n  - name: cpc_api_requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - partner\n      - operation\n  - name: utility_invoiced_amount\n    unit: USD\n    aggregation: sum\n    dimensions:\n      - account\n      - service_class\n      - region\nprinciples:\n  - name: Visibility\n    description: Pull SMT TPSP usage exports nightly to see authorized account interval data, and combine\n      with the customer's CenterPoint utility bill to reconcile observed kWh with billed kWh.\n  - name: Allocation\n    description: Tag SMT / Green Button authorizations with the consuming product team and the customer's\n      cost center so utility-data costs are allocated where the data drives business outcomes.\n  - name: Optimization\n    description: Use Green Button bulk authorization windows\
  \ rather than continuous polling; align SMT\n      requests with the overnight batch cadence; cache results that don't change intra-day.\n  - name: Accountability\n    description: Energy / facilities lead owns the utility bill; integration platform owner manages SMT\n      TPSP registration and Green Button consent flows; partner ops owns the Centerpoint Connect contract.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/centerpoint-energy/refs/heads/main/finops/centerpoint-energy-finops.yml
sources:
- https://www.smartmetertexas.com/
- https://www.energy.gov/data/green-button
- https://api-portal.centerpointconnect.io/
specification: FinOps Framework
tags:
- Energy
- Utility
- Smart Meter
- Green Button
- FinOps
- FOCUS
---
