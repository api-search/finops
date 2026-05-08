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
  pricingCategory: Hybrid
description: FOCUS-aligned FinOps profile. Tiered property SaaS plus payment processing.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Cloudbeds
  ProviderName: Cloudbeds
  PublisherName: Cloudbeds
  ServiceCategory: Hospitality
  ServiceName: Cloudbeds
layout: finops
meters:
- aggregation: sum
  description: Per-property monthly SaaS.
  dimensions:
  - account
  - property
  name: property_saas
  unit: property
- aggregation: sum
  description: Cloudbeds Payments processing volume.
  dimensions:
  - property
  name: payments_volume
  unit: USD
name: Cloudbeds Finops
provider_name: Cloudbeds
provider_slug: cloudbeds
publisher_name: Cloudbeds
service_category: Hospitality
slug: cloudbeds-finops
source_filename: cloudbeds-finops.yml
source_heading: FinOps Profile
source_url: https://www.cloudbeds.com/pricing/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Cloudbeds\nproviderId: cloudbeds\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: false\ntags:\n- Hospitality\n- Hotels\n- PMS\n- Property Management\n- FinOps\n- Cost Management\n- FOCUS\ndescription: FOCUS-aligned FinOps profile. Tiered property SaaS plus payment processing.\nnotes: Multi-currency billing.\nsources:\n- https://www.cloudbeds.com/pricing/\n- https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Cloudbeds\nserviceCategory: Hospitality\nbillingModel:\n  pricingCategory: Hybrid\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n  - Purchase\n  - Usage\n  - Adjustment\nfocusColumns:\n \
  \ ServiceName: Cloudbeds\n  ServiceCategory: Hospitality\n  ProviderName: Cloudbeds\n  PublisherName: Cloudbeds\n  InvoiceIssuerName: Cloudbeds\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n- name: property_saas\n  description: Per-property monthly SaaS.\n  unit: property\n  aggregation: sum\n  dimensions:\n  - account\n  - property\n- name: payments_volume\n  description: Cloudbeds Payments processing volume.\n  unit: USD\n  aggregation: sum\n  dimensions:\n  - property\nprinciples:\n- name: Visibility\n  description: Pull provider invoices or usage exports until a self-serve usage feed is documented.\n- name: Allocation\n  description: Tag invoice line items to consuming business units in your FinOps store.\n- name: Optimization\n  description: Levers depend on the provider's billing model; review at renewal once reconciled.\n- name: Accountability\n  description: Assign a contract owner to review billing against negotiated terms.\nmaintainers:\n- FN: Kin Lane\n  email:\
  \ kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/cloudbeds/refs/heads/main/finops/cloudbeds-finops.yml
sources:
- https://www.cloudbeds.com/pricing/
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Hospitality
- Hotels
- PMS
- Property Management
- FinOps
- Cost Management
- FOCUS
---
