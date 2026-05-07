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
  pricingCategory: Contract / Negotiated
description: FinOps shape for Triumph Group cannot be reconciled; the company is an aerospace manufacturer with no public API business and no usage telemetry surface.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Triumph Group, Inc.
  ProviderName: Triumph Group
  PublisherName: Triumph Group, Inc.
  ServiceCategory: Aerospace / Defense
  ServiceName: Triumph Group API
layout: finops
meters:
- aggregation: sum
  dimensions:
  - contract
  name: contract_fees
  unit: varies
name: Triumph Group Finops
provider_name: Triumph Group
provider_slug: triumph-group
publisher_name: Triumph Group, Inc.
service_category: Aerospace / Defense
slug: triumph-group-finops
source_filename: triumph-group-finops.yml
source_heading: FinOps Profile
source_url: https://www.triumphgroup.com
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Triumph Group\nproviderId: triumph-group\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Aerospace\n  - Defense\n  - Manufacturing\n  - FinOps\n  - FOCUS\ndescription: FinOps shape for Triumph Group cannot be reconciled; the company is an aerospace\n  manufacturer with no public API business and no usage telemetry surface.\nsources:\n  - https://www.triumphgroup.com\nnotes: Triumph Group is an aerospace / defense manufacturer; it does not publish API pricing,\n  billing, or usage telemetry. Any FOCUS mapping would only be valid against a bilateral supplier\n  agreement.\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Triumph Group, Inc.\nserviceCategory:\
  \ Aerospace / Defense\nbillingModel:\n  pricingCategory: Contract / Negotiated\n  billingFrequency: Per-Contract\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: Triumph Group API\n  ServiceCategory: Aerospace / Defense\n  ProviderName: Triumph Group\n  PublisherName: Triumph Group, Inc.\n  InvoiceIssuerName: Triumph Group, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: contract_fees\n    unit: varies\n    aggregation: sum\n    dimensions:\n      - contract\nprinciples:\n  - name: Visibility\n    description: No public consumption telemetry; visibility depends on whatever reporting clauses\n      live inside the Triumph supplier / customer agreement.\n  - name: Allocation\n    description: Allocate any cost to the consuming aerospace program (engine, landing gear,\n      actuation, etc.) using the contract identifier.\n  - name: Optimization\n    description: Optimization levers (volume, term length, multi-program bundling) are negotiated\n\
  \      rather than self-serve.\n  - name: Accountability\n    description: Aerospace program owner manages the relationship; procurement handles renewals\n      and contract amendments.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/triumph-group/refs/heads/main/finops/triumph-group-finops.yml
sources:
- https://www.triumphgroup.com
specification: FinOps Framework
tags:
- Aerospace
- Defense
- Manufacturing
- FinOps
- FOCUS
---
