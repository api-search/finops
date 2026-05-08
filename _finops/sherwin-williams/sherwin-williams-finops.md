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
  pricingCategory: Contract / Procurement
description: FOCUS-aligned FinOps placeholder for Sherwin-Williams supplier and EDI integrations. No public API pricing or billing surface exists; cost is reflected through procurement contracts and goods/services pricing rather than per-call usage charges.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: The Sherwin-Williams Company
  ProviderName: Sherwin-Williams
  PublisherName: The Sherwin-Williams Company
  ServiceCategory: B2B Supply Chain
  ServiceName: Sherwin-Williams
layout: finops
meters:
- aggregation: sum
  description: Volume and cost are governed by the supplier or EDI contract rather than per-API meters.
  name: contractual_integration
  unit: varies
name: Sherwin Williams Finops
provider_name: Sherwin-Williams
provider_slug: sherwin-williams
publisher_name: The Sherwin-Williams Company
service_category: B2B Supply Chain
slug: sherwin-williams-finops
source_filename: sherwin-williams-finops.yml
source_heading: FinOps Profile
source_url: https://www.sherwin-williams.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Sherwin-Williams\nproviderId: sherwin-williams\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - B2B\n  - Construction\n  - Fortune 500\n  - Paints\n  - Retail\n  - Supply Chain\n  - FinOps\n  - FOCUS\ndescription: FOCUS-aligned FinOps placeholder for Sherwin-Williams supplier and EDI integrations. No\n  public API pricing or billing surface exists; cost is reflected through procurement contracts and\n  goods/services pricing rather than per-call usage charges.\nsources:\n  - https://www.sherwin-williams.com/\nnotes: Sherwin-Williams does not bill API consumption directly. FinOps treatment is negotiated through\n  supplier contracts; no public billing model, FOCUS exports, or usage telemetry is documented.\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n \
  \ dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: The Sherwin-Williams Company\nserviceCategory: B2B Supply Chain\nbillingModel:\n  pricingCategory: Contract / Procurement\n  billingFrequency: Per-Contract\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: Sherwin-Williams\n  ServiceCategory: B2B Supply Chain\n  ProviderName: Sherwin-Williams\n  PublisherName: The Sherwin-Williams Company\n  InvoiceIssuerName: The Sherwin-Williams Company\n  BillingCurrency: USD\nmeters:\n  - name: contractual_integration\n    description: Volume and cost are governed by the supplier or EDI contract rather than per-API meters.\n    unit: varies\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Spend visibility for Sherwin-Williams integrations comes from procurement and AP systems\n      receiving the underlying goods/services invoices, not from a usage API.\n  - name: Allocation\n\
  \    description: Allocate cost via the originating purchase order, supplier ID, and cost center captured\n      in the procurement system; tag EDI traffic with the contract reference.\n  - name: Optimization\n    description: Optimization is contractual — renegotiate supplier terms, consolidate EDI partners,\n      and reduce duplicate integration touchpoints rather than tuning request volume.\n  - name: Accountability\n    description: Procurement and supply-chain leaders own Sherwin-Williams supplier spend; integration\n      teams own technical SLA conformance.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/sherwin-williams/refs/heads/main/finops/sherwin-williams-finops.yml
sources:
- https://www.sherwin-williams.com/
specification: FinOps Framework
tags:
- B2B
- Construction
- Fortune 500
- Paints
- Retail
- Supply Chain
- FinOps
- FOCUS
---
