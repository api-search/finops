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
description: FOCUS-aligned FinOps placeholder for Southwestern Energy / Expand Energy. There is no per-call API billing surface; counterparty integrations are invoiced per bilateral commercial contract.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Expand Energy Corporation
  ProviderName: Southwestern Energy
  PublisherName: Expand Energy Corporation
  ServiceCategory: Energy
  ServiceName: Southwestern Energy
layout: finops
meters:
- aggregation: sum
  description: Placeholder meter; actual billable units track physical commodity movement, not per-API-call usage.
  name: counterparty_integration
  unit: varies
name: Southwestern Energy Finops
provider_name: Southwestern Energy
provider_slug: southwestern-energy
publisher_name: Expand Energy Corporation
service_category: Energy (Upstream Natural Gas)
slug: southwestern-energy-finops
source_filename: southwestern-energy-finops.yml
source_heading: FinOps Profile
source_url: https://www.swn.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Southwestern Energy\nproviderId: southwestern-energy\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Fortune 500\n  - Natural Gas\n  - Energy\n  - Oil And Gas\n  - FinOps\n  - FOCUS\ndescription: FOCUS-aligned FinOps placeholder for Southwestern Energy / Expand\n  Energy. There is no per-call API billing surface; counterparty integrations are\n  invoiced per bilateral commercial contract.\nsources:\n  - https://www.swn.com/\n  - https://www.expandenergy.com/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Expand Energy Corporation\nserviceCategory: Energy (Upstream Natural Gas)\nbillingModel:\n  pricingCategory: Contact Sales\n  billingFrequency: Per-Contract\n\
  \  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: Southwestern Energy\n  ServiceCategory: Energy\n  ProviderName: Southwestern Energy\n  PublisherName: Expand Energy Corporation\n  InvoiceIssuerName: Expand Energy Corporation\n  BillingCurrency: USD\nmeters:\n  - name: counterparty_integration\n    description: Placeholder meter; actual billable units track physical commodity\n      movement, not per-API-call usage.\n    unit: varies\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Visibility is provided through nominations, allocation statements,\n      and EDI exchanges defined in the counterparty agreement; there is no public\n      usage API.\n  - name: Allocation\n    description: Costs are allocated against the contracting commercial / trading\n      desk that owns the counterparty relationship.\n  - name: Optimization\n    description: Optimization is commodity-commercial (basis, transportation,\n      hedging)\
  \ rather than per-call API tuning.\n  - name: Accountability\n    description: Owned by the trading or midstream commercial team that contracts\n      directly with the producer.\nnotes: No public per-call billing or FinOps surface; entry exists for catalog\n  completeness only.\nmaintainers:\n  - FN: API Evangelist\n    email: info@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/southwestern-energy/refs/heads/main/finops/southwestern-energy-finops.yml
sources:
- https://www.swn.com/
- https://www.expandenergy.com/
specification: FinOps Framework
tags:
- Fortune 500
- Natural Gas
- Energy
- Oil And Gas
- FinOps
- FOCUS
---
