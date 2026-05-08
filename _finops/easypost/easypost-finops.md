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
  - Subscription
  - Usage
  - Purchase
  pricingCategory: Subscription + Usage
description: 'FOCUS-aligned FinOps profile for EasyPost. Cost lines are: (1) platform/subscription fee for BYOA, (2) per-label charges for non-Wallet carriers, (3) carrier postage cost for purchased rates (passed through), (4) Tracking per-shipment, (5) Insurance 1% of value (min $1), and (6) any Forge/GlobalShip subscription. Optimize by using EasyPost Wallet for low-volume / SMB workflows up to 3,000 labels/month, batching label buys, and reducing tracker creation for already-delivered shipments.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: EasyPost
  ProviderName: EasyPost
  PublisherName: EasyPost
  ServiceCategory: Shipping
  ServiceName: EasyPost
layout: finops
meters:
- aggregation: sum
  description: Shipping labels purchased (Wallet vs. BYOA).
  dimensions:
  - carrier
  - service
  - wallet_or_byoa
  name: labels_purchased
  unit: label
- aggregation: sum
  description: Tracker creations / scan events billed.
  dimensions:
  - tier
  name: tracking_events
  unit: shipment
- aggregation: sum
  description: Insurance fees (1% of value, $1 min).
  dimensions:
  - service
  name: insurance_charges
  unit: USD
- aggregation: sum
  description: Carrier postage cost passed through to the shipper.
  dimensions:
  - carrier
  - service
  name: postage_passthrough
  unit: USD
name: Easypost Finops
provider_name: EasyPost
provider_slug: easypost
publisher_name: EasyPost
service_category: Shipping API
slug: easypost-finops
source_filename: easypost-finops.yml
source_heading: FinOps Profile
source_url: https://www.easypost.com/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: EasyPost\nproviderId: easypost\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: true\ntags:\n- Shipping\n- Logistics\n- Multi-Carrier\n- Tracking\n- Labels\n- Insurance\n- FinOps\n- Cost Management\n- FOCUS\ndescription: >-\n  FOCUS-aligned FinOps profile for EasyPost. Cost lines are: (1) platform/subscription fee for BYOA,\n  (2) per-label charges for non-Wallet carriers, (3) carrier postage cost for purchased rates (passed\n  through), (4) Tracking per-shipment, (5) Insurance 1% of value (min $1), and (6) any\n  Forge/GlobalShip subscription. Optimize by using EasyPost Wallet for low-volume / SMB workflows up\n  to 3,000 labels/month, batching label buys, and reducing tracker creation for already-delivered\n  shipments.\nnotes: Multiple metered lines; postage is pass-through. Wallet free tier covers many SMB use cases.\nsources:\n- https://www.easypost.com/pricing\n\
  - https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: EasyPost\nserviceCategory: Shipping API\nbillingModel:\n  pricingCategory: Subscription + Usage\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n  - Subscription\n  - Usage\n  - Purchase\nfocusColumns:\n  ServiceName: EasyPost\n  ServiceCategory: Shipping\n  ProviderName: EasyPost\n  PublisherName: EasyPost\n  InvoiceIssuerName: EasyPost\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n- name: labels_purchased\n  description: Shipping labels purchased (Wallet vs. BYOA).\n  unit: label\n  aggregation: sum\n  dimensions:\n  - carrier\n  - service\n  - wallet_or_byoa\n- name: tracking_events\n  description: Tracker creations / scan events billed.\n  unit: shipment\n  aggregation:\
  \ sum\n  dimensions:\n  - tier\n- name: insurance_charges\n  description: Insurance fees (1% of value, $1 min).\n  unit: USD\n  aggregation: sum\n  dimensions:\n  - service\n- name: postage_passthrough\n  description: Carrier postage cost passed through to the shipper.\n  unit: USD\n  aggregation: sum\n  dimensions:\n  - carrier\n  - service\nprinciples:\n- name: Visibility\n  description: Pull EasyPost Reports API monthly; reconcile labels, tracking, insurance, and postage by carrier.\n- name: Allocation\n  description: Tag shipments with order/customer ID for chargeback to the originating brand.\n- name: Optimization\n  description: Use Wallet carriers under 3,000 labels/month; batch high-volume label creation; avoid duplicate Tracker creations.\n- name: Accountability\n  description: Logistics/ops team owns EasyPost contract; engineering owns API-key hygiene.\nmaintainers:\n- FN: Kin Lane\n  email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/easypost/refs/heads/main/finops/easypost-finops.yml
sources:
- https://www.easypost.com/pricing
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Shipping
- Logistics
- Multi-Carrier
- Tracking
- Labels
- Insurance
- FinOps
- Cost Management
- FOCUS
---
