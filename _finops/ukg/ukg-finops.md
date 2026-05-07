---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: ukg-pro-hcm-openapi.yml
  format: yaml
  label: UKG Pro HCM API
  slug: ukg-pro-hcm-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/ukg/refs/heads/main/openapi/ukg-pro-hcm-openapi.yml
- filename: ukg-pro-wfm-openapi.yml
  format: yaml
  label: UKG Pro Workforce Management API
  slug: ukg-pro-wfm-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/ukg/refs/heads/main/openapi/ukg-pro-wfm-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Purchase
  - Tax
  - Adjustment
  pricingCategory: Enterprise Subscription
description: 'FOCUS-aligned FinOps for UKG: HCM SaaS billed under enterprise contract; per-employee / per-module pricing not published publicly. Spend reconciliation requires the customer-only Developer Hub and contract-side invoice detail.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: UKG Inc.
  ProviderName: UKG
  PublisherName: UKG Inc.
  ServiceCategory: HCM / Workforce Management
  ServiceName: UKG
layout: finops
meters:
- aggregation: max
  description: PEPM consumption (typical UKG billing primitive — exact value contractual)
  dimensions:
  - product
  - module
  name: employees_per_employee_per_month
  unit: seat
- aggregation: sum
  description: Module-level entitlement (Payroll, Time, Talent, Benefits, etc.)
  dimensions:
  - module
  name: module_subscription
  unit: month
name: Ukg Finops
provider_name: UKG
provider_slug: ukg
publisher_name: UKG Inc.
service_category: HCM / Workforce Management
slug: ukg-finops
source_filename: ukg-finops.yml
source_heading: FinOps Profile
source_url: https://developer.ukg.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: UKG\nproviderId: ukg\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - HCM\n  - Workforce Management\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps for UKG: HCM SaaS billed under enterprise contract; per-employee /\n  per-module pricing not published publicly. Spend reconciliation requires the customer-only Developer\n  Hub and contract-side invoice detail.'\nnotes: UKG does not publish public per-module / per-employee pricing or usage telemetry. Meters and FOCUS\n  columns are placeholders pending reconciliation against an actual contract and invoice.\nsources:\n  - https://developer.ukg.com/\n  - https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\n\
  publisherName: UKG Inc.\nserviceCategory: HCM / Workforce Management\nbillingModel:\n  pricingCategory: Enterprise Subscription\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Tax\n    - Adjustment\nfocusColumns:\n  ServiceName: UKG\n  ServiceCategory: HCM / Workforce Management\n  ProviderName: UKG\n  PublisherName: UKG Inc.\n  InvoiceIssuerName: UKG Inc.\n  BillingCurrency: USD\nmeters:\n  - name: employees_per_employee_per_month\n    description: PEPM consumption (typical UKG billing primitive — exact value contractual)\n    unit: seat\n    aggregation: max\n    dimensions:\n      - product\n      - module\n  - name: module_subscription\n    description: Module-level entitlement (Payroll, Time, Talent, Benefits, etc.)\n    unit: month\n    aggregation: sum\n    dimensions:\n      - module\nprinciples:\n  - name: Visibility\n    description: Track active employee headcount per UKG module via the gated Developer Hub APIs and\n      the\
  \ UKG admin console; reconcile against the contract PEPM rate.\n  - name: Allocation\n    description: Allocate to business units / cost centers using UKG organization hierarchy and labor-account\n      structures.\n  - name: Optimization\n    description: Right-size module subscriptions; deactivate unused entitlements during renewals; consolidate\n      between UKG Pro and UKG Ready footprints where possible.\n  - name: Accountability\n    description: HRIS / Total Rewards owners review headcount-driven UKG spend ahead of renewal; finance\n      validates PEPM against the invoice.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/ukg/refs/heads/main/finops/ukg-finops.yml
sources:
- https://developer.ukg.com/
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- HCM
- Workforce Management
- FinOps
- FOCUS
---
