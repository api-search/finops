---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: Per-Contract
  chargeCategories:
  - Purchase
  - Adjustment
  pricingCategory: Contract / Custom
description: FOCUS-aligned FinOps placeholder for Portland General Electric. The provider does not publish a public API pricing surface, so there are no documented meters or unit prices to align to FOCUS. Any cost allocation lives inside the bilateral partner / member contract.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Portland General Electric Company
  ProviderName: Portland General Electric
  PublisherName: Portland General Electric Company
  ServiceCategory: Utilities
  ServiceName: Portland General Electric
  ServiceSubcategory: Electric Utility
layout: finops
meters:
- aggregation: sum
  description: Negotiated contract fee or member dues; the actual unit (per-month, per-transaction, percent-of-spend) is defined in the executed agreement.
  dimensions:
  - contract
  - department
  name: contract_fee
  unit: varies
name: Portland General Electric Finops
provider_name: Portland General Electric
provider_slug: portland-general-electric
publisher_name: Portland General Electric Company
service_category: Utilities
slug: portland-general-electric-finops
source_filename: portland-general-electric-finops.yml
source_heading: FinOps Profile
source_url: https://portlandgeneral.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Portland General Electric\nproviderId: portland-general-electric\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Utilities\n  - Electric\n  - Energy\n  - FinOps\n  - FOCUS\ndescription: >-\n  FOCUS-aligned FinOps placeholder for Portland General Electric. The provider does not publish\n  a public API pricing surface, so there are no documented meters or unit\n  prices to align to FOCUS. Any cost allocation lives inside the bilateral\n  partner / member contract.\nsources:\n  - https://portlandgeneral.com/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Portland General Electric Company\nserviceCategory: Utilities\nbillingModel:\n  pricingCategory:\
  \ Contract / Custom\n  billingFrequency: Per-Contract\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Adjustment\nfocusColumns:\n  ServiceName: Portland General Electric\n  ServiceCategory: Utilities\n  ServiceSubcategory: Electric Utility\n  ProviderName: Portland General Electric\n  PublisherName: Portland General Electric Company\n  InvoiceIssuerName: Portland General Electric Company\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: contract_fee\n    description: Negotiated contract fee or member dues; the actual unit (per-month, per-transaction, percent-of-spend) is defined in the executed agreement.\n    unit: varies\n    aggregation: sum\n    dimensions:\n      - contract\n      - department\nprinciples:\n  - name: Visibility\n    description: Cost visibility for Portland General Electric comes from the negotiated contract artifacts and the consuming organization's AP / procurement system rather than from a provider usage API.\n  - name:\
  \ Allocation\n    description: Allocate by the cost center or business unit listed on the contract; there is no provider-side tag surface.\n  - name: Optimization\n    description: Renegotiate at renewal; consolidate purchasing through procurement; benchmark against peer organizations where possible.\n  - name: Accountability\n    description: The contract owner / category manager is accountable for spend; review at the contract renewal cadence.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\nnotes: >-\n  No public pricing or billing documentation exists. Reconciled=false\n  because there is nothing publicly published to align to FOCUS columns or\n  meters.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/portland-general-electric/refs/heads/main/finops/portland-general-electric-finops.yml
sources:
- https://portlandgeneral.com/
specification: FinOps Framework
tags:
- Utilities
- Electric
- Energy
- FinOps
- FOCUS
---
