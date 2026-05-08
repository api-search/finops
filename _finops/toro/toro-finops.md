---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: toro-horizon360-openapi.yml
  format: yaml
  label: Toro Horizon360
  slug: horizon360
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/toro/refs/heads/main/openapi/toro-horizon360-openapi.yml
- filename: toro-intellidash-openapi.yml
  format: yaml
  label: Toro IntelliDash
  slug: intellidash
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/toro/refs/heads/main/openapi/toro-intellidash-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Purchase
  - Tax
  - Adjustment
  - Refund
  pricingCategory: Tiered Subscription
description: 'FOCUS-aligned FinOps for Toro: monthly subscription (tiered by crew size) for the Horizon360 contractor SaaS, with other connected-product surfaces (IntelliDash, myTurf) sold via dealer channels without published list pricing. Cost allocation here is per Horizon360 subscription tier and crew capacity.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: The Toro Company
  PricingCategory: Subscription
  PricingUnit: month
  ProviderName: Toro
  PublisherName: The Toro Company
  ServiceCategory: Field Service SaaS
  ServiceName: Toro Horizon360
layout: finops
meters:
- aggregation: sum
  description: One month of a Horizon360 subscription on Essential, Basic, Premium, or Unlimited.
  dimensions:
  - tier
  - account
  name: horizon360_subscription_month
  unit: month
- aggregation: max
  description: Crew-member capacity associated with the active Horizon360 tier (1 / 5 / unlimited).
  dimensions:
  - tier
  - account
  name: horizon360_crew_capacity
  unit: seat
- aggregation: max
  description: Remaining days on a 30- or 60-day Horizon360 free trial.
  dimensions:
  - tier
  - account
  name: free_trial_days_remaining
  unit: day
name: Toro Finops
provider_name: Toro
provider_slug: toro
publisher_name: The Toro Company
service_category: Connected Products & Field Service SaaS
slug: toro-finops
source_filename: toro-finops.yml
source_heading: FinOps Profile
source_url: https://horizon360.toro.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Toro\nproviderId: toro\npublisherName: The Toro Company\nserviceCategory: Connected Products & Field Service SaaS\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - Landscaping\n  - Fleet Management\n  - Turf Management\n  - SaaS\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps for Toro: monthly subscription (tiered by crew size) for the Horizon360\n  contractor SaaS, with other connected-product surfaces (IntelliDash, myTurf) sold via dealer channels\n  without published list pricing. Cost allocation here is per Horizon360 subscription tier and crew capacity.'\nsources:\n  - https://horizon360.toro.com/\nbillingModel:\n\
  \  pricingCategory: Tiered Subscription\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Tax\n    - Adjustment\n    - Refund\nfocusColumns:\n  ServiceName: Toro Horizon360\n  ServiceCategory: Field Service SaaS\n  ProviderName: Toro\n  PublisherName: The Toro Company\n  InvoiceIssuerName: The Toro Company\n  BillingCurrency: USD\n  ChargeCategory: Purchase\n  PricingCategory: Subscription\n  PricingUnit: month\nmeters:\n  - name: horizon360_subscription_month\n    description: One month of a Horizon360 subscription on Essential, Basic, Premium, or Unlimited.\n    unit: month\n    aggregation: sum\n    dimensions:\n      - tier\n      - account\n  - name: horizon360_crew_capacity\n    description: Crew-member capacity associated with the active Horizon360 tier (1 / 5 / unlimited).\n    unit: seat\n    aggregation: max\n    dimensions:\n      - tier\n      - account\n  - name: free_trial_days_remaining\n    description: Remaining days on a\
  \ 30- or 60-day Horizon360 free trial.\n    unit: day\n    aggregation: max\n    dimensions:\n      - tier\n      - account\nprinciples:\n  - name: Visibility\n    description: Use the Horizon360 account console to see the active tier, billing date, and crew utilization;\n      no separate usage API is published.\n  - name: Allocation\n    description: For multi-business contractors, attribute Horizon360 subscriptions per account/legal\n      entity since seats are bound to the account rather than itemized per project.\n  - name: Optimization\n    description: Right-size by tier — Essential is free for solo operators, Premium covers up to 5 crew\n      members, and Unlimited only earns its cost above 5 active crew. Use the 30/60-day free trials before\n      committing.\n  - name: Accountability\n    description: Assign a single Horizon360 account owner per business; review the tier monthly against\n      actual crew count and trial expiry.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/toro/refs/heads/main/finops/toro-finops.yml
sources:
- https://horizon360.toro.com/
specification: FinOps Framework
tags:
- Landscaping
- Fleet Management
- Turf Management
- SaaS
- FinOps
- FOCUS
---
