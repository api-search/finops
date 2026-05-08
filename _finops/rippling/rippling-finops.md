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
  - Adjustment
  - Tax
  pricingCategory: Subscription Per Seat
description: Rippling's billing model is per-employee-per-month subscription pricing across composable HR, IT, and Finance products with custom-quoted enterprise contracts. This artifact maps Rippling charges to FOCUS columns for FinOps allocation across cost centers and product lines.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Rippling
  ProviderName: Rippling
  PublisherName: Rippling
  ServiceCategory: HR
  ServiceName: Rippling
layout: finops
meters:
- aggregation: sum
  description: Required Rippling Platform seats; foundation for every product.
  dimensions:
  - department
  - cost_center
  name: platform_seats
  unit: employee-month
- aggregation: sum
  description: HR Cloud (HRIS, time off, performance, learning) per-employee fees.
  dimensions:
  - department
  - cost_center
  name: hr_cloud_seats
  unit: employee-month
- aggregation: sum
  description: US payroll per-employee fees plus tax-filing services.
  dimensions:
  - state
  - cost_center
  name: payroll_seats
  unit: employee-month
- aggregation: sum
  description: Native global payroll per-employee fees.
  dimensions:
  - country
  - cost_center
  name: global_payroll_seats
  unit: employee-month
- aggregation: sum
  description: Employer-of-record seats with country-specific cost loadings.
  dimensions:
  - country
  - cost_center
  name: eor_seats
  unit: employee-month
- aggregation: sum
  description: IT Cloud seats covering devices, MDM, apps, and identity.
  dimensions:
  - department
  - cost_center
  name: it_seats
  unit: employee-month
- aggregation: sum
  description: Spend product seats (cards, expenses, bill pay).
  dimensions:
  - department
  - cost_center
  name: spend_seats
  unit: employee-month
- aggregation: sum
  description: Recruiting seats per active hiring user or per-employee model.
  dimensions:
  - department
  - cost_center
  name: recruiting_seats
  unit: employee-month
- aggregation: sum
  description: Statutory benefits, payroll taxes, EOR loadings, hardware purchases.
  dimensions:
  - service
  - country
  name: pass_through_costs
  unit: events
name: Rippling Finops
provider_name: Rippling
provider_slug: rippling
publisher_name: Rippling
service_category: HR
slug: rippling-finops
source_filename: rippling-finops.yml
source_heading: FinOps Profile
source_url: https://www.rippling.com/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Rippling\nproviderId: rippling\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: true\ntags:\n  - HR\n  - HCM\n  - IT\n  - Payroll\n  - Spend Management\n  - FinOps\n  - FOCUS\ndescription: >-\n  Rippling's billing model is per-employee-per-month subscription pricing\n  across composable HR, IT, and Finance products with custom-quoted enterprise\n  contracts. This artifact maps Rippling charges to FOCUS columns for FinOps\n  allocation across cost centers and product lines.\nsources:\n  - https://www.rippling.com/pricing\n  - https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Rippling\nserviceCategory: HR\nbillingModel:\n\
  \  pricingCategory: Subscription Per Seat\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Adjustment\n    - Tax\nfocusColumns:\n  ServiceName: Rippling\n  ServiceCategory: HR\n  ProviderName: Rippling\n  PublisherName: Rippling\n  InvoiceIssuerName: Rippling\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: platform_seats\n    description: Required Rippling Platform seats; foundation for every product.\n    unit: employee-month\n    aggregation: sum\n    dimensions:\n      - department\n      - cost_center\n  - name: hr_cloud_seats\n    description: HR Cloud (HRIS, time off, performance, learning) per-employee fees.\n    unit: employee-month\n    aggregation: sum\n    dimensions:\n      - department\n      - cost_center\n  - name: payroll_seats\n    description: US payroll per-employee fees plus tax-filing services.\n    unit: employee-month\n    aggregation: sum\n    dimensions:\n      - state\n      - cost_center\n\
  \  - name: global_payroll_seats\n    description: Native global payroll per-employee fees.\n    unit: employee-month\n    aggregation: sum\n    dimensions:\n      - country\n      - cost_center\n  - name: eor_seats\n    description: Employer-of-record seats with country-specific cost loadings.\n    unit: employee-month\n    aggregation: sum\n    dimensions:\n      - country\n      - cost_center\n  - name: it_seats\n    description: IT Cloud seats covering devices, MDM, apps, and identity.\n    unit: employee-month\n    aggregation: sum\n    dimensions:\n      - department\n      - cost_center\n  - name: spend_seats\n    description: Spend product seats (cards, expenses, bill pay).\n    unit: employee-month\n    aggregation: sum\n    dimensions:\n      - department\n      - cost_center\n  - name: recruiting_seats\n    description: Recruiting seats per active hiring user or per-employee model.\n    unit: employee-month\n    aggregation: sum\n    dimensions:\n      - department\n      - cost_center\n\
  \  - name: pass_through_costs\n    description: Statutory benefits, payroll taxes, EOR loadings, hardware purchases.\n    unit: events\n    aggregation: sum\n    dimensions:\n      - service\n      - country\nprinciples:\n  - name: Visibility\n    description: >-\n      Pull Rippling monthly invoices and product-line statements; match\n      seat counts to active employees in HRIS.\n  - name: Allocation\n    description: >-\n      Allocate seats by department, cost center, and country using HRIS\n      attributes pushed via Platform API or webhooks.\n  - name: Optimization\n    description: >-\n      Audit monthly which Rippling products each employee uses; remove\n      seats for unused products and renegotiate bundles at renewal.\n  - name: Accountability\n    description: >-\n      Designate per-product owners (HRBP, IT lead, Finance lead) and\n      review against negotiated MSA at renewal.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/rippling/refs/heads/main/finops/rippling-finops.yml
sources:
- https://www.rippling.com/pricing
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- HR
- HCM
- IT
- Payroll
- Spend Management
- FinOps
- FOCUS
---
