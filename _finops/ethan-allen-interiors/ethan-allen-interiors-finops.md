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
  pricingCategory: Custom Contract
description: 'FinOps view of Ethan Allen Interiors: no public metered API. Any integration cost is invoiced per partner contract rather than via a metered usage bill, so the FinOps surface is contract-tracking rather than per-API meter analysis.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Ethan Allen Global, Inc.
  ProviderName: Ethan Allen Interiors
  PublisherName: Ethan Allen Global, Inc.
  ServiceCategory: Retail / Furniture
  ServiceName: Ethan Allen Interiors
layout: finops
meters:
- aggregation: sum
  dimensions:
  - contract
  name: contract_fees
  unit: month
name: Ethan Allen Interiors Finops
provider_name: Ethan Allen Interiors
provider_slug: ethan-allen-interiors
publisher_name: Ethan Allen Global, Inc.
service_category: Retail / Furniture
slug: ethan-allen-interiors-finops
source_filename: ethan-allen-interiors-finops.yml
source_heading: FinOps Profile
source_url: https://www.ethanallen.com
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Ethan Allen Interiors\nproviderId: ethan-allen-interiors\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Furniture\n  - Retail\ndescription: 'FinOps view of Ethan Allen Interiors: no public metered API. Any integration cost is invoiced\n  per partner contract rather than via a metered usage bill, so the FinOps surface is contract-tracking\n  rather than per-API meter analysis.'\nsources:\n  - https://www.ethanallen.com\nnotes: No metered API billing surface; pricing is contract-based.\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Ethan Allen Global, Inc.\nserviceCategory: Retail / Furniture\nbillingModel:\n  pricingCategory:\
  \ Custom Contract\n  billingFrequency: Per-Contract\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: Ethan Allen Interiors\n  ServiceCategory: Retail / Furniture\n  ProviderName: Ethan Allen Interiors\n  PublisherName: Ethan Allen Global, Inc.\n  InvoiceIssuerName: Ethan Allen Global, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: contract_fees\n    unit: month\n    aggregation: sum\n    dimensions:\n      - contract\nprinciples:\n  - name: Visibility\n    description: Track per-contract integration spend in your AP system; reconcile invoices against agreed\n      milestones.\n  - name: Allocation\n    description: Tag contracts by consuming business unit (digital, retail ops, dealer network).\n  - name: Optimization\n    description: Renegotiate at renewal; consolidate overlapping integrations under a single MSA.\n  - name: Accountability\n    description: Contract owner approves invoices; finance reviews variance from forecast.\nmaintainers:\n\
  \  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/ethan-allen-interiors/refs/heads/main/finops/ethan-allen-interiors-finops.yml
sources:
- https://www.ethanallen.com
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Furniture
- Retail
---
