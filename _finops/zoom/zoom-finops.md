---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: zoom-chat--openapi-original.yml
  format: yaml
  label: Zoom Chat API
  slug: zoom-chat-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/zoom/refs/heads/main/openapi/zoom-chat--openapi-original.yml
- filename: zoom-group--openapi-original.yml
  format: yaml
  label: Zoom Group API
  slug: zoom-group-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/zoom/refs/heads/main/openapi/zoom-group--openapi-original.yml
- filename: zoom-device--openapi-original.yml
  format: yaml
  label: Zoom Device API
  slug: zoom-device-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/zoom/refs/heads/main/openapi/zoom-device--openapi-original.yml
- filename: zoom-im--openapi-original.yml
  format: yaml
  label: Zoom Instant Message API
  slug: zoom-instant-message-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/zoom/refs/heads/main/openapi/zoom-im--openapi-original.yml
- filename: zoom-account--openapi-original.yml
  format: yaml
  label: Zoom Account API
  slug: zoom-account-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/zoom/refs/heads/main/openapi/zoom-account--openapi-original.yml
- filename: zoom-recording--openapi-original.yml
  format: yaml
  label: Zoom Recording API
  slug: zoom-recording-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/zoom/refs/heads/main/openapi/zoom-recording--openapi-original.yml
- filename: zoom-meeting--openapi-original.yml
  format: yaml
  label: Zoom Meeting API
  slug: zoom-meeting-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/zoom/refs/heads/main/openapi/zoom-meeting--openapi-original.yml
- filename: zoom-metrics--openapi-original.yml
  format: yaml
  label: Zoom Metrics API
  slug: zoom-metrics-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/zoom/refs/heads/main/openapi/zoom-metrics--openapi-original.yml
- filename: zoom-report--openapi-original.yml
  format: yaml
  label: Zoom Report API
  slug: zoom-report-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/zoom/refs/heads/main/openapi/zoom-report--openapi-original.yml
- filename: zoom-user--openapi-original.yml
  format: yaml
  label: Zoom User API
  slug: zoom-user-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/zoom/refs/heads/main/openapi/zoom-user--openapi-original.yml
- filename: zoom-webinar--openapi-original.yml
  format: yaml
  label: Zoom Webinar API
  slug: zoom-webinar-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/zoom/refs/heads/main/openapi/zoom-webinar--openapi-original.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  pricingCategory: Per-Seat Subscription
description: FOCUS-aligned FinOps for Zoom.
focus_columns:
  BillingCurrency: USD
  ProviderName: Zoom
  PublisherName: Zoom
  ServiceCategory: Video Conferencing
  ServiceName: Zoom
layout: finops
meters:
- aggregation: max
  dimensions:
  - plan
  name: user_seats
  unit: seat-month
- aggregation: max
  name: cloud_recording_storage
  unit: GB-month
- aggregation: sum
  name: phone_minutes
  unit: minute
- aggregation: sum
  name: webinar_attendees
  unit: attendee
- aggregation: sum
  name: events_attendees
  unit: attendee
name: Zoom Finops
provider_name: Zoom
provider_slug: zoom
publisher_name: Zoom
service_category: Video Conferencing
slug: zoom-finops
source_filename: zoom-finops.yml
source_heading: FinOps Profile
source_url: https://zoom.us/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Zoom\nproviderId: zoom\ncreated: '2026-05-04'\nmodified: '2026-05-04'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Video Conferencing\ndescription: FOCUS-aligned FinOps for Zoom.\nsources:\n  - https://zoom.us/pricing\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Zoom\nserviceCategory: Video Conferencing\nbillingModel:\n  pricingCategory: Per-Seat Subscription\n  billingFrequency: Monthly\n  billingCurrency: USD\nfocusColumns:\n  ServiceName: Zoom\n  ServiceCategory: Video Conferencing\n  ProviderName: Zoom\n  PublisherName: Zoom\n  BillingCurrency: USD\nmeters:\n  - name: user_seats\n    unit: seat-month\n    aggregation: max\n    dimensions:\n      - plan\n  - name:\
  \ cloud_recording_storage\n    unit: GB-month\n    aggregation: max\n  - name: phone_minutes\n    unit: minute\n    aggregation: sum\n  - name: webinar_attendees\n    unit: attendee\n    aggregation: sum\n  - name: events_attendees\n    unit: attendee\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Track Zoom consumption monthly via admin/billing exports.\n  - name: Allocation\n    description: Tag seats/usage to teams or cost centers for chargeback.\n  - name: Optimization\n    description: Right-size tier and seat count quarterly; reclaim inactive seats.\n  - name: Accountability\n    description: Set spend alerts and renew at observed active utilization.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/zoom/refs/heads/main/finops/zoom-finops.yml
sources:
- https://zoom.us/pricing
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Video Conferencing
---
