---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: looker-studio-api-openapi.yml
  format: yaml
  label: Looker Studio API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/looker-studio/refs/heads/main/openapi/looker-studio-api-openapi.yml
- filename: looker-studio-linking-api-openapi.yml
  format: yaml
  label: Looker Studio Linking API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/looker-studio/refs/heads/main/openapi/looker-studio-linking-api-openapi.yml
- filename: looker-studio-embedding-api-openapi.yml
  format: yaml
  label: Looker Studio Embedding API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/looker-studio/refs/heads/main/openapi/looker-studio-embedding-api-openapi.yml
- filename: looker-studio-community-connector-api-openapi.yml
  format: yaml
  label: Looker Studio Community Connector API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/looker-studio/refs/heads/main/openapi/looker-studio-community-connector-api-openapi.yml
- filename: looker-studio-community-visualization-api-openapi.yml
  format: yaml
  label: Looker Studio Community Visualization API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/looker-studio/refs/heads/main/openapi/looker-studio-community-visualization-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  - Tax
  - Adjustment
  pricingCategory: Per-Seat Subscription
description: 'FOCUS-aligned FinOps for Looker Studio: free per-user usage plus a $10/user/month Pro tier. Cost is dominated by per-seat Pro licenses; connector and underlying data-source costs (BigQuery, Sheets, third-party APIs) accrue separately.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Google LLC
  ProviderName: Google Cloud
  PublisherName: Google LLC
  ServiceCategory: Business Intelligence
  ServiceName: Looker Studio
layout: finops
meters:
- aggregation: max
  name: pro_seats
  unit: seat
- aggregation: max
  name: free_users
  unit: seat
- aggregation: sum
  dimensions:
  - api
  name: api_requests
  unit: request
name: Looker Studio Finops
provider_name: Looker Studio
provider_slug: looker-studio
publisher_name: Google LLC
service_category: Business Intelligence
slug: looker-studio-finops
source_filename: looker-studio-finops.yml
source_heading: FinOps Profile
source_url: https://cloud.google.com/looker-studio
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Looker Studio\nproviderId: looker-studio\ncreated: '2026-05-04'\nmodified: '2026-05-05'\ntags:\n  - FinOps\n  - FOCUS\n  - Business Intelligence\n  - Google\nreconciled: true\ndescription: 'FOCUS-aligned FinOps for Looker Studio: free per-user usage plus a $10/user/month Pro tier.\n  Cost is dominated by per-seat Pro licenses; connector and underlying data-source costs (BigQuery,\n  Sheets, third-party APIs) accrue separately.'\nsources:\n  - https://cloud.google.com/looker-studio\n  - https://cloud.google.com/looker/pricing\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Google LLC\nserviceCategory: Business Intelligence\nbillingModel:\n  pricingCategory: Per-Seat Subscription\n\
  \  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Adjustment\nfocusColumns:\n  ServiceName: Looker Studio\n  ServiceCategory: Business Intelligence\n  ProviderName: Google Cloud\n  PublisherName: Google LLC\n  InvoiceIssuerName: Google LLC\n  BillingCurrency: USD\nmeters:\n  - name: pro_seats\n    unit: seat\n    aggregation: max\n  - name: free_users\n    unit: seat\n    aggregation: max\n  - name: api_requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\nprinciples:\n  - name: Visibility\n    description: Inventory Pro seats via the Looker Studio admin console; track underlying data source\n      query volume in BigQuery / connector logs.\n  - name: Allocation\n    description: Map Pro seats to Cloud Identity groups for chargeback; tag reports by team/department.\n  - name: Optimization\n    description: Use the free tier for ad-hoc analysts; reserve Pro seats for users that need team\n\
  \      workspaces and managed support; cache report queries to lower upstream BigQuery cost.\n  - name: Accountability\n    description: Owners review Pro seat utilization quarterly; reclaim inactive seats to control monthly burn.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/looker-studio/refs/heads/main/finops/looker-studio-finops.yml
sources:
- https://cloud.google.com/looker-studio
- https://cloud.google.com/looker/pricing
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Business Intelligence
- Google
---
