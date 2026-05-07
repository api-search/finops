---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: fullstory-server-api-openapi.yml
  format: yaml
  label: FullStory Server API
  slug: server-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/fullstory/refs/heads/main/openapi/fullstory-server-api-openapi.yml
- filename: fullstory-segments-export-api-openapi.yml
  format: yaml
  label: FullStory Segments Export API
  slug: segments-export-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/fullstory/refs/heads/main/openapi/fullstory-segments-export-api-openapi.yml
- filename: fullstory-sessions-api-openapi.yml
  format: yaml
  label: FullStory Sessions API
  slug: sessions-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/fullstory/refs/heads/main/openapi/fullstory-sessions-api-openapi.yml
- filename: fullstory-webhooks-api-openapi.yml
  format: yaml
  label: FullStory Webhooks API
  slug: webhooks-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/fullstory/refs/heads/main/openapi/fullstory-webhooks-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  pricingCategory: Custom Annual Contract
description: FOCUS-aligned FinOps for Fullstory.
focus_columns:
  BillingCurrency: USD
  ProviderName: Fullstory
  PublisherName: Fullstory
  ServiceCategory: Digital Experience Intelligence
  ServiceName: Fullstory
layout: finops
meters:
- aggregation: max
  name: monthly_unique_visitors
  unit: user
- aggregation: sum
  name: session_replays
  unit: replay
- aggregation: sum
  name: events
  unit: event
- aggregation: max
  name: user_seats
  unit: seat-month
name: Fullstory Finops
provider_name: FullStory
provider_slug: fullstory
publisher_name: Fullstory
service_category: Digital Experience Intelligence
slug: fullstory-finops
source_filename: fullstory-finops.yml
source_heading: FinOps Profile
source_url: https://www.fullstory.com/pricing/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Fullstory\nproviderId: fullstory\ncreated: '2026-05-04'\nmodified: '2026-05-04'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Digital Experience Intelligence\ndescription: FOCUS-aligned FinOps for Fullstory.\nsources:\n  - https://www.fullstory.com/pricing/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Fullstory\nserviceCategory: Digital Experience Intelligence\nbillingModel:\n  pricingCategory: Custom Annual Contract\n  billingFrequency: Monthly\n  billingCurrency: USD\nfocusColumns:\n  ServiceName: Fullstory\n  ServiceCategory: Digital Experience Intelligence\n  ProviderName: Fullstory\n  PublisherName: Fullstory\n  BillingCurrency: USD\nmeters:\n  - name: monthly_unique_visitors\n\
  \    unit: user\n    aggregation: max\n  - name: session_replays\n    unit: replay\n    aggregation: sum\n  - name: events\n    unit: event\n    aggregation: sum\n  - name: user_seats\n    unit: seat-month\n    aggregation: max\nprinciples:\n  - name: Visibility\n    description: Track Fullstory consumption monthly.\n  - name: Allocation\n    description: Tag usage to teams/cost centers.\n  - name: Optimization\n    description: Right-size; reclaim unused entitlements.\n  - name: Accountability\n    description: Set spend alerts; quarterly review.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/fullstory/refs/heads/main/finops/fullstory-finops.yml
sources:
- https://www.fullstory.com/pricing/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Digital Experience Intelligence
---
