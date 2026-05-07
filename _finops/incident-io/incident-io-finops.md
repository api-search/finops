---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  pricingCategory: Per-User Subscription + On-Call Add-On
description: FOCUS-aligned FinOps for incident.io.
focus_columns:
  BillingCurrency: USD
  ProviderName: incident.io
  PublisherName: incident.io
  ServiceCategory: Incident Response
  ServiceName: incident.io
layout: finops
meters:
- aggregation: max
  dimensions:
  - plan
  name: user_seats
  unit: seat-month
- aggregation: max
  name: oncall_seats
  unit: seat-month
- aggregation: sum
  name: incidents
  unit: incident
- aggregation: max
  name: live_call_routing_numbers
  unit: number-month
name: Incident Io Finops
provider_name: Incident.io
provider_slug: incident-io
publisher_name: incident.io
service_category: Incident Response
slug: incident-io-finops
source_filename: incident-io-finops.yml
source_heading: FinOps Profile
source_url: https://incident.io/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: incident.io\nproviderId: incident-io\ncreated: '2026-05-04'\nmodified: '2026-05-04'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Incident Response\ndescription: FOCUS-aligned FinOps for incident.io.\nsources:\n  - https://incident.io/pricing\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: incident.io\nserviceCategory: Incident Response\nbillingModel:\n  pricingCategory: Per-User Subscription + On-Call Add-On\n  billingFrequency: Monthly\n  billingCurrency: USD\nfocusColumns:\n  ServiceName: incident.io\n  ServiceCategory: Incident Response\n  ProviderName: incident.io\n  PublisherName: incident.io\n  BillingCurrency: USD\nmeters:\n  - name: user_seats\n    unit: seat-month\n\
  \    aggregation: max\n    dimensions:\n      - plan\n  - name: oncall_seats\n    unit: seat-month\n    aggregation: max\n  - name: incidents\n    unit: incident\n    aggregation: sum\n  - name: live_call_routing_numbers\n    unit: number-month\n    aggregation: max\nprinciples:\n  - name: Visibility\n    description: Track incident.io consumption monthly.\n  - name: Allocation\n    description: Tag usage to teams/cost centers.\n  - name: Optimization\n    description: Right-size; reclaim unused entitlements.\n  - name: Accountability\n    description: Set spend alerts; quarterly review.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/incident-io/refs/heads/main/finops/incident-io-finops.yml
sources:
- https://incident.io/pricing
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Incident Response
---
