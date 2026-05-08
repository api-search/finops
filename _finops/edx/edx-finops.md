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
  - Usage
  - Adjustment
  pricingCategory: Hybrid
description: FOCUS-aligned FinOps profile. Open-source self-host costs are infrastructure-only; partner programs follow contractual subscription.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: edX
  ProviderName: edX
  PublisherName: edX
  ServiceCategory: Education & Training
  ServiceName: edX
layout: finops
meters:
- aggregation: sum
  description: Self-host Open edX infrastructure costs.
  dimensions:
  - deployment
  name: infrastructure
  unit: varies
- aggregation: sum
  description: edX partner subscription line item.
  dimensions:
  - account
  name: partner_subscription
  unit: subscription
name: Edx Finops
provider_name: edX
provider_slug: edx
publisher_name: edX
service_category: Education & Training
slug: edx-finops
source_filename: edx-finops.yml
source_heading: FinOps Profile
source_url: https://openedx.org/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: edX\nproviderId: edx\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: false\ntags:\n- EdTech\n- Online Learning\n- Open Source\n- MOOC\n- FinOps\n- Cost Management\n- FOCUS\ndescription: FOCUS-aligned FinOps profile. Open-source self-host costs are infrastructure-only; partner\n  programs follow contractual subscription.\nnotes: Internal FinOps focus is on hosting and content licensing.\nsources:\n- https://openedx.org/\n- https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: edX\nserviceCategory: Education & Training\nbillingModel:\n  pricingCategory: Hybrid\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n\
  \  - Purchase\n  - Usage\n  - Adjustment\nfocusColumns:\n  ServiceName: edX\n  ServiceCategory: Education & Training\n  ProviderName: edX\n  PublisherName: edX\n  InvoiceIssuerName: edX\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n- name: infrastructure\n  description: Self-host Open edX infrastructure costs.\n  unit: varies\n  aggregation: sum\n  dimensions:\n  - deployment\n- name: partner_subscription\n  description: edX partner subscription line item.\n  unit: subscription\n  aggregation: sum\n  dimensions:\n  - account\nprinciples:\n- name: Visibility\n  description: Pull provider invoices or usage exports until a self-serve usage feed is documented.\n- name: Allocation\n  description: Tag invoice line items to consuming business units in your FinOps store.\n- name: Optimization\n  description: Levers depend on the provider's billing model; review at renewal once reconciled.\n- name: Accountability\n  description: Assign a contract owner to review billing against negotiated\
  \ terms.\nmaintainers:\n- FN: Kin Lane\n  email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/edx/refs/heads/main/finops/edx-finops.yml
sources:
- https://openedx.org/
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- EdTech
- Online Learning
- Open Source
- MOOC
- FinOps
- Cost Management
- FOCUS
---
