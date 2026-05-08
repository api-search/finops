---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: opsgenie-alert-openapi.yml
  format: yaml
  label: OpsGenie Alert API
  slug: opsgenie-alert
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/opsgenie/refs/heads/main/openapi/opsgenie-alert-openapi.yml
- filename: opsgenie-incident-openapi.yml
  format: yaml
  label: OpsGenie Incident API
  slug: opsgenie-incident
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/opsgenie/refs/heads/main/openapi/opsgenie-incident-openapi.yml
- filename: opsgenie-user-openapi.yml
  format: yaml
  label: OpsGenie User API
  slug: opsgenie-user
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/opsgenie/refs/heads/main/openapi/opsgenie-user-openapi.yml
- filename: opsgenie-team-openapi.yml
  format: yaml
  label: OpsGenie Team API
  slug: opsgenie-team
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/opsgenie/refs/heads/main/openapi/opsgenie-team-openapi.yml
- filename: opsgenie-schedule-openapi.yml
  format: yaml
  label: OpsGenie Schedule API
  slug: opsgenie-schedule
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/opsgenie/refs/heads/main/openapi/opsgenie-schedule-openapi.yml
- filename: opsgenie-escalation-openapi.yml
  format: yaml
  label: OpsGenie Escalation API
  slug: opsgenie-escalation
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/opsgenie/refs/heads/main/openapi/opsgenie-escalation-openapi.yml
- filename: opsgenie-integration-openapi.yml
  format: yaml
  label: OpsGenie Integration API
  slug: opsgenie-integration
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/opsgenie/refs/heads/main/openapi/opsgenie-integration-openapi.yml
- filename: opsgenie-heartbeat-openapi.yml
  format: yaml
  label: OpsGenie Heartbeat API
  slug: opsgenie-heartbeat
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/opsgenie/refs/heads/main/openapi/opsgenie-heartbeat-openapi.yml
- filename: opsgenie-service-openapi.yml
  format: yaml
  label: OpsGenie Service API
  slug: opsgenie-service
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/opsgenie/refs/heads/main/openapi/opsgenie-service-openapi.yml
- filename: opsgenie-notification-rule-openapi.yml
  format: yaml
  label: OpsGenie Notification Rule API
  slug: opsgenie-notification-rule
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/opsgenie/refs/heads/main/openapi/opsgenie-notification-rule-openapi.yml
- filename: opsgenie-account-openapi.yml
  format: yaml
  label: OpsGenie Account API
  slug: opsgenie-account
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/opsgenie/refs/heads/main/openapi/opsgenie-account-openapi.yml
- filename: opsgenie-maintenance-openapi.yml
  format: yaml
  label: OpsGenie Maintenance API
  slug: opsgenie-maintenance
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/opsgenie/refs/heads/main/openapi/opsgenie-maintenance-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  pricingCategory: Per-User Subscription
description: FOCUS-aligned FinOps for Opsgenie.
focus_columns:
  BillingCurrency: USD
  ProviderName: Opsgenie
  PublisherName: Opsgenie
  ServiceCategory: Incident Response
  ServiceName: Opsgenie
layout: finops
meters:
- aggregation: max
  dimensions:
  - plan
  name: user_seats
  unit: seat-month
- aggregation: sum
  name: international_notifications
  unit: notification
- aggregation: sum
  name: alerts_processed
  unit: alert
- aggregation: sum
  name: incidents
  unit: incident
name: Opsgenie Finops
provider_name: OpsGenie
provider_slug: opsgenie
publisher_name: Opsgenie
service_category: Incident Response
slug: opsgenie-finops
source_filename: opsgenie-finops.yml
source_heading: FinOps Profile
source_url: https://www.atlassian.com/software/opsgenie/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Opsgenie\nproviderId: opsgenie\ncreated: '2026-05-04'\nmodified: '2026-05-04'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Incident Response\ndescription: FOCUS-aligned FinOps for Opsgenie.\nsources:\n  - https://www.atlassian.com/software/opsgenie/pricing\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Opsgenie\nserviceCategory: Incident Response\nbillingModel:\n  pricingCategory: Per-User Subscription\n  billingFrequency: Monthly\n  billingCurrency: USD\nfocusColumns:\n  ServiceName: Opsgenie\n  ServiceCategory: Incident Response\n  ProviderName: Opsgenie\n  PublisherName: Opsgenie\n  BillingCurrency: USD\nmeters:\n  - name: user_seats\n    unit: seat-month\n    aggregation:\
  \ max\n    dimensions:\n      - plan\n  - name: international_notifications\n    unit: notification\n    aggregation: sum\n  - name: alerts_processed\n    unit: alert\n    aggregation: sum\n  - name: incidents\n    unit: incident\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Track Opsgenie consumption monthly.\n  - name: Allocation\n    description: Tag usage to teams/cost centers.\n  - name: Optimization\n    description: Right-size; reclaim unused entitlements.\n  - name: Accountability\n    description: Set spend alerts; quarterly review.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/opsgenie/refs/heads/main/finops/opsgenie-finops.yml
sources:
- https://www.atlassian.com/software/opsgenie/pricing
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Incident Response
---
