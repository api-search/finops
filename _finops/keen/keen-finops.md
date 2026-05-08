---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: keen-event-collection-api-openapi.yml
  format: yaml
  label: Keen Event Collection API
  slug: event-collection-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/keen/refs/heads/main/openapi/keen-event-collection-api-openapi.yml
- filename: keen-query-api-openapi.yml
  format: yaml
  label: Keen Query API
  slug: query-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/keen/refs/heads/main/openapi/keen-query-api-openapi.yml
- filename: keen-cached-queries-api-openapi.yml
  format: yaml
  label: Keen Cached Queries API
  slug: cached-queries-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/keen/refs/heads/main/openapi/keen-cached-queries-api-openapi.yml
- filename: keen-saved-queries-api-openapi.yml
  format: yaml
  label: Keen Saved Queries API
  slug: saved-queries-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/keen/refs/heads/main/openapi/keen-saved-queries-api-openapi.yml
- filename: keen-data-extraction-api-openapi.yml
  format: yaml
  label: Keen Data Extraction API
  slug: data-extraction-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/keen/refs/heads/main/openapi/keen-data-extraction-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  - Adjustment
  - Credit
  pricingCategory: Tiered Subscription + Overage
description: 'FOCUS-aligned FinOps for Keen: tiered subscription (Team/Business/Custom) with per-unit overages on events, queries, cached queries, and cached datasets.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Keen IO, Inc.
  ProviderName: Keen
  PublisherName: Keen IO, Inc.
  ServiceCategory: Analytics
  ServiceName: Keen
layout: finops
meters:
- aggregation: sum
  dimensions:
  - project
  - collection
  name: events_recorded
  unit: event
- aggregation: sum
  dimensions:
  - project
  - query_type
  name: queries_executed
  unit: query
- aggregation: max
  dimensions:
  - project
  name: cached_queries
  unit: cached_query
- aggregation: max
  dimensions:
  - project
  name: cached_datasets
  unit: cached_dataset
- aggregation: sum
  dimensions:
  - plan
  name: subscription_fees
  unit: month
- aggregation: sum
  name: s3_streaming_addon
  unit: month
name: Keen Finops
provider_name: Keen
provider_slug: keen
publisher_name: Keen IO, Inc.
service_category: Analytics
slug: keen-finops
source_filename: keen-finops.yml
source_heading: FinOps Profile
source_url: https://keen.io/pricing/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Keen\nproviderId: keen\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Analytics\n  - Event Analytics\n  - Embedded Analytics\ndescription: 'FOCUS-aligned FinOps for Keen: tiered subscription (Team/Business/Custom) with per-unit\n  overages on events, queries, cached queries, and cached datasets.'\nsources:\n  - https://keen.io/pricing/\n  - https://keen.io/docs/api/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Keen IO, Inc.\nserviceCategory: Analytics\nbillingModel:\n  pricingCategory: Tiered Subscription + Overage\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    -\
  \ Adjustment\n    - Credit\nfocusColumns:\n  ServiceName: Keen\n  ServiceCategory: Analytics\n  ProviderName: Keen\n  PublisherName: Keen IO, Inc.\n  InvoiceIssuerName: Keen IO, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: events_recorded\n    unit: event\n    aggregation: sum\n    dimensions:\n      - project\n      - collection\n  - name: queries_executed\n    unit: query\n    aggregation: sum\n    dimensions:\n      - project\n      - query_type\n  - name: cached_queries\n    unit: cached_query\n    aggregation: max\n    dimensions:\n      - project\n  - name: cached_datasets\n    unit: cached_dataset\n    aggregation: max\n    dimensions:\n      - project\n  - name: subscription_fees\n    unit: month\n    aggregation: sum\n    dimensions:\n      - plan\n  - name: s3_streaming_addon\n    unit: month\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Use Keen's project usage dashboard and the Account API to monitor monthly event and query\n      consumption\
  \ against included quotas.\n  - name: Allocation\n    description: Separate consuming teams into distinct Keen projects (each with its own keys) so events\n      and queries roll up cleanly to a chargeback dimension.\n  - name: Optimization\n    description: Move recurring dashboards to cached queries and cached datasets to bypass ad-hoc query\n      limits and avoid query overage charges; commit annually for a 10% discount.\n  - name: Accountability\n    description: Project owners reconcile event/query overages monthly and tune retention and dashboard\n      patterns before the next billing cycle.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/keen/refs/heads/main/finops/keen-finops.yml
sources:
- https://keen.io/pricing/
- https://keen.io/docs/api/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Analytics
- Event Analytics
- Embedded Analytics
---
