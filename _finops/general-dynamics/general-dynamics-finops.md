---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: general-dynamics-mission-systems-api-openapi.yml
  format: yaml
  label: General Dynamics Mission Systems API
  slug: mission-systems-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/general-dynamics/refs/heads/main/openapi/general-dynamics-mission-systems-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Per-Invoice
  chargeCategories:
  - Purchase
  - Adjustment
  pricingCategory: Contract / Program
description: General Dynamics revenue is contract-based across defense, aerospace, marine, and technology services. There is no SaaS or API billing surface; FinOps for downstream consumers applies to program / contract management rather than per-call usage.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: General Dynamics Corporation
  ProviderName: General Dynamics
  PublisherName: General Dynamics Corporation
  ServiceCategory: Defense & Aerospace
  ServiceName: General Dynamics
layout: finops
meters:
- aggregation: count
  dimensions:
  - program
  - contract_id
  name: contract_milestones
  unit: milestone
- aggregation: sum
  dimensions:
  - program
  - labor_category
  name: program_hours
  unit: hour
- aggregation: sum
  dimensions:
  - program
  - cdrl
  name: deliverables
  unit: unit
name: General Dynamics Finops
provider_name: General Dynamics
provider_slug: general-dynamics
publisher_name: General Dynamics Corporation
service_category: Defense & Aerospace
slug: general-dynamics-finops
source_filename: general-dynamics-finops.yml
source_heading: FinOps Profile
source_url: https://www.gd.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: General Dynamics\nproviderId: general-dynamics\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Defense\n  - Aerospace\ndescription: General Dynamics revenue is contract-based across defense, aerospace, marine, and\n  technology services. There is no SaaS or API billing surface; FinOps for downstream consumers\n  applies to program / contract management rather than per-call usage.\nnotes: No public API or pricing surface; FinOps shape inferred from a defense-contractor program\n  model.\nsources:\n  - https://www.gd.com/\n  - https://www.gdit.com/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: General Dynamics Corporation\nserviceCategory:\
  \ Defense & Aerospace\nbillingModel:\n  pricingCategory: Contract / Program\n  billingFrequency: Per-Invoice\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Adjustment\nfocusColumns:\n  ServiceName: General Dynamics\n  ServiceCategory: Defense & Aerospace\n  ProviderName: General Dynamics\n  PublisherName: General Dynamics Corporation\n  InvoiceIssuerName: General Dynamics Corporation\n  BillingCurrency: USD\nmeters:\n  - name: contract_milestones\n    unit: milestone\n    aggregation: count\n    dimensions:\n      - program\n      - contract_id\n  - name: program_hours\n    unit: hour\n    aggregation: sum\n    dimensions:\n      - program\n      - labor_category\n  - name: deliverables\n    unit: unit\n    aggregation: sum\n    dimensions:\n      - program\n      - cdrl\nprinciples:\n  - name: Visibility\n    description: Reconcile General Dynamics invoices against contract line items (CLINs) and\n      milestone schedules; track earned-value per program.\n  - name:\
  \ Allocation\n    description: Allocate program cost to mission / capability owners; tag CLINs to\n      appropriations.\n  - name: Optimization\n    description: Use IDIQ / multi-award vehicles to drive task-order competition; right-size\n      labor categories; review fixed-price vs cost-plus mix.\n  - name: Accountability\n    description: Program manager owns spend and EVM variance; contracting officer governs\n      change orders.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/general-dynamics/refs/heads/main/finops/general-dynamics-finops.yml
sources:
- https://www.gd.com/
- https://www.gdit.com/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Defense
- Aerospace
---
