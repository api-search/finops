---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: Not Applicable
  chargeCategories:
  - Purchase
  pricingCategory: Not Applicable
description: 'FOCUS-aligned FinOps for ConocoPhillips: not an API/SaaS provider but an upstream oil and gas company. Treat ConocoPhillips as a non-software counterparty whose digital surface is vendor-portal driven; FinOps applies to the third-party SaaS that hosts those portals, not to ConocoPhillips itself.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: ConocoPhillips Company
  ProviderName: ConocoPhillips
  PublisherName: ConocoPhillips Company
  ServiceCategory: Energy / Oil and Gas
  ServiceName: ConocoPhillips
layout: finops
meters:
- aggregation: sum
  description: Procurement / commercial invoices from ConocoPhillips as counterparty (not API consumption)
  dimensions:
  - business_unit
  - contract
  name: counterparty_invoice
  unit: invoice
name: Conocophillips Finops
provider_name: ConocoPhillips
provider_slug: conocophillips
publisher_name: ConocoPhillips Company
service_category: Energy / Oil and Gas
slug: conocophillips-finops
source_filename: conocophillips-finops.yml
source_heading: FinOps Profile
source_url: https://www.conocophillips.com
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: ConocoPhillips\nproviderId: conocophillips\npublisherName: ConocoPhillips Company\nserviceCategory: Energy / Oil and Gas\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Energy\n  - Oil and Gas\n  - LNG\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps for ConocoPhillips: not an API/SaaS provider but an upstream oil and\n  gas company. Treat ConocoPhillips as a non-software counterparty whose digital surface is vendor-portal\n  driven; FinOps applies to the third-party SaaS that hosts those portals, not to ConocoPhillips itself.'\nnotes: ConocoPhillips is not a software/API vendor; this artifact is included for\
  \ catalog completeness\n  but is not reconciled to a billing surface.\nsources:\n  - https://www.conocophillips.com\nbillingModel:\n  pricingCategory: Not Applicable\n  billingFrequency: Not Applicable\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: ConocoPhillips\n  ServiceCategory: Energy / Oil and Gas\n  ProviderName: ConocoPhillips\n  PublisherName: ConocoPhillips Company\n  InvoiceIssuerName: ConocoPhillips Company\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: counterparty_invoice\n    description: Procurement / commercial invoices from ConocoPhillips as counterparty (not API consumption)\n    unit: invoice\n    aggregation: sum\n    dimensions:\n      - business_unit\n      - contract\nprinciples:\n  - name: Visibility\n    description: Counterparty invoices flow through the procurement / treasury system rather than a developer\n      console; visibility is provided by the customer's own AP/AR systems.\n  - name:\
  \ Allocation\n    description: Allocate vendor-portal access cost via the underlying SaaS provider (Ariba / GEP / Taulia)\n      rather than through ConocoPhillips directly.\n  - name: Optimization\n    description: No software-side optimization is applicable; commercial optimization happens through\n      the master vendor / supply agreements.\n  - name: Accountability\n    description: Procurement and treasury own ConocoPhillips counterparty spend; no API budget owner exists.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/conocophillips/refs/heads/main/finops/conocophillips-finops.yml
sources:
- https://www.conocophillips.com
specification: FinOps Framework
tags:
- Energy
- Oil and Gas
- LNG
- FinOps
- FOCUS
---
