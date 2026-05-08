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
  pricingCategory: Enterprise Contract
description: FOCUS-aligned FinOps for Quest Diagnostics enterprise integrations is contract-based; Quanum Data Exchange and other interoperability surfaces are billed per the customer agreement rather than on a public per-API tariff.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Quest Diagnostics Incorporated
  ProviderName: Quest Diagnostics
  PublisherName: Quest Diagnostics Incorporated
  ServiceCategory: Healthcare
  ServiceName: Quest Diagnostics
layout: finops
meters:
- aggregation: sum
  description: Enterprise integration contract covering Quanum Data Exchange and related interfaces.
  dimensions:
  - contract
  name: integration_contract
  unit: varies
name: Quest Diagnostics Finops
provider_name: Quest Diagnostics
provider_slug: quest-diagnostics
publisher_name: Quest Diagnostics Incorporated
service_category: Healthcare
slug: quest-diagnostics-finops
source_filename: quest-diagnostics-finops.yml
source_heading: FinOps Profile
source_url: https://www.questdiagnostics.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Quest Diagnostics\nproviderId: quest-diagnostics\npublisherName: Quest Diagnostics Incorporated\nserviceCategory: Healthcare\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Healthcare\n  - Diagnostics\n  - FinOps\n  - FOCUS\nnotes: Quest does not publish a per-API meter or invoice surface; FinOps mapping is anchored to the\n  enterprise integration contract.\ndescription: FOCUS-aligned FinOps for Quest Diagnostics enterprise integrations is contract-based;\n  Quanum Data Exchange and other interoperability surfaces are billed per the customer agreement rather\n  than on a public per-API tariff.\nsources:\n  - https://www.questdiagnostics.com/\n\
  billingModel:\n  pricingCategory: Enterprise Contract\n  billingFrequency: Per-Invoice\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: Quest Diagnostics\n  ServiceCategory: Healthcare\n  ProviderName: Quest Diagnostics\n  PublisherName: Quest Diagnostics Incorporated\n  InvoiceIssuerName: Quest Diagnostics Incorporated\n  BillingCurrency: USD\nmeters:\n  - name: integration_contract\n    description: Enterprise integration contract covering Quanum Data Exchange and related interfaces.\n    unit: varies\n    aggregation: sum\n    dimensions:\n      - contract\nprinciples:\n  - name: Visibility\n    description: Surface Quest integration spend through procurement records and the customer-side\n      EHR vendor's billing data; Quest does not expose a self-serve usage API.\n  - name: Allocation\n    description: Allocate the contract spend against the consuming clinical or operations cost center\n      named in the agreement.\n  - name: Optimization\n\
  \    description: Optimization happens at contract renewal; consolidate Quanum interfaces and prune unused\n      lab order/result feeds.\n  - name: Accountability\n    description: Healthcare IT and clinical informatics co-own the Quest contract; engineering routes\n      changes through the Quest account team.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/quest-diagnostics/refs/heads/main/finops/quest-diagnostics-finops.yml
sources:
- https://www.questdiagnostics.com/
specification: FinOps Framework
tags:
- Healthcare
- Diagnostics
- FinOps
- FOCUS
---
