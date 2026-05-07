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
  - Usage
  - Purchase
  pricingCategory: Contract-Negotiated
description: FinOps shape for Wintrust Financial is contract-driven; the holding company does not publish a public API pricing surface, so meters and FOCUS columns are minimum placeholders pending a banking agreement.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Wintrust Financial Corporation
  ProviderName: Wintrust Financial
  PublisherName: Wintrust Financial Corporation
  ServiceCategory: Banking
  ServiceName: Wintrust Financial
layout: finops
meters:
- aggregation: sum
  dimensions:
  - service
  name: contracted_service
  unit: varies
name: Wintrust Financial Finops
provider_name: Wintrust Financial
provider_slug: wintrust-financial
publisher_name: Wintrust Financial Corporation
service_category: Banking
slug: wintrust-financial-finops
source_filename: wintrust-financial-finops.yml
source_heading: FinOps Profile
source_url: https://www.wintrust.com
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Wintrust Financial\nproviderId: wintrust-financial\npublisherName: Wintrust Financial Corporation\nserviceCategory: Banking\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Banking\n  - Financial Services\n  - Community\n  - FinOps\n  - FOCUS\n  - Contact Sales\ndescription: FinOps shape for Wintrust Financial is contract-driven; the holding company does not publish a public API pricing surface, so meters and FOCUS columns are minimum placeholders pending a banking agreement.\nsources:\n  - https://www.wintrust.com\nnotes: No public pricing/billing pages exist. Populate meters and chargeCategories from an actual treasury\
  \ / commercial-banking contract once one exists.\nbillingModel:\n  pricingCategory: Contract-Negotiated\n  billingFrequency: Per-Invoice\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\nfocusColumns:\n  ServiceName: Wintrust Financial\n  ServiceCategory: Banking\n  ProviderName: Wintrust Financial\n  PublisherName: Wintrust Financial Corporation\n  InvoiceIssuerName: Wintrust Financial Corporation\n  BillingCurrency: USD\nmeters:\n  - name: contracted_service\n    unit: varies\n    aggregation: sum\n    dimensions:\n      - service\nprinciples:\n  - name: Visibility\n    description: Consumption signal comes from Wintrust's commercial / treasury portals and contracted reporting; no public usage API exists.\n  - name: Allocation\n    description: Spend is allocated through the underlying contract (account, treasury product) rather than via API tags.\n  - name: Optimization\n    description: Optimization is commercial - account consolidation, product selection,\
  \ contract renegotiation.\n  - name: Accountability\n    description: Treasury / finance is the natural owner; engineering owns only integration cost since no per-call price is published.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/wintrust-financial/refs/heads/main/finops/wintrust-financial-finops.yml
sources:
- https://www.wintrust.com
specification: FinOps Framework
tags:
- Banking
- Financial Services
- Community
- FinOps
- FOCUS
- Contact Sales
---
