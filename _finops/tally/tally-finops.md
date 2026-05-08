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
  pricingCategory: Subscription (flat)
description: FOCUS-aligned FinOps profile for Tally. Billing is exclusively a flat monthly subscription on Pro ($24) or Business ($74); the Free plan is perpetual. Submissions are unlimited under fair use, so cost is independent of submission volume. EU-based, GDPR-compliant.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Tally
  PricingUnit: plan-month
  ProviderName: Tally
  PublisherName: Tally
  ServiceCategory: Forms
  ServiceName: Tally
layout: finops
meters:
- aggregation: sum
  description: Flat monthly Tally Pro / Business plan fee.
  dimensions:
  - workspace
  - plan
  name: plan_subscription
  unit: month
- aggregation: max
  description: Active forms in the workspace (informational).
  dimensions:
  - workspace
  name: forms
  unit: form
- aggregation: sum
  description: Submissions count (informational; not billed).
  dimensions:
  - workspace
  - form
  name: submissions
  unit: submission
name: Tally Finops
provider_name: Tally
provider_slug: tally
publisher_name: Tally
service_category: Forms / Surveys
slug: tally-finops
source_filename: tally-finops.yml
source_heading: FinOps Profile
source_url: https://tally.so/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Tally\nproviderId: tally\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: true\ntags:\n- Forms\n- Surveys\n- No-Code\n- Free\n- Notion-style\n- FinOps\n- Cost Management\n- FOCUS\ndescription: >-\n  FOCUS-aligned FinOps profile for Tally. Billing is exclusively a flat\n  monthly subscription on Pro ($24) or Business ($74); the Free plan is\n  perpetual. Submissions are unlimited under fair use, so cost is independent\n  of submission volume. EU-based, GDPR-compliant.\nnotes: >-\n  Only optimisation lever is right-sizing Free vs Pro vs Business based on\n  required features (custom branding, custom domain, version retention).\nsources:\n- https://tally.so/pricing\n- https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion:\
  \ '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Tally\nserviceCategory: Forms / Surveys\nbillingModel:\n  pricingCategory: Subscription (flat)\n  billingFrequency: Monthly / Annual\n  billingCurrency: USD\n  chargeCategories:\n  - Purchase\nfocusColumns:\n  ServiceName: Tally\n  ServiceCategory: Forms\n  ProviderName: Tally\n  PublisherName: Tally\n  InvoiceIssuerName: Tally\n  BillingCurrency: USD\n  ChargeCategory: Purchase\n  PricingUnit: plan-month\nmeters:\n- name: plan_subscription\n  description: Flat monthly Tally Pro / Business plan fee.\n  unit: month\n  aggregation: sum\n  dimensions:\n  - workspace\n  - plan\n- name: forms\n  description: Active forms in the workspace (informational).\n  unit: form\n  aggregation: max\n  dimensions:\n  - workspace\n- name: submissions\n  description: Submissions count (informational; not billed).\n  unit: submission\n  aggregation: sum\n  dimensions:\n  - workspace\n  - form\nprinciples:\n- name: Visibility\n\
  \  description: Track plan tier per workspace; submissions are not billed but worth monitoring for capacity.\n- name: Allocation\n  description: One workspace per team / cost centre.\n- name: Optimization\n  description: Right-size to Free vs Pro vs Business based on actual feature need; consolidate workspaces where possible.\n- name: Accountability\n  description: Assign workspace owner; monitor renewal cadence.\nmaintainers:\n- FN: Kin Lane\n  email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/tally/refs/heads/main/finops/tally-finops.yml
sources:
- https://tally.so/pricing
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Forms
- Surveys
- No-Code
- Free
- Notion-style
- FinOps
- Cost Management
- FOCUS
---
