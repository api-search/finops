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
description: FinOps scaffold for AAM. The company invoices suppliers and customers via standard automotive supply-chain settlement (POs, payments, EDI 810/820) rather than a metered API. FOCUS mappings remain conceptual.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: American Axle & Manufacturing Holdings, Inc.
  ProviderName: American Axle and Manufacturing
  PublisherName: American Axle & Manufacturing Holdings, Inc.
  ServiceCategory: Automotive Supply Chain
  ServiceName: AAM iSupplier Portal
layout: finops
meters:
- aggregation: sum
  description: Placeholder meter for engagements settled outside a metered API. Real meters cannot be enumerated until American Axle and Manufacturing publishes a metered API billing surface.
  name: contracted_engagement
  unit: varies
name: American Axle And Manufacturing Finops
provider_name: American Axle and Manufacturing
provider_slug: american-axle-and-manufacturing
publisher_name: American Axle & Manufacturing Holdings, Inc.
service_category: Automotive Supply Chain
slug: american-axle-and-manufacturing-finops
source_filename: american-axle-and-manufacturing-finops.yml
source_heading: FinOps Profile
source_url: https://www.aam.com/suppliers/doing-business-with-aam
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: American Axle and Manufacturing\nproviderId: american-axle-and-manufacturing\npublisherName: American Axle & Manufacturing Holdings, Inc.\nserviceCategory: Automotive Supply Chain\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Automotive\n  - Manufacturing\n  - Driveline\n  - Automotive Supplier\n  - EDI\n  - Supply Chain\n  - FinOps\n  - FOCUS\ndescription: >-\n  FinOps scaffold for AAM. The company invoices suppliers and customers via standard automotive supply-chain settlement (POs, payments, EDI 810/820) rather than a metered API. FOCUS mappings remain conceptual.\nnotes: >-\n  American Axle & Manufacturing (now Dauch Corporation) operates supplier-facing EDI and the iSupplier portal rather than a public, priced API. EDI onboarding is mandatory for suppliers but governed by the standard automotive Tier-1 supply agreement, not\
  \ a public price list. No public rate-limit documentation. Reconcile if AAM publishes a public API.\nsources:\n  - https://www.aam.com/suppliers/doing-business-with-aam\n  - https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nbillingModel:\n  pricingCategory: Enterprise / Bilateral\n  billingFrequency: Per-Contract\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\n    - Tax\n    - Adjustment\nfocusColumns:\n  ServiceName: AAM iSupplier Portal\n  ServiceCategory: Automotive Supply Chain\n  ProviderName: American Axle and Manufacturing\n  PublisherName: American Axle & Manufacturing Holdings, Inc.\n  InvoiceIssuerName: American Axle & Manufacturing Holdings, Inc.\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: contracted_engagement\n\
  \    description: >-\n      Placeholder meter for engagements settled outside a metered API. Real\n      meters cannot be enumerated until American Axle and Manufacturing publishes a metered\n      API billing surface.\n    unit: varies\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: >-\n      Without a public usage API, consumers must rely on contract reporting,\n      invoice line items, and any tenant dashboards provided under the\n      partner agreement.\n  - name: Allocation\n    description: >-\n      Allocate spend by purchase order, contract identifier, or business unit\n      receiving the American Axle and Manufacturing service. Tag at the procurement layer, not\n      the API call layer.\n  - name: Optimization\n    description: >-\n      Optimization levers live in commercial negotiation (volume commitments,\n      term length, scope) rather than in API-level caching or throttling.\n  - name: Accountability\n    description: >-\n      Procurement\
  \ and the business owner of the American Axle and Manufacturing relationship own\n      the spend; finance reviews invoice lines on the contract cadence.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/american-axle-and-manufacturing/refs/heads/main/finops/american-axle-and-manufacturing-finops.yml
sources:
- https://www.aam.com/suppliers/doing-business-with-aam
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Automotive
- Manufacturing
- Driveline
- Automotive Supplier
- EDI
- Supply Chain
- FinOps
- FOCUS
---
