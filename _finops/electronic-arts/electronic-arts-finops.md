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
  - Tax
  - Refund
  pricingCategory: Subscription
description: FOCUS-aligned FinOps shell for Electronic Arts; the only visible commercial billing is the consumer EA Play subscription. There is no developer API to allocate against.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Electronic Arts Inc.
  ProviderName: Electronic Arts
  PublisherName: Electronic Arts Inc.
  ServiceCategory: Entertainment / Subscription
  ServiceName: EA Play
layout: finops
meters:
- aggregation: sum
  dimensions:
  - tier
  - country
  name: subscription_seats
  unit: seat
- aggregation: sum
  dimensions:
  - title
  - country
  name: in_game_purchases
  unit: transaction
name: Electronic Arts Finops
provider_name: Electronic Arts
provider_slug: electronic-arts
publisher_name: Electronic Arts Inc.
service_category: Entertainment
slug: electronic-arts-finops
source_filename: electronic-arts-finops.yml
source_heading: FinOps Profile
source_url: https://www.ea.com/ea-play
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Electronic Arts\nproviderId: electronic-arts\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Gaming\n  - Entertainment\ndescription: 'FOCUS-aligned FinOps shell for Electronic Arts; the only visible commercial billing is\n  the consumer EA Play subscription. There is no developer API to allocate against.'\nnotes: EA does not expose a public developer API. Meters and FOCUS columns describe expected consumer\n  subscription billing only.\nsources:\n  - https://www.ea.com/ea-play\n  - https://www.ea.com\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Electronic Arts Inc.\nserviceCategory: Entertainment\nbillingModel:\n  pricingCategory:\
  \ Subscription\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Tax\n    - Refund\nfocusColumns:\n  ServiceName: EA Play\n  ServiceCategory: Entertainment / Subscription\n  ProviderName: Electronic Arts\n  PublisherName: Electronic Arts Inc.\n  InvoiceIssuerName: Electronic Arts Inc.\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: subscription_seats\n    unit: seat\n    aggregation: sum\n    dimensions:\n      - tier\n      - country\n  - name: in_game_purchases\n    unit: transaction\n    aggregation: sum\n    dimensions:\n      - title\n      - country\nprinciples:\n  - name: Visibility\n    description: Pull EA account billing history; no telemetry API for organizations.\n  - name: Allocation\n    description: For business deployments, allocate EA Play seat costs to the specific cost-center.\n  - name: Optimization\n    description: Annual billing is cheaper per month than monthly; right-size to active employee\
  \ gamers.\n  - name: Accountability\n    description: HR/IT (for corporate Play perks) reviews seat utilization quarterly.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/electronic-arts/refs/heads/main/finops/electronic-arts-finops.yml
sources:
- https://www.ea.com/ea-play
- https://www.ea.com
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Gaming
- Entertainment
---
