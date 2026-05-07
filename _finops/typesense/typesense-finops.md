---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: typesense-search-api-openapi.yml
  format: yaml
  label: Typesense Search API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/typesense/refs/heads/main/openapi/typesense-search-api-openapi.yml
- filename: typesense-vector-search-api-openapi.yml
  format: yaml
  label: Typesense Vector Search API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/typesense/refs/heads/main/openapi/typesense-vector-search-api-openapi.yml
- filename: typesense-conversational-search-api-openapi.yml
  format: yaml
  label: Typesense Conversational Search API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/typesense/refs/heads/main/openapi/typesense-conversational-search-api-openapi.yml
- filename: typesense-analytics-api-openapi.yml
  format: yaml
  label: Typesense Analytics API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/typesense/refs/heads/main/openapi/typesense-analytics-api-openapi.yml
- filename: typesense-cloud-management-api-openapi.yml
  format: yaml
  label: Typesense Cloud Management API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/typesense/refs/heads/main/openapi/typesense-cloud-management-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  pricingCategory: Per-Node-Hour
description: FOCUS-aligned FinOps for Typesense.
focus_columns:
  BillingCurrency: USD
  ProviderName: Typesense
  PublisherName: Typesense
  ServiceCategory: Search
  ServiceName: Typesense
layout: finops
meters:
- aggregation: sum
  dimensions:
  - size
  - ha
  - region
  name: cluster_hours
  unit: node-hour
- aggregation: max
  name: storage
  unit: GB-month
- aggregation: sum
  name: search_queries
  unit: query
- aggregation: max
  name: indexed_documents
  unit: document-month
name: Typesense Finops
provider_name: Typesense
provider_slug: typesense
publisher_name: Typesense
service_category: Search
slug: typesense-finops
source_filename: typesense-finops.yml
source_heading: FinOps Profile
source_url: https://typesense.org/cloud/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Typesense\nproviderId: typesense\ncreated: '2026-05-04'\nmodified: '2026-05-04'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Search\ndescription: FOCUS-aligned FinOps for Typesense.\nsources:\n  - https://typesense.org/cloud/\n  - https://cloud.typesense.org/pricing\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Typesense\nserviceCategory: Search\nbillingModel:\n  pricingCategory: Per-Node-Hour\n  billingFrequency: Monthly\n  billingCurrency: USD\nfocusColumns:\n  ServiceName: Typesense\n  ServiceCategory: Search\n  ProviderName: Typesense\n  PublisherName: Typesense\n  BillingCurrency: USD\nmeters:\n  - name: cluster_hours\n    unit: node-hour\n    aggregation: sum\n\
  \    dimensions:\n      - size\n      - ha\n      - region\n  - name: storage\n    unit: GB-month\n    aggregation: max\n  - name: search_queries\n    unit: query\n    aggregation: sum\n  - name: indexed_documents\n    unit: document-month\n    aggregation: max\nprinciples:\n  - name: Visibility\n    description: Track Typesense consumption monthly.\n  - name: Allocation\n    description: Tag usage to teams/cost centers.\n  - name: Optimization\n    description: Right-size; reclaim unused entitlements.\n  - name: Accountability\n    description: Set spend alerts; quarterly review.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/typesense/refs/heads/main/finops/typesense-finops.yml
sources:
- https://typesense.org/cloud/
- https://cloud.typesense.org/pricing
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Search
---
