---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: amplitude-http-v2-api-openapi.yml
  format: yaml
  label: Amplitude HTTP V2 API
  slug: http-v2-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/amplitude/refs/heads/main/openapi/amplitude-http-v2-api-openapi.yml
- filename: amplitude-identify-api-openapi.yml
  format: yaml
  label: Amplitude Identify API
  slug: identify-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/amplitude/refs/heads/main/openapi/amplitude-identify-api-openapi.yml
- filename: amplitude-dashboard-rest-api-openapi.yml
  format: yaml
  label: Amplitude Dashboard REST API
  slug: dashboard-rest-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/amplitude/refs/heads/main/openapi/amplitude-dashboard-rest-api-openapi.yml
- filename: amplitude-export-api-openapi.yml
  format: yaml
  label: Amplitude Export API
  slug: export-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/amplitude/refs/heads/main/openapi/amplitude-export-api-openapi.yml
- filename: amplitude-behavioral-cohorts-api-openapi.yml
  format: yaml
  label: Amplitude Behavioral Cohorts API
  slug: behavioral-cohorts-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/amplitude/refs/heads/main/openapi/amplitude-behavioral-cohorts-api-openapi.yml
- filename: amplitude-taxonomy-api-openapi.yml
  format: yaml
  label: Amplitude Taxonomy API
  slug: taxonomy-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/amplitude/refs/heads/main/openapi/amplitude-taxonomy-api-openapi.yml
- filename: amplitude-attribution-api-openapi.yml
  format: yaml
  label: Amplitude Attribution API
  slug: attribution-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/amplitude/refs/heads/main/openapi/amplitude-attribution-api-openapi.yml
- filename: amplitude-chart-annotations-api-openapi.yml
  format: yaml
  label: Amplitude Chart Annotations API
  slug: chart-annotations-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/amplitude/refs/heads/main/openapi/amplitude-chart-annotations-api-openapi.yml
- filename: amplitude-user-profile-api-openapi.yml
  format: yaml
  label: Amplitude User Profile API
  slug: user-profile-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/amplitude/refs/heads/main/openapi/amplitude-user-profile-api-openapi.yml
- filename: amplitude-user-mapping-api-openapi.yml
  format: yaml
  label: Amplitude User Mapping API
  slug: user-mapping-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/amplitude/refs/heads/main/openapi/amplitude-user-mapping-api-openapi.yml
- filename: amplitude-scim-api-openapi.yml
  format: yaml
  label: Amplitude SCIM API
  slug: scim-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/amplitude/refs/heads/main/openapi/amplitude-scim-api-openapi.yml
- filename: amplitude-dsar-api-openapi.yml
  format: yaml
  label: Amplitude Data Subject Access Request API
  slug: dsar-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/amplitude/refs/heads/main/openapi/amplitude-dsar-api-openapi.yml
- filename: amplitude-experiment-evaluation-api-openapi.yml
  format: yaml
  label: Amplitude Experiment Evaluation API
  slug: experiment-evaluation-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/amplitude/refs/heads/main/openapi/amplitude-experiment-evaluation-api-openapi.yml
- filename: amplitude-experiment-management-api-openapi.yml
  format: yaml
  label: Amplitude Experiment Management API
  slug: experiment-management-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/amplitude/refs/heads/main/openapi/amplitude-experiment-management-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  pricingCategory: MTU/Event-Based
description: FOCUS-aligned FinOps for Amplitude.
focus_columns:
  BillingCurrency: USD
  ProviderName: Amplitude
  PublisherName: Amplitude
  ServiceCategory: Product Analytics
  ServiceName: Amplitude
layout: finops
meters:
- aggregation: max
  name: monthly_tracked_users
  unit: MTU
- aggregation: sum
  name: tracked_events
  unit: event
- aggregation: sum
  name: session_replays
  unit: replay
- aggregation: sum
  name: feature_flags_evaluations
  unit: evaluation
name: Amplitude Finops
provider_name: Amplitude
provider_slug: amplitude
publisher_name: Amplitude
service_category: Product Analytics
slug: amplitude-finops
source_filename: amplitude-finops.yml
source_heading: FinOps Profile
source_url: https://amplitude.com/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Amplitude\nproviderId: amplitude\ncreated: '2026-05-04'\nmodified: '2026-05-04'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Product Analytics\ndescription: FOCUS-aligned FinOps for Amplitude.\nsources:\n  - https://amplitude.com/pricing\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Amplitude\nserviceCategory: Product Analytics\nbillingModel:\n  pricingCategory: MTU/Event-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\nfocusColumns:\n  ServiceName: Amplitude\n  ServiceCategory: Product Analytics\n  ProviderName: Amplitude\n  PublisherName: Amplitude\n  BillingCurrency: USD\nmeters:\n  - name: monthly_tracked_users\n    unit: MTU\n    aggregation: max\n  -\
  \ name: tracked_events\n    unit: event\n    aggregation: sum\n  - name: session_replays\n    unit: replay\n    aggregation: sum\n  - name: feature_flags_evaluations\n    unit: evaluation\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Track Amplitude consumption monthly via admin/billing exports.\n  - name: Allocation\n    description: Tag seats/usage to teams or cost centers for chargeback.\n  - name: Optimization\n    description: Right-size tier and seat count quarterly; reclaim inactive seats.\n  - name: Accountability\n    description: Set spend alerts and renew at observed active utilization.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/amplitude/refs/heads/main/finops/amplitude-finops.yml
sources:
- https://amplitude.com/pricing
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Product Analytics
---
