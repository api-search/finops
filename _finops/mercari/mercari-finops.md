---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: Per Transaction
  chargeCategories:
  - Usage
  - Adjustment
  pricingCategory: Commission
description: FOCUS-aligned FinOps profile. Seller fees on completed sales.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Mercari
  ProviderName: Mercari
  PublisherName: Mercari
  ServiceCategory: Marketplace
  ServiceName: Mercari
layout: finops
meters:
- aggregation: sum
  description: Per-sale fee on completed transactions.
  dimensions:
  - seller
  name: selling_fee
  unit: USD
name: Mercari Finops
provider_name: Mercari
provider_slug: mercari
publisher_name: Mercari
service_category: Marketplace
slug: mercari-finops
source_filename: mercari-finops.yml
source_heading: FinOps Profile
source_url: https://www.mercari.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Mercari\nproviderId: mercari\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: false\ntags:\n- Marketplace\n- Resale\n- P2P\n- Ecommerce\n- FinOps\n- Cost Management\n- FOCUS\ndescription: FOCUS-aligned FinOps profile. Seller fees on completed sales.\nnotes: Free listings; cost realized on sale.\nsources:\n- https://www.mercari.com/\n- https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Mercari\nserviceCategory: Marketplace\nbillingModel:\n  pricingCategory: Commission\n  billingFrequency: Per Transaction\n  billingCurrency: USD\n  chargeCategories:\n  - Usage\n  - Adjustment\nfocusColumns:\n  ServiceName: Mercari\n  ServiceCategory:\
  \ Marketplace\n  ProviderName: Mercari\n  PublisherName: Mercari\n  InvoiceIssuerName: Mercari\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n- name: selling_fee\n  description: Per-sale fee on completed transactions.\n  unit: USD\n  aggregation: sum\n  dimensions:\n  - seller\nprinciples:\n- name: Visibility\n  description: Pull provider invoices or usage exports until a self-serve usage feed is documented.\n- name: Allocation\n  description: Tag invoice line items to consuming business units in your FinOps store.\n- name: Optimization\n  description: Levers depend on the provider's billing model; review at renewal once reconciled.\n- name: Accountability\n  description: Assign a contract owner to review billing against negotiated terms.\nmaintainers:\n- FN: Kin Lane\n  email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/mercari/refs/heads/main/finops/mercari-finops.yml
sources:
- https://www.mercari.com/
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Marketplace
- Resale
- P2P
- Ecommerce
- FinOps
- Cost Management
- FOCUS
---
