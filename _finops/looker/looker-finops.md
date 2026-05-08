---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: looker-api-openapi.yml
  format: yaml
  label: Looker API
  slug: api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/looker/refs/heads/main/openapi/looker-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Usage
  - Purchase
  - Tax
  - Adjustment
  - Credit
  pricingCategory: Subscription + Token Overage
description: 'FOCUS-aligned FinOps for Looker (Google Cloud): annual edition subscription (Standard / Enterprise / Embed) priced by sales quote, plus per-user license add-ons (Developer / Standard / Viewer) with per-user Conversational Analytics token quotas; overage on tokens after Oct 1 2026.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Google LLC
  ProviderName: Google Cloud
  PublisherName: Google LLC
  ServiceCategory: Business Intelligence
  ServiceName: Looker
layout: finops
meters:
- aggregation: sum
  dimensions:
  - edition
  name: edition_subscription
  unit: year
- aggregation: max
  name: developer_users
  unit: seat
- aggregation: max
  name: standard_users
  unit: seat
- aggregation: max
  name: viewer_users
  unit: seat
- aggregation: sum
  dimensions:
  - edition
  name: api_calls_query
  unit: request
- aggregation: sum
  dimensions:
  - edition
  name: api_calls_admin
  unit: request
- aggregation: sum
  dimensions:
  - user_role
  name: conversational_tokens_input
  unit: token
- aggregation: sum
  dimensions:
  - user_role
  name: conversational_tokens_output
  unit: token
name: Looker Finops
provider_name: Looker
provider_slug: looker
publisher_name: Google LLC
service_category: Business Intelligence
slug: looker-finops
source_filename: looker-finops.yml
source_heading: FinOps Profile
source_url: https://cloud.google.com/looker/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Looker\nproviderId: looker\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - BI Platform\n  - Business Intelligence\n  - Embedded Analytics\ndescription: 'FOCUS-aligned FinOps for Looker (Google Cloud): annual edition subscription (Standard /\n  Enterprise / Embed) priced by sales quote, plus per-user license add-ons (Developer / Standard / Viewer)\n  with per-user Conversational Analytics token quotas; overage on tokens after Oct 1 2026.'\nsources:\n  - https://cloud.google.com/looker/pricing\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Google LLC\nserviceCategory: Business Intelligence\nbillingModel:\n  pricingCategory: Subscription\
  \ + Token Overage\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Adjustment\n    - Credit\nfocusColumns:\n  ServiceName: Looker\n  ServiceCategory: Business Intelligence\n  ProviderName: Google Cloud\n  PublisherName: Google LLC\n  InvoiceIssuerName: Google LLC\n  BillingCurrency: USD\nmeters:\n  - name: edition_subscription\n    unit: year\n    aggregation: sum\n    dimensions:\n      - edition\n  - name: developer_users\n    unit: seat\n    aggregation: max\n  - name: standard_users\n    unit: seat\n    aggregation: max\n  - name: viewer_users\n    unit: seat\n    aggregation: max\n  - name: api_calls_query\n    unit: request\n    aggregation: sum\n    dimensions:\n      - edition\n  - name: api_calls_admin\n    unit: request\n    aggregation: sum\n    dimensions:\n      - edition\n  - name: conversational_tokens_input\n    unit: token\n    aggregation: sum\n    dimensions:\n      - user_role\n  - name: conversational_tokens_output\n\
  \    unit: token\n    aggregation: sum\n    dimensions:\n      - user_role\nprinciples:\n  - name: Visibility\n    description: Track edition API call usage in the Looker admin console; track per-user Conversational\n      Analytics token consumption via the Looker usage reports.\n  - name: Allocation\n    description: Map Looker users to Google Cloud projects/folders and tag for chargeback; allocate\n      Conversational Analytics costs by user role.\n  - name: Optimization\n    description: Right-size edition (Standard vs Enterprise vs Embed) to API quota; prefer Standard / Viewer\n      seats for read-only audiences; cache dashboards and use scheduled deliveries to reduce live API calls.\n  - name: Accountability\n    description: Ahead of Oct 1 2026 token billing, set per-team budgets on Conversational Analytics\n      input/output tokens and review against $3/1M input + $20/1M output.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/looker/refs/heads/main/finops/looker-finops.yml
sources:
- https://cloud.google.com/looker/pricing
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- BI Platform
- Business Intelligence
- Embedded Analytics
---
