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
description: FOCUS-aligned FinOps profile. Restaurants pay platform SaaS + per-cover network fees.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Resy
  ProviderName: Resy
  PublisherName: Resy
  ServiceCategory: Hospitality
  ServiceName: Resy
layout: finops
meters:
- aggregation: sum
  description: Monthly Resy OS subscription.
  dimensions:
  - restaurant
  name: platform_saas
  unit: subscription
- aggregation: sum
  description: Per-cover fees on Resy network bookings.
  dimensions:
  - restaurant
  name: network_covers
  unit: cover
name: Resy Finops
provider_name: Resy
provider_slug: resy
publisher_name: Resy
service_category: Hospitality
slug: resy-finops
source_filename: resy-finops.yml
source_heading: FinOps Profile
source_url: https://resy.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Resy\nproviderId: resy\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: false\ntags:\n- Hospitality\n- Reservations\n- Restaurants\n- FinOps\n- Cost Management\n- FOCUS\ndescription: FOCUS-aligned FinOps profile. Restaurants pay platform SaaS + per-cover network fees.\nnotes: Owned by American Express; cross-promo with Amex card holders.\nsources:\n- https://resy.com/\n- https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Resy\nserviceCategory: Hospitality\nbillingModel:\n  pricingCategory: Hybrid\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n  - Purchase\n  - Usage\n  - Adjustment\nfocusColumns:\n\
  \  ServiceName: Resy\n  ServiceCategory: Hospitality\n  ProviderName: Resy\n  PublisherName: Resy\n  InvoiceIssuerName: Resy\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n- name: platform_saas\n  description: Monthly Resy OS subscription.\n  unit: subscription\n  aggregation: sum\n  dimensions:\n  - restaurant\n- name: network_covers\n  description: Per-cover fees on Resy network bookings.\n  unit: cover\n  aggregation: sum\n  dimensions:\n  - restaurant\nprinciples:\n- name: Visibility\n  description: Pull provider invoices or usage exports until a self-serve usage feed is documented.\n- name: Allocation\n  description: Tag invoice line items to consuming business units in your FinOps store.\n- name: Optimization\n  description: Levers depend on the provider's billing model; review at renewal once reconciled.\n- name: Accountability\n  description: Assign a contract owner to review billing against negotiated terms.\nmaintainers:\n- FN: Kin Lane\n  email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/resy/refs/heads/main/finops/resy-finops.yml
sources:
- https://resy.com/
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Hospitality
- Reservations
- Restaurants
- FinOps
- Cost Management
- FOCUS
---
