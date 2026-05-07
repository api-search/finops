---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: segment-public-api-openapi.yml
  format: yaml
  label: Segment Public API
  slug: public-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/segment/refs/heads/main/openapi/segment-public-api-openapi.yml
- filename: segment-http-tracking-api-openapi.yml
  format: yaml
  label: Segment HTTP Tracking API
  slug: http-tracking-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/segment/refs/heads/main/openapi/segment-http-tracking-api-openapi.yml
- filename: segment-profile-api-openapi.yml
  format: yaml
  label: Segment Profile API
  slug: profile-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/segment/refs/heads/main/openapi/segment-profile-api-openapi.yml
- filename: segment-config-api-openapi.yml
  format: yaml
  label: Segment Config API
  slug: config-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/segment/refs/heads/main/openapi/segment-config-api-openapi.yml
- filename: segment-pixel-tracking-api-openapi.yml
  format: yaml
  label: Segment Pixel Tracking API
  slug: pixel-tracking-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/segment/refs/heads/main/openapi/segment-pixel-tracking-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  pricingCategory: MTU + Event-Based (custom contract)
description: FOCUS-aligned FinOps for Twilio Segment.
focus_columns:
  BillingCurrency: USD
  ProviderName: Twilio Segment
  PublisherName: Twilio Segment
  ServiceCategory: Customer Data Platform
  ServiceName: Twilio Segment
layout: finops
meters:
- aggregation: max
  name: monthly_tracked_users
  unit: MTU
- aggregation: sum
  dimensions:
  - source
  name: tracked_events
  unit: event
- aggregation: max
  name: destinations_active
  unit: destination-month
- aggregation: sum
  name: function_invocations
  unit: invocation
- aggregation: sum
  name: reverse_etl_rows
  unit: row
name: Segment Finops
provider_name: segment
provider_slug: segment
publisher_name: Twilio Segment
service_category: Customer Data Platform
slug: segment-finops
source_filename: segment-finops.yml
source_heading: FinOps Profile
source_url: https://www.twilio.com/en-us/pricing/customer-data
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Twilio Segment\nproviderId: segment\ncreated: '2026-05-04'\nmodified: '2026-05-04'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Customer Data Platform\ndescription: FOCUS-aligned FinOps for Twilio Segment.\nsources:\n  - https://www.twilio.com/en-us/pricing/customer-data\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Twilio Segment\nserviceCategory: Customer Data Platform\nbillingModel:\n  pricingCategory: MTU + Event-Based (custom contract)\n  billingFrequency: Monthly\n  billingCurrency: USD\nfocusColumns:\n  ServiceName: Twilio Segment\n  ServiceCategory: Customer Data Platform\n  ProviderName: Twilio Segment\n  PublisherName: Twilio Segment\n  BillingCurrency: USD\n\
  meters:\n  - name: monthly_tracked_users\n    unit: MTU\n    aggregation: max\n  - name: tracked_events\n    unit: event\n    aggregation: sum\n    dimensions:\n      - source\n  - name: destinations_active\n    unit: destination-month\n    aggregation: max\n  - name: function_invocations\n    unit: invocation\n    aggregation: sum\n  - name: reverse_etl_rows\n    unit: row\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Track Twilio Segment consumption monthly via admin/billing exports.\n  - name: Allocation\n    description: Tag seats/usage to teams or cost centers for chargeback.\n  - name: Optimization\n    description: Right-size tier and seat count quarterly; reclaim inactive seats.\n  - name: Accountability\n    description: Set spend alerts and renew at observed active utilization.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/segment/refs/heads/main/finops/segment-finops.yml
sources:
- https://www.twilio.com/en-us/pricing/customer-data
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Customer Data Platform
---
