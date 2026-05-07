---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: Per Contract Milestone
  chargeCategories:
  - Purchase
  pricingCategory: Project / Contract (T&M, FFP, Cost-Plus)
description: Structural FinOps placeholder for Parsons Corporation. Government / engineering services contractor; engagements are project-based with no public per-API pricing.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Parsons Corporation
  ProviderName: Parsons Corporation
  PublisherName: Parsons Corporation
  ServiceCategory: Engineering Services
  ServiceName: Parsons Engineering Services
layout: finops
meters:
- aggregation: count
  description: Contract milestone or progress-payment line
  dimensions:
  - contract
  - program
  name: contract_milestone
  unit: milestone
- aggregation: sum
  description: Billable labor hours for time-and-materials contracts
  dimensions:
  - role
  - program
  name: labor_hours
  unit: hour
name: Parsons Finops
provider_name: Parsons Corporation
provider_slug: parsons
publisher_name: Parsons Corporation
service_category: Engineering Services
slug: parsons-finops
source_filename: parsons-finops.yml
source_heading: FinOps Profile
source_url: https://www.parsons.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Parsons Corporation\nproviderId: parsons\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\nnotes: No public pricing or APIs — services-based government contractor. Structural FinOps\n  placeholder only.\ntags:\n  - FinOps\n  - FOCUS\n  - Engineering\n  - Defense\n  - Government\ndescription: Structural FinOps placeholder for Parsons Corporation. Government / engineering\n  services contractor; engagements are project-based with no public per-API pricing.\nsources:\n  - https://www.parsons.com/\n  - https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Parsons Corporation\nserviceCategory: Engineering Services\nbillingModel:\n\
  \  pricingCategory: Project / Contract (T&M, FFP, Cost-Plus)\n  billingFrequency: Per Contract Milestone\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: Parsons Engineering Services\n  ServiceCategory: Engineering Services\n  ProviderName: Parsons Corporation\n  PublisherName: Parsons Corporation\n  InvoiceIssuerName: Parsons Corporation\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: contract_milestone\n    description: Contract milestone or progress-payment line\n    unit: milestone\n    aggregation: count\n    dimensions:\n      - contract\n      - program\n  - name: labor_hours\n    description: Billable labor hours for time-and-materials contracts\n    unit: hour\n    aggregation: sum\n    dimensions:\n      - role\n      - program\nprinciples:\n  - name: Visibility\n    description: Visibility comes from contract reporting and earned-value management; not\n      from a public usage API.\n  - name: Allocation\n  \
  \  description: Allocate by program / contract and by labor category per FAR/CAS standards.\n  - name: Optimization\n    description: Optimization is contract-specific; managed via scope, schedule, and labor\n      mix.\n  - name: Accountability\n    description: Program manager accountable for cost performance; CFO oversight at the contract\n      level.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/parsons/refs/heads/main/finops/parsons-finops.yml
sources:
- https://www.parsons.com/
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Engineering
- Defense
- Government
---
