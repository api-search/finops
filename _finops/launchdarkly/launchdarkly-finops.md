---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: launchdarkly-rest-api-openapi.yml
  format: yaml
  label: LaunchDarkly REST API
  slug: rest-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/launchdarkly/refs/heads/main/openapi/launchdarkly-rest-api-openapi.yml
- filename: launchdarkly-webhooks-asyncapi.yml
  format: yaml
  label: LaunchDarkly Webhooks API
  slug: webhooks-api
  spec_type: AsyncAPI
  url: https://raw.githubusercontent.com/api-evangelist/launchdarkly/refs/heads/main/asyncapi/launchdarkly-webhooks-asyncapi.yml
- filename: launchdarkly-relay-proxy-openapi.yml
  format: yaml
  label: LaunchDarkly Relay Proxy
  slug: relay-proxy
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/launchdarkly/refs/heads/main/openapi/launchdarkly-relay-proxy-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  pricingCategory: Per-Service-Connection + Per-MAU
description: FOCUS-aligned FinOps for LaunchDarkly.
focus_columns:
  BillingCurrency: USD
  ProviderName: LaunchDarkly
  PublisherName: LaunchDarkly
  ServiceCategory: Feature Management
  ServiceName: LaunchDarkly
layout: finops
meters:
- aggregation: max
  name: service_connections
  unit: connection-month
- aggregation: max
  name: client_side_mau
  unit: MAU
- aggregation: sum
  name: flag_evaluations
  unit: evaluation
- aggregation: sum
  name: session_replays
  unit: replay
- aggregation: sum
  name: errors
  unit: error
- aggregation: sum
  name: logs_and_traces
  unit: GB
name: Launchdarkly Finops
provider_name: launchdarkly
provider_slug: launchdarkly
publisher_name: LaunchDarkly
service_category: Feature Management
slug: launchdarkly-finops
source_filename: launchdarkly-finops.yml
source_heading: FinOps Profile
source_url: https://launchdarkly.com/pricing/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: LaunchDarkly\nproviderId: launchdarkly\ncreated: '2026-05-04'\nmodified: '2026-05-04'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Feature Management\ndescription: FOCUS-aligned FinOps for LaunchDarkly.\nsources:\n  - https://launchdarkly.com/pricing/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: LaunchDarkly\nserviceCategory: Feature Management\nbillingModel:\n  pricingCategory: Per-Service-Connection + Per-MAU\n  billingFrequency: Monthly\n  billingCurrency: USD\nfocusColumns:\n  ServiceName: LaunchDarkly\n  ServiceCategory: Feature Management\n  ProviderName: LaunchDarkly\n  PublisherName: LaunchDarkly\n  BillingCurrency: USD\nmeters:\n  - name: service_connections\n\
  \    unit: connection-month\n    aggregation: max\n  - name: client_side_mau\n    unit: MAU\n    aggregation: max\n  - name: flag_evaluations\n    unit: evaluation\n    aggregation: sum\n  - name: session_replays\n    unit: replay\n    aggregation: sum\n  - name: errors\n    unit: error\n    aggregation: sum\n  - name: logs_and_traces\n    unit: GB\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Track LaunchDarkly consumption monthly.\n  - name: Allocation\n    description: Tag usage to teams/cost centers.\n  - name: Optimization\n    description: Right-size; reclaim unused entitlements.\n  - name: Accountability\n    description: Set spend alerts; quarterly review.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/launchdarkly/refs/heads/main/finops/launchdarkly-finops.yml
sources:
- https://launchdarkly.com/pricing/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Feature Management
---
