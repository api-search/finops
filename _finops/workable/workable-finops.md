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
  - Tax
  pricingCategory: Subscription
description: Workable's billing model is monthly subscription with optional add-ons (Texting+, Video Interviews+, Assessments+, Performance Reviews+) and a 20% annual discount. This artifact maps Workable charges to FOCUS columns for FinOps allocation across recruiting cost centers.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Workable
  ProviderName: Workable
  PublisherName: Workable
  ServiceCategory: HR
  ServiceName: Workable
layout: finops
meters:
- aggregation: sum
  description: Standard / Premier / Enterprise monthly or annual subscription.
  dimensions:
  - tier
  - cost_center
  name: workable_subscription
  unit: subscription-month
- aggregation: sum
  description: Texting+ / Video Interviews+ / Assessments+ / Performance Reviews+ add-ons (Standard plan only).
  dimensions:
  - addon
  - cost_center
  name: workable_addons
  unit: addon-month
- aggregation: sum
  description: Premium job board postings, third-party assessments, and SMS pass-through.
  dimensions:
  - service
  name: pass_through_costs
  unit: events
name: Workable Finops
provider_name: Workable
provider_slug: workable
publisher_name: Workable
service_category: HR
slug: workable-finops
source_filename: workable-finops.yml
source_heading: FinOps Profile
source_url: https://www.workable.com/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Workable\nproviderId: workable\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: true\ntags:\n  - HR\n  - ATS\n  - Recruiting\n  - FinOps\n  - FOCUS\ndescription: >-\n  Workable's billing model is monthly subscription with optional add-ons\n  (Texting+, Video Interviews+, Assessments+, Performance Reviews+) and a\n  20% annual discount. This artifact maps Workable charges to FOCUS columns\n  for FinOps allocation across recruiting cost centers.\nsources:\n  - https://www.workable.com/pricing\n  - https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Workable\nserviceCategory: HR\nbillingModel:\n  pricingCategory: Subscription\n\
  \  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Adjustment\n    - Tax\nfocusColumns:\n  ServiceName: Workable\n  ServiceCategory: HR\n  ProviderName: Workable\n  PublisherName: Workable\n  InvoiceIssuerName: Workable\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: workable_subscription\n    description: Standard / Premier / Enterprise monthly or annual subscription.\n    unit: subscription-month\n    aggregation: sum\n    dimensions:\n      - tier\n      - cost_center\n  - name: workable_addons\n    description: Texting+ / Video Interviews+ / Assessments+ / Performance Reviews+ add-ons (Standard plan only).\n    unit: addon-month\n    aggregation: sum\n    dimensions:\n      - addon\n      - cost_center\n  - name: pass_through_costs\n    description: Premium job board postings, third-party assessments, and SMS pass-through.\n    unit: events\n    aggregation: sum\n    dimensions:\n      - service\nprinciples:\n  -\
  \ name: Visibility\n    description: >-\n      Pull monthly Workable invoices and renewal proposals; reconcile\n      against actual usage of texting and video minutes.\n  - name: Allocation\n    description: >-\n      Allocate Workable subscription cost to recruiting / talent functions;\n      tag add-ons by department.\n  - name: Optimization\n    description: >-\n      Compare Premier (bundled) vs. Standard + add-ons monthly cost; opt\n      for the bundle when 2+ add-ons are active.\n  - name: Accountability\n    description: >-\n      Designate Talent Operations as the contract owner; review at renewal\n      and lock 20% annual discount.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/workable/refs/heads/main/finops/workable-finops.yml
sources:
- https://www.workable.com/pricing
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- HR
- ATS
- Recruiting
- FinOps
- FOCUS
---
