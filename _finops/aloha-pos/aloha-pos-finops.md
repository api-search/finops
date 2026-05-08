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
description: FOCUS-aligned FinOps profile. Per-location restaurant SaaS plus payment processing.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Aloha POS
  ProviderName: Aloha POS
  PublisherName: Aloha POS
  ServiceCategory: Payments & POS
  ServiceName: Aloha POS
layout: finops
meters:
- aggregation: sum
  description: Per-location monthly SaaS.
  dimensions:
  - merchant
  - location
  name: per_location_saas
  unit: subscription
- aggregation: sum
  description: Card processing volume.
  dimensions:
  - merchant
  name: processing_volume
  unit: USD
name: Aloha Pos Finops
provider_name: Aloha POS
provider_slug: aloha-pos
publisher_name: Aloha POS
service_category: Payments & POS
slug: aloha-pos-finops
source_filename: aloha-pos-finops.yml
source_heading: FinOps Profile
source_url: https://www.ncrvoyix.com/restaurants/aloha-cloud
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Aloha POS\nproviderId: aloha-pos\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: false\ntags:\n- POS\n- Restaurant\n- Hospitality\n- NCR\n- FinOps\n- Cost Management\n- FOCUS\ndescription: FOCUS-aligned FinOps profile. Per-location restaurant SaaS plus payment processing.\nnotes: Hardware capex separate from SaaS opex.\nsources:\n- https://www.ncrvoyix.com/restaurants/aloha-cloud\n- https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Aloha POS\nserviceCategory: Payments & POS\nbillingModel:\n  pricingCategory: Subscription\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n  - Purchase\n  - Usage\n\
  \  - Adjustment\nfocusColumns:\n  ServiceName: Aloha POS\n  ServiceCategory: Payments & POS\n  ProviderName: Aloha POS\n  PublisherName: Aloha POS\n  InvoiceIssuerName: Aloha POS\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n- name: per_location_saas\n  description: Per-location monthly SaaS.\n  unit: subscription\n  aggregation: sum\n  dimensions:\n  - merchant\n  - location\n- name: processing_volume\n  description: Card processing volume.\n  unit: USD\n  aggregation: sum\n  dimensions:\n  - merchant\nprinciples:\n- name: Visibility\n  description: Pull provider invoices or usage exports until a self-serve usage feed is documented.\n- name: Allocation\n  description: Tag invoice line items to consuming business units in your FinOps store.\n- name: Optimization\n  description: Levers depend on the provider's billing model; review at renewal once reconciled.\n- name: Accountability\n  description: Assign a contract owner to review billing against negotiated terms.\nmaintainers:\n\
  - FN: Kin Lane\n  email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/aloha-pos/refs/heads/main/finops/aloha-pos-finops.yml
sources:
- https://www.ncrvoyix.com/restaurants/aloha-cloud
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- POS
- Restaurant
- Hospitality
- NCR
- FinOps
- Cost Management
- FOCUS
---
