---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: lemon-squeezy-api-openapi.yml
  format: yaml
  label: Lemon Squeezy API
  slug: lemon-squeezy-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/lemon-squeezy/refs/heads/main/openapi/lemon-squeezy-api-openapi.yml
- filename: lemon-squeezy-license-api-openapi.yml
  format: yaml
  label: Lemon Squeezy License API
  slug: lemon-squeezy-license-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/lemon-squeezy/refs/heads/main/openapi/lemon-squeezy-license-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  pricingCategory: Per-Transaction Take Rate
description: FOCUS-aligned FinOps for Lemon Squeezy.
focus_columns:
  BillingCurrency: USD
  ProviderName: Lemon Squeezy
  PublisherName: Lemon Squeezy
  ServiceCategory: Merchant of Record / Payments
  ServiceName: Lemon Squeezy
layout: finops
meters:
- aggregation: sum
  dimensions:
  - product
  - currency
  - country
  name: transactions
  unit: transaction
- aggregation: sum
  name: transaction_volume
  unit: USD
- aggregation: sum
  name: subscription_renewals
  unit: renewal
- aggregation: sum
  name: abandoned_cart_recoveries
  unit: recovery
- aggregation: sum
  name: affiliate_referrals
  unit: referral
name: Lemon Squeezy Finops
provider_name: Lemon Squeezy
provider_slug: lemon-squeezy
publisher_name: Lemon Squeezy
service_category: Merchant of Record / Payments
slug: lemon-squeezy-finops
source_filename: lemon-squeezy-finops.yml
source_heading: FinOps Profile
source_url: https://www.lemonsqueezy.com/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Lemon Squeezy\nproviderId: lemon-squeezy\ncreated: '2026-05-04'\nmodified: '2026-05-04'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Merchant of Record / Payments\ndescription: FOCUS-aligned FinOps for Lemon Squeezy.\nsources:\n  - https://www.lemonsqueezy.com/pricing\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Lemon Squeezy\nserviceCategory: Merchant of Record / Payments\nbillingModel:\n  pricingCategory: Per-Transaction Take Rate\n  billingFrequency: Monthly\n  billingCurrency: USD\nfocusColumns:\n  ServiceName: Lemon Squeezy\n  ServiceCategory: Merchant of Record / Payments\n  ProviderName: Lemon Squeezy\n  PublisherName: Lemon Squeezy\n  BillingCurrency: USD\nmeters:\n\
  \  - name: transactions\n    unit: transaction\n    aggregation: sum\n    dimensions:\n      - product\n      - currency\n      - country\n  - name: transaction_volume\n    unit: USD\n    aggregation: sum\n  - name: subscription_renewals\n    unit: renewal\n    aggregation: sum\n  - name: abandoned_cart_recoveries\n    unit: recovery\n    aggregation: sum\n  - name: affiliate_referrals\n    unit: referral\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Track Lemon Squeezy consumption monthly.\n  - name: Allocation\n    description: Tag usage to teams/cost centers.\n  - name: Optimization\n    description: Right-size; reclaim unused entitlements.\n  - name: Accountability\n    description: Set spend alerts; quarterly review.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/lemon-squeezy/refs/heads/main/finops/lemon-squeezy-finops.yml
sources:
- https://www.lemonsqueezy.com/pricing
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Merchant of Record / Payments
---
