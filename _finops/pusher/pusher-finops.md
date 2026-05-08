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
  pricingCategory: Subscription
description: FinOps view of Pusher. Subscription-only billing per Channels app at the chosen tier; daily cap and connection cap define the tier. Beams subscription is separate, billed by monthly active devices.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Subscription
  InvoiceIssuerName: Pusher
  ProviderName: Pusher
  PublisherName: Pusher (MessageBird/Bird)
  ServiceCategory: Realtime Infrastructure
  ServiceName: Pusher Channels and Beams
layout: finops
meters:
- aggregation: sum
  description: Monthly Channels app subscription.
  dimensions:
  - app
  name: channels_subscription
  unit: month
- aggregation: sum
  description: Monthly Beams instance subscription (by MAU).
  dimensions:
  - instance
  name: beams_subscription
  unit: month
name: Pusher Finops
provider_name: Pusher
provider_slug: pusher
publisher_name: Pusher (MessageBird/Bird)
service_category: Realtime Infrastructure
slug: pusher-finops
source_filename: pusher-finops.yml
source_heading: FinOps Profile
source_url: https://pusher.com/channels/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Pusher\nproviderId: pusher\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: true\ntags:\n  - Realtime\n  - FinOps\n  - FOCUS\ndescription: >-\n  FinOps view of Pusher. Subscription-only billing per Channels app at the chosen tier; daily\n  cap and connection cap define the tier. Beams subscription is separate, billed by monthly\n  active devices.\nsources:\n  - https://pusher.com/channels/pricing\n  - https://pusher.com/beams/pricing\n  - https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Pusher (MessageBird/Bird)\nserviceCategory: Realtime Infrastructure\nbillingModel:\n  pricingCategory: Subscription\n  billingFrequency:\
  \ Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Subscription\nfocusColumns:\n  ServiceName: Pusher Channels and Beams\n  ServiceCategory: Realtime Infrastructure\n  ProviderName: Pusher\n  PublisherName: Pusher (MessageBird/Bird)\n  InvoiceIssuerName: Pusher\n  BillingCurrency: USD\n  ChargeCategory: Subscription\nmeters:\n  - name: channels_subscription\n    description: Monthly Channels app subscription.\n    unit: month\n    aggregation: sum\n    dimensions:\n      - app\n  - name: beams_subscription\n    description: Monthly Beams instance subscription (by MAU).\n    unit: month\n    aggregation: sum\n    dimensions:\n      - instance\nprinciples:\n  - name: Visibility\n    description: Pull Pusher daily message and connection telemetry into FinOps store.\n  - name: Allocation\n    description: One Pusher app per consuming product or environment.\n  - name: Optimization\n    description: Right-size between tiers based on measured peak day; downgrade when below cap consistently.\n\
  \  - name: Accountability\n    description: Assign a billing owner per app; review at renewal.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/pusher/refs/heads/main/finops/pusher-finops.yml
sources:
- https://pusher.com/channels/pricing
- https://pusher.com/beams/pricing
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Realtime
- FinOps
- FOCUS
---
