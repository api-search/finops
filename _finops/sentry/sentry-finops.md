---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: sentry-api-openapi.yml
  format: yaml
  label: Sentry Error Monitoring API
  slug: sentry-error-monitoring-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/sentry/refs/heads/main/openapi/sentry-api-openapi.yml
- filename: sentry-webhooks-asyncapi.yml
  format: yaml
  label: Sentry Integration Platform API
  slug: sentry-integration-platform-api
  spec_type: AsyncAPI
  url: https://raw.githubusercontent.com/api-evangelist/sentry/refs/heads/main/asyncapi/sentry-webhooks-asyncapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  pricingCategory: Subscription + Volume
description: FOCUS-aligned FinOps for Sentry.
focus_columns:
  BillingCurrency: USD
  ProviderName: Sentry
  PublisherName: Sentry
  ServiceCategory: Error Monitoring
  ServiceName: Sentry
layout: finops
meters:
- aggregation: sum
  dimensions:
  - project
  - environment
  name: errors
  unit: error
- aggregation: sum
  name: spans
  unit: span
- aggregation: sum
  name: session_replays
  unit: replay
- aggregation: max
  name: uptime_monitors
  unit: monitor-month
- aggregation: max
  name: cron_monitors
  unit: monitor-month
- aggregation: max
  name: attachments_bytes
  unit: GB-month
name: Sentry Finops
provider_name: Sentry
provider_slug: sentry
publisher_name: Sentry
service_category: Error Monitoring
slug: sentry-finops
source_filename: sentry-finops.yml
source_heading: FinOps Profile
source_url: https://sentry.io/pricing/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Sentry\nproviderId: sentry\ncreated: '2026-05-04'\nmodified: '2026-05-04'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Error Monitoring\ndescription: FOCUS-aligned FinOps for Sentry.\nsources:\n  - https://sentry.io/pricing/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Sentry\nserviceCategory: Error Monitoring\nbillingModel:\n  pricingCategory: Subscription + Volume\n  billingFrequency: Monthly\n  billingCurrency: USD\nfocusColumns:\n  ServiceName: Sentry\n  ServiceCategory: Error Monitoring\n  ProviderName: Sentry\n  PublisherName: Sentry\n  BillingCurrency: USD\nmeters:\n  - name: errors\n    unit: error\n    aggregation: sum\n    dimensions:\n      - project\n   \
  \   - environment\n  - name: spans\n    unit: span\n    aggregation: sum\n  - name: session_replays\n    unit: replay\n    aggregation: sum\n  - name: uptime_monitors\n    unit: monitor-month\n    aggregation: max\n  - name: cron_monitors\n    unit: monitor-month\n    aggregation: max\n  - name: attachments_bytes\n    unit: GB-month\n    aggregation: max\nprinciples:\n  - name: Visibility\n    description: Track Sentry consumption monthly via admin/billing exports.\n  - name: Allocation\n    description: Tag seats/usage to teams or cost centers for chargeback.\n  - name: Optimization\n    description: Right-size tier and seat count quarterly; reclaim inactive seats.\n  - name: Accountability\n    description: Set spend alerts and renew at observed active utilization.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/sentry/refs/heads/main/finops/sentry-finops.yml
sources:
- https://sentry.io/pricing/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Error Monitoring
---
