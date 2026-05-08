---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: N/A
  chargeCategories:
  - Adjustment
  pricingCategory: Free
description: FOCUS-aligned FinOps profile. Khan Academy is free; no consumer billing.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Khan Academy
  ProviderName: Khan Academy
  PublisherName: Khan Academy
  ServiceCategory: Education & Training
  ServiceName: Khan Academy
layout: finops
meters:
- aggregation: sum
  description: No billable meter; service is free.
  dimensions:
  - account
  name: free_use
  unit: n/a
name: Khan Academy Finops
provider_name: Khan Academy
provider_slug: khan-academy
publisher_name: Khan Academy
service_category: Education & Training
slug: khan-academy-finops
source_filename: khan-academy-finops.yml
source_heading: FinOps Profile
source_url: https://www.khanacademy.org/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Khan Academy\nproviderId: khan-academy\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: false\ntags:\n- EdTech\n- Online Learning\n- Non-Profit\n- K-12\n- FinOps\n- Cost Management\n- FOCUS\ndescription: FOCUS-aligned FinOps profile. Khan Academy is free; no consumer billing.\nnotes: No financial integration required for free use.\nsources:\n- https://www.khanacademy.org/\n- https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Khan Academy\nserviceCategory: Education & Training\nbillingModel:\n  pricingCategory: Free\n  billingFrequency: N/A\n  billingCurrency: USD\n  chargeCategories:\n  - Adjustment\nfocusColumns:\n  ServiceName:\
  \ Khan Academy\n  ServiceCategory: Education & Training\n  ProviderName: Khan Academy\n  PublisherName: Khan Academy\n  InvoiceIssuerName: Khan Academy\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n- name: free_use\n  description: No billable meter; service is free.\n  unit: n/a\n  aggregation: sum\n  dimensions:\n  - account\nprinciples:\n- name: Visibility\n  description: Pull provider invoices or usage exports until a self-serve usage feed is documented.\n- name: Allocation\n  description: Tag invoice line items to consuming business units in your FinOps store.\n- name: Optimization\n  description: Levers depend on the provider's billing model; review at renewal once reconciled.\n- name: Accountability\n  description: Assign a contract owner to review billing against negotiated terms.\nmaintainers:\n- FN: Kin Lane\n  email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/khan-academy/refs/heads/main/finops/khan-academy-finops.yml
sources:
- https://www.khanacademy.org/
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- EdTech
- Online Learning
- Non-Profit
- K-12
- FinOps
- Cost Management
- FOCUS
---
