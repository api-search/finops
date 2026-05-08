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
  pricingCategory: Contract / Negotiated
description: FinOps shape for TriNet cannot be reconciled from public sources; pricing is consultative-only and PEO billing is delivered via traditional invoice rather than a usage API.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: TriNet Group, Inc.
  ProviderName: TriNet
  PublisherName: TriNet Group, Inc.
  ServiceCategory: HR / PEO
  ServiceName: TriNet
layout: finops
meters:
- aggregation: avg
  dimensions:
  - state
  - benefits_plan
  name: worksite_employees
  unit: seat
name: Trinet Group Finops
provider_name: TriNet Group
provider_slug: trinet-group
publisher_name: TriNet Group, Inc.
service_category: HR / PEO
slug: trinet-group-finops
source_filename: trinet-group-finops.yml
source_heading: FinOps Profile
source_url: https://www.trinet.com
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: TriNet Group\nproviderId: trinet-group\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - HR\n  - PEO\n  - Benefits\n  - Payroll\n  - FinOps\n  - FOCUS\ndescription: FinOps shape for TriNet cannot be reconciled from public sources; pricing is\n  consultative-only and PEO billing is delivered via traditional invoice rather than a usage API.\nsources:\n  - https://www.trinet.com\nnotes: TriNet is a PEO; pricing is per-company-quote and consumption telemetry for any partner\n  integration sits inside the authenticated partner portal. FOCUS columns and meters can only be\n  validated against the executed PEO contract.\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName:\
  \ TriNet Group, Inc.\nserviceCategory: HR / PEO\nbillingModel:\n  pricingCategory: Contract / Negotiated\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: TriNet\n  ServiceCategory: HR / PEO\n  ProviderName: TriNet\n  PublisherName: TriNet Group, Inc.\n  InvoiceIssuerName: TriNet Group, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: worksite_employees\n    unit: seat\n    aggregation: avg\n    dimensions:\n      - state\n      - benefits_plan\nprinciples:\n  - name: Visibility\n    description: Worksite employee count, benefits enrollment, and payroll runs are visible inside\n      the TriNet platform; finance reconciles against the monthly PEO invoice.\n  - name: Allocation\n    description: Allocate cost per worksite employee, state, and benefits plan using TriNet's\n      existing employee record dimensions.\n  - name: Optimization\n    description: Optimization is contractual — review benefits plan mix and PEO\
  \ scope at renewal.\n  - name: Accountability\n    description: HR / People Operations owns the TriNet relationship; finance manages the monthly\n      PEO invoice cycle.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/trinet-group/refs/heads/main/finops/trinet-group-finops.yml
sources:
- https://www.trinet.com
specification: FinOps Framework
tags:
- HR
- PEO
- Benefits
- Payroll
- FinOps
- FOCUS
---
