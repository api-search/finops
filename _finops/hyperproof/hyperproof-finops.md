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
description: FOCUS-aligned FinOps profile. Hyperproof bills via annual subscription.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Hyperproof
  ProviderName: Hyperproof
  PublisherName: Hyperproof
  ServiceCategory: Compliance & Governance
  ServiceName: Hyperproof
layout: finops
meters:
- aggregation: sum
  description: Annual subscription with users and integrations.
  dimensions:
  - account
  - users
  name: subscription
  unit: subscription
name: Hyperproof Finops
provider_name: Hyperproof
provider_slug: hyperproof
publisher_name: Hyperproof
service_category: Compliance & Governance
slug: hyperproof-finops
source_filename: hyperproof-finops.yml
source_heading: FinOps Profile
source_url: https://hyperproof.io/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Hyperproof\nproviderId: hyperproof\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: false\ntags:\n- GRC\n- Compliance\n- Risk\n- Audit\n- SOC 2\n- FinOps\n- Cost Management\n- FOCUS\ndescription: FOCUS-aligned FinOps profile. Hyperproof bills via annual subscription.\nnotes: API access included in subscription.\nsources:\n- https://hyperproof.io/\n- https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Hyperproof\nserviceCategory: Compliance & Governance\nbillingModel:\n  pricingCategory: Subscription\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n  - Purchase\n  - Adjustment\nfocusColumns:\n  ServiceName:\
  \ Hyperproof\n  ServiceCategory: Compliance & Governance\n  ProviderName: Hyperproof\n  PublisherName: Hyperproof\n  InvoiceIssuerName: Hyperproof\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n- name: subscription\n  description: Annual subscription with users and integrations.\n  unit: subscription\n  aggregation: sum\n  dimensions:\n  - account\n  - users\nprinciples:\n- name: Visibility\n  description: Pull provider invoices or usage exports until a self-serve usage feed is documented.\n- name: Allocation\n  description: Tag invoice line items to consuming business units in your FinOps store.\n- name: Optimization\n  description: Levers depend on the provider's billing model; review at renewal once reconciled.\n- name: Accountability\n  description: Assign a contract owner to review billing against negotiated terms.\nmaintainers:\n- FN: Kin Lane\n  email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/hyperproof/refs/heads/main/finops/hyperproof-finops.yml
sources:
- https://hyperproof.io/
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- GRC
- Compliance
- Risk
- Audit
- SOC 2
- FinOps
- Cost Management
- FOCUS
---
