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
description: FOCUS-aligned FinOps profile. Subscription billed annually via PowerSchool master agreement.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Schoology
  ProviderName: Schoology
  PublisherName: Schoology
  ServiceCategory: Education & Training
  ServiceName: Schoology
layout: finops
meters:
- aggregation: sum
  description: Annual district subscription line item.
  dimensions:
  - account
  - students
  name: district_subscription
  unit: subscription
name: Schoology Finops
provider_name: Schoology
provider_slug: schoology
publisher_name: Schoology
service_category: Education & Training
slug: schoology-finops
source_filename: schoology-finops.yml
source_heading: FinOps Profile
source_url: https://www.schoology.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Schoology\nproviderId: schoology\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: false\ntags:\n- EdTech\n- LMS\n- K-12\n- FinOps\n- Cost Management\n- FOCUS\ndescription: FOCUS-aligned FinOps profile. Subscription billed annually via PowerSchool master agreement.\nnotes: K-12 procurement cycles drive renewal patterns.\nsources:\n- https://www.schoology.com/\n- https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Schoology\nserviceCategory: Education & Training\nbillingModel:\n  pricingCategory: Subscription\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n  - Purchase\n  - Adjustment\nfocusColumns:\n\
  \  ServiceName: Schoology\n  ServiceCategory: Education & Training\n  ProviderName: Schoology\n  PublisherName: Schoology\n  InvoiceIssuerName: Schoology\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n- name: district_subscription\n  description: Annual district subscription line item.\n  unit: subscription\n  aggregation: sum\n  dimensions:\n  - account\n  - students\nprinciples:\n- name: Visibility\n  description: Pull provider invoices or usage exports until a self-serve usage feed is documented.\n- name: Allocation\n  description: Tag invoice line items to consuming business units in your FinOps store.\n- name: Optimization\n  description: Levers depend on the provider's billing model; review at renewal once reconciled.\n- name: Accountability\n  description: Assign a contract owner to review billing against negotiated terms.\nmaintainers:\n- FN: Kin Lane\n  email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/schoology/refs/heads/main/finops/schoology-finops.yml
sources:
- https://www.schoology.com/
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- EdTech
- LMS
- K-12
- FinOps
- Cost Management
- FOCUS
---
