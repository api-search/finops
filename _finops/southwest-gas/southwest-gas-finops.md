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
  pricingCategory: Contact Sales
description: FOCUS-aligned FinOps placeholder for Southwest Gas. The utility does not expose a per-call API billing surface; any partner data integration cost is contractual.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Southwest Gas Holdings, Inc.
  ProviderName: Southwest Gas
  PublisherName: Southwest Gas Holdings, Inc.
  ServiceCategory: Utility
  ServiceName: Southwest Gas
layout: finops
meters:
- aggregation: sum
  description: Placeholder meter; actual billable units are defined per integration / EDI / data-sharing agreement.
  name: contracted_integration
  unit: varies
name: Southwest Gas Finops
provider_name: Southwest Gas
provider_slug: southwest-gas
publisher_name: Southwest Gas Holdings, Inc.
service_category: Utility (Natural Gas)
slug: southwest-gas-finops
source_filename: southwest-gas-finops.yml
source_heading: FinOps Profile
source_url: https://www.swgas.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Southwest Gas\nproviderId: southwest-gas\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Fortune 1000\n  - Natural Gas\n  - Utility\n  - Energy\n  - FinOps\n  - FOCUS\ndescription: FOCUS-aligned FinOps placeholder for Southwest Gas. The utility does\n  not expose a per-call API billing surface; any partner data integration cost\n  is contractual.\nsources:\n  - https://www.swgas.com/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Southwest Gas Holdings, Inc.\nserviceCategory: Utility (Natural Gas)\nbillingModel:\n  pricingCategory: Contact Sales\n  billingFrequency: Per-Contract\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n\
  \  ServiceName: Southwest Gas\n  ServiceCategory: Utility\n  ProviderName: Southwest Gas\n  PublisherName: Southwest Gas Holdings, Inc.\n  InvoiceIssuerName: Southwest Gas Holdings, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: contracted_integration\n    description: Placeholder meter; actual billable units are defined per\n      integration / EDI / data-sharing agreement.\n    unit: varies\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: No public usage API. Visibility is provided through the deliverables\n      agreed with the utility (statements, EDI exchanges, regulatory filings).\n  - name: Allocation\n    description: Costs related to Southwest Gas integrations are allocated against\n      the contracting business unit (energy procurement, builder programs).\n  - name: Optimization\n    description: Optimization is contractual / regulatory rather than technical;\n      tariffs, transportation contracts, and Green Button consent govern cost.\n  - name:\
  \ Accountability\n    description: Owned by the contracting energy or facilities manager. The utility\n      does not provide self-serve cost-management tooling.\nnotes: No public per-call billing or FinOps surface; entry exists for catalog\n  completeness only.\nmaintainers:\n  - FN: API Evangelist\n    email: info@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/southwest-gas/refs/heads/main/finops/southwest-gas-finops.yml
sources:
- https://www.swgas.com/
specification: FinOps Framework
tags:
- Fortune 1000
- Natural Gas
- Utility
- Energy
- FinOps
- FOCUS
---
