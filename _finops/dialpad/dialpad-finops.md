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
description: FOCUS-aligned FinOps placeholder for Dialpad. Pipeline will replace with real billing details.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Dialpad
  ProviderName: Dialpad
  PublisherName: Dialpad
  ServiceCategory: Communications
  ServiceName: Dialpad
layout: finops
meters:
- aggregation: sum
  description: Catch-all meter pending reconciliation.
  dimensions:
  - account
  - resource
  name: api_usage
  unit: varies
name: Dialpad Finops
provider_name: Dialpad
provider_slug: dialpad
publisher_name: Dialpad
service_category: Communications
slug: dialpad-finops
source_filename: dialpad-finops.yml
source_heading: FinOps Profile
source_url: https://www.dialpad.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Dialpad\nproviderId: dialpad\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: false\ntags:\n- Communications\n- Voice\n- AI\n- Contact Center\n- UCaaS\n- FinOps\n- Cost Management\n- FOCUS\ndescription: FOCUS-aligned FinOps placeholder for Dialpad. Pipeline will replace with real billing details.\nnotes: \"Initial scaffold \\u2014 billing model has not yet been reconciled.\"\nsources:\n- https://www.dialpad.com/\n- https://developers.dialpad.com/\n- https://developers.dialpad.com/reference\n- https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Dialpad\nserviceCategory: Communications\nbillingModel:\n  pricingCategory: To\
  \ Be Reconciled\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n  - Usage\n  - Purchase\n  - Adjustment\nfocusColumns:\n  ServiceName: Dialpad\n  ServiceCategory: Communications\n  ProviderName: Dialpad\n  PublisherName: Dialpad\n  InvoiceIssuerName: Dialpad\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n- name: api_usage\n  description: Catch-all meter pending reconciliation.\n  unit: varies\n  aggregation: sum\n  dimensions:\n  - account\n  - resource\nprinciples:\n- name: Visibility\n  description: Pull provider invoices or usage exports until a self-serve usage feed is documented.\n- name: Allocation\n  description: Tag invoice line items to consuming business units in your FinOps store.\n- name: Optimization\n  description: Levers depend on the provider's billing model; review at renewal once reconciled.\n- name: Accountability\n  description: Assign a contract owner to review billing against negotiated terms.\nmaintainers:\n- FN: Kin Lane\n\
  \  email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/dialpad/refs/heads/main/finops/dialpad-finops.yml
sources:
- https://www.dialpad.com/
- https://developers.dialpad.com/
- https://developers.dialpad.com/reference
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Communications
- Voice
- AI
- Contact Center
- UCaaS
- FinOps
- Cost Management
- FOCUS
---
