---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: Per Pay Cycle / Monthly
  chargeCategories:
  - Purchase
  - Usage
  - Tax
  pricingCategory: Subscription + Per-Employee Per-Payroll
description: FinOps definition for Paychex. APIs are bundled with the underlying payroll / HR / benefits product subscription; no standalone API rate card. Meters reflect typical payroll-SaaS billing (employees, payrolls run, benefits administration).
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Paychex, Inc.
  ProviderName: Paychex
  PublisherName: Paychex, Inc.
  ServiceCategory: Payroll / HR
  ServiceName: Paychex
layout: finops
meters:
- aggregation: sum
  description: Active employees included in a payroll run
  dimensions:
  - company
  - pay_cycle
  name: employees_paid
  unit: employee
- aggregation: count
  description: Number of payroll runs in the billing period
  dimensions:
  - company
  - frequency
  name: payrolls_run
  unit: payroll
- aggregation: max
  description: Employees enrolled in administered benefits
  dimensions:
  - company
  - plan
  name: benefits_seats
  unit: seat-month
- aggregation: count
  description: API requests against Paychex Developer APIs (bundled, not separately metered in public pricing)
  dimensions:
  - client_id
  - product
  name: api_requests
  unit: request
name: Paychex Finops
provider_name: Paychex
provider_slug: paychex
publisher_name: Paychex, Inc.
service_category: Payroll / HR
slug: paychex-finops
source_filename: paychex-finops.yml
source_heading: FinOps Profile
source_url: https://developer.paychex.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Paychex\nproviderId: paychex\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\nnotes: No public per-API price. Paychex bills clients for the underlying payroll / HR / benefits\n  product; API access is bundled. Structural FinOps placeholder reflecting the SaaS payroll\n  shape.\ntags:\n  - FinOps\n  - FOCUS\n  - Payroll\n  - HR\n  - Benefits\ndescription: FinOps definition for Paychex. APIs are bundled with the underlying payroll\n  / HR / benefits product subscription; no standalone API rate card. Meters reflect typical\n  payroll-SaaS billing (employees, payrolls run, benefits administration).\nsources:\n  - https://developer.paychex.com/\n  - https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n\
  \  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Paychex, Inc.\nserviceCategory: Payroll / HR\nbillingModel:\n  pricingCategory: Subscription + Per-Employee Per-Payroll\n  billingFrequency: Per Pay Cycle / Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\n    - Tax\nfocusColumns:\n  ServiceName: Paychex\n  ServiceCategory: Payroll / HR\n  ProviderName: Paychex\n  PublisherName: Paychex, Inc.\n  InvoiceIssuerName: Paychex, Inc.\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: employees_paid\n    description: Active employees included in a payroll run\n    unit: employee\n    aggregation: sum\n    dimensions:\n      - company\n      - pay_cycle\n  - name: payrolls_run\n    description: Number of payroll runs in the billing period\n    unit: payroll\n    aggregation: count\n    dimensions:\n      - company\n      - frequency\n  - name: benefits_seats\n    description: Employees enrolled in administered\
  \ benefits\n    unit: seat-month\n    aggregation: max\n    dimensions:\n      - company\n      - plan\n  - name: api_requests\n    description: API requests against Paychex Developer APIs (bundled, not separately metered\n      in public pricing)\n    unit: request\n    aggregation: count\n    dimensions:\n      - client_id\n      - product\nprinciples:\n  - name: Visibility\n    description: Visibility comes from the Paychex client portal and the monthly invoice;\n      API requests are not separately billed line items in public pricing.\n  - name: Allocation\n    description: Allocate by Paychex client number and by integrated app (client_id) when\n      using the developer APIs.\n  - name: Optimization\n    description: Optimize by reducing manual payroll adjustments (which can carry per-action\n      fees), automating onboarding/offboarding through the API, and rationalizing benefits\n      plans.\n  - name: Accountability\n    description: Payroll / HR director accountable for the\
  \ Paychex contract; integration\n      owner accountable for API consumer behavior.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/paychex/refs/heads/main/finops/paychex-finops.yml
sources:
- https://developer.paychex.com/
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Payroll
- HR
- Benefits
---
