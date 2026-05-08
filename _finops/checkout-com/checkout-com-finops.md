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
description: FOCUS-aligned FinOps placeholder for Checkout.com. Pipeline will replace with real billing details.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Checkout.com
  ProviderName: Checkout.com
  PublisherName: Checkout.com
  ServiceCategory: Fintech
  ServiceName: Checkout.com
layout: finops
meters:
- aggregation: sum
  description: Catch-all meter pending reconciliation.
  dimensions:
  - account
  - resource
  name: api_usage
  unit: varies
name: Checkout Com Finops
provider_name: Checkout.com
provider_slug: checkout-com
publisher_name: Checkout.com
service_category: Fintech
slug: checkout-com-finops
source_filename: checkout-com-finops.yml
source_heading: FinOps Profile
source_url: https://www.checkout.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Checkout.com\nproviderId: checkout-com\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: false\ntags:\n- Fintech\n- Payments\n- Cards\n- Acquiring\n- Cross-Border\n- FinOps\n- Cost Management\n- FOCUS\ndescription: FOCUS-aligned FinOps placeholder for Checkout.com. Pipeline will replace with real billing details.\nnotes: \"Initial scaffold \\u2014 billing model has not yet been reconciled.\"\nsources:\n- https://www.checkout.com/\n- https://www.checkout.com/docs\n- https://api-reference.checkout.com/\n- https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Checkout.com\nserviceCategory: Fintech\nbillingModel:\n  pricingCategory:\
  \ To Be Reconciled\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n  - Usage\n  - Purchase\n  - Adjustment\nfocusColumns:\n  ServiceName: Checkout.com\n  ServiceCategory: Fintech\n  ProviderName: Checkout.com\n  PublisherName: Checkout.com\n  InvoiceIssuerName: Checkout.com\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n- name: api_usage\n  description: Catch-all meter pending reconciliation.\n  unit: varies\n  aggregation: sum\n  dimensions:\n  - account\n  - resource\nprinciples:\n- name: Visibility\n  description: Pull provider invoices or usage exports until a self-serve usage feed is documented.\n- name: Allocation\n  description: Tag invoice line items to consuming business units in your FinOps store.\n- name: Optimization\n  description: Levers depend on the provider's billing model; review at renewal once reconciled.\n- name: Accountability\n  description: Assign a contract owner to review billing against negotiated terms.\nmaintainers:\n\
  - FN: Kin Lane\n  email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/checkout-com/refs/heads/main/finops/checkout-com-finops.yml
sources:
- https://www.checkout.com/
- https://www.checkout.com/docs
- https://api-reference.checkout.com/
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Fintech
- Payments
- Cards
- Acquiring
- Cross-Border
- FinOps
- Cost Management
- FOCUS
---
