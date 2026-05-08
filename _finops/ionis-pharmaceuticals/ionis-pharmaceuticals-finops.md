---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  - Usage
  - Tax
  pricingCategory: Subscription
description: 'FOCUS-aligned FinOps placeholder for Ionis Pharmaceuticals: an RNA-focused biotech with no public API or rate card. FinOps applies primarily to internal cloud and validated-system spend rather than a public API surface.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Ionis Pharmaceuticals, Inc.
  ProviderName: Ionis Pharmaceuticals
  PublisherName: Ionis Pharmaceuticals, Inc.
  ServiceCategory: Biotech / Pharmaceuticals
  ServiceName: Ionis Pharmaceuticals
layout: finops
meters:
- aggregation: sum
  dimensions:
  - partner
  - integration_type
  name: integration_subscription
  unit: month
- aggregation: sum
  dimensions:
  - study
  name: clinical_data_volume
  unit: GB
name: Ionis Pharmaceuticals Finops
provider_name: Ionis Pharmaceuticals
provider_slug: ionis-pharmaceuticals
publisher_name: Ionis Pharmaceuticals, Inc.
service_category: Biotech / Pharmaceuticals
slug: ionis-pharmaceuticals-finops
source_filename: ionis-pharmaceuticals-finops.yml
source_heading: FinOps Profile
source_url: https://www.ionispharma.com
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Ionis Pharmaceuticals\nproviderId: ionis-pharmaceuticals\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Pharmaceuticals\n  - Biotech\ndescription: 'FOCUS-aligned FinOps placeholder for Ionis Pharmaceuticals: an RNA-focused biotech with\n  no public API or rate card. FinOps applies primarily to internal cloud and validated-system spend\n  rather than a public API surface.'\nnotes: Ionis does not publish an API rate card. Meters below model the typical partner / clinical-system\n  integration surface; cannot be reconciled without a customer contract.\nsources:\n  - https://www.ionispharma.com\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\n\
  publisherName: Ionis Pharmaceuticals, Inc.\nserviceCategory: Biotech / Pharmaceuticals\nbillingModel:\n  pricingCategory: Subscription\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\n    - Tax\nfocusColumns:\n  ServiceName: Ionis Pharmaceuticals\n  ServiceCategory: Biotech / Pharmaceuticals\n  ProviderName: Ionis Pharmaceuticals\n  PublisherName: Ionis Pharmaceuticals, Inc.\n  InvoiceIssuerName: Ionis Pharmaceuticals, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: integration_subscription\n    unit: month\n    aggregation: sum\n    dimensions:\n      - partner\n      - integration_type\n  - name: clinical_data_volume\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - study\nprinciples:\n  - name: Visibility\n    description: Track partner integration invoices and validated-system cloud spend against study\n      and program codes; no public Ionis usage API.\n  - name: Allocation\n    description: Allocate integration cost\
  \ to the clinical program / study driving the data exchange.\n  - name: Optimization\n    description: Consolidate partner platforms and reuse validated environments across studies where\n      compliance allows.\n  - name: Accountability\n    description: Clinical operations + IT jointly own integration spend; quarterly review against study\n      budgets.\nmaintainers:\n  - FN: API Evangelist\n    email: info@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/ionis-pharmaceuticals/refs/heads/main/finops/ionis-pharmaceuticals-finops.yml
sources:
- https://www.ionispharma.com
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Pharmaceuticals
- Biotech
---
