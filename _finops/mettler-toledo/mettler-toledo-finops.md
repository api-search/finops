---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD/EUR/CHF
  billingFrequency: Per-Invoice
  chargeCategories:
  - Purchase
  - Usage
  - Tax
  - Adjustment
  pricingCategory: Subscription
description: 'FOCUS-aligned FinOps for Mettler-Toledo: contract-priced industrial/lab instrumentation software with bundled API access. No public pricing surface; cost is captured at the contract line level rather than per-API-call.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Mettler-Toledo International Inc.
  ProviderName: Mettler-Toledo International
  PublisherName: Mettler-Toledo International Inc.
  ServiceCategory: Industrial / Laboratory Instruments
  ServiceName: Mettler-Toledo International
layout: finops
meters:
- aggregation: sum
  dimensions:
  - product
  - site
  name: software_subscription
  unit: month
- aggregation: sum
  dimensions:
  - product
  name: instrument_connector_seats
  unit: seat
- aggregation: sum
  dimensions:
  - product
  - integration
  name: api_calls
  unit: request
name: Mettler Toledo Finops
provider_name: Mettler-Toledo International
provider_slug: mettler-toledo
publisher_name: Mettler-Toledo International Inc.
service_category: Industrial / Laboratory Instruments
slug: mettler-toledo-finops
source_filename: mettler-toledo-finops.yml
source_heading: FinOps Profile
source_url: https://www.mt.com/us/en/home.html
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Mettler-Toledo International\nproviderId: mettler-toledo\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Laboratory\n  - Instruments\n  - Precision\ndescription: 'FOCUS-aligned FinOps for Mettler-Toledo: contract-priced industrial/lab instrumentation\n  software with bundled API access. No public pricing surface; cost is captured at the contract line\n  level rather than per-API-call.'\nsources:\n  - https://www.mt.com/us/en/home.html\nnotes: No public API pricing surface; FOCUS columns reflect contract-level invoicing rather than usage\n  metering.\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Mettler-Toledo International\
  \ Inc.\nserviceCategory: Industrial / Laboratory Instruments\nbillingModel:\n  pricingCategory: Subscription\n  billingFrequency: Per-Invoice\n  billingCurrency: USD/EUR/CHF\n  chargeCategories:\n    - Purchase\n    - Usage\n    - Tax\n    - Adjustment\nfocusColumns:\n  ServiceName: Mettler-Toledo International\n  ServiceCategory: Industrial / Laboratory Instruments\n  ProviderName: Mettler-Toledo International\n  PublisherName: Mettler-Toledo International Inc.\n  InvoiceIssuerName: Mettler-Toledo International Inc.\n  BillingCurrency: USD\nmeters:\n  - name: software_subscription\n    unit: month\n    aggregation: sum\n    dimensions:\n      - product\n      - site\n  - name: instrument_connector_seats\n    unit: seat\n    aggregation: sum\n    dimensions:\n      - product\n  - name: api_calls\n    unit: request\n    aggregation: sum\n    dimensions:\n      - product\n      - integration\nprinciples:\n  - name: Visibility\n    description: Reconcile Mettler-Toledo invoice line items\
  \ against site-level usage of LabX, RetailSuite,\n      and instrument connectors; APIs are not metered separately on the invoice.\n  - name: Allocation\n    description: Allocate spend by site, lab, and instrument family using purchase order metadata\n      and contract IDs.\n  - name: Optimization\n    description: Right-size instrument connector seat counts and consolidate site licenses; renegotiate\n      multi-year contracts where instrument footprint is stable.\n  - name: Accountability\n    description: Assign cost ownership to lab/site managers tied to the originating purchase order;\n      review annually at contract renewal.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/mettler-toledo/refs/heads/main/finops/mettler-toledo-finops.yml
sources:
- https://www.mt.com/us/en/home.html
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Laboratory
- Instruments
- Precision
---
