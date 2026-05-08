---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: Per-Policy
  chargeCategories:
  - Purchase
  - Tax
  - Adjustment
  pricingCategory: Insurance Commission Economics (Not API-Billed)
description: FOCUS-aligned FinOps stub for FGL Holdings / F&G Annuities & Life. No public developer API exists; carrier integrations are agent/IMO channel via DTCC, IRI, and proprietary distribution portals. API-FinOps is therefore N/A; commercial flows are commission/policy economics, not API consumption.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: F&G Annuities & Life
  PricingCategory: Insurance Commission
  PricingUnit: not applicable
  ProviderName: F&G Annuities & Life
  PublisherName: F&G Annuities & Life
  ServiceCategory: Insurance / Annuities
  ServiceName: F&G Annuities & Life
layout: finops
meters: []
name: Fgl Holdings Finops
provider_name: FGL Holdings
provider_slug: fgl-holdings
publisher_name: F&G Annuities & Life (subsidiary of Fidelity National Financial)
service_category: Insurance / Annuities
slug: fgl-holdings-finops
source_filename: fgl-holdings-finops.yml
source_heading: FinOps Profile
source_url: https://www.fglife.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: FGL Holdings\nproviderId: fgl-holdings\npublisherName: F&G Annuities & Life (subsidiary of Fidelity National Financial)\nserviceCategory: Insurance / Annuities\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Insurance\n  - Annuities\n  - Financial Services\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FOCUS-aligned FinOps stub for FGL Holdings / F&G Annuities & Life. No public developer API\n  exists; carrier integrations are agent/IMO channel via DTCC, IRI, and proprietary distribution portals.\n  API-FinOps is therefore N/A; commercial flows are commission/policy economics, not API consumption.\nnotes: No public API; FinOps lives in the policy administration\
  \ / commission system. Retained as a stub.\nsources:\n  - https://www.fglife.com/\nprinciples:\n  - name: Visibility\n    description: Not applicable to API consumption; visibility lives in the policy administration / commission\n      system used by the IMO.\n  - name: Allocation\n    description: Allocation is at the policy / agent / IMO level in the carrier's policy admin system,\n      not via API meters.\n  - name: Optimization\n    description: Optimization is product / commission design, not API engineering.\n  - name: Accountability\n    description: Distribution / IMO relationship management owns the partner relationship; no API budget\n      owner exists.\nbillingModel:\n  pricingCategory: Insurance Commission Economics (Not API-Billed)\n  billingFrequency: Per-Policy\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Tax\n    - Adjustment\nfocusColumns:\n  ServiceName: F&G Annuities & Life\n  ServiceCategory: Insurance / Annuities\n  ProviderName: F&G Annuities\
  \ & Life\n  PublisherName: F&G Annuities & Life\n  InvoiceIssuerName: F&G Annuities & Life\n  PricingCategory: Insurance Commission\n  PricingUnit: not applicable\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters: []\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/fgl-holdings/refs/heads/main/finops/fgl-holdings-finops.yml
sources:
- https://www.fglife.com/
specification: FinOps Framework
tags:
- Insurance
- Annuities
- Financial Services
- FinOps
- Cost Management
- FOCUS
---
