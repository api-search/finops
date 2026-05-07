---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: sage-accounting-openapi.yml
  format: yaml
  label: Sage Accounting API
  slug: accounting
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/sage/refs/heads/main/openapi/sage-accounting-openapi.yml
billing_model:
  billingCurrency: USD/GBP/EUR
  billingFrequency: Monthly or Annual
  chargeCategories:
  - Purchase
  pricingCategory: Subscription / Contact Sales
description: 'FOCUS-aligned FinOps placeholder for Sage: API access is bundled with paid Sage product subscriptions whose pricing varies by product, region, and seat. With public pages bot-gated, this artifact reflects a contracted-spend posture rather than usage-based billing.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Sage Software, Inc. (US) / The Sage Group plc (regional entities)
  ProviderName: Sage
  PublisherName: The Sage Group plc
  ServiceCategory: ERP / Accounting Software
  ServiceName: Sage
layout: finops
meters:
- aggregation: max
  dimensions:
  - product
  - region
  name: subscription_seats
  unit: seat
- aggregation: sum
  dimensions:
  - product
  name: product_modules
  unit: varies
name: Sage Finops
provider_name: Sage
provider_slug: sage
publisher_name: The Sage Group plc
service_category: Business Software / ERP / Accounting
slug: sage-finops
source_filename: sage-finops.yml
source_heading: FinOps Profile
source_url: https://developer.sage.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Sage\nproviderId: sage\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Accounting\n  - ERP\n  - B2B\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps placeholder for Sage: API access is bundled with paid Sage product\n  subscriptions whose pricing varies by product, region, and seat. With public pages bot-gated, this artifact\n  reflects a contracted-spend posture rather than usage-based billing.'\nsources:\n  - https://developer.sage.com/\n  - https://www.sage.com/\nnotes: Sage marketing and developer pages returned 403; per-product invoice line items, per-call prices,\n  and FOCUS-friendly meter mappings could not be verified. This file is a Contact-Sales placeholder.\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n \
  \ dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: The Sage Group plc\nserviceCategory: Business Software / ERP / Accounting\nbillingModel:\n  pricingCategory: Subscription / Contact Sales\n  billingFrequency: Monthly or Annual\n  billingCurrency: USD/GBP/EUR\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: Sage\n  ServiceCategory: ERP / Accounting Software\n  ProviderName: Sage\n  PublisherName: The Sage Group plc\n  InvoiceIssuerName: Sage Software, Inc. (US) / The Sage Group plc (regional entities)\n  BillingCurrency: USD\nmeters:\n  - name: subscription_seats\n    unit: seat\n    aggregation: max\n    dimensions:\n      - product\n      - region\n  - name: product_modules\n    unit: varies\n    aggregation: sum\n    dimensions:\n      - product\nprinciples:\n  - name: Visibility\n    description: Pull seat / module usage from each Sage product portal (Accounting, Intacct, People).\n      There is no unified Sage-wide usage API; consolidate\
  \ at the procurement layer.\n  - name: Allocation\n    description: Allocate by Sage product, region, and entity since Sage commonly invoices through regional\n      entities; tag internal cost centers by Sage tenant.\n  - name: Optimization\n    description: Right-size seats at renewal, retire unused modules, and consolidate tenants where Sage\n      product / region permits.\n  - name: Accountability\n    description: Finance owns the Sage subscription portfolio; engineering owns API integration health.\n      Reconcile invoice line items against tenant seat counts each renewal cycle.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/sage/refs/heads/main/finops/sage-finops.yml
sources:
- https://developer.sage.com/
- https://www.sage.com/
specification: FinOps Framework
tags:
- Accounting
- ERP
- B2B
- FinOps
- FOCUS
---
