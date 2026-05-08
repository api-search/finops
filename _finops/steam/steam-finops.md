---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly Payouts; One-Time Submission Fees
  billingTerm: Per Steam Distribution Agreement
  chargeCategories:
  - Purchase
  - Adjustment
  - Tax
  commitmentDiscount: Graduated revenue-share tiers based on lifetime gross sales.
  pricingCategory: One-Time Submission Fee + Revenue Share (Payouts)
description: 'Steam''s billing surface is unusual relative to typical SaaS. Valve does not invoice Steamworks customers a per-call API fee. Instead, the relationship inverts — Valve disburses revenue to publishers (revenue share, after refunds, chargebacks, and applicable taxes) and charges a one-time non-refundable $100 USD Steam Direct submission fee per product. Charges (in the typical FinOps direction) appear only as the Steam Direct fee plus any Steamworks-specific publisher costs (e.g., physical shipping for keys, Steam Marketplace transaction fees borne by buyers, currency-conversion deltas). For a buyer the relationship is also unusual: end-users prepay a Steam Wallet balance which is then drawn down on store purchases. For a publisher''s accounting, the FinOps surface is fundamentally a payouts surface, not an expense surface.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Valve Corporation
  PricingCategory: Standard Pricing
  ProviderName: Valve Corporation
  PublisherName: Valve Corporation
  ServiceCategory: Gaming Distribution
  ServiceName: Steam (Steamworks)
layout: finops
meters:
- aggregation: count
  description: Per-product submission fees ($100 each, recoupable after $1K adjusted gross revenue).
  dimensions:
  - publisher
  - product
  name: steam_direct_submissions
  unit: product
- aggregation: sum
  description: Gross sales attributed to the 30% revenue-share tier (first $10M lifetime).
  dimensions:
  - publisher
  - product
  - country
  name: revenue_share_tier_1
  unit: usd
- aggregation: sum
  description: Gross sales attributed to the 25% revenue-share tier ($10M-$50M lifetime).
  dimensions:
  - publisher
  - product
  - country
  name: revenue_share_tier_2
  unit: usd
- aggregation: sum
  description: Gross sales attributed to the 20% revenue-share tier (above $50M lifetime).
  dimensions:
  - publisher
  - product
  - country
  name: revenue_share_tier_3
  unit: usd
- aggregation: sum
  description: Customer refunds netted against publisher payouts.
  dimensions:
  - publisher
  - product
  - reason
  name: refunds
  unit: usd
- aggregation: sum
  description: Card-network chargebacks netted against publisher payouts.
  dimensions:
  - publisher
  - product
  name: chargebacks
  unit: usd
- aggregation: sum
  description: Steam Marketplace transaction fees deducted from item-trade proceeds.
  dimensions:
  - publisher
  - product
  - market
  name: marketplace_transaction_fees
  unit: usd
- aggregation: sum
  description: Steamworks Web API call volume (no monetary cost; tracked for soft-quota management).
  dimensions:
  - api_key
  - interface
  - method
  name: api_calls
  unit: call
name: Steam Finops
provider_name: Steam
provider_slug: steam
publisher_name: Valve Corporation
service_category: Gaming Distribution
slug: steam-finops
source_filename: steam-finops.yml
source_heading: FinOps Profile
source_url: https://partner.steamgames.com/steamdirect
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Steam\nproviderId: steam\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: true\ntags:\n  - Gaming\n  - Valve\n  - Steamworks\n  - Distribution\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: >-\n  Steam's billing surface is unusual relative to typical SaaS. Valve does not invoice Steamworks customers a per-call API fee. Instead, the relationship inverts — Valve disburses revenue to publishers (revenue share, after refunds, chargebacks, and applicable taxes) and charges a one-time non-refundable $100 USD Steam Direct submission fee per product. Charges (in the typical FinOps direction) appear only as the Steam Direct fee plus any Steamworks-specific publisher costs (e.g., physical shipping for keys, Steam Marketplace transaction fees borne by buyers, currency-conversion deltas). For a buyer the relationship is also unusual: end-users prepay\
  \ a Steam Wallet balance which is then drawn down on store purchases. For a publisher's accounting, the FinOps surface is fundamentally a payouts surface, not an expense surface.\nnotes: >-\n  Reconciled at the model level on 2026-05-08. This artifact deliberately models Steam from the publisher / partner perspective because that is the side with developer-API obligations. Adjust focusColumns interpretation if profiling Steam from the buyer or end-user perspective.\nsources:\n  - https://partner.steamgames.com/steamdirect\n  - https://partner.steamgames.com/doc/webapi\n  - https://store.steampowered.com/subscriber_agreement/\n  - https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Valve Corporation\nserviceCategory: Gaming Distribution\nbillingModel:\n  pricingCategory:\
  \ One-Time Submission Fee + Revenue Share (Payouts)\n  billingFrequency: Monthly Payouts; One-Time Submission Fees\n  billingTerm: Per Steam Distribution Agreement\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Adjustment\n    - Tax\n  commitmentDiscount: Graduated revenue-share tiers based on lifetime gross sales.\nfocusColumns:\n  ServiceName: Steam (Steamworks)\n  ServiceCategory: Gaming Distribution\n  ProviderName: Valve Corporation\n  PublisherName: Valve Corporation\n  InvoiceIssuerName: Valve Corporation\n  BillingCurrency: USD\n  ChargeCategory: Purchase\n  PricingCategory: Standard Pricing\nmeters:\n  - name: steam_direct_submissions\n    description: Per-product submission fees ($100 each, recoupable after $1K adjusted gross revenue).\n    unit: product\n    aggregation: count\n    dimensions:\n      - publisher\n      - product\n  - name: revenue_share_tier_1\n    description: Gross sales attributed to the 30% revenue-share tier (first $10M lifetime).\n\
  \    unit: usd\n    aggregation: sum\n    dimensions:\n      - publisher\n      - product\n      - country\n  - name: revenue_share_tier_2\n    description: Gross sales attributed to the 25% revenue-share tier ($10M-$50M lifetime).\n    unit: usd\n    aggregation: sum\n    dimensions:\n      - publisher\n      - product\n      - country\n  - name: revenue_share_tier_3\n    description: Gross sales attributed to the 20% revenue-share tier (above $50M lifetime).\n    unit: usd\n    aggregation: sum\n    dimensions:\n      - publisher\n      - product\n      - country\n  - name: refunds\n    description: Customer refunds netted against publisher payouts.\n    unit: usd\n    aggregation: sum\n    dimensions:\n      - publisher\n      - product\n      - reason\n  - name: chargebacks\n    description: Card-network chargebacks netted against publisher payouts.\n    unit: usd\n    aggregation: sum\n    dimensions:\n      - publisher\n      - product\n  - name: marketplace_transaction_fees\n  \
  \  description: Steam Marketplace transaction fees deducted from item-trade proceeds.\n    unit: usd\n    aggregation: sum\n    dimensions:\n      - publisher\n      - product\n      - market\n  - name: api_calls\n    description: Steamworks Web API call volume (no monetary cost; tracked for soft-quota management).\n    unit: call\n    aggregation: sum\n    dimensions:\n      - api_key\n      - interface\n      - method\nprinciples:\n  - name: Visibility\n    description: >-\n      Pull the monthly Steamworks revenue report and Steam Direct submission ledger. Reconcile each game's reported gross to your own analytics; track Steam Wallet net deductions (refunds, chargebacks, marketplace fees) line-by-line.\n  - name: Allocation\n    description: >-\n      Allocate Steam payouts and submission fees per product / studio / publisher entity in your finance system; track Web API call volume per API key for ops attribution.\n  - name: Optimization\n    description: >-\n      Use the Steamworks\
  \ discounting and bundle tooling deliberately; minimize refunds with clear store-page expectations; consider promotional Steam Sale calendar timing; recoup the $100 Steam Direct fee promptly by promoting first-week sales above $1K.\n  - name: Accountability\n    description: >-\n      Assign a Steamworks publisher account owner; monitor Steam Direct submission lifecycle, payout timeliness, and Web API key rotation; review the Steam Distribution Agreement at every renewal/amendment.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/steam/refs/heads/main/finops/steam-finops.yml
sources:
- https://partner.steamgames.com/steamdirect
- https://partner.steamgames.com/doc/webapi
- https://store.steampowered.com/subscriber_agreement/
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Gaming
- Valve
- Steamworks
- Distribution
- FinOps
- Cost Management
- FOCUS
---
