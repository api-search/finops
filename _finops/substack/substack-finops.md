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
  - Usage
  - Purchase
  - Adjustment
  pricingCategory: To Be Reconciled
description: FOCUS-aligned FinOps placeholder for Substack. Pipeline will replace with real billing details.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Substack
  ProviderName: Substack
  PublisherName: Substack
  ServiceCategory: Newsletter
  ServiceName: Substack
layout: finops
meters:
- aggregation: sum
  description: Catch-all meter pending reconciliation.
  dimensions:
  - account
  - resource
  name: api_usage
  unit: varies
name: Substack Finops
provider_name: Substack
provider_slug: substack
publisher_name: Substack
service_category: Newsletter
slug: substack-finops
source_filename: substack-finops.yml
source_heading: FinOps Profile
source_url: https://substack.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Substack\nproviderId: substack\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: false\ntags:\n- Newsletter\n- Creator\n- Email\n- Subscription\n- Publishing\n- FinOps\n- Cost Management\n- FOCUS\ndescription: FOCUS-aligned FinOps placeholder for Substack. Pipeline will replace with real billing details.\nnotes: \"Initial scaffold \\u2014 billing model has not yet been reconciled.\"\nsources:\n- https://substack.com/\n- https://substack.com/help\n- https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Substack\nserviceCategory: Newsletter\nbillingModel:\n  pricingCategory: To Be Reconciled\n  billingFrequency: Monthly\n  billingCurrency:\
  \ USD\n  chargeCategories:\n  - Usage\n  - Purchase\n  - Adjustment\nfocusColumns:\n  ServiceName: Substack\n  ServiceCategory: Newsletter\n  ProviderName: Substack\n  PublisherName: Substack\n  InvoiceIssuerName: Substack\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n- name: api_usage\n  description: Catch-all meter pending reconciliation.\n  unit: varies\n  aggregation: sum\n  dimensions:\n  - account\n  - resource\nprinciples:\n- name: Visibility\n  description: Pull provider invoices or usage exports until a self-serve usage feed is documented.\n- name: Allocation\n  description: Tag invoice line items to consuming business units in your FinOps store.\n- name: Optimization\n  description: Levers depend on the provider's billing model; review at renewal once reconciled.\n- name: Accountability\n  description: Assign a contract owner to review billing against negotiated terms.\nmaintainers:\n- FN: Kin Lane\n  email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/substack/refs/heads/main/finops/substack-finops.yml
sources:
- https://substack.com/
- https://substack.com/help
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Newsletter
- Creator
- Email
- Subscription
- Publishing
- FinOps
- Cost Management
- FOCUS
---
