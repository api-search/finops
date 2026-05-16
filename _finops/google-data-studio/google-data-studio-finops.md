---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: google-data-studio-api-openapi.yml
  format: yaml
  label: Google Data Studio API
  slug: google-data-studio-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/google-data-studio/refs/heads/main/openapi/google-data-studio-api-openapi.yml
- filename: google-data-studio-linking-api-openapi.yml
  format: yaml
  label: Looker Studio Linking API
  slug: looker-studio-linking-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/google-data-studio/refs/heads/main/openapi/google-data-studio-linking-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  - Tax
  - Adjustment
  pricingCategory: Subscription + Usage (tokens)
description: 'FOCUS-aligned FinOps for Looker Studio / Looker: Looker Studio Pro is a per-user subscription billed via Google Cloud; Looker editions (Standard / Enterprise / Embed) are annual instance-based commitments with included user allocations and API call buckets; Conversational Analytics adds a token meter starting October 2026. Indirect cost flows through the underlying data source (often BigQuery), which dominates total dashboarding spend.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Google LLC
  ProviderName: Google Cloud
  PublisherName: Google LLC
  ServiceCategory: Business Intelligence
  ServiceName: Looker Studio / Looker
layout: finops
meters:
- aggregation: max
  description: Active Looker Studio Pro per-user licenses
  dimensions:
  - workspace
  name: looker_studio_pro_seats
  unit: seat-month
- aggregation: max
  description: Looker production instance under annual commitment (Standard / Enterprise / Embed)
  dimensions:
  - edition
  - region
  name: looker_instance
  unit: instance-month
- aggregation: max
  description: Looker per-user licenses by class (Developer / Standard / Viewer)
  dimensions:
  - user_class
  - edition
  name: looker_user_licenses
  unit: seat-month
- aggregation: sum
  description: Looker Query API calls
  dimensions:
  - edition
  - instance
  name: query_api_calls
  unit: request
- aggregation: sum
  description: Looker Admin API calls
  dimensions:
  - edition
  - instance
  name: admin_api_calls
  unit: request
- aggregation: sum
  description: Conversational Analytics input tokens
  dimensions:
  - user_class
  - instance
  name: data_tokens_input
  unit: token
- aggregation: sum
  description: Conversational Analytics output tokens
  dimensions:
  - user_class
  - instance
  name: data_tokens_output
  unit: token
- aggregation: sum
  description: Cost incurred at the connected data source (e.g., BigQuery bytes-scanned) when dashboards run queries
  dimensions:
  - data_source
  - dashboard
  name: underlying_data_source_cost
  unit: USD
name: Google Data Studio Finops
provider_name: Google Data Studio
provider_slug: google-data-studio
publisher_name: Google LLC
service_category: Business Intelligence / Analytics
slug: google-data-studio-finops
source_filename: google-data-studio-finops.yml
source_heading: FinOps Profile
source_url: https://cloud.google.com/looker/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Google Data Studio\nproviderId: google-data-studio\npublisherName: Google LLC\nserviceCategory: Business Intelligence / Analytics\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - Business Intelligence\n  - Reporting\n  - Dashboards\n  - Google Cloud\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps for Looker Studio / Looker: Looker Studio Pro is a per-user subscription\n  billed via Google Cloud; Looker editions (Standard / Enterprise / Embed) are annual instance-based commitments\n  with included user allocations and API call buckets; Conversational Analytics adds a token meter starting\n  October 2026. Indirect\
  \ cost flows through the underlying data source (often BigQuery), which dominates\n  total dashboarding spend.'\nsources:\n  - https://cloud.google.com/looker/pricing\n  - https://cloud.google.com/billing/docs/how-to/export-data-bigquery\nbillingModel:\n  pricingCategory: Subscription + Usage (tokens)\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Adjustment\nfocusColumns:\n  ServiceName: Looker Studio / Looker\n  ServiceCategory: Business Intelligence\n  ProviderName: Google Cloud\n  PublisherName: Google LLC\n  InvoiceIssuerName: Google LLC\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: looker_studio_pro_seats\n    description: Active Looker Studio Pro per-user licenses\n    unit: seat-month\n    aggregation: max\n    dimensions:\n      - workspace\n  - name: looker_instance\n    description: Looker production instance under annual commitment (Standard / Enterprise / Embed)\n    unit: instance-month\n\
  \    aggregation: max\n    dimensions:\n      - edition\n      - region\n  - name: looker_user_licenses\n    description: Looker per-user licenses by class (Developer / Standard / Viewer)\n    unit: seat-month\n    aggregation: max\n    dimensions:\n      - user_class\n      - edition\n  - name: query_api_calls\n    description: Looker Query API calls\n    unit: request\n    aggregation: sum\n    dimensions:\n      - edition\n      - instance\n  - name: admin_api_calls\n    description: Looker Admin API calls\n    unit: request\n    aggregation: sum\n    dimensions:\n      - edition\n      - instance\n  - name: data_tokens_input\n    description: Conversational Analytics input tokens\n    unit: token\n    aggregation: sum\n    dimensions:\n      - user_class\n      - instance\n  - name: data_tokens_output\n    description: Conversational Analytics output tokens\n    unit: token\n    aggregation: sum\n    dimensions:\n      - user_class\n      - instance\n  - name: underlying_data_source_cost\n\
  \    description: Cost incurred at the connected data source (e.g., BigQuery bytes-scanned) when dashboards\n      run queries\n    unit: USD\n    aggregation: sum\n    dimensions:\n      - data_source\n      - dashboard\napis:\n  - name: Looker Studio\n    baseURL: https://lookerstudio.google.com\n    serviceName: Looker Studio\n    serviceCategory: Business Intelligence\n  - name: Looker (Google Cloud Core)\n    baseURL: https://cloud.google.com/looker\n    serviceName: Looker\n    serviceCategory: Business Intelligence\nprinciples:\n  - name: Visibility\n    description: Use Cloud Billing detailed export filtered to the Looker SKU and Looker Studio Pro SKU;\n      pair with INFORMATION_SCHEMA on connected BigQuery datasets to attribute query cost to the originating\n      report.\n  - name: Allocation\n    description: Allocate Looker Studio Pro seats to product/marketing teams; tag connected data sources\n      with team labels so dashboard query cost can be charged back through the\
  \ BigQuery (or other source)\n      bill.\n  - name: Optimization\n    description: Use Looker extract scheduling and dashboard caching to avoid re-running expensive queries\n      on every viewer load; right-size BigQuery on-demand vs slot reservation per dashboard workload;\n      monitor Conversational Analytics token burn approaching the October 2026 paid cutover.\n  - name: Accountability\n    description: Designate a dashboard owner per top-spending data source query; review monthly Looker\n      API call usage to avoid edition-level API quota overages; review Conversational Analytics token\n      consumption per user class.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/google-data-studio/refs/heads/main/finops/google-data-studio-finops.yml
sources:
- https://cloud.google.com/looker/pricing
- https://cloud.google.com/billing/docs/how-to/export-data-bigquery
specification: FinOps Framework
tags:
- Business Intelligence
- Reporting
- Dashboards
- Google Cloud
- FinOps
- FOCUS
---
