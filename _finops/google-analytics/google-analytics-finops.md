---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: google-analytics-data-api.yaml
  format: yaml
  label: Google Analytics Data API (GA4)
  slug: google-analytics-data-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/google-analytics/refs/heads/main/openapi/google-analytics-data-api.yaml
- filename: google-analytics-admin-api.yaml
  format: yaml
  label: Google Analytics Admin API
  slug: google-analytics-admin-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/google-analytics/refs/heads/main/openapi/google-analytics-admin-api.yaml
- filename: google-analytics-measurement-protocol.yaml
  format: yaml
  label: Google Analytics Measurement Protocol (GA4)
  slug: google-analytics-measurement-protocol
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/google-analytics/refs/heads/main/openapi/google-analytics-measurement-protocol.yaml
- filename: google-analytics-user-deletion-api.yaml
  format: yaml
  label: Google Analytics User Deletion API
  slug: google-analytics-user-deletion-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/google-analytics/refs/heads/main/openapi/google-analytics-user-deletion-api.yaml
- filename: google-analytics-reporting-api-v4.yaml
  format: yaml
  label: Google Analytics Reporting API v4 (Universal Analytics)
  slug: google-analytics-reporting-api-v4
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/google-analytics/refs/heads/main/openapi/google-analytics-reporting-api-v4.yaml
- filename: google-analytics-management-api-v3.yaml
  format: yaml
  label: Google Analytics Management API v3
  slug: google-analytics-management-api-v3
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/google-analytics/refs/heads/main/openapi/google-analytics-management-api-v3.yaml
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  - Adjustment
  pricingCategory: Subscription (Free + Enterprise)
description: 'FOCUS-aligned FinOps for Google Analytics: GA4 Standard is free with token-quota throttling rather than line-item billing; Analytics 360 is a contracted enterprise license invoiced annually by Google. The token quota functions as the practical FinOps lever for GA4 spend predictability.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Google LLC
  ProviderName: Google
  PublisherName: Google LLC
  ServiceCategory: Web Analytics
  ServiceName: Google Analytics
layout: finops
meters:
- aggregation: max
  description: Active GA4 Standard or 360 property under the account
  dimensions:
  - sku
  - region
  name: ga4_property_license
  unit: property
- aggregation: sum
  description: Tokens consumed against the Data API token quota (Core/Realtime/Funnel)
  dimensions:
  - property
  - category
  - api_method
  name: data_api_tokens
  unit: token
- aggregation: sum
  description: Count of Data API / Admin API / Measurement Protocol requests
  dimensions:
  - api
  - property
  - consumer
  name: api_requests
  unit: request
- aggregation: sum
  description: Bytes exported from GA4 to BigQuery (billed via the BigQuery surface, not GA)
  dimensions:
  - property
  - dataset
  name: bigquery_export_volume
  unit: GB
name: Google Analytics Finops
provider_name: Google Analytics
provider_slug: google-analytics
publisher_name: Google LLC
service_category: Web Analytics
slug: google-analytics-finops
source_filename: google-analytics-finops.yml
source_heading: FinOps Profile
source_url: https://developers.google.com/analytics/devguides/reporting/data/v1/quotas
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Google Analytics\nproviderId: google-analytics\npublisherName: Google LLC\nserviceCategory: Web Analytics\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - Analytics\n  - Web Analytics\n  - Google\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps for Google Analytics: GA4 Standard is free with token-quota throttling\n  rather than line-item billing; Analytics 360 is a contracted enterprise license invoiced annually by\n  Google. The token quota functions as the practical FinOps lever for GA4 spend predictability.'\nsources:\n  - https://developers.google.com/analytics/devguides/reporting/data/v1/quotas\n  - https://marketingplatform.google.com/about/analytics-360/\n\
  \  - https://support.google.com/analytics/answer/11202874\nbillingModel:\n  pricingCategory: Subscription (Free + Enterprise)\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Adjustment\nfocusColumns:\n  ServiceName: Google Analytics\n  ServiceCategory: Web Analytics\n  ProviderName: Google\n  PublisherName: Google LLC\n  InvoiceIssuerName: Google LLC\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: ga4_property_license\n    description: Active GA4 Standard or 360 property under the account\n    unit: property\n    aggregation: max\n    dimensions:\n      - sku\n      - region\n  - name: data_api_tokens\n    description: Tokens consumed against the Data API token quota (Core/Realtime/Funnel)\n    unit: token\n    aggregation: sum\n    dimensions:\n      - property\n      - category\n      - api_method\n  - name: api_requests\n    description: Count of Data API / Admin API / Measurement Protocol requests\n    unit: request\n\
  \    aggregation: sum\n    dimensions:\n      - api\n      - property\n      - consumer\n  - name: bigquery_export_volume\n    description: Bytes exported from GA4 to BigQuery (billed via the BigQuery surface, not GA)\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - property\n      - dataset\napis:\n  - name: Google Analytics Data API (GA4)\n    baseURL: https://analyticsdata.googleapis.com\n    serviceName: Google Analytics Data API (GA4)\n    serviceCategory: Web Analytics\n  - name: Google Analytics Admin API\n    baseURL: https://analyticsadmin.googleapis.com\n    serviceName: Google Analytics Admin API\n    serviceCategory: Web Analytics\n  - name: Google Analytics Measurement Protocol (GA4)\n    baseURL: https://www.google-analytics.com\n    serviceName: Google Analytics Measurement Protocol (GA4)\n    serviceCategory: Web Analytics\n  - name: Google Analytics User Deletion API\n    baseURL: https://www.googleapis.com/analytics/v3\n    serviceName: Google Analytics User\
  \ Deletion API\n    serviceCategory: Web Analytics\nprinciples:\n  - name: Visibility\n    description: Send returnPropertyQuota=true on Data API calls to surface remaining Core/Realtime/Funnel\n      tokens; pipe quota telemetry into Cloud Monitoring or BigQuery for trend dashboards.\n  - name: Allocation\n    description: Allocate Analytics 360 license cost to product lines via property mapping; for Standard,\n      tag API consumers by GCP project and property to chargeback the BigQuery export side of the cost.\n  - name: Optimization\n    description: Reduce Core token spend by lowering report cardinality, narrowing date ranges, batching\n      requests via runReport batch, and caching repeat queries. Move heavy analytical workloads to BigQuery\n      export rather than the Data API.\n  - name: Accountability\n    description: Designate a property owner per GA4 property; review quota burn weekly and escalate to\n      a 360 upgrade only when token throttling materially blocks reporting\
  \ needs.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/google-analytics/refs/heads/main/finops/google-analytics-finops.yml
sources:
- https://developers.google.com/analytics/devguides/reporting/data/v1/quotas
- https://marketingplatform.google.com/about/analytics-360/
- https://support.google.com/analytics/answer/11202874
specification: FinOps Framework
tags:
- Analytics
- Web Analytics
- Google
- FinOps
- FOCUS
---
