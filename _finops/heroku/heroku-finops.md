---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: heroku-platform-api.yml
  format: yaml
  label: Heroku Platform API
  slug: heroku-platform-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/heroku/refs/heads/main/openapi/heroku-platform-api.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  pricingCategory: Per-Dyno Subscription
description: FOCUS-aligned FinOps for Heroku.
focus_columns:
  BillingCurrency: USD
  ProviderName: Heroku
  PublisherName: Heroku
  ServiceCategory: Platform-as-a-Service
  ServiceName: Heroku
layout: finops
meters:
- aggregation: sum
  dimensions:
  - app
  - dyno_type
  name: dyno_hours
  unit: dyno-hour
- aggregation: max
  name: postgres_subscriptions
  unit: instance-month
- aggregation: max
  name: kv_subscriptions
  unit: instance-month
- aggregation: sum
  name: data_transfer
  unit: GB
- aggregation: max
  name: addon_subscriptions
  unit: addon-month
name: Heroku Finops
provider_name: Heroku
provider_slug: heroku
publisher_name: Heroku
service_category: Platform-as-a-Service
slug: heroku-finops
source_filename: heroku-finops.yml
source_heading: FinOps Profile
source_url: https://www.heroku.com/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Heroku\nproviderId: heroku\ncreated: '2026-05-04'\nmodified: '2026-05-04'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Platform-as-a-Service\ndescription: FOCUS-aligned FinOps for Heroku.\nsources:\n  - https://www.heroku.com/pricing\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Heroku\nserviceCategory: Platform-as-a-Service\nbillingModel:\n  pricingCategory: Per-Dyno Subscription\n  billingFrequency: Monthly\n  billingCurrency: USD\nfocusColumns:\n  ServiceName: Heroku\n  ServiceCategory: Platform-as-a-Service\n  ProviderName: Heroku\n  PublisherName: Heroku\n  BillingCurrency: USD\nmeters:\n  - name: dyno_hours\n    unit: dyno-hour\n    aggregation: sum\n    dimensions:\n\
  \      - app\n      - dyno_type\n  - name: postgres_subscriptions\n    unit: instance-month\n    aggregation: max\n  - name: kv_subscriptions\n    unit: instance-month\n    aggregation: max\n  - name: data_transfer\n    unit: GB\n    aggregation: sum\n  - name: addon_subscriptions\n    unit: addon-month\n    aggregation: max\nprinciples:\n  - name: Visibility\n    description: Track Heroku consumption monthly.\n  - name: Allocation\n    description: Tag usage to teams/cost centers.\n  - name: Optimization\n    description: Right-size; reclaim unused entitlements.\n  - name: Accountability\n    description: Set spend alerts; quarterly review.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/heroku/refs/heads/main/finops/heroku-finops.yml
sources:
- https://www.heroku.com/pricing
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Platform-as-a-Service
---
