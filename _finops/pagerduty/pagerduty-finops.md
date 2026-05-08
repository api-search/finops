---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: pagerduty-openapi-original.yml
  format: yaml
  label: PagerDuty REST API
  slug: pagerduty-rest-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/pagerduty/refs/heads/main/openapi/pagerduty-openapi-original.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  pricingCategory: Per-Seat Subscription + Credits
description: 'FOCUS-aligned FinOps for PagerDuty: per-user seat subscription plus PagerDuty Advance credit metering.'
focus_columns:
  BillingCurrency: USD
  ProviderName: PagerDuty
  PublisherName: PagerDuty, Inc.
  ServiceCategory: Incident Response
  ServiceName: PagerDuty
layout: finops
meters:
- aggregation: max
  dimensions:
  - plan
  - team
  name: user_seats
  unit: seat-month
- aggregation: sum
  name: international_notifications
  unit: notification
- aggregation: sum
  name: advance_credits
  unit: credit
- aggregation: sum
  name: events_v2_ingest
  unit: event
name: Pagerduty Finops
provider_name: PagerDuty
provider_slug: pagerduty
publisher_name: PagerDuty, Inc.
service_category: Incident Response
slug: pagerduty-finops
source_filename: pagerduty-finops.yml
source_heading: FinOps Profile
source_url: https://www.pagerduty.com/pricing/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: PagerDuty\nproviderId: pagerduty\ncreated: '2026-05-04'\nmodified: '2026-05-04'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - On-Call\ndescription: 'FOCUS-aligned FinOps for PagerDuty: per-user seat subscription plus PagerDuty Advance credit\n  metering.'\nsources:\n  - https://www.pagerduty.com/pricing/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: PagerDuty, Inc.\nserviceCategory: Incident Response\nbillingModel:\n  pricingCategory: Per-Seat Subscription + Credits\n  billingFrequency: Monthly\n  billingCurrency: USD\nfocusColumns:\n  ServiceName: PagerDuty\n  ServiceCategory: Incident Response\n  ProviderName: PagerDuty\n  PublisherName: PagerDuty, Inc.\n  BillingCurrency:\
  \ USD\nmeters:\n  - name: user_seats\n    unit: seat-month\n    aggregation: max\n    dimensions:\n      - plan\n      - team\n  - name: international_notifications\n    unit: notification\n    aggregation: sum\n  - name: advance_credits\n    unit: credit\n    aggregation: sum\n  - name: events_v2_ingest\n    unit: event\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Use Audit Trail and User Reports to track active vs licensed seats.\n  - name: Allocation\n    description: Tag teams to escalation policies; report seat consumption per business unit.\n  - name: Optimization\n    description: 'Right-size plan: stop paying Business for Pro features unused; reclaim inactive seats.'\n  - name: Accountability\n    description: Quarterly seat audit; renew at lower committed seat count where reclaim history supports\n      it.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/pagerduty/refs/heads/main/finops/pagerduty-finops.yml
sources:
- https://www.pagerduty.com/pricing/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- On-Call
---
