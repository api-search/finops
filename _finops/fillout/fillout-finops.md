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
  - Purchase
  pricingCategory: Subscription (response-tiered)
description: FOCUS-aligned FinOps profile for Fillout. Billing is a flat monthly tier fee (Free / Starter / Pro / Business / Enterprise) with monthly response caps as the primary scaling driver. Annual billing offers material discounts. Unlimited seats and unlimited forms across tiers, so per-form-per-team allocation is straightforward.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Fillout
  PricingUnit: plan-month
  ProviderName: Fillout
  PublisherName: Fillout
  ServiceCategory: Forms
  ServiceName: Fillout
layout: finops
meters:
- aggregation: sum
  description: Flat monthly Fillout plan fee.
  dimensions:
  - account
  - plan
  name: plan_subscription
  unit: month
- aggregation: sum
  description: Form responses counted against the plan's monthly cap.
  dimensions:
  - account
  - form
  name: monthly_responses
  unit: response
- aggregation: max
  description: Active forms (informational).
  dimensions:
  - account
  name: forms
  unit: form
name: Fillout Finops
provider_name: Fillout
provider_slug: fillout
publisher_name: Fillout
service_category: Forms / Workflow
slug: fillout-finops
source_filename: fillout-finops.yml
source_heading: FinOps Profile
source_url: https://www.fillout.com/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Fillout\nproviderId: fillout\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: true\ntags:\n- Forms\n- Surveys\n- No-Code\n- Airtable\n- Notion\n- FinOps\n- Cost Management\n- FOCUS\ndescription: >-\n  FOCUS-aligned FinOps profile for Fillout. Billing is a flat monthly tier fee\n  (Free / Starter / Pro / Business / Enterprise) with monthly response caps as\n  the primary scaling driver. Annual billing offers material discounts.\n  Unlimited seats and unlimited forms across tiers, so per-form-per-team\n  allocation is straightforward.\nnotes: >-\n  Optimisation levers are right-sizing tier and stepping up for the lowest\n  feature set required (custom domain, branding removal, analytics) — not\n  meter-based.\nsources:\n- https://www.fillout.com/pricing\n- https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation\
  \ Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Fillout\nserviceCategory: Forms / Workflow\nbillingModel:\n  pricingCategory: Subscription (response-tiered)\n  billingFrequency: Monthly / Annual\n  billingCurrency: USD\n  chargeCategories:\n  - Purchase\nfocusColumns:\n  ServiceName: Fillout\n  ServiceCategory: Forms\n  ProviderName: Fillout\n  PublisherName: Fillout\n  InvoiceIssuerName: Fillout\n  BillingCurrency: USD\n  ChargeCategory: Purchase\n  PricingUnit: plan-month\nmeters:\n- name: plan_subscription\n  description: Flat monthly Fillout plan fee.\n  unit: month\n  aggregation: sum\n  dimensions:\n  - account\n  - plan\n- name: monthly_responses\n  description: Form responses counted against the plan's monthly cap.\n  unit: response\n  aggregation: sum\n  dimensions:\n  - account\n  - form\n- name: forms\n  description: Active forms (informational).\n\
  \  unit: form\n  aggregation: max\n  dimensions:\n  - account\nprinciples:\n- name: Visibility\n  description: Use Fillout admin response counter; export submissions for finance allocation if needed.\n- name: Allocation\n  description: Use account or workspace structure to allocate forms by team.\n- name: Optimization\n  description: Right-size tier annually; switch to annual billing for ~25% effective discount; consolidate low-traffic forms.\n- name: Accountability\n  description: Assign account owner; alert on response burn-down.\nmaintainers:\n- FN: Kin Lane\n  email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/fillout/refs/heads/main/finops/fillout-finops.yml
sources:
- https://www.fillout.com/pricing
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Forms
- Surveys
- No-Code
- Airtable
- Notion
- FinOps
- Cost Management
- FOCUS
---
