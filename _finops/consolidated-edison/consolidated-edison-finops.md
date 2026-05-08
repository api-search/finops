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
  - Tax
  - Adjustment
  pricingCategory: Regulated Utility Tariff
description: 'FOCUS-aligned FinOps for Consolidated Edison: regulated utility delivering energy under NY PSC tariffs; programmatic surface (Green Button Connect My Data) is consent-based and not separately billed. FinOps focuses on the underlying utility bill rather than API consumption.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Consolidated Edison Company of New York, Inc.
  ProviderName: Consolidated Edison
  PublisherName: Consolidated Edison Company of New York, Inc.
  ServiceCategory: Regulated Utility / Energy
  ServiceName: Consolidated Edison
layout: finops
meters:
- aggregation: sum
  description: Electricity delivered, kilowatt-hours, per regulated tariff
  dimensions:
  - service_class
  - rate_zone
  - account
  name: kwh_delivered
  unit: kWh
- aggregation: sum
  description: Natural gas delivered, therms
  dimensions:
  - service_class
  - account
  name: therms_delivered
  unit: therm
- aggregation: count
  description: Active Green Button Connect My Data authorizations (no charge)
  dimensions:
  - third_party
  name: gbc_authorizations
  unit: authorization
name: Consolidated Edison Finops
provider_name: Consolidated Edison
provider_slug: consolidated-edison
publisher_name: Consolidated Edison Company of New York, Inc.
service_category: Regulated Utility / Energy
slug: consolidated-edison-finops
source_filename: consolidated-edison-finops.yml
source_heading: FinOps Profile
source_url: https://www.coned.com
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Consolidated Edison\nproviderId: consolidated-edison\npublisherName: Consolidated Edison Company of New York, Inc.\nserviceCategory: Regulated Utility / Energy\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Energy\n  - Green Button\n  - Utility\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps for Consolidated Edison: regulated utility delivering energy under\n  NY PSC tariffs; programmatic surface (Green Button Connect My Data) is consent-based and not separately\n  billed. FinOps focuses on the underlying utility bill rather than API consumption.'\nnotes: Con Edison's commercial product is regulated electric\
  \ / gas / steam delivery, billed through utility\n  tariffs. The Green Button Connect feed itself is not metered or priced.\nsources:\n  - https://www.coned.com\n  - https://www.greenbuttondata.org\nbillingModel:\n  pricingCategory: Regulated Utility Tariff\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Tax\n    - Adjustment\nfocusColumns:\n  ServiceName: Consolidated Edison\n  ServiceCategory: Regulated Utility / Energy\n  ProviderName: Consolidated Edison\n  PublisherName: Consolidated Edison Company of New York, Inc.\n  InvoiceIssuerName: Consolidated Edison Company of New York, Inc.\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: kwh_delivered\n    description: Electricity delivered, kilowatt-hours, per regulated tariff\n    unit: kWh\n    aggregation: sum\n    dimensions:\n      - service_class\n      - rate_zone\n      - account\n  - name: therms_delivered\n    description: Natural gas delivered, therms\n    unit:\
  \ therm\n    aggregation: sum\n    dimensions:\n      - service_class\n      - account\n  - name: gbc_authorizations\n    description: Active Green Button Connect My Data authorizations (no charge)\n    unit: authorization\n    aggregation: count\n    dimensions:\n      - third_party\nprinciples:\n  - name: Visibility\n    description: Use Con Edison's My Account portal and Green Button Download My Data exports to surface\n      consumption per meter; the GBC feed gives Third Parties customer-consented near-real-time usage.\n  - name: Allocation\n    description: Allocate energy spend by physical meter / account / facility; for multi-tenant facilities\n      use submetering and ESPI feeds per consenting customer.\n  - name: Optimization\n    description: Demand-response programs, time-of-use rate selection, energy-efficiency rebates, and\n      gas-vs-electric optimization are the primary cost levers; the GBC feed surfaces interval data needed\n      to drive these decisions.\n  - name:\
  \ Accountability\n    description: Facilities / sustainability teams typically own utility spend; Third-Party authorized\n      services own the operational accuracy of the GBC integration.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/consolidated-edison/refs/heads/main/finops/consolidated-edison-finops.yml
sources:
- https://www.coned.com
- https://www.greenbuttondata.org
specification: FinOps Framework
tags:
- Energy
- Green Button
- Utility
- FinOps
- FOCUS
---
