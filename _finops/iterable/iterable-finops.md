---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: iterable-rest-api-openapi.yml
  format: yaml
  label: Iterable REST API
  slug: rest-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/iterable/refs/heads/main/openapi/iterable-rest-api-openapi.yml
- filename: iterable-export-api-openapi.yml
  format: yaml
  label: Iterable Export API
  slug: export-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/iterable/refs/heads/main/openapi/iterable-export-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  pricingCategory: Per-MAU Annual Contract
description: FOCUS-aligned FinOps for Iterable.
focus_columns:
  BillingCurrency: USD
  ProviderName: Iterable
  PublisherName: Iterable
  ServiceCategory: Marketing Automation
  ServiceName: Iterable
layout: finops
meters:
- aggregation: max
  name: monthly_active_users
  unit: MAU
- aggregation: sum
  name: email_sends
  unit: email
- aggregation: sum
  name: sms_sends
  unit: segment
- aggregation: sum
  name: push_sends
  unit: notification
- aggregation: sum
  name: in_app_messages
  unit: message
name: Iterable Finops
provider_name: Iterable
provider_slug: iterable
publisher_name: Iterable
service_category: Marketing Automation
slug: iterable-finops
source_filename: iterable-finops.yml
source_heading: FinOps Profile
source_url: https://www.iterable.com/pricing/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Iterable\nproviderId: iterable\ncreated: '2026-05-04'\nmodified: '2026-05-04'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Marketing Automation\ndescription: FOCUS-aligned FinOps for Iterable.\nsources:\n  - https://www.iterable.com/pricing/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Iterable\nserviceCategory: Marketing Automation\nbillingModel:\n  pricingCategory: Per-MAU Annual Contract\n  billingFrequency: Monthly\n  billingCurrency: USD\nfocusColumns:\n  ServiceName: Iterable\n  ServiceCategory: Marketing Automation\n  ProviderName: Iterable\n  PublisherName: Iterable\n  BillingCurrency: USD\nmeters:\n  - name: monthly_active_users\n    unit: MAU\n    aggregation:\
  \ max\n  - name: email_sends\n    unit: email\n    aggregation: sum\n  - name: sms_sends\n    unit: segment\n    aggregation: sum\n  - name: push_sends\n    unit: notification\n    aggregation: sum\n  - name: in_app_messages\n    unit: message\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Track Iterable consumption monthly.\n  - name: Allocation\n    description: Tag usage to teams/cost centers.\n  - name: Optimization\n    description: Right-size; reclaim unused entitlements.\n  - name: Accountability\n    description: Set spend alerts; quarterly review.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/iterable/refs/heads/main/finops/iterable-finops.yml
sources:
- https://www.iterable.com/pricing/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Marketing Automation
---
