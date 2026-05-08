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
description: FOCUS-aligned FinOps placeholder for PotlatchDeltic. The provider does not publish a public API pricing surface, so there are no documented meters or unit prices to align to FOCUS. Any cost allocation lives inside the bilateral partner / member contract.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: PotlatchDeltic Corporation (now part of Rayonier Inc.)
  ProviderName: PotlatchDeltic
  PublisherName: PotlatchDeltic Corporation (now part of Rayonier Inc.)
  ServiceCategory: Materials
  ServiceName: PotlatchDeltic
  ServiceSubcategory: Timber and Wood Products
layout: finops
meters:
- aggregation: sum
  description: Negotiated contract fee or member dues; the actual unit (per-month, per-transaction, percent-of-spend) is defined in the executed agreement.
  dimensions:
  - contract
  - department
  name: contract_fee
  unit: varies
name: Potlatch Finops
provider_name: PotlatchDeltic
provider_slug: potlatch
publisher_name: PotlatchDeltic Corporation (now part of Rayonier Inc.)
service_category: Materials
slug: potlatch-finops
source_filename: potlatch-finops.yml
source_heading: FinOps Profile
source_url: https://www.rayonier.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: PotlatchDeltic\nproviderId: potlatch\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Timber\n  - Real Estate\n  - Wood Products\n  - FinOps\n  - FOCUS\ndescription: >-\n  FOCUS-aligned FinOps placeholder for PotlatchDeltic. The provider does not publish\n  a public API pricing surface, so there are no documented meters or unit\n  prices to align to FOCUS. Any cost allocation lives inside the bilateral\n  partner / member contract.\nsources:\n  - https://www.rayonier.com/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: PotlatchDeltic Corporation (now part of Rayonier Inc.)\nserviceCategory: Materials\nbillingModel:\n  pricingCategory: Contract / Custom\n\
  \  billingFrequency: Per-Contract\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Adjustment\nfocusColumns:\n  ServiceName: PotlatchDeltic\n  ServiceCategory: Materials\n  ServiceSubcategory: Timber and Wood Products\n  ProviderName: PotlatchDeltic\n  PublisherName: PotlatchDeltic Corporation (now part of Rayonier Inc.)\n  InvoiceIssuerName: PotlatchDeltic Corporation (now part of Rayonier Inc.)\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: contract_fee\n    description: Negotiated contract fee or member dues; the actual unit (per-month, per-transaction, percent-of-spend) is defined in the executed agreement.\n    unit: varies\n    aggregation: sum\n    dimensions:\n      - contract\n      - department\nprinciples:\n  - name: Visibility\n    description: Cost visibility for PotlatchDeltic comes from the negotiated contract artifacts and the consuming organization's AP / procurement system rather than from a provider usage API.\n  - name: Allocation\n\
  \    description: Allocate by the cost center or business unit listed on the contract; there is no provider-side tag surface.\n  - name: Optimization\n    description: Renegotiate at renewal; consolidate purchasing through procurement; benchmark against peer organizations where possible.\n  - name: Accountability\n    description: The contract owner / category manager is accountable for spend; review at the contract renewal cadence.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\nnotes: >-\n  No public pricing or billing documentation exists. Reconciled=false\n  because there is nothing publicly published to align to FOCUS columns or\n  meters.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/potlatch/refs/heads/main/finops/potlatch-finops.yml
sources:
- https://www.rayonier.com/
specification: FinOps Framework
tags:
- Timber
- Real Estate
- Wood Products
- FinOps
- FOCUS
---
