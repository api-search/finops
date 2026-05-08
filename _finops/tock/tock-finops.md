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
description: FOCUS-aligned FinOps profile. Restaurant SaaS + ticket fees.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Tock
  ProviderName: Tock
  PublisherName: Tock
  ServiceCategory: Hospitality
  ServiceName: Tock
layout: finops
meters:
- aggregation: sum
  description: Monthly Tock subscription.
  dimensions:
  - restaurant
  name: monthly_saas
  unit: subscription
- aggregation: sum
  description: Per-ticket fee on ticketed events.
  dimensions:
  - restaurant
  name: per_ticket
  unit: ticket
name: Tock Finops
provider_name: Tock
provider_slug: tock
publisher_name: Tock
service_category: Hospitality
slug: tock-finops
source_filename: tock-finops.yml
source_heading: FinOps Profile
source_url: https://www.exploretock.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Tock\nproviderId: tock\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: false\ntags:\n- Hospitality\n- Reservations\n- Restaurants\n- Events\n- FinOps\n- Cost Management\n- FOCUS\ndescription: FOCUS-aligned FinOps profile. Restaurant SaaS + ticket fees.\nnotes: Owned by Squarespace; integrations may also surface in Squarespace billing.\nsources:\n- https://www.exploretock.com/\n- https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Tock\nserviceCategory: Hospitality\nbillingModel:\n  pricingCategory: Hybrid\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n  - Purchase\n  - Usage\n  - Adjustment\n\
  focusColumns:\n  ServiceName: Tock\n  ServiceCategory: Hospitality\n  ProviderName: Tock\n  PublisherName: Tock\n  InvoiceIssuerName: Tock\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n- name: monthly_saas\n  description: Monthly Tock subscription.\n  unit: subscription\n  aggregation: sum\n  dimensions:\n  - restaurant\n- name: per_ticket\n  description: Per-ticket fee on ticketed events.\n  unit: ticket\n  aggregation: sum\n  dimensions:\n  - restaurant\nprinciples:\n- name: Visibility\n  description: Pull provider invoices or usage exports until a self-serve usage feed is documented.\n- name: Allocation\n  description: Tag invoice line items to consuming business units in your FinOps store.\n- name: Optimization\n  description: Levers depend on the provider's billing model; review at renewal once reconciled.\n- name: Accountability\n  description: Assign a contract owner to review billing against negotiated terms.\nmaintainers:\n- FN: Kin Lane\n  email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/tock/refs/heads/main/finops/tock-finops.yml
sources:
- https://www.exploretock.com/
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Hospitality
- Reservations
- Restaurants
- Events
- FinOps
- Cost Management
- FOCUS
---
