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
  - Usage
  pricingCategory: Custom Contract
description: FOCUS-aligned FinOps shell for Dycom Industries; no public API billing surface, so meters and FOCUS columns describe the expected partner-contract billing pattern only.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Dycom Industries, Inc.
  ProviderName: Dycom Industries
  PublisherName: Dycom Industries, Inc.
  ServiceCategory: Specialty Contracting
  ServiceName: Dycom Industries API
layout: finops
meters:
- aggregation: sum
  dimensions:
  - partner
  name: api_requests
  unit: request
- aggregation: sum
  dimensions:
  - engagement
  name: project_hours
  unit: hour
name: Dycom Industries Finops
provider_name: Dycom Industries
provider_slug: dycom-industries
publisher_name: Dycom Industries, Inc.
service_category: Specialty Contracting
slug: dycom-industries-finops
source_filename: dycom-industries-finops.yml
source_heading: FinOps Profile
source_url: https://www.dycomind.com
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Dycom Industries\nproviderId: dycom-industries\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Telecom\n  - Utilities\n  - Construction\ndescription: 'FOCUS-aligned FinOps shell for Dycom Industries; no public API billing surface, so meters\n  and FOCUS columns describe the expected partner-contract billing pattern only.'\nnotes: Dycom Industries does not publish public API pricing or billing. Reconcile FOCUS columns against\n  actual partner invoices.\nsources:\n  - https://www.dycomind.com\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Dycom Industries, Inc.\nserviceCategory: Specialty Contracting\nbillingModel:\n  pricingCategory:\
  \ Custom Contract\n  billingFrequency: Per-Invoice\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\nfocusColumns:\n  ServiceName: Dycom Industries API\n  ServiceCategory: Specialty Contracting\n  ProviderName: Dycom Industries\n  PublisherName: Dycom Industries, Inc.\n  InvoiceIssuerName: Dycom Industries, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: api_requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - partner\n  - name: project_hours\n    unit: hour\n    aggregation: sum\n    dimensions:\n      - engagement\nprinciples:\n  - name: Visibility\n    description: Pull partner-invoice line items into FOCUS-formatted tables; no public billing API.\n  - name: Allocation\n    description: Tag any API consumption by engagement / project / business unit.\n  - name: Optimization\n    description: Renegotiate at contract renewal; consolidate volume across business units.\n  - name: Accountability\n    description: Engagement owner reviews invoice;\
  \ flag deviations.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/dycom-industries/refs/heads/main/finops/dycom-industries-finops.yml
sources:
- https://www.dycomind.com
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Telecom
- Utilities
- Construction
---
