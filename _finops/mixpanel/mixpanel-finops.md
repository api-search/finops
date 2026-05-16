---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: openapi
  format: yaml
  label: Mixpanel Ingestion API
  slug: mixpanel-ingestion-api
  spec_type: OpenAPI
  url: https://developer.mixpanel.com/reference/openapi
- filename: openapi
  format: yaml
  label: Mixpanel Query API
  slug: mixpanel-query-api
  spec_type: OpenAPI
  url: https://developer.mixpanel.com/reference/openapi
- filename: openapi
  format: yaml
  label: Mixpanel Data Pipelines API
  slug: mixpanel-data-pipelines-api
  spec_type: OpenAPI
  url: https://developer.mixpanel.com/reference/openapi
- filename: mixpanel-identity-openapi.yml
  format: yaml
  label: Mixpanel Identity API
  slug: mixpanel-identity-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/mixpanel/refs/heads/main/openapi/mixpanel-identity-openapi.yml
- filename: mixpanel-event-export-openapi.yml
  format: yaml
  label: Mixpanel Event Export API
  slug: mixpanel-event-export-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/mixpanel/refs/heads/main/openapi/mixpanel-event-export-openapi.yml
- filename: mixpanel-lexicon-schemas-openapi.yml
  format: yaml
  label: Mixpanel Lexicon Schemas API
  slug: mixpanel-lexicon-schemas-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/mixpanel/refs/heads/main/openapi/mixpanel-lexicon-schemas-openapi.yml
- filename: mixpanel-service-accounts-openapi.yml
  format: yaml
  label: Mixpanel Service Accounts API
  slug: mixpanel-service-accounts-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/mixpanel/refs/heads/main/openapi/mixpanel-service-accounts-openapi.yml
- filename: mixpanel-annotations-openapi.yml
  format: yaml
  label: Mixpanel Annotations API
  slug: mixpanel-annotations-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/mixpanel/refs/heads/main/openapi/mixpanel-annotations-openapi.yml
- filename: mixpanel-gdpr-ccpa-openapi.yml
  format: yaml
  label: Mixpanel GDPR and CCPA API
  slug: mixpanel-gdpr-and-ccpa-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/mixpanel/refs/heads/main/openapi/mixpanel-gdpr-ccpa-openapi.yml
- filename: mixpanel-warehouse-connectors-openapi.yml
  format: yaml
  label: Mixpanel Warehouse Connectors API
  slug: mixpanel-warehouse-connectors-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/mixpanel/refs/heads/main/openapi/mixpanel-warehouse-connectors-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  pricingCategory: Event-Based + Replay-Based
description: FOCUS-aligned FinOps for Mixpanel.
focus_columns:
  BillingCurrency: USD
  ProviderName: Mixpanel
  PublisherName: Mixpanel
  ServiceCategory: Product Analytics
  ServiceName: Mixpanel
layout: finops
meters:
- aggregation: sum
  dimensions:
  - project
  name: tracked_events
  unit: event
- aggregation: sum
  name: session_replays
  unit: replay
- aggregation: sum
  name: spark_ai_queries
  unit: query
name: Mixpanel Finops
provider_name: Mixpanel
provider_slug: mixpanel
publisher_name: Mixpanel
service_category: Product Analytics
slug: mixpanel-finops
source_filename: mixpanel-finops.yml
source_heading: FinOps Profile
source_url: https://mixpanel.com/pricing/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Mixpanel\nproviderId: mixpanel\ncreated: '2026-05-04'\nmodified: '2026-05-04'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Product Analytics\ndescription: FOCUS-aligned FinOps for Mixpanel.\nsources:\n  - https://mixpanel.com/pricing/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Mixpanel\nserviceCategory: Product Analytics\nbillingModel:\n  pricingCategory: Event-Based + Replay-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\nfocusColumns:\n  ServiceName: Mixpanel\n  ServiceCategory: Product Analytics\n  ProviderName: Mixpanel\n  PublisherName: Mixpanel\n  BillingCurrency: USD\nmeters:\n  - name: tracked_events\n    unit: event\n    aggregation: sum\n    dimensions:\n\
  \      - project\n  - name: session_replays\n    unit: replay\n    aggregation: sum\n  - name: spark_ai_queries\n    unit: query\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Track Mixpanel consumption monthly via admin/billing exports.\n  - name: Allocation\n    description: Tag seats/usage to teams or cost centers for chargeback.\n  - name: Optimization\n    description: Right-size tier and seat count quarterly; reclaim inactive seats.\n  - name: Accountability\n    description: Set spend alerts and renew at observed active utilization.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/mixpanel/refs/heads/main/finops/mixpanel-finops.yml
sources:
- https://mixpanel.com/pricing/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Product Analytics
---
