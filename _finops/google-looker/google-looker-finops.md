---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: Looker.4.0.oas.json
  format: json
  label: Looker API
  slug: looker-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/looker-open-source/sdk-codegen/main/spec/Looker.4.0.oas.json
- filename: rest
  format: yaml
  label: Looker (Google Cloud core) API
  slug: looker-google-cloud-core-api
  spec_type: OpenAPI
  url: https://looker.googleapis.com/$discovery/rest?version=v1
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  - Usage
  - Tax
  - Adjustment
  - Credit
  pricingCategory: Tiered Subscription
description: 'FOCUS-aligned FinOps for Google Looker (Google Cloud core): edition-based subscription with bundled instance, seat, and API-call entitlements, plus token-metered Conversational Analytics overages starting October 2026.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Google LLC
  ProviderName: Google
  PublisherName: Google LLC
  ServiceCategory: Analytics
  ServiceName: Google Looker
layout: finops
meters:
- aggregation: sum
  description: Production Looker instance hours billed per edition
  dimensions:
  - edition
  - region
  name: looker_instance
  unit: instance-month
- aggregation: max
  description: Standard user seats consumed
  dimensions:
  - edition
  name: standard_users
  unit: seat
- aggregation: max
  description: Developer user seats consumed
  dimensions:
  - edition
  name: developer_users
  unit: seat
- aggregation: max
  description: Viewer user seats consumed
  dimensions:
  - edition
  name: viewer_users
  unit: seat
- aggregation: sum
  description: Query-based API calls against the Looker instance
  dimensions:
  - edition
  - endpoint
  name: query_api_calls
  unit: request
- aggregation: sum
  description: Admin API calls against the Looker instance
  dimensions:
  - edition
  - endpoint
  name: admin_api_calls
  unit: request
- aggregation: sum
  description: Input data tokens consumed by Conversational Analytics
  dimensions:
  - user_type
  name: conversational_input_tokens
  unit: token
- aggregation: sum
  description: Output data tokens produced by Conversational Analytics
  dimensions:
  - user_type
  name: conversational_output_tokens
  unit: token
name: Google Looker Finops
provider_name: Google Looker
provider_slug: google-looker
publisher_name: Google LLC
service_category: Analytics
slug: google-looker-finops
source_filename: google-looker-finops.yml
source_heading: FinOps Profile
source_url: https://cloud.google.com/looker/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Google Looker\nproviderId: google-looker\npublisherName: Google LLC\nserviceCategory: Analytics\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Business Intelligence\n  - Analytics\n  - Google Cloud\ndescription: 'FOCUS-aligned FinOps for Google Looker (Google Cloud core): edition-based subscription with\n  bundled instance, seat, and API-call entitlements, plus token-metered Conversational Analytics overages\n  starting October 2026.'\nsources:\n  - https://cloud.google.com/looker/pricing\n  - https://cloud.google.com/billing/docs\nbillingModel:\n  pricingCategory: Tiered Subscription\n  billingFrequency:\
  \ Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\n    - Tax\n    - Adjustment\n    - Credit\nfocusColumns:\n  ServiceName: Google Looker\n  ServiceCategory: Analytics\n  ProviderName: Google\n  PublisherName: Google LLC\n  InvoiceIssuerName: Google LLC\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: looker_instance\n    description: Production Looker instance hours billed per edition\n    unit: instance-month\n    aggregation: sum\n    dimensions:\n      - edition\n      - region\n  - name: standard_users\n    description: Standard user seats consumed\n    unit: seat\n    aggregation: max\n    dimensions:\n      - edition\n  - name: developer_users\n    description: Developer user seats consumed\n    unit: seat\n    aggregation: max\n    dimensions:\n      - edition\n  - name: viewer_users\n    description: Viewer user seats consumed\n    unit: seat\n    aggregation: max\n    dimensions:\n      - edition\n  - name: query_api_calls\n\
  \    description: Query-based API calls against the Looker instance\n    unit: request\n    aggregation: sum\n    dimensions:\n      - edition\n      - endpoint\n  - name: admin_api_calls\n    description: Admin API calls against the Looker instance\n    unit: request\n    aggregation: sum\n    dimensions:\n      - edition\n      - endpoint\n  - name: conversational_input_tokens\n    description: Input data tokens consumed by Conversational Analytics\n    unit: token\n    aggregation: sum\n    dimensions:\n      - user_type\n  - name: conversational_output_tokens\n    description: Output data tokens produced by Conversational Analytics\n    unit: token\n    aggregation: sum\n    dimensions:\n      - user_type\nprinciples:\n  - name: Visibility\n    description: Use Cloud Billing exports to BigQuery and the Looker admin usage panel to monitor seat,\n      API, and Conversational Analytics token consumption.\n  - name: Allocation\n    description: Map Looker user groups and Cloud projects\
  \ to consuming teams; tag projects so billed\n      Looker SKUs roll up correctly to chargeback owners.\n  - name: Optimization\n    description: Right-size the Looker edition to API-call profile; cap viewer Data Token spend with\n      governance; consolidate dev/test instances; review LookML for expensive queries.\n  - name: Accountability\n    description: Set Cloud Billing budgets and anomaly alerts on Looker SKUs; review monthly seat and\n      token utilization vs. forecast with BI owners.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/google-looker/refs/heads/main/finops/google-looker-finops.yml
sources:
- https://cloud.google.com/looker/pricing
- https://cloud.google.com/billing/docs
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Business Intelligence
- Analytics
- Google Cloud
---
