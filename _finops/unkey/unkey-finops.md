---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: unkey-openapi.yml
  format: yaml
  label: Unkey API
  slug: unkey-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/unkey/refs/heads/main/openapi/unkey-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  pricingCategory: Subscription + Usage Credits
description: FOCUS-aligned FinOps for Unkey.
focus_columns:
  BillingCurrency: USD
  ProviderName: Unkey
  PublisherName: Unkey
  ServiceCategory: API Management
  ServiceName: Unkey
layout: finops
meters:
- aggregation: sum
  name: compute_usage
  unit: vCPU-hour
- aggregation: sum
  name: memory_usage
  unit: GB-hour
- aggregation: sum
  name: egress
  unit: GB
- aggregation: sum
  name: ratelimit_evaluations
  unit: evaluation
- aggregation: sum
  name: key_verifications
  unit: verification
name: Unkey Finops
provider_name: Unkey
provider_slug: unkey
publisher_name: Unkey
service_category: API Management
slug: unkey-finops
source_filename: unkey-finops.yml
source_heading: FinOps Profile
source_url: https://www.unkey.com/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Unkey\nproviderId: unkey\ncreated: '2026-05-04'\nmodified: '2026-05-04'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - API Management\ndescription: FOCUS-aligned FinOps for Unkey.\nsources:\n  - https://www.unkey.com/pricing\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Unkey\nserviceCategory: API Management\nbillingModel:\n  pricingCategory: Subscription + Usage Credits\n  billingFrequency: Monthly\n  billingCurrency: USD\nfocusColumns:\n  ServiceName: Unkey\n  ServiceCategory: API Management\n  ProviderName: Unkey\n  PublisherName: Unkey\n  BillingCurrency: USD\nmeters:\n  - name: compute_usage\n    unit: vCPU-hour\n    aggregation: sum\n  - name: memory_usage\n    unit:\
  \ GB-hour\n    aggregation: sum\n  - name: egress\n    unit: GB\n    aggregation: sum\n  - name: ratelimit_evaluations\n    unit: evaluation\n    aggregation: sum\n  - name: key_verifications\n    unit: verification\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Track Unkey consumption monthly.\n  - name: Allocation\n    description: Tag usage to teams/cost centers.\n  - name: Optimization\n    description: Right-size; reclaim unused entitlements.\n  - name: Accountability\n    description: Set spend alerts; quarterly review.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/unkey/refs/heads/main/finops/unkey-finops.yml
sources:
- https://www.unkey.com/pricing
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- API Management
---
