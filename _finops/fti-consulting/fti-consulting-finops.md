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
  - Adjustment
  pricingCategory: Professional Services
description: FTI Consulting bills under professional-services engagements (hourly, fixed-fee, or retainer) rather than as a SaaS or API surface. FinOps treatment focuses on engagement-level budget allocation and burn-rate tracking.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: FTI Consulting, Inc.
  ProviderName: FTI Consulting
  PublisherName: FTI Consulting, Inc.
  ServiceCategory: Professional Services
  ServiceName: FTI Consulting
layout: finops
meters:
- aggregation: sum
  dimensions:
  - engagement
  - resource_level
  name: consulting_hours
  unit: hour
- aggregation: count
  dimensions:
  - engagement
  name: fixed_fee_milestones
  unit: milestone
- aggregation: sum
  dimensions:
  - engagement
  - category
  name: expenses
  unit: USD
name: Fti Consulting Finops
provider_name: FTI Consulting
provider_slug: fti-consulting
publisher_name: FTI Consulting, Inc.
service_category: Professional Services
slug: fti-consulting-finops
source_filename: fti-consulting-finops.yml
source_heading: FinOps Profile
source_url: https://www.fticonsulting.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: FTI Consulting\nproviderId: fti-consulting\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Consulting\n  - Professional Services\ndescription: FTI Consulting bills under professional-services engagements (hourly, fixed-fee, or\n  retainer) rather than as a SaaS or API surface. FinOps treatment focuses on engagement-level\n  budget allocation and burn-rate tracking.\nnotes: No public API or pricing surface; FinOps shape inferred from a professional-services\n  engagement model.\nsources:\n  - https://www.fticonsulting.com/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: FTI Consulting, Inc.\nserviceCategory: Professional Services\n\
  billingModel:\n  pricingCategory: Professional Services\n  billingFrequency: Per-Invoice\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Adjustment\nfocusColumns:\n  ServiceName: FTI Consulting\n  ServiceCategory: Professional Services\n  ProviderName: FTI Consulting\n  PublisherName: FTI Consulting, Inc.\n  InvoiceIssuerName: FTI Consulting, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: consulting_hours\n    unit: hour\n    aggregation: sum\n    dimensions:\n      - engagement\n      - resource_level\n  - name: fixed_fee_milestones\n    unit: milestone\n    aggregation: count\n    dimensions:\n      - engagement\n  - name: expenses\n    unit: USD\n    aggregation: sum\n    dimensions:\n      - engagement\n      - category\nprinciples:\n  - name: Visibility\n    description: Reconcile FTI invoices against engagement statements of work; track hours-burned\n      against approved budget per workstream.\n  - name: Allocation\n    description: Tag every engagement to\
  \ a sponsoring business unit; allocate fixed-fee\n      milestones at completion.\n  - name: Optimization\n    description: Negotiate tiered rate cards by resource level; consider blended-rate or capped\n      fixed-fee structures for predictable scopes.\n  - name: Accountability\n    description: Engagement sponsor owns burn-rate; PMO reviews variance vs SOW monthly.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/fti-consulting/refs/heads/main/finops/fti-consulting-finops.yml
sources:
- https://www.fticonsulting.com/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Consulting
- Professional Services
---
