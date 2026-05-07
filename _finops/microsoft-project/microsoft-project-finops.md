---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: microsoft-project-rest-api.yaml
  format: yaml
  label: Microsoft Project Online REST API
  slug: rest-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-project/refs/heads/main/openapi/microsoft-project-rest-api.yaml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  - Tax
  - Adjustment
  - Credit
  pricingCategory: Tiered Subscription
description: 'FOCUS-aligned FinOps for Microsoft Project: tiered per-user subscriptions (Planner, Plan 1, Plan 3) plus optional one-time on-prem licenses, billed monthly via Microsoft 365 commerce.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Microsoft Corporation
  PricingUnit: seat-month
  ProviderName: Microsoft
  PublisherName: Microsoft Corporation
  ServiceCategory: Project Management
  ServiceName: Microsoft Project
layout: finops
meters:
- aggregation: sum
  dimensions:
  - tenant
  - assigned_user
  name: planner_seats
  unit: seat-month
- aggregation: sum
  dimensions:
  - tenant
  - assigned_user
  name: plan1_seats
  unit: seat-month
- aggregation: sum
  dimensions:
  - tenant
  - assigned_user
  name: plan3_seats
  unit: seat-month
- aggregation: count
  dimensions:
  - tenant
  name: standard_2024_licenses
  unit: license
- aggregation: count
  dimensions:
  - tenant
  name: professional_2024_licenses
  unit: license
- aggregation: sum
  dimensions:
  - user
  - environment
  name: power_platform_requests
  unit: request
name: Microsoft Project Finops
provider_name: Microsoft Project
provider_slug: microsoft-project
publisher_name: Microsoft Corporation
service_category: Project Management
slug: microsoft-project-finops
source_filename: microsoft-project-finops.yml
source_heading: FinOps Profile
source_url: https://www.microsoft.com/en-us/microsoft-365/project/compare-microsoft-project-management-software
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Microsoft Project\nproviderId: microsoft-project\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Cost Management\n  - Microsoft\n  - Project Management\ndescription: 'FOCUS-aligned FinOps for Microsoft Project: tiered per-user subscriptions (Planner, Plan 1,\n  Plan 3) plus optional one-time on-prem licenses, billed monthly via Microsoft 365 commerce.'\nsources:\n  - https://www.microsoft.com/en-us/microsoft-365/project/compare-microsoft-project-management-software\n  - https://learn.microsoft.com/en-us/power-platform/admin/api-request-limits-allocations\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Microsoft Corporation\nserviceCategory:\
  \ Project Management\nbillingModel:\n  pricingCategory: Tiered Subscription\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Adjustment\n    - Credit\nfocusColumns:\n  ServiceName: Microsoft Project\n  ServiceCategory: Project Management\n  ProviderName: Microsoft\n  PublisherName: Microsoft Corporation\n  InvoiceIssuerName: Microsoft Corporation\n  BillingCurrency: USD\n  PricingUnit: seat-month\n  ChargeCategory: Usage\nmeters:\n  - name: planner_seats\n    unit: seat-month\n    aggregation: sum\n    dimensions:\n      - tenant\n      - assigned_user\n  - name: plan1_seats\n    unit: seat-month\n    aggregation: sum\n    dimensions:\n      - tenant\n      - assigned_user\n  - name: plan3_seats\n    unit: seat-month\n    aggregation: sum\n    dimensions:\n      - tenant\n      - assigned_user\n  - name: standard_2024_licenses\n    unit: license\n    aggregation: count\n    dimensions:\n      - tenant\n  - name: professional_2024_licenses\n\
  \    unit: license\n    aggregation: count\n    dimensions:\n      - tenant\n  - name: power_platform_requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - user\n      - environment\nprinciples:\n  - name: Visibility\n    description: Use the Microsoft 365 admin center license-usage report and the Power Platform admin\n      center capacity reports to expose per-tenant seat consumption and Power Platform request usage\n      over time.\n  - name: Allocation\n    description: Allocate Plan 1 / Plan 3 seats by Microsoft 365 license group; tag each Project\n      Online tenant with cost-center metadata to roll up to PMO budget owners.\n  - name: Optimization\n    description: Right-size between Planner-included, Plan 1 ($10), and Plan 3 ($30) per actual usage;\n      avoid blanket Plan 3 assignment for users who only need Planner. Reserve on-prem one-time licenses\n      for users who never need cloud collaboration. Plan migration off Plan 5 before 2026-05-01 EOS.\n\
  \  - name: Accountability\n    description: Review monthly Plan 3 utilization against checked-in projects; reclaim seats from\n      inactive users; enforce a finance approval step on >100-seat additions.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/microsoft-project/refs/heads/main/finops/microsoft-project-finops.yml
sources:
- https://www.microsoft.com/en-us/microsoft-365/project/compare-microsoft-project-management-software
- https://learn.microsoft.com/en-us/power-platform/admin/api-request-limits-allocations
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Cost Management
- Microsoft
- Project Management
---
