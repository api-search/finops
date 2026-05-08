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
  pricingCategory: Subscription (response-tiered)
description: FOCUS-aligned FinOps profile for Typeform. Billing is a flat per-month plan fee (Basic, Plus, Business, Talent, Growth Flow) with response-tiered bundles, plus per-seat consumption inside the plan's user limits. Annual billing is ~30% cheaper. Enterprise / Growth Custom contracts are negotiated.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Typeform
  PricingUnit: plan-month
  ProviderName: Typeform
  PublisherName: Typeform
  ServiceCategory: Forms
  ServiceName: Typeform
layout: finops
meters:
- aggregation: max
  description: Seats consumed in the plan (capped at plan ceiling).
  dimensions:
  - workspace
  name: plan_seat
  unit: user-month
- aggregation: sum
  description: Form submissions counted against the plan's monthly bundle.
  dimensions:
  - workspace
  - form
  name: responses
  unit: response
- aggregation: sum
  description: Flat plan fee (Basic / Plus / Business / Talent / Growth Flow).
  dimensions:
  - account
  - plan
  name: plan_subscription
  unit: month
name: Typeform Finops
provider_name: Typeform
provider_slug: typeform
publisher_name: Typeform
service_category: Forms / Surveys
slug: typeform-finops
source_filename: typeform-finops.yml
source_heading: FinOps Profile
source_url: https://www.typeform.com/pricing/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Typeform\nproviderId: typeform\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: true\ntags:\n- Forms\n- Surveys\n- Conversational\n- Lead Capture\n- SaaS\n- FinOps\n- Cost Management\n- FOCUS\ndescription: >-\n  FOCUS-aligned FinOps profile for Typeform. Billing is a flat per-month plan\n  fee (Basic, Plus, Business, Talent, Growth Flow) with response-tiered\n  bundles, plus per-seat consumption inside the plan's user limits. Annual\n  billing is ~30% cheaper. Enterprise / Growth Custom contracts are\n  negotiated.\nnotes: >-\n  Cost optimisation is mostly about right-sizing the response tier (10K\n  responses sit between Plus 1K and Business 10K). The Workspaces feature\n  enables internal allocation by team.\nsources:\n- https://www.typeform.com/pricing/\n- https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation\
  \ Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Typeform\nserviceCategory: Forms / Surveys\nbillingModel:\n  pricingCategory: Subscription (response-tiered)\n  billingFrequency: Monthly / Annual\n  billingCurrency: USD\n  chargeCategories:\n  - Usage\n  - Purchase\n  - Adjustment\nfocusColumns:\n  ServiceName: Typeform\n  ServiceCategory: Forms\n  ProviderName: Typeform\n  PublisherName: Typeform\n  InvoiceIssuerName: Typeform\n  BillingCurrency: USD\n  ChargeCategory: Purchase\n  PricingUnit: plan-month\nmeters:\n- name: plan_seat\n  description: Seats consumed in the plan (capped at plan ceiling).\n  unit: user-month\n  aggregation: max\n  dimensions:\n  - workspace\n- name: responses\n  description: Form submissions counted against the plan's monthly bundle.\n  unit: response\n  aggregation: sum\n  dimensions:\n  - workspace\n  - form\n- name:\
  \ plan_subscription\n  description: Flat plan fee (Basic / Plus / Business / Talent / Growth Flow).\n  unit: month\n  aggregation: sum\n  dimensions:\n  - account\n  - plan\nprinciples:\n- name: Visibility\n  description: Use the Typeform admin Usage page; export form-level submission counts for chargeback.\n- name: Allocation\n  description: Use Workspaces to map forms to teams; allocate seat + response cost downstream.\n- name: Optimization\n  description: Right-size plan tier annually; archive low-traffic forms; prefer webhook delivery over Responses-API polling.\n- name: Accountability\n  description: Assign workspace owners; alert when responses approach plan cap.\nmaintainers:\n- FN: Kin Lane\n  email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/typeform/refs/heads/main/finops/typeform-finops.yml
sources:
- https://www.typeform.com/pricing/
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Forms
- Surveys
- Conversational
- Lead Capture
- SaaS
- FinOps
- Cost Management
- FOCUS
---
