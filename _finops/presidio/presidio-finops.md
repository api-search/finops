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
description: FOCUS-aligned FinOps placeholder for Presidio Inc. The provider does not publish a public API pricing surface, so there are no documented meters or unit prices to align to FOCUS. Any cost allocation lives inside the bilateral partner / member contract.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Presidio, Inc.
  ProviderName: Presidio Inc
  PublisherName: Presidio, Inc.
  ServiceCategory: IT Services
  ServiceName: Presidio Inc
  ServiceSubcategory: Cloud, Security, and Digital Infrastructure
layout: finops
meters:
- aggregation: sum
  description: Negotiated contract fee or member dues; the actual unit (per-month, per-transaction, percent-of-spend) is defined in the executed agreement.
  dimensions:
  - contract
  - department
  name: contract_fee
  unit: varies
name: Presidio Finops
provider_name: Presidio Inc
provider_slug: presidio
publisher_name: Presidio, Inc.
service_category: IT Services
slug: presidio-finops
source_filename: presidio-finops.yml
source_heading: FinOps Profile
source_url: https://www.presidio.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Presidio Inc\nproviderId: presidio\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - IT Solutions\n  - Cloud\n  - Security\n  - FinOps\n  - FOCUS\ndescription: >-\n  FOCUS-aligned FinOps placeholder for Presidio Inc. The provider does not publish\n  a public API pricing surface, so there are no documented meters or unit\n  prices to align to FOCUS. Any cost allocation lives inside the bilateral\n  partner / member contract.\nsources:\n  - https://www.presidio.com/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Presidio, Inc.\nserviceCategory: IT Services\nbillingModel:\n  pricingCategory: Contract / Custom\n  billingFrequency: Per-Contract\n  billingCurrency:\
  \ USD\n  chargeCategories:\n    - Purchase\n    - Adjustment\nfocusColumns:\n  ServiceName: Presidio Inc\n  ServiceCategory: IT Services\n  ServiceSubcategory: Cloud, Security, and Digital Infrastructure\n  ProviderName: Presidio Inc\n  PublisherName: Presidio, Inc.\n  InvoiceIssuerName: Presidio, Inc.\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: contract_fee\n    description: Negotiated contract fee or member dues; the actual unit (per-month, per-transaction, percent-of-spend) is defined in the executed agreement.\n    unit: varies\n    aggregation: sum\n    dimensions:\n      - contract\n      - department\nprinciples:\n  - name: Visibility\n    description: Cost visibility for Presidio Inc comes from the negotiated contract artifacts and the consuming organization's AP / procurement system rather than from a provider usage API.\n  - name: Allocation\n    description: Allocate by the cost center or business unit listed on the contract; there is no provider-side\
  \ tag surface.\n  - name: Optimization\n    description: Renegotiate at renewal; consolidate purchasing through procurement; benchmark against peer organizations where possible.\n  - name: Accountability\n    description: The contract owner / category manager is accountable for spend; review at the contract renewal cadence.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\nnotes: >-\n  No public pricing or billing documentation exists. Reconciled=false\n  because there is nothing publicly published to align to FOCUS columns or\n  meters.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/presidio/refs/heads/main/finops/presidio-finops.yml
sources:
- https://www.presidio.com/
specification: FinOps Framework
tags:
- IT Solutions
- Cloud
- Security
- FinOps
- FOCUS
---
