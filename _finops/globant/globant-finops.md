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
  - Purchase
  - Adjustment
  pricingCategory: Professional Services
description: 'FinOps framing for Globant: professional-services engagement with output-based AI Pods and time-and-materials lines. Not a SaaS or API consumption model.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Globant S.A.
  ProviderName: Globant
  PublisherName: Globant S.A.
  ServiceCategory: Professional Services
  ServiceName: Globant
layout: finops
meters:
- aggregation: max
  description: Active AI Pods engaged on output-based delivery
  name: ai_pods
  unit: pod-month
- aggregation: sum
  description: Time-and-materials consultant hours billed
  dimensions:
  - role
  - region
  name: consultant_hours
  unit: hour
- aggregation: count
  description: Fixed-bid project milestones invoiced
  name: fixed_bid_milestones
  unit: milestone
name: Globant Finops
provider_name: Globant
provider_slug: globant
publisher_name: Globant S.A.
service_category: Professional Services
slug: globant-finops
source_filename: globant-finops.yml
source_heading: FinOps Profile
source_url: https://www.globant.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Globant\nproviderId: globant\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Consulting\n  - Software\ndescription: 'FinOps framing for Globant: professional-services engagement with output-based AI Pods\n  and time-and-materials lines. Not a SaaS or API consumption model.'\nnotes: Reconcile only if Globant publishes a productized rate card.\nsources:\n  - https://www.globant.com/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Globant S.A.\nserviceCategory: Professional Services\nbillingModel:\n  pricingCategory: Professional Services\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n\
  \    - Adjustment\nfocusColumns:\n  ServiceName: Globant\n  ServiceCategory: Professional Services\n  ProviderName: Globant\n  PublisherName: Globant S.A.\n  InvoiceIssuerName: Globant S.A.\n  BillingCurrency: USD\nmeters:\n  - name: ai_pods\n    description: Active AI Pods engaged on output-based delivery\n    unit: pod-month\n    aggregation: max\n  - name: consultant_hours\n    description: Time-and-materials consultant hours billed\n    unit: hour\n    aggregation: sum\n    dimensions:\n      - role\n      - region\n  - name: fixed_bid_milestones\n    description: Fixed-bid project milestones invoiced\n    unit: milestone\n    aggregation: count\nprinciples:\n  - name: Visibility\n    description: Track Globant invoices, pod outputs, and time-tracking exports against engagement budget.\n  - name: Allocation\n    description: Allocate Globant cost to the consuming initiative / business unit; AI Pods to specific\n      product squads.\n  - name: Optimization\n    description: Negotiate\
  \ pod-output SLAs; transition repeatable work from time-and-materials to fixed-bid;\n      ensure early-engagement scope clarity.\n  - name: Accountability\n    description: Engagement sponsor owns Globant spend; finance reviews monthly invoice variance.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/globant/refs/heads/main/finops/globant-finops.yml
sources:
- https://www.globant.com/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Consulting
- Software
---
