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
  - Adjustment
  pricingCategory: Subscription with MAU Allowance
description: FinOps view of PubNub. MAU-only billing model. Cost forecast hinges on accurately predicting Monthly Active Users; messages, channels, and storage within tier are bundled. Unlike competitors, peak concurrent connections do not generate separate cost.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Subscription
  InvoiceIssuerName: PubNub
  ProviderName: PubNub
  PublisherName: PubNub
  ServiceCategory: Realtime Infrastructure
  ServiceName: PubNub Realtime
layout: finops
meters:
- aggregation: sum
  description: Monthly subscription per keyset; tier sets MAU allowance.
  dimensions:
  - keyset
  name: subscription
  unit: month
- aggregation: count_distinct
  description: Monthly Active Users (distinct UUIDs in the period).
  dimensions:
  - keyset
  name: mau
  unit: user_month
name: Pubnub Finops
provider_name: PubNub
provider_slug: pubnub
publisher_name: PubNub
service_category: Realtime Infrastructure
slug: pubnub-finops
source_filename: pubnub-finops.yml
source_heading: FinOps Profile
source_url: https://www.pubnub.com/pricing/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: PubNub\nproviderId: pubnub\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: true\ntags:\n  - Realtime\n  - FinOps\n  - FOCUS\ndescription: >-\n  FinOps view of PubNub. MAU-only billing model. Cost forecast hinges on accurately predicting\n  Monthly Active Users; messages, channels, and storage within tier are bundled. Unlike\n  competitors, peak concurrent connections do not generate separate cost.\nsources:\n  - https://www.pubnub.com/pricing/\n  - https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: PubNub\nserviceCategory: Realtime Infrastructure\nbillingModel:\n  pricingCategory: Subscription with MAU Allowance\n  billingFrequency:\
  \ Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Subscription\n    - Adjustment\nfocusColumns:\n  ServiceName: PubNub Realtime\n  ServiceCategory: Realtime Infrastructure\n  ProviderName: PubNub\n  PublisherName: PubNub\n  InvoiceIssuerName: PubNub\n  BillingCurrency: USD\n  ChargeCategory: Subscription\nmeters:\n  - name: subscription\n    description: Monthly subscription per keyset; tier sets MAU allowance.\n    unit: month\n    aggregation: sum\n    dimensions:\n      - keyset\n  - name: mau\n    description: Monthly Active Users (distinct UUIDs in the period).\n    unit: user_month\n    aggregation: count_distinct\n    dimensions:\n      - keyset\nprinciples:\n  - name: Visibility\n    description: Track distinct PubNub UUIDs per month per keyset; map to product.\n  - name: Allocation\n    description: Allocate by keyset and product line.\n  - name: Optimization\n    description: De-duplicate UUIDs across products; reuse a single keyset where possible to amortize MAU\
  \ floor.\n  - name: Accountability\n    description: Assign a billing owner per keyset; review at renewal.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/pubnub/refs/heads/main/finops/pubnub-finops.yml
sources:
- https://www.pubnub.com/pricing/
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Realtime
- FinOps
- FOCUS
---
