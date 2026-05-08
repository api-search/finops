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
  pricingCategory: Subscription (tiered ceilings)
description: FOCUS-aligned FinOps profile for Jotform. Costs are flat monthly tier fees (Starter free / Bronze $39 / Silver $49 / Gold $129 / Enterprise custom) with implicit ceilings on active forms, monthly submissions, storage and daily API calls. Annual billing reduces effective rate.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Jotform
  PricingUnit: plan-month
  ProviderName: Jotform
  PublisherName: Jotform
  ServiceCategory: Forms
  ServiceName: Jotform
layout: finops
meters:
- aggregation: sum
  description: Flat plan fee (Bronze/Silver/Gold/Enterprise).
  dimensions:
  - account
  - plan
  name: plan_subscription
  unit: month
- aggregation: sum
  description: Form submissions counted against the plan's monthly ceiling.
  dimensions:
  - account
  - form
  name: monthly_submissions
  unit: submission
- aggregation: max
  description: Active forms in the account (counts toward plan ceiling).
  dimensions:
  - account
  name: active_forms
  unit: form
- aggregation: avg
  description: File and submission storage used.
  dimensions:
  - account
  name: storage
  unit: GB-month
- aggregation: sum
  description: Daily API calls counted against tier daily ceiling.
  dimensions:
  - account
  name: api_calls
  unit: request
name: Jotform Finops
provider_name: Jotform
provider_slug: jotform
publisher_name: Jotform
service_category: Forms / Workflow
slug: jotform-finops
source_filename: jotform-finops.yml
source_heading: FinOps Profile
source_url: https://www.jotform.com/pricing/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Jotform\nproviderId: jotform\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: true\ntags:\n- Forms\n- Surveys\n- No-Code\n- Data Collection\n- Workflow\n- FinOps\n- Cost Management\n- FOCUS\ndescription: >-\n  FOCUS-aligned FinOps profile for Jotform. Costs are flat monthly tier fees\n  (Starter free / Bronze $39 / Silver $49 / Gold $129 / Enterprise custom)\n  with implicit ceilings on active forms, monthly submissions, storage and\n  daily API calls. Annual billing reduces effective rate.\nnotes: >-\n  Optimisation is mostly about right-sizing the tier — submissions, storage\n  and API daily-call rates are the dominant scaling drivers.\nsources:\n- https://www.jotform.com/pricing/\n- https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec:\
  \ FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Jotform\nserviceCategory: Forms / Workflow\nbillingModel:\n  pricingCategory: Subscription (tiered ceilings)\n  billingFrequency: Monthly / Annual\n  billingCurrency: USD\n  chargeCategories:\n  - Usage\n  - Purchase\n  - Adjustment\nfocusColumns:\n  ServiceName: Jotform\n  ServiceCategory: Forms\n  ProviderName: Jotform\n  PublisherName: Jotform\n  InvoiceIssuerName: Jotform\n  BillingCurrency: USD\n  ChargeCategory: Purchase\n  PricingUnit: plan-month\nmeters:\n- name: plan_subscription\n  description: Flat plan fee (Bronze/Silver/Gold/Enterprise).\n  unit: month\n  aggregation: sum\n  dimensions:\n  - account\n  - plan\n- name: monthly_submissions\n  description: Form submissions counted against the plan's monthly ceiling.\n  unit: submission\n  aggregation: sum\n  dimensions:\n  - account\n  - form\n- name: active_forms\n  description: Active forms in the account (counts\
  \ toward plan ceiling).\n  unit: form\n  aggregation: max\n  dimensions:\n  - account\n- name: storage\n  description: File and submission storage used.\n  unit: GB-month\n  aggregation: avg\n  dimensions:\n  - account\n- name: api_calls\n  description: Daily API calls counted against tier daily ceiling.\n  unit: request\n  aggregation: sum\n  dimensions:\n  - account\nprinciples:\n- name: Visibility\n  description: Use the Jotform admin Usage page; export submission counts per form.\n- name: Allocation\n  description: Use sub-accounts (Enterprise) or form-naming conventions to allocate by team.\n- name: Optimization\n  description: Archive low-traffic forms; right-size tier annually; prefer webhooks over /submissions polling to keep API calls low.\n- name: Accountability\n  description: Assign account owners; alert at 75% of plan submission ceiling.\nmaintainers:\n- FN: Kin Lane\n  email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/jotform/refs/heads/main/finops/jotform-finops.yml
sources:
- https://www.jotform.com/pricing/
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Forms
- Surveys
- No-Code
- Data Collection
- Workflow
- FinOps
- Cost Management
- FOCUS
---
