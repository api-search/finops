---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: merge-hris-api-openapi.yaml
  format: yaml
  label: Merge HRIS API
  slug: hris-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/merge/refs/heads/main/openapi/merge-hris-api-openapi.yaml
- filename: merge-ats-api-openapi.yaml
  format: yaml
  label: Merge ATS API
  slug: ats-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/merge/refs/heads/main/openapi/merge-ats-api-openapi.yaml
- filename: merge-accounting-api-openapi.yaml
  format: yaml
  label: Merge Accounting API
  slug: accounting-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/merge/refs/heads/main/openapi/merge-accounting-api-openapi.yaml
- filename: merge-ticketing-api-openapi.yaml
  format: yaml
  label: Merge Ticketing API
  slug: ticketing-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/merge/refs/heads/main/openapi/merge-ticketing-api-openapi.yaml
- filename: merge-crm-api-openapi.yaml
  format: yaml
  label: Merge CRM API
  slug: crm-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/merge/refs/heads/main/openapi/merge-crm-api-openapi.yaml
- filename: merge-file-storage-api-openapi.yaml
  format: yaml
  label: Merge File Storage API
  slug: file-storage-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/merge/refs/heads/main/openapi/merge-file-storage-api-openapi.yaml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  pricingCategory: Per-Linked-Account + Subscription
description: FOCUS-aligned FinOps for Merge.
focus_columns:
  BillingCurrency: USD
  ProviderName: Merge
  PublisherName: Merge
  ServiceCategory: Unified API
  ServiceName: Merge
layout: finops
meters:
- aggregation: max
  dimensions:
  - category
  - integration
  name: linked_accounts
  unit: account-month
- aggregation: sum
  name: api_requests
  unit: request
- aggregation: max
  name: log_retention_days
  unit: day
name: Merge Finops
provider_name: Merge
provider_slug: merge
publisher_name: Merge
service_category: Unified API
slug: merge-finops
source_filename: merge-finops.yml
source_heading: FinOps Profile
source_url: https://www.merge.dev/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Merge\nproviderId: merge\ncreated: '2026-05-04'\nmodified: '2026-05-04'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Unified API\ndescription: FOCUS-aligned FinOps for Merge.\nsources:\n  - https://www.merge.dev/pricing\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Merge\nserviceCategory: Unified API\nbillingModel:\n  pricingCategory: Per-Linked-Account + Subscription\n  billingFrequency: Monthly\n  billingCurrency: USD\nfocusColumns:\n  ServiceName: Merge\n  ServiceCategory: Unified API\n  ProviderName: Merge\n  PublisherName: Merge\n  BillingCurrency: USD\nmeters:\n  - name: linked_accounts\n    unit: account-month\n    aggregation: max\n    dimensions:\n      - category\n\
  \      - integration\n  - name: api_requests\n    unit: request\n    aggregation: sum\n  - name: log_retention_days\n    unit: day\n    aggregation: max\nprinciples:\n  - name: Visibility\n    description: Track Merge consumption monthly.\n  - name: Allocation\n    description: Tag usage to teams/cost centers.\n  - name: Optimization\n    description: Right-size; reclaim unused entitlements.\n  - name: Accountability\n    description: Set spend alerts; quarterly review.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/merge/refs/heads/main/finops/merge-finops.yml
sources:
- https://www.merge.dev/pricing
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Unified API
---
