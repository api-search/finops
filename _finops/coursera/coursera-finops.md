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
description: FOCUS-aligned FinOps profile. Catalog API is free; enterprise products are subscription-based.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Coursera
  ProviderName: Coursera
  PublisherName: Coursera
  ServiceCategory: Education & Training
  ServiceName: Coursera
layout: finops
meters:
- aggregation: sum
  description: Coursera for Business/Campus annual subscription.
  dimensions:
  - account
  - seats
  name: subscription
  unit: subscription
name: Coursera Finops
provider_name: Coursera
provider_slug: coursera
publisher_name: Coursera
service_category: Education & Training
slug: coursera-finops
source_filename: coursera-finops.yml
source_heading: FinOps Profile
source_url: https://www.coursera.org/business
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Coursera\nproviderId: coursera\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: false\ntags:\n- EdTech\n- Online Learning\n- Catalog\n- MOOC\n- FinOps\n- Cost Management\n- FOCUS\ndescription: FOCUS-aligned FinOps profile. Catalog API is free; enterprise products are subscription-based.\nnotes: API itself does not generate billable usage in the public Catalog tier.\nsources:\n- https://www.coursera.org/business\n- https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Coursera\nserviceCategory: Education & Training\nbillingModel:\n  pricingCategory: Subscription\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n\
  \  - Purchase\n  - Adjustment\nfocusColumns:\n  ServiceName: Coursera\n  ServiceCategory: Education & Training\n  ProviderName: Coursera\n  PublisherName: Coursera\n  InvoiceIssuerName: Coursera\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n- name: subscription\n  description: Coursera for Business/Campus annual subscription.\n  unit: subscription\n  aggregation: sum\n  dimensions:\n  - account\n  - seats\nprinciples:\n- name: Visibility\n  description: Pull provider invoices or usage exports until a self-serve usage feed is documented.\n- name: Allocation\n  description: Tag invoice line items to consuming business units in your FinOps store.\n- name: Optimization\n  description: Levers depend on the provider's billing model; review at renewal once reconciled.\n- name: Accountability\n  description: Assign a contract owner to review billing against negotiated terms.\nmaintainers:\n- FN: Kin Lane\n  email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/coursera/refs/heads/main/finops/coursera-finops.yml
sources:
- https://www.coursera.org/business
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- EdTech
- Online Learning
- Catalog
- MOOC
- FinOps
- Cost Management
- FOCUS
---
