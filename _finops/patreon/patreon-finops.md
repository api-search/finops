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
  - Usage
  - Tax
  - Adjustment
  pricingCategory: Revenue Share
description: FOCUS-aligned FinOps profile for Patreon's revenue-share creator pricing.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Patreon
  ProviderName: Patreon
  PublisherName: Patreon
  ServiceCategory: Creator Economy
  ServiceName: Patreon Creator Platform
layout: finops
meters:
- aggregation: sum
  description: 10% of creator earnings.
  dimensions:
  - campaign
  - currency
  name: platform_fee
  unit: percent_of_earnings
- aggregation: sum
  description: Stripe/PayPal-style processing fees on member charges.
  dimensions:
  - payment_method
  - currency
  name: payment_processing_fee
  unit: percent_plus_fixed
- aggregation: sum
  description: Foreign-exchange fee on cross-currency payouts.
  dimensions:
  - source_currency
  - target_currency
  name: currency_conversion_fee
  unit: percent
- aggregation: sum
  description: Per-payout transfer fee.
  dimensions:
  - payout_method
  name: payout_fee
  unit: fixed
name: Patreon Finops
provider_name: Patreon
provider_slug: patreon
publisher_name: Patreon
service_category: Creator Economy
slug: patreon-finops
source_filename: patreon-finops.yml
source_heading: FinOps Profile
source_url: https://www.patreon.com/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Patreon\nproviderId: patreon\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: true\ntags:\n- Creator Economy\n- Membership\n- FinOps\n- Cost Management\n- FOCUS\ndescription: FOCUS-aligned FinOps profile for Patreon's revenue-share creator pricing.\nnotes: >-\n  Patreon's billing model is revenue-based — creators pay a 10% platform fee on income\n  earned plus payment processing, currency conversion, payout, and applicable tax fees.\n  There is no per-call API charge.\nsources:\n- https://www.patreon.com/pricing\n- https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Patreon\nserviceCategory: Creator Economy\nbillingModel:\n\
  \  pricingCategory: Revenue Share\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n  - Usage\n  - Tax\n  - Adjustment\nfocusColumns:\n  ServiceName: Patreon Creator Platform\n  ServiceCategory: Creator Economy\n  ProviderName: Patreon\n  PublisherName: Patreon\n  InvoiceIssuerName: Patreon\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n- name: platform_fee\n  description: 10% of creator earnings.\n  unit: percent_of_earnings\n  aggregation: sum\n  dimensions:\n  - campaign\n  - currency\n- name: payment_processing_fee\n  description: Stripe/PayPal-style processing fees on member charges.\n  unit: percent_plus_fixed\n  aggregation: sum\n  dimensions:\n  - payment_method\n  - currency\n- name: currency_conversion_fee\n  description: Foreign-exchange fee on cross-currency payouts.\n  unit: percent\n  aggregation: sum\n  dimensions:\n  - source_currency\n  - target_currency\n- name: payout_fee\n  description: Per-payout transfer fee.\n  unit: fixed\n \
  \ aggregation: sum\n  dimensions:\n  - payout_method\nprinciples:\n- name: Visibility\n  description: Pull monthly creator earnings and fee statements; correlate with platform fee, processing, FX, and payout meters.\n- name: Allocation\n  description: Allocate fees to specific campaigns, tiers, and currencies for clear unit economics.\n- name: Optimization\n  description: Optimize payout cadence and member-side payment methods to minimize processing and FX fees.\n- name: Accountability\n  description: Assign a creator-finance owner to reconcile Patreon statements against ledger revenue.\nmaintainers:\n- FN: Kin Lane\n  email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/patreon/refs/heads/main/finops/patreon-finops.yml
sources:
- https://www.patreon.com/pricing
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Creator Economy
- Membership
- FinOps
- Cost Management
- FOCUS
---
