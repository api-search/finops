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
description: FinOps scaffold for Amedisys. The company does not publish a public API billing surface. Healthcare data exchange is governed by HIPAA business-associate agreements rather than metered API billing. FOCUS mappings remain conceptual until a metered API offering is published.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Amedisys, Inc.
  ProviderName: Amedisys
  PublisherName: Amedisys, Inc.
  ServiceCategory: Healthcare
  ServiceName: Amedisys API
layout: finops
meters:
- aggregation: sum
  description: Placeholder meter for engagements settled outside a metered API. Real meters cannot be enumerated until Amedisys publishes a metered API billing surface.
  name: contracted_engagement
  unit: varies
name: Amedisys Finops
provider_name: Amedisys
provider_slug: amedisys
publisher_name: Amedisys, Inc.
service_category: Healthcare
slug: amedisys-finops
source_filename: amedisys-finops.yml
source_heading: FinOps Profile
source_url: https://www.amedisys.com
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Amedisys\nproviderId: amedisys\npublisherName: Amedisys, Inc.\nserviceCategory: Healthcare\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Home Health\n  - Hospice\n  - Healthcare\n  - FinOps\n  - FOCUS\ndescription: >-\n  FinOps scaffold for Amedisys. The company does not publish a public API billing surface. Healthcare data exchange is governed by HIPAA business-associate agreements rather than metered API billing. FOCUS mappings remain conceptual until a metered API offering is published.\nnotes: >-\n  Amedisys is a home health and hospice provider; it does not publish a public API developer portal or commercial API offering. Any data exchanges with payers, EHR systems, or referral partners are governed by HIPAA-compliant integration agreements rather than a public price list. Reconcile if Amedisys publishes a public API.\nsources:\n\
  \  - https://www.amedisys.com\n  - https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nbillingModel:\n  pricingCategory: Enterprise / Bilateral\n  billingFrequency: Per-Contract\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\n    - Tax\n    - Adjustment\nfocusColumns:\n  ServiceName: Amedisys API\n  ServiceCategory: Healthcare\n  ProviderName: Amedisys\n  PublisherName: Amedisys, Inc.\n  InvoiceIssuerName: Amedisys, Inc.\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: contracted_engagement\n    description: >-\n      Placeholder meter for engagements settled outside a metered API. Real\n      meters cannot be enumerated until Amedisys publishes a metered\n      API billing surface.\n    unit: varies\n    aggregation: sum\n\
  principles:\n  - name: Visibility\n    description: >-\n      Without a public usage API, consumers must rely on contract reporting,\n      invoice line items, and any tenant dashboards provided under the\n      partner agreement.\n  - name: Allocation\n    description: >-\n      Allocate spend by purchase order, contract identifier, or business unit\n      receiving the Amedisys service. Tag at the procurement layer, not\n      the API call layer.\n  - name: Optimization\n    description: >-\n      Optimization levers live in commercial negotiation (volume commitments,\n      term length, scope) rather than in API-level caching or throttling.\n  - name: Accountability\n    description: >-\n      Procurement and the business owner of the Amedisys relationship own\n      the spend; finance reviews invoice lines on the contract cadence.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/amedisys/refs/heads/main/finops/amedisys-finops.yml
sources:
- https://www.amedisys.com
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Home Health
- Hospice
- Healthcare
- FinOps
- FOCUS
---
