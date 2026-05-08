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
description: FOCUS-aligned FinOps placeholder for Gong. Pipeline will replace with real billing details.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Gong
  ProviderName: Gong
  PublisherName: Gong
  ServiceCategory: Sales
  ServiceName: Gong
layout: finops
meters:
- aggregation: sum
  description: Catch-all meter pending reconciliation.
  dimensions:
  - account
  - resource
  name: api_usage
  unit: varies
name: Gong Finops
provider_name: Gong
provider_slug: gong
publisher_name: Gong
service_category: Sales
slug: gong-finops
source_filename: gong-finops.yml
source_heading: FinOps Profile
source_url: https://www.gong.io/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Gong\nproviderId: gong\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: false\ntags:\n- Sales\n- Revenue Intelligence\n- Conversation\n- Analytics\n- AI\n- FinOps\n- Cost Management\n- FOCUS\ndescription: FOCUS-aligned FinOps placeholder for Gong. Pipeline will replace with real billing details.\nnotes: \"Initial scaffold \\u2014 billing model has not yet been reconciled.\"\nsources:\n- https://www.gong.io/\n- https://app.gong.io/settings/api/documentation\n- https://app.gong.io/settings/api/documentation\n- https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Gong\nserviceCategory: Sales\nbillingModel:\n  pricingCategory:\
  \ To Be Reconciled\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n  - Usage\n  - Purchase\n  - Adjustment\nfocusColumns:\n  ServiceName: Gong\n  ServiceCategory: Sales\n  ProviderName: Gong\n  PublisherName: Gong\n  InvoiceIssuerName: Gong\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n- name: api_usage\n  description: Catch-all meter pending reconciliation.\n  unit: varies\n  aggregation: sum\n  dimensions:\n  - account\n  - resource\nprinciples:\n- name: Visibility\n  description: Pull provider invoices or usage exports until a self-serve usage feed is documented.\n- name: Allocation\n  description: Tag invoice line items to consuming business units in your FinOps store.\n- name: Optimization\n  description: Levers depend on the provider's billing model; review at renewal once reconciled.\n- name: Accountability\n  description: Assign a contract owner to review billing against negotiated terms.\nmaintainers:\n- FN: Kin Lane\n  email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/gong/refs/heads/main/finops/gong-finops.yml
sources:
- https://www.gong.io/
- https://app.gong.io/settings/api/documentation
- https://app.gong.io/settings/api/documentation
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Sales
- Revenue Intelligence
- Conversation
- Analytics
- AI
- FinOps
- Cost Management
- FOCUS
---
