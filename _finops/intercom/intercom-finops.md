---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: intercom-openapi.yml
  format: yaml
  label: Intercom API
  slug: intercom-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/intercom/refs/heads/main/openapi/intercom-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  pricingCategory: Per-Seat + Per-Resolution
description: FOCUS-aligned FinOps for Intercom.
focus_columns:
  BillingCurrency: USD
  ProviderName: Intercom
  PublisherName: Intercom
  ServiceCategory: Customer Support
  ServiceName: Intercom
layout: finops
meters:
- aggregation: max
  dimensions:
  - plan
  name: user_seats
  unit: seat-month
- aggregation: sum
  name: fin_resolutions
  unit: resolution
- aggregation: sum
  dimensions:
  - channel
  name: outbound_messages
  unit: message
- aggregation: sum
  name: phone_minutes
  unit: minute
- aggregation: sum
  name: sms_segments
  unit: segment
- aggregation: sum
  name: email_sends
  unit: email
name: Intercom Finops
provider_name: Intercom
provider_slug: intercom
publisher_name: Intercom
service_category: Customer Support
slug: intercom-finops
source_filename: intercom-finops.yml
source_heading: FinOps Profile
source_url: https://www.intercom.com/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Intercom\nproviderId: intercom\ncreated: '2026-05-04'\nmodified: '2026-05-04'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Customer Support\ndescription: FOCUS-aligned FinOps for Intercom.\nsources:\n  - https://www.intercom.com/pricing\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Intercom\nserviceCategory: Customer Support\nbillingModel:\n  pricingCategory: Per-Seat + Per-Resolution\n  billingFrequency: Monthly\n  billingCurrency: USD\nfocusColumns:\n  ServiceName: Intercom\n  ServiceCategory: Customer Support\n  ProviderName: Intercom\n  PublisherName: Intercom\n  BillingCurrency: USD\nmeters:\n  - name: user_seats\n    unit: seat-month\n    aggregation: max\n    dimensions:\n\
  \      - plan\n  - name: fin_resolutions\n    unit: resolution\n    aggregation: sum\n  - name: outbound_messages\n    unit: message\n    aggregation: sum\n    dimensions:\n      - channel\n  - name: phone_minutes\n    unit: minute\n    aggregation: sum\n  - name: sms_segments\n    unit: segment\n    aggregation: sum\n  - name: email_sends\n    unit: email\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Track Intercom consumption monthly via admin/billing exports.\n  - name: Allocation\n    description: Tag seats/usage to teams or cost centers for chargeback.\n  - name: Optimization\n    description: Right-size tier and seat count quarterly; reclaim inactive seats.\n  - name: Accountability\n    description: Set spend alerts and renew at observed active utilization.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/intercom/refs/heads/main/finops/intercom-finops.yml
sources:
- https://www.intercom.com/pricing
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Customer Support
---
