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
description: FOCUS-aligned FinOps profile. Sellers pay selling fees on GMV; developers pay nothing for API access (free).
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Reverb
  ProviderName: Reverb
  PublisherName: Reverb
  ServiceCategory: Marketplace
  ServiceName: Reverb
layout: finops
meters:
- aggregation: sum
  description: Per-sale Reverb selling fee.
  dimensions:
  - seller
  name: selling_fee
  unit: USD
- aggregation: sum
  description: Payment processing on completed sales.
  dimensions:
  - seller
  name: payment_processing
  unit: USD
name: Reverb Finops
provider_name: Reverb
provider_slug: reverb
publisher_name: Reverb
service_category: Marketplace
slug: reverb-finops
source_filename: reverb-finops.yml
source_heading: FinOps Profile
source_url: https://reverb.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Reverb\nproviderId: reverb\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: false\ntags:\n- Marketplace\n- Music\n- Instruments\n- Ecommerce\n- FinOps\n- Cost Management\n- FOCUS\ndescription: FOCUS-aligned FinOps profile. Sellers pay selling fees on GMV; developers pay nothing for\n  API access (free).\nnotes: Owned by Etsy; broader Etsy seller economics may apply.\nsources:\n- https://reverb.com/\n- https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Reverb\nserviceCategory: Marketplace\nbillingModel:\n  pricingCategory: Commission\n  billingFrequency: Per Transaction\n  billingCurrency: USD\n  chargeCategories:\n  - Usage\n\
  \  - Adjustment\nfocusColumns:\n  ServiceName: Reverb\n  ServiceCategory: Marketplace\n  ProviderName: Reverb\n  PublisherName: Reverb\n  InvoiceIssuerName: Reverb\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n- name: selling_fee\n  description: Per-sale Reverb selling fee.\n  unit: USD\n  aggregation: sum\n  dimensions:\n  - seller\n- name: payment_processing\n  description: Payment processing on completed sales.\n  unit: USD\n  aggregation: sum\n  dimensions:\n  - seller\nprinciples:\n- name: Visibility\n  description: Pull provider invoices or usage exports until a self-serve usage feed is documented.\n- name: Allocation\n  description: Tag invoice line items to consuming business units in your FinOps store.\n- name: Optimization\n  description: Levers depend on the provider's billing model; review at renewal once reconciled.\n- name: Accountability\n  description: Assign a contract owner to review billing against negotiated terms.\nmaintainers:\n- FN: Kin Lane\n  email:\
  \ kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/reverb/refs/heads/main/finops/reverb-finops.yml
sources:
- https://reverb.com/
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Marketplace
- Music
- Instruments
- Ecommerce
- FinOps
- Cost Management
- FOCUS
---
