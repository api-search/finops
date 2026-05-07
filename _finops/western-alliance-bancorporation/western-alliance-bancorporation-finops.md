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
description: FinOps shape for Western Alliance Bancorporation is contract-driven; the bank does not publish a public API pricing surface, so meters and FOCUS columns are minimum placeholders pending a customer agreement.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Western Alliance Bancorporation
  ProviderName: Western Alliance Bancorporation
  PublisherName: Western Alliance Bancorporation
  ServiceCategory: Banking
  ServiceName: Western Alliance Bancorporation
layout: finops
meters:
- aggregation: sum
  dimensions:
  - service
  name: contracted_service
  unit: varies
name: Western Alliance Bancorporation Finops
provider_name: Western Alliance Bancorporation
provider_slug: western-alliance-bancorporation
publisher_name: Western Alliance Bancorporation
service_category: Banking
slug: western-alliance-bancorporation-finops
source_filename: western-alliance-bancorporation-finops.yml
source_heading: FinOps Profile
source_url: https://www.westernalliancebancorp.com
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Western Alliance Bancorporation\nproviderId: western-alliance-bancorporation\npublisherName: Western Alliance Bancorporation\nserviceCategory: Banking\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Banking\n  - Financial Services\n  - FinOps\n  - FOCUS\n  - Contact Sales\ndescription: FinOps shape for Western Alliance Bancorporation is contract-driven; the bank does not publish a public API pricing surface, so meters and FOCUS columns are minimum placeholders pending a customer agreement.\nsources:\n  - https://www.westernalliancebancorp.com\nnotes: No public pricing/billing pages are available. Treat this artifact\
  \ as a placeholder; populate meters and chargeCategories from an actual banking/treasury contract once one exists.\nbillingModel:\n  pricingCategory: Contract-Negotiated\n  billingFrequency: Per-Invoice\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\nfocusColumns:\n  ServiceName: Western Alliance Bancorporation\n  ServiceCategory: Banking\n  ProviderName: Western Alliance Bancorporation\n  PublisherName: Western Alliance Bancorporation\n  InvoiceIssuerName: Western Alliance Bancorporation\n  BillingCurrency: USD\nmeters:\n  - name: contracted_service\n    unit: varies\n    aggregation: sum\n    dimensions:\n      - service\nprinciples:\n  - name: Visibility\n    description: Consumption signal comes from the bank's customer-facing treasury / commercial portals and contracted reporting; no public usage API exists.\n  - name: Allocation\n    description: Spend is allocated through the underlying contract (account, treasury product, partner agreement) rather than\
  \ via API tags.\n  - name: Optimization\n    description: Optimization levers are commercial - renegotiating terms, consolidating accounts, or selecting different banking products.\n  - name: Accountability\n    description: Treasury / finance is the natural owner; engineering owns only integration cost, since the bank publishes no per-call price.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/western-alliance-bancorporation/refs/heads/main/finops/western-alliance-bancorporation-finops.yml
sources:
- https://www.westernalliancebancorp.com
specification: FinOps Framework
tags:
- Banking
- Financial Services
- FinOps
- FOCUS
- Contact Sales
---
