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
description: FOCUS-aligned FinOps profile. OneTrust bills via annual enterprise subscription with per-module line items.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: OneTrust
  ProviderName: OneTrust
  PublisherName: OneTrust
  ServiceCategory: Compliance & Governance
  ServiceName: OneTrust
layout: finops
meters:
- aggregation: sum
  description: Per-module annual subscription line item.
  dimensions:
  - account
  - module
  name: module_subscription
  unit: subscription
name: Onetrust Finops
provider_name: OneTrust
provider_slug: onetrust
publisher_name: OneTrust
service_category: Compliance & Governance
slug: onetrust-finops
source_filename: onetrust-finops.yml
source_heading: FinOps Profile
source_url: https://www.onetrust.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: OneTrust\nproviderId: onetrust\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: false\ntags:\n- Privacy\n- GRC\n- Compliance\n- Consent\n- TPRM\n- FinOps\n- Cost Management\n- FOCUS\ndescription: FOCUS-aligned FinOps profile. OneTrust bills via annual enterprise subscription with per-module\n  line items.\nnotes: Negotiated multi-year contracts are common.\nsources:\n- https://www.onetrust.com/\n- https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: OneTrust\nserviceCategory: Compliance & Governance\nbillingModel:\n  pricingCategory: Subscription\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n \
  \ - Purchase\n  - Adjustment\nfocusColumns:\n  ServiceName: OneTrust\n  ServiceCategory: Compliance & Governance\n  ProviderName: OneTrust\n  PublisherName: OneTrust\n  InvoiceIssuerName: OneTrust\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n- name: module_subscription\n  description: Per-module annual subscription line item.\n  unit: subscription\n  aggregation: sum\n  dimensions:\n  - account\n  - module\nprinciples:\n- name: Visibility\n  description: Pull provider invoices or usage exports until a self-serve usage feed is documented.\n- name: Allocation\n  description: Tag invoice line items to consuming business units in your FinOps store.\n- name: Optimization\n  description: Levers depend on the provider's billing model; review at renewal once reconciled.\n- name: Accountability\n  description: Assign a contract owner to review billing against negotiated terms.\nmaintainers:\n- FN: Kin Lane\n  email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/onetrust/refs/heads/main/finops/onetrust-finops.yml
sources:
- https://www.onetrust.com/
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Privacy
- GRC
- Compliance
- Consent
- TPRM
- FinOps
- Cost Management
- FOCUS
---
