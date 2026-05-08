---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: rtx-eagle-api-openapi.yml
  format: yaml
  label: RTX EAGLE API
  slug: eagle-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/rtx/refs/heads/main/openapi/rtx-eagle-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Per Contract
  chargeCategories:
  - Purchase
  pricingCategory: Government Program Contract
description: RTX defense and aerospace software is sold under government program contracts. FinOps treatment is program-cost driven, not usage-metered.
focus_columns:
  BillingCurrency: USD
  ProviderName: RTX
  PublisherName: RTX Corporation
  ServiceCategory: Defense / Aerospace Software
  ServiceName: RTX Defense Software
layout: finops
meters:
- aggregation: sum
  description: Program-contract obligation lines (FFP, cost-plus, T&M)
  dimensions:
  - program
  - contract_type
  name: program_cost
  unit: contract_line
name: Rtx Finops
provider_name: RTX
provider_slug: rtx
publisher_name: RTX Corporation
service_category: Defense / Aerospace Software
slug: rtx-finops
source_filename: rtx-finops.yml
source_heading: FinOps Profile
source_url: https://www.rtx.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: RTX\nproviderId: rtx\npublisherName: RTX Corporation\nserviceCategory: Defense / Aerospace Software\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Defense\n  - Aerospace\n  - Government\n  - FinOps\n  - FOCUS\ndescription: >-\n  RTX defense and aerospace software is sold under government program contracts. FinOps\n  treatment is program-cost driven, not usage-metered.\nnotes: >-\n  No public usage API or itemized billing exists. Cost is dominated by program-of-record\n  contracts and FFP / cost-plus structures rather than pay-as-you-go meters.\nsources:\n  - https://www.rtx.com/\nbillingModel:\n  pricingCategory: Government\
  \ Program Contract\n  billingFrequency: Per Contract\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: RTX Defense Software\n  ServiceCategory: Defense / Aerospace Software\n  ProviderName: RTX\n  PublisherName: RTX Corporation\n  BillingCurrency: USD\nmeters:\n  - name: program_cost\n    description: Program-contract obligation lines (FFP, cost-plus, T&M)\n    unit: contract_line\n    aggregation: sum\n    dimensions:\n      - program\n      - contract_type\nprinciples:\n  - name: Visibility\n    description: >-\n      Track RTX program cost through DFARS-compliant cost-accounting reports and the prime\n      contractor's program-management dashboards.\n  - name: Allocation\n    description: >-\n      Allocate RTX program cost to the contract WBS and the consuming program-of-record, not\n      to general IT.\n  - name: Optimization\n    description: >-\n      Optimization levers are program-management driven (scope control, EVM, sub-contract\n\
  \      management) rather than infrastructure auto-scaling.\n  - name: Accountability\n    description: >-\n      Program managers and contracting officers own RTX-related cost; review through standard\n      EVM and milestone reviews.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/rtx/refs/heads/main/finops/rtx-finops.yml
sources:
- https://www.rtx.com/
specification: FinOps Framework
tags:
- Defense
- Aerospace
- Government
- FinOps
- FOCUS
---
