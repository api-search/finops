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
  - Purchase
  - Usage
  - Tax
  pricingCategory: Custom Contract
description: FOCUS-aligned FinOps shell for East West Bancorp; treasury-services integrations are billed through relationship-banking agreements rather than a public consumption meter.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: East West Bank
  ProviderName: East West Bancorp
  PublisherName: East West Bank
  ServiceCategory: Banking
  ServiceName: East West Bancorp API
layout: finops
meters:
- aggregation: sum
  dimensions:
  - product
  - account
  name: api_requests
  unit: request
- aggregation: sum
  name: ach_transactions
  unit: transaction
- aggregation: sum
  name: wire_transactions
  unit: transaction
name: East West Bancorp Finops
provider_name: East West Bancorp
provider_slug: east-west-bancorp
publisher_name: East West Bank
service_category: Banking
slug: east-west-bancorp-finops
source_filename: east-west-bancorp-finops.yml
source_heading: FinOps Profile
source_url: https://www.eastwestbank.com
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: East West Bancorp\nproviderId: east-west-bancorp\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Banking\n  - Financial Services\ndescription: 'FOCUS-aligned FinOps shell for East West Bancorp; treasury-services integrations are billed\n  through relationship-banking agreements rather than a public consumption meter.'\nnotes: No public API pricing or billing exists. Reconcile FOCUS columns and meters against actual treasury-services\n  fee schedules once available.\nsources:\n  - https://www.eastwestbank.com\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: East West Bank\nserviceCategory: Banking\nbillingModel:\n  pricingCategory:\
  \ Custom Contract\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\n    - Tax\nfocusColumns:\n  ServiceName: East West Bancorp API\n  ServiceCategory: Banking\n  ProviderName: East West Bancorp\n  PublisherName: East West Bank\n  InvoiceIssuerName: East West Bank\n  BillingCurrency: USD\nmeters:\n  - name: api_requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - product\n      - account\n  - name: ach_transactions\n    unit: transaction\n    aggregation: sum\n  - name: wire_transactions\n    unit: transaction\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Pull treasury-services analysis statements; map to FOCUS-formatted records.\n  - name: Allocation\n    description: Tag any API-driven payment by initiating business unit and cost center.\n  - name: Optimization\n    description: Negotiate volume tiers in account-analysis pricing; consolidate banking relationships.\n  - name: Accountability\n\
  \    description: Treasury operations owns reconciliation of monthly bank-fee charges.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/east-west-bancorp/refs/heads/main/finops/east-west-bancorp-finops.yml
sources:
- https://www.eastwestbank.com
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Banking
- Financial Services
---
