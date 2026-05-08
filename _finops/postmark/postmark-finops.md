---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: postmark-api-openapi.yml
  format: yaml
  label: Postmark API
  slug: postmark-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/postmark/refs/heads/main/openapi/postmark-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  pricingCategory: Tiered Subscription by Volume
description: FOCUS-aligned FinOps for Postmark.
focus_columns:
  BillingCurrency: USD
  ProviderName: Postmark
  PublisherName: Postmark
  ServiceCategory: Transactional Email
  ServiceName: Postmark
layout: finops
meters:
- aggregation: sum
  dimensions:
  - server
  - stream
  name: emails_sent
  unit: email
- aggregation: max
  name: monthly_subscription
  unit: month
name: Postmark Finops
provider_name: Postmark
provider_slug: postmark
publisher_name: Postmark
service_category: Transactional Email
slug: postmark-finops
source_filename: postmark-finops.yml
source_heading: FinOps Profile
source_url: https://postmarkapp.com/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Postmark\nproviderId: postmark\ncreated: '2026-05-04'\nmodified: '2026-05-04'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Transactional Email\ndescription: FOCUS-aligned FinOps for Postmark.\nsources:\n  - https://postmarkapp.com/pricing\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Postmark\nserviceCategory: Transactional Email\nbillingModel:\n  pricingCategory: Tiered Subscription by Volume\n  billingFrequency: Monthly\n  billingCurrency: USD\nfocusColumns:\n  ServiceName: Postmark\n  ServiceCategory: Transactional Email\n  ProviderName: Postmark\n  PublisherName: Postmark\n  BillingCurrency: USD\nmeters:\n  - name: emails_sent\n    unit: email\n    aggregation: sum\n\
  \    dimensions:\n      - server\n      - stream\n  - name: monthly_subscription\n    unit: month\n    aggregation: max\nprinciples:\n  - name: Visibility\n    description: Track Postmark consumption monthly.\n  - name: Allocation\n    description: Tag usage to teams/cost centers.\n  - name: Optimization\n    description: Right-size; reclaim unused entitlements.\n  - name: Accountability\n    description: Set spend alerts; quarterly review.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/postmark/refs/heads/main/finops/postmark-finops.yml
sources:
- https://postmarkapp.com/pricing
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Transactional Email
---
