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
  - Usage
  - Tax
  - Adjustment
  pricingCategory: Enterprise / Bilateral
description: FinOps scaffold for Ameren. The Share My Usage / Green Button program is a regulator-driven data-sharing service rather than a commercial API; access is granted under the Illinois Commerce Commission framework with no documented metered billing. FOCUS mappings remain conceptual.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Ameren Corporation
  ProviderName: Ameren
  PublisherName: Ameren Corporation
  ServiceCategory: Utility / Energy
  ServiceName: Ameren Share My Usage API
layout: finops
meters:
- aggregation: sum
  description: Placeholder meter for engagements settled outside a metered API. Real meters cannot be enumerated until Ameren publishes a metered API billing surface.
  name: contracted_engagement
  unit: varies
name: Ameren Finops
provider_name: Ameren
provider_slug: ameren
publisher_name: Ameren Corporation
service_category: Utility / Energy
slug: ameren-finops
source_filename: ameren-finops.yml
source_heading: FinOps Profile
source_url: https://www.ameren.com/partners/account-and-data/share-my-usage
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Ameren\nproviderId: ameren\npublisherName: Ameren Corporation\nserviceCategory: Utility / Energy\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Utility\n  - Energy\n  - Electric\n  - Natural Gas\n  - Smart Grid\n  - Green Button\n  - Renewable Energy\n  - FinOps\n  - FOCUS\ndescription: >-\n  FinOps scaffold for Ameren. The Share My Usage / Green Button program is a regulator-driven data-sharing service rather than a commercial API; access is granted under the Illinois Commerce Commission framework with no documented metered billing. FOCUS mappings remain conceptual.\nnotes: >-\n  Ameren Illinois operates the Share My Usage / Green Button Connect My Data program (operated by data custodian Aclara) under the ESPI standard. Access for authorized third parties is governed by a registration and testing process rather than a metered, priced\
  \ API. Rate limits are not publicly published; the program documents a 2-4 week onboarding and 24-month rolling data window. Reconcile if Ameren or Aclara publishes specific rate-limit or pricing values.\nsources:\n  - https://www.ameren.com/partners/account-and-data/share-my-usage\n  - https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nbillingModel:\n  pricingCategory: Enterprise / Bilateral\n  billingFrequency: Per-Contract\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\n    - Tax\n    - Adjustment\nfocusColumns:\n  ServiceName: Ameren Share My Usage API\n  ServiceCategory: Utility / Energy\n  ProviderName: Ameren\n  PublisherName: Ameren Corporation\n  InvoiceIssuerName: Ameren Corporation\n  BillingCurrency: USD\n  ChargeCategory: Purchase\n\
  meters:\n  - name: contracted_engagement\n    description: >-\n      Placeholder meter for engagements settled outside a metered API. Real\n      meters cannot be enumerated until Ameren publishes a metered\n      API billing surface.\n    unit: varies\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: >-\n      Without a public usage API, consumers must rely on contract reporting,\n      invoice line items, and any tenant dashboards provided under the\n      partner agreement.\n  - name: Allocation\n    description: >-\n      Allocate spend by purchase order, contract identifier, or business unit\n      receiving the Ameren service. Tag at the procurement layer, not\n      the API call layer.\n  - name: Optimization\n    description: >-\n      Optimization levers live in commercial negotiation (volume commitments,\n      term length, scope) rather than in API-level caching or throttling.\n  - name: Accountability\n    description: >-\n      Procurement and the\
  \ business owner of the Ameren relationship own\n      the spend; finance reviews invoice lines on the contract cadence.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/ameren/refs/heads/main/finops/ameren-finops.yml
sources:
- https://www.ameren.com/partners/account-and-data/share-my-usage
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Utility
- Energy
- Electric
- Natural Gas
- Smart Grid
- Green Button
- Renewable Energy
- FinOps
- FOCUS
---
