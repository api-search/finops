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
description: FinOps shape for Trex Company cannot be reconciled; the company does not operate a public API business and no usage telemetry surface is published.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Trex Company, Inc.
  ProviderName: Trex Company
  PublisherName: Trex Company, Inc.
  ServiceCategory: Building Products
  ServiceName: Trex Company API
layout: finops
meters:
- aggregation: sum
  dimensions:
  - contract
  name: contract_fees
  unit: varies
name: Trex Finops
provider_name: Trex Company
provider_slug: trex
publisher_name: Trex Company, Inc.
service_category: Building Products
slug: trex-finops
source_filename: trex-finops.yml
source_heading: FinOps Profile
source_url: https://www.trex.com
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Trex Company\nproviderId: trex\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Composite Decking\n  - Outdoor\n  - Building Products\n  - FinOps\n  - FOCUS\ndescription: FinOps shape for Trex Company cannot be reconciled; the company does not operate a\n  public API business and no usage telemetry surface is published.\nsources:\n  - https://www.trex.com\nnotes: Trex Company is a manufacturer; it does not publish API pricing, billing, or usage telemetry.\n  Any FOCUS mapping would only be valid against a bilateral partner agreement.\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Trex Company, Inc.\nserviceCategory: Building Products\nbillingModel:\n\
  \  pricingCategory: Contract / Negotiated\n  billingFrequency: Per-Contract\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: Trex Company API\n  ServiceCategory: Building Products\n  ProviderName: Trex Company\n  PublisherName: Trex Company, Inc.\n  InvoiceIssuerName: Trex Company, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: contract_fees\n    unit: varies\n    aggregation: sum\n    dimensions:\n      - contract\nprinciples:\n  - name: Visibility\n    description: No public consumption telemetry; visibility depends on whatever reporting clauses\n      live inside the Trex partner agreement.\n  - name: Allocation\n    description: Allocate any cost to the integrating B2B / dealer program using the contract\n      identifier.\n  - name: Optimization\n    description: Optimization levers (volume, term length) are negotiated rather than self-serve.\n  - name: Accountability\n    description: B2B / dealer program owner manages the relationship;\
  \ procurement handles renewals.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/trex/refs/heads/main/finops/trex-finops.yml
sources:
- https://www.trex.com
specification: FinOps Framework
tags:
- Composite Decking
- Outdoor
- Building Products
- FinOps
- FOCUS
---
