---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly / Per-Milestone
  chargeCategories:
  - Purchase
  - Usage
  - Adjustment
  - Credit
  pricingCategory: Government Contract (FFP / T&M / Per-Transaction)
description: 'FOCUS-aligned FinOps shape for Maximus: government / commercial contractor priced via contract vehicles (fixed-price, time-and-materials, per-case). FinOps focus is on contract milestone tracking and per-transaction unit economics, not per-API-call billing.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Maximus, Inc.
  ProviderName: Maximus
  PublisherName: Maximus, Inc.
  ServiceCategory: Government Services / IT Modernization
  ServiceName: Maximus Services
layout: finops
meters:
- aggregation: max
  description: Total contract / task-order value, billed against milestones.
  dimensions:
  - contract
  - clin
  - agency
  name: contract_value
  unit: USD
- aggregation: sum
  description: Eligibility cases or contact-center calls handled (per-transaction contract vehicles).
  dimensions:
  - contract
  - state
  - program
  name: cases_handled
  unit: case
- aggregation: sum
  description: Billable labor hours under T&M contracts.
  dimensions:
  - contract
  - labor_category
  name: labor_hours
  unit: hour
name: Maximus Finops
provider_name: Maximus
provider_slug: maximus
publisher_name: Maximus, Inc.
service_category: Government Services / IT Modernization
slug: maximus-finops
source_filename: maximus-finops.yml
source_heading: FinOps Profile
source_url: https://www.maximus.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Maximus\nproviderId: maximus\npublisherName: Maximus, Inc.\nserviceCategory: Government Services / IT Modernization\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Government Services\n  - Health\n  - Technology\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps shape for Maximus: government / commercial contractor priced via\n  contract vehicles (fixed-price, time-and-materials, per-case). FinOps focus is on contract milestone\n  tracking and per-transaction unit economics, not per-API-call billing.'\nnotes: |\n  No public per-API pricing. Cost is allocated by program / contract / task order; meters represent\n\
  \  contract-level economic units rather than API requests.\nsources:\n  - https://www.maximus.com/\n  - https://www.maximus.com/federal\nprinciples:\n  - name: Visibility\n    description: Track program spend at the task-order / contract-line-item-number (CLIN) level via\n      government invoicing systems (e.g. WAWF / iRAPT for DoD, Treasury IPP for civilian) and integrate\n      with internal ERP for project burn-down.\n  - name: Allocation\n    description: Allocate by contract / task order / CLIN. For state / health programs, allocate by\n      state and program (Medicaid, CHIP, child support); for federal IT, allocate by agency, system,\n      and ATO boundary.\n  - name: Optimization\n    description: Optimize contract structure (firm-fixed-price vs. T&M vs. per-case), automate eligibility\n      and contact-center tasks where appropriate, and pursue option years / extensions where unit economics\n      improve at scale.\n  - name: Accountability\n    description: Assign a contract\
  \ / program manager per CLIN responsible for invoicing, milestone delivery,\n      and government acceptance of deliverables.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Allocation\n      - Reporting and Analytics\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Workload Optimization\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - Invoicing and Chargeback\n      - Onboarding Workloads\nbillingModel:\n  pricingCategory: Government Contract (FFP / T&M / Per-Transaction)\n  billingFrequency: Monthly / Per-Milestone\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\n    - Adjustment\n    - Credit\nfocusColumns:\n  ServiceName: Maximus Services\n  ServiceCategory: Government Services / IT Modernization\n  ProviderName: Maximus\n\
  \  PublisherName: Maximus, Inc.\n  InvoiceIssuerName: Maximus, Inc.\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: contract_value\n    description: Total contract / task-order value, billed against milestones.\n    unit: USD\n    aggregation: max\n    dimensions:\n      - contract\n      - clin\n      - agency\n  - name: cases_handled\n    description: Eligibility cases or contact-center calls handled (per-transaction contract vehicles).\n    unit: case\n    aggregation: sum\n    dimensions:\n      - contract\n      - state\n      - program\n  - name: labor_hours\n    description: Billable labor hours under T&M contracts.\n    unit: hour\n    aggregation: sum\n    dimensions:\n      - contract\n      - labor_category\napis:\n  - name: Maximus API\n    baseURL: https://api.maximus.com\n    tags:\n      - Government Services\n      - Health\n      - Technology\n    serviceName: Maximus API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per Case Handled\n\
  \    metric: billed_cost / cases_handled\n    target: TBD\n  - name: Labor Recovery Rate\n    metric: billable_hours / total_hours\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/maximus/refs/heads/main/finops/maximus-finops.yml
sources:
- https://www.maximus.com/
- https://www.maximus.com/federal
specification: FinOps Framework
tags:
- Government Services
- Health
- Technology
- FinOps
- FOCUS
---
