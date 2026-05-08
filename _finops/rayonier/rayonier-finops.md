---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: Per-Invoice
  chargeCategories:
  - Purchase
  pricingCategory: Contract
description: Rayonier exposes no public developer API or usage-billed surface; this artifact describes the FinOps shape only nominally for inventory completeness.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Rayonier Inc.
  ProviderName: Rayonier
  PublisherName: Rayonier Inc.
  ServiceCategory: Forestry / Real Estate
  ServiceName: Rayonier
layout: finops
meters:
- aggregation: sum
  description: Per-contract invoice line for any negotiated timber, land, or data integration
  name: contract_invoice
  unit: contract
name: Rayonier Finops
provider_name: Rayonier
provider_slug: rayonier
publisher_name: Rayonier Inc.
service_category: Forestry / Real Estate
slug: rayonier-finops
source_filename: rayonier-finops.yml
source_heading: FinOps Profile
source_url: https://www.rayonier.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Rayonier\nproviderId: rayonier\npublisherName: Rayonier Inc.\nserviceCategory: Forestry / Real Estate\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Timber\n  - Real Estate\n  - Forest Products\n  - FinOps\n  - FOCUS\ndescription: Rayonier exposes no public developer API or usage-billed surface; this artifact\n  describes the FinOps shape only nominally for inventory completeness.\nsources:\n  - https://www.rayonier.com/\nnotes: No public API or usage-billing model exists for Rayonier; FOCUS columns and meters here\n  are placeholder-only and should not be treated as a billing schema.\nbillingModel:\n  pricingCategory:\
  \ Contract\n  billingFrequency: Per-Invoice\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: Rayonier\n  ServiceCategory: Forestry / Real Estate\n  ProviderName: Rayonier\n  PublisherName: Rayonier Inc.\n  InvoiceIssuerName: Rayonier Inc.\n  BillingCurrency: USD\nmeters:\n  - name: contract_invoice\n    description: Per-contract invoice line for any negotiated timber, land, or data integration\n    unit: contract\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Spend with Rayonier is captured on the customer's accounts-payable system at\n      contract level; there is no developer-facing usage telemetry.\n  - name: Allocation\n    description: Allocation occurs at the procurement / cost-center level rather than per API\n      call.\n  - name: Optimization\n    description: Optimization happens through commercial negotiation (volume, term length) at\n      contract renewal.\n  - name: Accountability\n    description: Procurement\
  \ and the line-of-business sponsor own the contract relationship.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/rayonier/refs/heads/main/finops/rayonier-finops.yml
sources:
- https://www.rayonier.com/
specification: FinOps Framework
tags:
- Timber
- Real Estate
- Forest Products
- FinOps
- FOCUS
---
