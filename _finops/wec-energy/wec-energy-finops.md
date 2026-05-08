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
  pricingCategory: Regulated Utility Tariff
description: FinOps placement for WEC Energy Group. The "spend" surface here is regulated utility charges (kWh / therms) at the operating-company level plus any data-sharing-agreement fees, not a metered developer API.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: We Energies / WPS / Peoples Gas / North Shore Gas / MGU / MERC / UMERC
  ProviderName: WEC Energy Group
  PublisherName: WEC Energy Group, Inc.
  ServiceCategory: Energy / Utility
  ServiceName: WEC Energy Group
layout: finops
meters:
- aggregation: sum
  description: Electricity delivered to the meter at the operating-company tariff.
  dimensions:
  - operating_company
  - rate_class
  - meter_id
  name: electric_consumption
  unit: kWh
- aggregation: sum
  description: Natural gas delivered to the meter at the operating-company tariff.
  dimensions:
  - operating_company
  - rate_class
  - meter_id
  name: gas_consumption
  unit: therm
name: Wec Energy Finops
provider_name: WEC Energy Group
provider_slug: wec-energy
publisher_name: WEC Energy Group, Inc.
service_category: Energy / Utility
slug: wec-energy-finops
source_filename: wec-energy-finops.yml
source_heading: FinOps Profile
source_url: https://www.wecenergygroup.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: WEC Energy Group\nproviderId: wec-energy\npublisherName: WEC Energy Group, Inc.\nserviceCategory: Energy / Utility\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Energy\n  - Electric Utility\n  - Fortune 500\n  - Green Button\n  - FinOps\n  - FOCUS\n  - Contact Sales\ndescription: FinOps placement for WEC Energy Group. The \"spend\" surface here is regulated utility\n  charges (kWh / therms) at the operating-company level plus any data-sharing-agreement fees, not a\n  metered developer API.\nnotes: No public usage-billing API for developer integrations. FOCUS mapping reflects utility-billing\n  shape only.\nsources:\n\
  \  - https://www.wecenergygroup.com/\nbillingModel:\n  pricingCategory: Regulated Utility Tariff\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Tax\nfocusColumns:\n  ServiceName: WEC Energy Group\n  ServiceCategory: Energy / Utility\n  ProviderName: WEC Energy Group\n  PublisherName: WEC Energy Group, Inc.\n  InvoiceIssuerName: We Energies / WPS / Peoples Gas / North Shore Gas / MGU / MERC / UMERC\n  BillingCurrency: USD\nmeters:\n  - name: electric_consumption\n    description: Electricity delivered to the meter at the operating-company tariff.\n    unit: kWh\n    aggregation: sum\n    dimensions:\n      - operating_company\n      - rate_class\n      - meter_id\n  - name: gas_consumption\n    description: Natural gas delivered to the meter at the operating-company tariff.\n    unit: therm\n    aggregation: sum\n    dimensions:\n      - operating_company\n      - rate_class\n      - meter_id\nprinciples:\n  - name: Visibility\n    description:\
  \ Spend visibility is via the operating-company customer portal and Green Button\n      Download / Connect for the authorized customer; there is no public corporate usage API.\n  - name: Allocation\n    description: Allocate energy spend by site / meter / rate-class using the operating-company account\n      hierarchy and Green Button service-point IDs.\n  - name: Optimization\n    description: Optimization levers are tariff selection, demand-response participation, energy-efficiency\n      programs, and on-site generation under the operating company's interconnection rules.\n  - name: Accountability\n    description: Facilities / energy-management owners hold accountability and engage the operating\n      company's commercial / large-customer team for tariff and program decisions.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/wec-energy/refs/heads/main/finops/wec-energy-finops.yml
sources:
- https://www.wecenergygroup.com/
specification: FinOps Framework
tags:
- Energy
- Electric Utility
- Fortune 500
- Green Button
- FinOps
- FOCUS
- Contact Sales
---
