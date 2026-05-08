---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly / Annual
  chargeCategories:
  - Usage
  - Purchase
  - Adjustment
  pricingCategory: Subscription (capped)
description: FOCUS-aligned FinOps profile for Formspree. Billing is a flat plan fee (Free or one of three paid tiers — Personal, Professional, Business) with the monthly submission cap as the dominant constraint. There are no usage overages — you are throttled, not metered, above plan cap.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Formspree
  PricingUnit: plan-month
  ProviderName: Formspree
  PublisherName: Formspree
  ServiceCategory: Forms
  ServiceName: Formspree
layout: finops
meters:
- aggregation: sum
  description: Flat monthly plan fee.
  dimensions:
  - account
  - plan
  name: plan_subscription
  unit: month
- aggregation: sum
  description: Submissions counted against plan cap (50 on Free).
  dimensions:
  - account
  - form
  name: monthly_submissions
  unit: submission
- aggregation: max
  description: Days of submission history retained (30 on Free; full on paid).
  dimensions:
  - account
  name: archive_retention
  unit: days
name: Formspree Finops
provider_name: Formspree
provider_slug: formspree
publisher_name: Formspree
service_category: Forms / Backend
slug: formspree-finops
source_filename: formspree-finops.yml
source_heading: FinOps Profile
source_url: https://formspree.io/plans
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Formspree\nproviderId: formspree\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: true\ntags:\n- Forms\n- Backend\n- Static Sites\n- Email\n- Webhooks\n- FinOps\n- Cost Management\n- FOCUS\ndescription: >-\n  FOCUS-aligned FinOps profile for Formspree. Billing is a flat plan fee\n  (Free or one of three paid tiers — Personal, Professional, Business) with\n  the monthly submission cap as the dominant constraint. There are no usage\n  overages — you are throttled, not metered, above plan cap.\nnotes: >-\n  Cost optimisation is mostly about right-sizing the tier to actual monthly\n  submissions. Free's 30-day archive retention is the chief operational\n  optimisation — schedule exports if downgrading or near-archive age.\nsources:\n- https://formspree.io/plans\n- https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation\
  \ Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Formspree\nserviceCategory: Forms / Backend\nbillingModel:\n  pricingCategory: Subscription (capped)\n  billingFrequency: Monthly / Annual\n  billingCurrency: USD\n  chargeCategories:\n  - Usage\n  - Purchase\n  - Adjustment\nfocusColumns:\n  ServiceName: Formspree\n  ServiceCategory: Forms\n  ProviderName: Formspree\n  PublisherName: Formspree\n  InvoiceIssuerName: Formspree\n  BillingCurrency: USD\n  ChargeCategory: Purchase\n  PricingUnit: plan-month\nmeters:\n- name: plan_subscription\n  description: Flat monthly plan fee.\n  unit: month\n  aggregation: sum\n  dimensions:\n  - account\n  - plan\n- name: monthly_submissions\n  description: Submissions counted against plan cap (50 on Free).\n  unit: submission\n  aggregation: sum\n  dimensions:\n  - account\n  - form\n- name: archive_retention\n\
  \  description: Days of submission history retained (30 on Free; full on paid).\n  unit: days\n  aggregation: max\n  dimensions:\n  - account\nprinciples:\n- name: Visibility\n  description: Use Formspree dashboard usage page; threshold emails at 50/75/90% of cap.\n- name: Allocation\n  description: Use per-form hashids to allocate by team / project.\n- name: Optimization\n  description: Right-size plan tier to actual monthly submissions; schedule exports before archive expiry on Free.\n- name: Accountability\n  description: Assign account owner; alert on threshold notifications.\nmaintainers:\n- FN: Kin Lane\n  email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/formspree/refs/heads/main/finops/formspree-finops.yml
sources:
- https://formspree.io/plans
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Forms
- Backend
- Static Sites
- Email
- Webhooks
- FinOps
- Cost Management
- FOCUS
---
