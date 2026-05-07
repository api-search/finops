---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: bugsnag-data-access-openapi.yml
  format: yaml
  label: Bugsnag Data Access API
  slug: data-access-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/bugsnag/refs/heads/main/openapi/bugsnag-data-access-openapi.yml
- filename: bugsnag-error-reporting-openapi.yml
  format: yaml
  label: Bugsnag Error Reporting API
  slug: error-reporting-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/bugsnag/refs/heads/main/openapi/bugsnag-error-reporting-openapi.yml
- filename: bugsnag-session-tracking-openapi.yml
  format: yaml
  label: Bugsnag Session Tracking API
  slug: session-tracking-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/bugsnag/refs/heads/main/openapi/bugsnag-session-tracking-openapi.yml
- filename: bugsnag-build-openapi.yml
  format: yaml
  label: Bugsnag Build API
  slug: build-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/bugsnag/refs/heads/main/openapi/bugsnag-build-openapi.yml
- filename: bugsnag-trace-openapi.yml
  format: yaml
  label: Bugsnag Trace API
  slug: trace-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/bugsnag/refs/heads/main/openapi/bugsnag-trace-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  pricingCategory: Tiered Subscription (Events + Spans)
description: FOCUS-aligned FinOps for Bugsnag.
focus_columns:
  BillingCurrency: USD
  ProviderName: Bugsnag
  PublisherName: Bugsnag
  ServiceCategory: Error Monitoring
  ServiceName: Bugsnag
layout: finops
meters:
- aggregation: sum
  dimensions:
  - project
  - release_stage
  name: events
  unit: event
- aggregation: sum
  name: spans
  unit: span
- aggregation: max
  name: user_seats
  unit: seat-month
name: Bugsnag Finops
provider_name: bugsnag
provider_slug: bugsnag
publisher_name: Bugsnag
service_category: Error Monitoring
slug: bugsnag-finops
source_filename: bugsnag-finops.yml
source_heading: FinOps Profile
source_url: https://bugsnag.com/pricing/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Bugsnag\nproviderId: bugsnag\ncreated: '2026-05-04'\nmodified: '2026-05-04'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Error Monitoring\ndescription: FOCUS-aligned FinOps for Bugsnag.\nsources:\n  - https://bugsnag.com/pricing/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Bugsnag\nserviceCategory: Error Monitoring\nbillingModel:\n  pricingCategory: Tiered Subscription (Events + Spans)\n  billingFrequency: Monthly\n  billingCurrency: USD\nfocusColumns:\n  ServiceName: Bugsnag\n  ServiceCategory: Error Monitoring\n  ProviderName: Bugsnag\n  PublisherName: Bugsnag\n  BillingCurrency: USD\nmeters:\n  - name: events\n    unit: event\n    aggregation: sum\n    dimensions:\n\
  \      - project\n      - release_stage\n  - name: spans\n    unit: span\n    aggregation: sum\n  - name: user_seats\n    unit: seat-month\n    aggregation: max\nprinciples:\n  - name: Visibility\n    description: Track Bugsnag consumption monthly.\n  - name: Allocation\n    description: Tag usage to teams/cost centers.\n  - name: Optimization\n    description: Right-size tier; reclaim unused entitlements.\n  - name: Accountability\n    description: Set spend alerts; quarterly review.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/bugsnag/refs/heads/main/finops/bugsnag-finops.yml
sources:
- https://bugsnag.com/pricing/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Error Monitoring
---
