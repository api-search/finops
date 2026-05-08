---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: braze-openapi.yml
  format: yaml
  label: Braze REST API
  slug: braze
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/braze/refs/heads/main/openapi/braze-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  pricingCategory: Custom Enterprise (MAU + Channels)
description: FOCUS-aligned FinOps for Braze.
focus_columns:
  BillingCurrency: USD
  ProviderName: Braze
  PublisherName: Braze
  ServiceCategory: Customer Engagement
  ServiceName: Braze
layout: finops
meters:
- aggregation: max
  name: monthly_active_users
  unit: MAU
- aggregation: sum
  dimensions:
  - channel
  - campaign
  name: messages_sent
  unit: message
- aggregation: sum
  name: sms_segments
  unit: segment
- aggregation: sum
  name: ai_credits
  unit: credit
name: Braze Finops
provider_name: Braze
provider_slug: braze
publisher_name: Braze
service_category: Customer Engagement
slug: braze-finops
source_filename: braze-finops.yml
source_heading: FinOps Profile
source_url: https://www.braze.com/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Braze\nproviderId: braze\ncreated: '2026-05-04'\nmodified: '2026-05-04'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Customer Engagement\ndescription: FOCUS-aligned FinOps for Braze.\nsources:\n  - https://www.braze.com/pricing\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Braze\nserviceCategory: Customer Engagement\nbillingModel:\n  pricingCategory: Custom Enterprise (MAU + Channels)\n  billingFrequency: Monthly\n  billingCurrency: USD\nfocusColumns:\n  ServiceName: Braze\n  ServiceCategory: Customer Engagement\n  ProviderName: Braze\n  PublisherName: Braze\n  BillingCurrency: USD\nmeters:\n  - name: monthly_active_users\n    unit: MAU\n    aggregation: max\n  - name:\
  \ messages_sent\n    unit: message\n    aggregation: sum\n    dimensions:\n      - channel\n      - campaign\n  - name: sms_segments\n    unit: segment\n    aggregation: sum\n  - name: ai_credits\n    unit: credit\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Track Braze consumption monthly.\n  - name: Allocation\n    description: Tag usage to teams/cost centers.\n  - name: Optimization\n    description: Right-size tier; reclaim unused entitlements.\n  - name: Accountability\n    description: Set spend alerts; quarterly review.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/braze/refs/heads/main/finops/braze-finops.yml
sources:
- https://www.braze.com/pricing
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Customer Engagement
---
