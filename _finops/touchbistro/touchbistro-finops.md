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
  - Usage
  - Adjustment
  pricingCategory: Subscription
description: FOCUS-aligned FinOps profile. Per-license SaaS plus optional payment processing.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: TouchBistro
  ProviderName: TouchBistro
  PublisherName: TouchBistro
  ServiceCategory: Payments & POS
  ServiceName: TouchBistro
layout: finops
meters:
- aggregation: sum
  description: Per-license monthly SaaS.
  dimensions:
  - merchant
  name: per_license_saas
  unit: license
name: Touchbistro Finops
provider_name: TouchBistro
provider_slug: touchbistro
publisher_name: TouchBistro
service_category: Payments & POS
slug: touchbistro-finops
source_filename: touchbistro-finops.yml
source_heading: FinOps Profile
source_url: https://www.touchbistro.com/pricing/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: TouchBistro\nproviderId: touchbistro\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: false\ntags:\n- POS\n- Restaurant\n- Hospitality\n- FinOps\n- Cost Management\n- FOCUS\ndescription: FOCUS-aligned FinOps profile. Per-license SaaS plus optional payment processing.\nnotes: Negotiated multi-license discounts available.\nsources:\n- https://www.touchbistro.com/pricing/\n- https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: TouchBistro\nserviceCategory: Payments & POS\nbillingModel:\n  pricingCategory: Subscription\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n  - Purchase\n  - Usage\n  - Adjustment\n\
  focusColumns:\n  ServiceName: TouchBistro\n  ServiceCategory: Payments & POS\n  ProviderName: TouchBistro\n  PublisherName: TouchBistro\n  InvoiceIssuerName: TouchBistro\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n- name: per_license_saas\n  description: Per-license monthly SaaS.\n  unit: license\n  aggregation: sum\n  dimensions:\n  - merchant\nprinciples:\n- name: Visibility\n  description: Pull provider invoices or usage exports until a self-serve usage feed is documented.\n- name: Allocation\n  description: Tag invoice line items to consuming business units in your FinOps store.\n- name: Optimization\n  description: Levers depend on the provider's billing model; review at renewal once reconciled.\n- name: Accountability\n  description: Assign a contract owner to review billing against negotiated terms.\nmaintainers:\n- FN: Kin Lane\n  email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/touchbistro/refs/heads/main/finops/touchbistro-finops.yml
sources:
- https://www.touchbistro.com/pricing/
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- POS
- Restaurant
- Hospitality
- FinOps
- Cost Management
- FOCUS
---
