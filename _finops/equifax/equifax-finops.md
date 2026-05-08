---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  - Adjustment
  pricingCategory: Pay-Per-Inquiry / Custom Contract
description: 'FOCUS-aligned FinOps for Equifax: per-pull / per-inquiry billing on contracted unit prices, invoiced monthly. Pricing is custom and not publicly listed; meters reflect typical bureau billing lines.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Equifax Inc.
  ProviderName: Equifax
  PublisherName: Equifax Inc.
  ServiceCategory: Credit Bureau / Identity Data
  ServiceName: Equifax
layout: finops
meters:
- aggregation: sum
  dimensions:
  - product
  - permissible_purpose
  - subscriber_code
  name: credit_inquiries
  unit: inquiry
- aggregation: sum
  dimensions:
  - product
  name: identity_checks
  unit: check
- aggregation: sum
  dimensions:
  - product
  name: verification_pulls
  unit: pull
- aggregation: sum
  dimensions:
  - audience
  name: marketing_records
  unit: record
- aggregation: sum
  dimensions:
  - product
  name: subscription_fees
  unit: month
name: Equifax Finops
provider_name: Equifax
provider_slug: equifax
publisher_name: Equifax Inc.
service_category: Credit Bureau / Identity Data
slug: equifax-finops
source_filename: equifax-finops.yml
source_heading: FinOps Profile
source_url: https://developer.equifax.com/products
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Equifax\nproviderId: equifax\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Credit Bureau\n  - Identity\n  - Verification\ndescription: 'FOCUS-aligned FinOps for Equifax: per-pull / per-inquiry billing on contracted unit prices,\n  invoiced monthly. Pricing is custom and not publicly listed; meters reflect typical bureau billing\n  lines.'\nsources:\n  - https://developer.equifax.com/products\n  - https://www.equifax.com\nnotes: No public pricing; meter unit prices must be reconciled with your Equifax contract.\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Equifax Inc.\nserviceCategory: Credit Bureau / Identity Data\nbillingModel:\n\
  \  pricingCategory: Pay-Per-Inquiry / Custom Contract\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Adjustment\nfocusColumns:\n  ServiceName: Equifax\n  ServiceCategory: Credit Bureau / Identity Data\n  ProviderName: Equifax\n  PublisherName: Equifax Inc.\n  InvoiceIssuerName: Equifax Inc.\n  BillingCurrency: USD\nmeters:\n  - name: credit_inquiries\n    unit: inquiry\n    aggregation: sum\n    dimensions:\n      - product\n      - permissible_purpose\n      - subscriber_code\n  - name: identity_checks\n    unit: check\n    aggregation: sum\n    dimensions:\n      - product\n  - name: verification_pulls\n    unit: pull\n    aggregation: sum\n    dimensions:\n      - product\n  - name: marketing_records\n    unit: record\n    aggregation: sum\n    dimensions:\n      - audience\n  - name: subscription_fees\n    unit: month\n    aggregation: sum\n    dimensions:\n      - product\nprinciples:\n  - name: Visibility\n    description:\
  \ Reconcile monthly Equifax invoices against your subscriber-code-level usage logs; instrument\n      every API call with the permissible-purpose and product code.\n  - name: Allocation\n    description: Tag inquiries with consuming business unit and decision context (origination, account\n      management, marketing) so cost is allocable.\n  - name: Optimization\n    description: Use prescreen / batch services for marketing rather than individual pulls; cache where\n      FCRA permits; renegotiate unit prices at volume tier inflection points.\n  - name: Accountability\n    description: Compliance and finance jointly own bureau spend; risk owners must justify pull volume\n      against business outcomes.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/equifax/refs/heads/main/finops/equifax-finops.yml
sources:
- https://developer.equifax.com/products
- https://www.equifax.com
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Credit Bureau
- Identity
- Verification
---
