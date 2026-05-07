---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: Per-Invoice
  chargeCategories:
  - Purchase
  pricingCategory: Subscription
description: FOCUS-aligned FinOps scaffold for TTEC Holdings. TTEC engagements are sales-led professional services / managed services contracts; there is no public usage-based price list to map to FOCUS columns until a specific engagement is in place.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: TTEC Holdings, Inc.
  ProviderName: TTEC Holdings
  PublisherName: TTEC Holdings, Inc.
  ServiceCategory: Customer Experience Services
  ServiceName: TTEC Holdings
layout: finops
meters:
- aggregation: sum
  dimensions:
  - engagement_id
  name: engagement_charges
  unit: varies
name: Teletech Finops
provider_name: TTEC Holdings
provider_slug: teletech
publisher_name: TTEC Holdings, Inc.
service_category: Customer Experience Services
slug: teletech-finops
source_filename: teletech-finops.yml
source_heading: FinOps Profile
source_url: https://www.ttec.com/digital
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: TTEC Holdings\nproviderId: teletech\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Customer Experience\n  - BPO\ndescription: >-\n  FOCUS-aligned FinOps scaffold for TTEC Holdings. TTEC engagements are sales-led professional services\n  / managed services contracts; there is no public usage-based price list to map to FOCUS columns until\n  a specific engagement is in place.\nsources:\n  - https://www.ttec.com/digital\n  - https://www.ttec.com/contact-us\n  - https://focus.finops.org/focus-specification/v1-3/\nnotes: >-\n  No public API or usage telemetry exists. Reconciliation is engagement-specific and pending direct sales\n  contact.\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\n\
  publisherName: TTEC Holdings, Inc.\nserviceCategory: Customer Experience Services\nbillingModel:\n  pricingCategory: Subscription\n  billingFrequency: Per-Invoice\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: TTEC Holdings\n  ServiceCategory: Customer Experience Services\n  ProviderName: TTEC Holdings\n  PublisherName: TTEC Holdings, Inc.\n  InvoiceIssuerName: TTEC Holdings, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: engagement_charges\n    unit: varies\n    aggregation: sum\n    dimensions:\n      - engagement_id\nprinciples:\n  - name: Visibility\n    description: Engagement invoices and TTEC client portal reports are the primary visibility surface;\n      no programmatic usage API is published.\n  - name: Allocation\n    description: Allocate spend per TTEC engagement / business unit based on invoice line items defined\n      in the master service agreement.\n  - name: Optimization\n    description: Renegotiate scope, seat counts,\
  \ and AHT-driven pricing levers at contract review windows\n      with the TTEC account team.\n  - name: Accountability\n    description: Engagement owner inside the customer organization owns TTEC spend and reviews invoices\n      and KPIs against the SOW.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/teletech/refs/heads/main/finops/teletech-finops.yml
sources:
- https://www.ttec.com/digital
- https://www.ttec.com/contact-us
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Customer Experience
- BPO
---
