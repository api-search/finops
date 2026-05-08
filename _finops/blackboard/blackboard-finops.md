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
  - Adjustment
  pricingCategory: Subscription
description: FOCUS-aligned FinOps profile. Anthology bills via annual enterprise subscription per module.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Blackboard
  ProviderName: Blackboard
  PublisherName: Blackboard
  ServiceCategory: Education & Training
  ServiceName: Blackboard
layout: finops
meters:
- aggregation: sum
  description: Per-module annual subscription.
  dimensions:
  - account
  - module
  name: module_subscription
  unit: subscription
name: Blackboard Finops
provider_name: Blackboard
provider_slug: blackboard
publisher_name: Blackboard
service_category: Education & Training
slug: blackboard-finops
source_filename: blackboard-finops.yml
source_heading: FinOps Profile
source_url: https://www.anthology.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Blackboard\nproviderId: blackboard\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: false\ntags:\n- EdTech\n- LMS\n- Learning Management\n- FinOps\n- Cost Management\n- FOCUS\ndescription: FOCUS-aligned FinOps profile. Anthology bills via annual enterprise subscription per module.\nnotes: Negotiated multi-year contracts common in higher ed.\nsources:\n- https://www.anthology.com/\n- https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Blackboard\nserviceCategory: Education & Training\nbillingModel:\n  pricingCategory: Subscription\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n  - Purchase\n  -\
  \ Adjustment\nfocusColumns:\n  ServiceName: Blackboard\n  ServiceCategory: Education & Training\n  ProviderName: Blackboard\n  PublisherName: Blackboard\n  InvoiceIssuerName: Blackboard\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n- name: module_subscription\n  description: Per-module annual subscription.\n  unit: subscription\n  aggregation: sum\n  dimensions:\n  - account\n  - module\nprinciples:\n- name: Visibility\n  description: Pull provider invoices or usage exports until a self-serve usage feed is documented.\n- name: Allocation\n  description: Tag invoice line items to consuming business units in your FinOps store.\n- name: Optimization\n  description: Levers depend on the provider's billing model; review at renewal once reconciled.\n- name: Accountability\n  description: Assign a contract owner to review billing against negotiated terms.\nmaintainers:\n- FN: Kin Lane\n  email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/blackboard/refs/heads/main/finops/blackboard-finops.yml
sources:
- https://www.anthology.com/
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- EdTech
- LMS
- Learning Management
- FinOps
- Cost Management
- FOCUS
---
