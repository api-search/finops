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
  - Purchase
  - Usage
  - Adjustment
  pricingCategory: Subscription
description: FOCUS-aligned FinOps profile. Per-terminal SaaS plus optional payment processing and hardware.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Revel Systems
  ProviderName: Revel Systems
  PublisherName: Revel Systems
  ServiceCategory: Payments & POS
  ServiceName: Revel Systems
layout: finops
meters:
- aggregation: sum
  description: Per-terminal monthly SaaS.
  dimensions:
  - merchant
  - establishment
  name: per_terminal_saas
  unit: terminal
name: Revel Systems Finops
provider_name: Revel Systems
provider_slug: revel-systems
publisher_name: Revel Systems
service_category: Payments & POS
slug: revel-systems-finops
source_filename: revel-systems-finops.yml
source_heading: FinOps Profile
source_url: https://revelsystems.com/pricing/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Revel Systems\nproviderId: revel-systems\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: false\ntags:\n- POS\n- Restaurant\n- Retail\n- iPad\n- FinOps\n- Cost Management\n- FOCUS\ndescription: FOCUS-aligned FinOps profile. Per-terminal SaaS plus optional payment processing and hardware.\nnotes: Hardware separately invoiced.\nsources:\n- https://revelsystems.com/pricing/\n- https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Revel Systems\nserviceCategory: Payments & POS\nbillingModel:\n  pricingCategory: Subscription\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n  - Purchase\n  - Usage\n  -\
  \ Adjustment\nfocusColumns:\n  ServiceName: Revel Systems\n  ServiceCategory: Payments & POS\n  ProviderName: Revel Systems\n  PublisherName: Revel Systems\n  InvoiceIssuerName: Revel Systems\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n- name: per_terminal_saas\n  description: Per-terminal monthly SaaS.\n  unit: terminal\n  aggregation: sum\n  dimensions:\n  - merchant\n  - establishment\nprinciples:\n- name: Visibility\n  description: Pull provider invoices or usage exports until a self-serve usage feed is documented.\n- name: Allocation\n  description: Tag invoice line items to consuming business units in your FinOps store.\n- name: Optimization\n  description: Levers depend on the provider's billing model; review at renewal once reconciled.\n- name: Accountability\n  description: Assign a contract owner to review billing against negotiated terms.\nmaintainers:\n- FN: Kin Lane\n  email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/revel-systems/refs/heads/main/finops/revel-systems-finops.yml
sources:
- https://revelsystems.com/pricing/
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- POS
- Restaurant
- Retail
- iPad
- FinOps
- Cost Management
- FOCUS
---
