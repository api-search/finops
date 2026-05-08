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
  pricingCategory: Not Applicable
description: 'FOCUS-aligned FinOps placeholder for SM Energy: not a software vendor; no public API invoice-line catalog exists.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: SM Energy Company
  ProviderName: SM Energy
  PublisherName: SM Energy Company
  ServiceCategory: Oil and Gas Exploration and Production
  ServiceName: SM Energy
layout: finops
meters:
- aggregation: sum
  description: SM Energy does not bill API consumption.
  dimensions: []
  name: not_applicable
  unit: varies
name: Sm Energy Finops
provider_name: SM Energy
provider_slug: sm-energy
publisher_name: SM Energy Company
service_category: Oil and Gas Exploration and Production
slug: sm-energy-finops
source_filename: sm-energy-finops.yml
source_heading: FinOps Profile
source_url: https://www.sm-energy.com
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: SM Energy\nproviderId: sm-energy\npublisherName: SM Energy Company\nserviceCategory: Oil and Gas Exploration and Production\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Oil and Gas\n  - Energy\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps placeholder for SM Energy: not a software vendor; no public API\n  invoice-line catalog exists.'\nsources:\n  - https://www.sm-energy.com\nnotes: |\n  Not a software / API vendor. Retained as a placeholder for catalog completeness only; no FOCUS\n  invoice-line modeling is meaningful for an upstream E&P company.\nbillingModel:\n  pricingCategory: Not Applicable\n  billingFrequency:\
  \ Per-Invoice\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: SM Energy\n  ServiceCategory: Oil and Gas Exploration and Production\n  ProviderName: SM Energy\n  PublisherName: SM Energy Company\n  InvoiceIssuerName: SM Energy Company\n  BillingCurrency: USD\nmeters:\n  - name: not_applicable\n    description: SM Energy does not bill API consumption.\n    unit: varies\n    aggregation: sum\n    dimensions: []\nprinciples:\n  - name: Visibility\n    description: Not applicable - SM Energy is an upstream E&P operator, not an API vendor.\n  - name: Allocation\n    description: Not applicable.\n  - name: Optimization\n    description: Not applicable.\n  - name: Accountability\n    description: Not applicable.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/sm-energy/refs/heads/main/finops/sm-energy-finops.yml
sources:
- https://www.sm-energy.com
specification: FinOps Framework
tags:
- Oil and Gas
- Energy
- FinOps
- FOCUS
---
