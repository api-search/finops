---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: Per-Mandate
  chargeCategories:
  - Purchase
  pricingCategory: Advisory Fees / AUM-Based
description: 'FinOps view of Evercore Inc: no metered SaaS billing surface. Fees are advisory and engagement-based (retainers, success fees, AUM percentages) invoiced per mandate.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Evercore Inc.
  ProviderName: Evercore Inc
  PublisherName: Evercore Inc.
  ServiceCategory: Investment Banking / Advisory
  ServiceName: Evercore Inc
layout: finops
meters:
- aggregation: sum
  dimensions:
  - mandate
  name: advisory_fees
  unit: USD
- aggregation: max
  dimensions:
  - account
  name: aum_basis_points
  unit: basis_point
name: Evercore Finops
provider_name: Evercore Inc
provider_slug: evercore
publisher_name: Evercore Inc.
service_category: Investment Banking / Advisory
slug: evercore-finops
source_filename: evercore-finops.yml
source_heading: FinOps Profile
source_url: https://www.evercore.com
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Evercore Inc\nproviderId: evercore\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Investment Banking\n  - Advisory\ndescription: 'FinOps view of Evercore Inc: no metered SaaS billing surface. Fees are advisory and engagement-based\n  (retainers, success fees, AUM percentages) invoiced per mandate.'\nsources:\n  - https://www.evercore.com\nnotes: Not a metered API surface; FinOps is contract-tracking against advisory engagement letters.\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Evercore Inc.\nserviceCategory: Investment Banking / Advisory\nbillingModel:\n  pricingCategory: Advisory Fees / AUM-Based\n  billingFrequency:\
  \ Per-Mandate\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: Evercore Inc\n  ServiceCategory: Investment Banking / Advisory\n  ProviderName: Evercore Inc\n  PublisherName: Evercore Inc.\n  InvoiceIssuerName: Evercore Inc.\n  BillingCurrency: USD\nmeters:\n  - name: advisory_fees\n    unit: USD\n    aggregation: sum\n    dimensions:\n      - mandate\n  - name: aum_basis_points\n    unit: basis_point\n    aggregation: max\n    dimensions:\n      - account\nprinciples:\n  - name: Visibility\n    description: Track Evercore advisory and AUM fees in your AP/treasury system; reconcile invoices\n      against the engagement letter.\n  - name: Allocation\n    description: Tag fees to the deal, fund, or account they relate to.\n  - name: Optimization\n    description: Negotiate fee caps and success-fee thresholds at engagement-letter signing.\n  - name: Accountability\n    description: Deal sponsor or fund treasurer owns the relationship and approves\
  \ fee invoices.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/evercore/refs/heads/main/finops/evercore-finops.yml
sources:
- https://www.evercore.com
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Investment Banking
- Advisory
---
