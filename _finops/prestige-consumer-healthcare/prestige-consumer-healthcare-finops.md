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
description: FOCUS-aligned FinOps placeholder for Prestige Consumer Healthcare. The provider does not publish a public API pricing surface, so there are no documented meters or unit prices to align to FOCUS. Any cost allocation lives inside the bilateral partner / member contract.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Prestige Consumer Healthcare Inc.
  ProviderName: Prestige Consumer Healthcare
  PublisherName: Prestige Consumer Healthcare Inc.
  ServiceCategory: Consumer Healthcare
  ServiceName: Prestige Consumer Healthcare
  ServiceSubcategory: Over-the-Counter Healthcare Brands
layout: finops
meters:
- aggregation: sum
  description: Negotiated contract fee or member dues; the actual unit (per-month, per-transaction, percent-of-spend) is defined in the executed agreement.
  dimensions:
  - contract
  - department
  name: contract_fee
  unit: varies
name: Prestige Consumer Healthcare Finops
provider_name: Prestige Consumer Healthcare
provider_slug: prestige-consumer-healthcare
publisher_name: Prestige Consumer Healthcare Inc.
service_category: Consumer Healthcare
slug: prestige-consumer-healthcare-finops
source_filename: prestige-consumer-healthcare-finops.yml
source_heading: FinOps Profile
source_url: https://www.prestigebrands.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Prestige Consumer Healthcare\nproviderId: prestige-consumer-healthcare\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Consumer Healthcare\n  - OTC\n  - FinOps\n  - FOCUS\ndescription: >-\n  FOCUS-aligned FinOps placeholder for Prestige Consumer Healthcare. The provider does not publish\n  a public API pricing surface, so there are no documented meters or unit\n  prices to align to FOCUS. Any cost allocation lives inside the bilateral\n  partner / member contract.\nsources:\n  - https://www.prestigebrands.com/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Prestige Consumer Healthcare Inc.\nserviceCategory: Consumer Healthcare\nbillingModel:\n  pricingCategory:\
  \ Contract / Custom\n  billingFrequency: Per-Contract\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Adjustment\nfocusColumns:\n  ServiceName: Prestige Consumer Healthcare\n  ServiceCategory: Consumer Healthcare\n  ServiceSubcategory: Over-the-Counter Healthcare Brands\n  ProviderName: Prestige Consumer Healthcare\n  PublisherName: Prestige Consumer Healthcare Inc.\n  InvoiceIssuerName: Prestige Consumer Healthcare Inc.\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: contract_fee\n    description: Negotiated contract fee or member dues; the actual unit (per-month, per-transaction, percent-of-spend) is defined in the executed agreement.\n    unit: varies\n    aggregation: sum\n    dimensions:\n      - contract\n      - department\nprinciples:\n  - name: Visibility\n    description: Cost visibility for Prestige Consumer Healthcare comes from the negotiated contract artifacts and the consuming organization's AP / procurement system rather than\
  \ from a provider usage API.\n  - name: Allocation\n    description: Allocate by the cost center or business unit listed on the contract; there is no provider-side tag surface.\n  - name: Optimization\n    description: Renegotiate at renewal; consolidate purchasing through procurement; benchmark against peer organizations where possible.\n  - name: Accountability\n    description: The contract owner / category manager is accountable for spend; review at the contract renewal cadence.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\nnotes: >-\n  No public pricing or billing documentation exists. Reconciled=false\n  because there is nothing publicly published to align to FOCUS columns or\n  meters.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/prestige-consumer-healthcare/refs/heads/main/finops/prestige-consumer-healthcare-finops.yml
sources:
- https://www.prestigebrands.com/
specification: FinOps Framework
tags:
- Consumer Healthcare
- OTC
- FinOps
- FOCUS
---
