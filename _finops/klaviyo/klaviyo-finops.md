---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: klaviyo-openapi.json
  format: json
  label: Klaviyo API
  slug: klaviyo-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/klaviyo/refs/heads/main/openapi/klaviyo-openapi.json
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  pricingCategory: Tiered by Profile Count + SMS Credits
description: FOCUS-aligned FinOps for Klaviyo.
focus_columns:
  BillingCurrency: USD
  ProviderName: Klaviyo
  PublisherName: Klaviyo
  ServiceCategory: Marketing Automation
  ServiceName: Klaviyo
layout: finops
meters:
- aggregation: max
  name: active_profiles
  unit: profile
- aggregation: sum
  name: email_sends
  unit: email
- aggregation: sum
  name: sms_credits_used
  unit: credit
- aggregation: sum
  name: mobile_push_sends
  unit: push
name: Klaviyo Finops
provider_name: Klaviyo
provider_slug: klaviyo
publisher_name: Klaviyo
service_category: Marketing Automation
slug: klaviyo-finops
source_filename: klaviyo-finops.yml
source_heading: FinOps Profile
source_url: https://www.klaviyo.com/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Klaviyo\nproviderId: klaviyo\ncreated: '2026-05-04'\nmodified: '2026-05-04'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Marketing Automation\ndescription: FOCUS-aligned FinOps for Klaviyo.\nsources:\n  - https://www.klaviyo.com/pricing\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Klaviyo\nserviceCategory: Marketing Automation\nbillingModel:\n  pricingCategory: Tiered by Profile Count + SMS Credits\n  billingFrequency: Monthly\n  billingCurrency: USD\nfocusColumns:\n  ServiceName: Klaviyo\n  ServiceCategory: Marketing Automation\n  ProviderName: Klaviyo\n  PublisherName: Klaviyo\n  BillingCurrency: USD\nmeters:\n  - name: active_profiles\n    unit: profile\n    aggregation:\
  \ max\n  - name: email_sends\n    unit: email\n    aggregation: sum\n  - name: sms_credits_used\n    unit: credit\n    aggregation: sum\n  - name: mobile_push_sends\n    unit: push\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Track Klaviyo consumption monthly via admin/billing exports.\n  - name: Allocation\n    description: Tag seats/usage to teams or cost centers for chargeback.\n  - name: Optimization\n    description: Right-size tier and seat count quarterly; reclaim inactive seats.\n  - name: Accountability\n    description: Set spend alerts and renew at observed active utilization.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/klaviyo/refs/heads/main/finops/klaviyo-finops.yml
sources:
- https://www.klaviyo.com/pricing
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Marketing Automation
---
