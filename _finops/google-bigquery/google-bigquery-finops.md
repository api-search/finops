---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: bigquery-api-openapi.yml
  format: yaml
  label: BigQuery API
  slug: bigquery
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/google-bigquery/refs/heads/main/openapi/bigquery-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  - Tax
  - Adjustment
  - Credit
  pricingCategory: Pay-As-You-Go + Committed Use
description: 'FOCUS-aligned FinOps for BigQuery: separate compute (on-demand TB-scanned or capacity slot-hours) and storage (active vs long-term, logical vs physical) meters, billed continuously through Google Cloud Billing. Detailed export to BigQuery itself is the canonical visibility surface.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Google LLC
  ProviderName: Google Cloud
  PublisherName: Google LLC
  ServiceCategory: Database / Data Warehouse
  ServiceName: BigQuery
layout: finops
meters:
- aggregation: sum
  description: Bytes processed by on-demand SQL queries
  dimensions:
  - project
  - region
  - user
  - job_id
  name: query_bytes_processed
  unit: TB
- aggregation: sum
  description: Slot-hours consumed under a capacity reservation (Standard/Enterprise/Enterprise Plus)
  dimensions:
  - reservation
  - edition
  - region
  name: slot_hours
  unit: slot-hour
- aggregation: sum
  description: Active table storage (modified within 90 days) - logical or physical
  dimensions:
  - dataset
  - region
  - billing_model
  name: active_storage
  unit: GB-month
- aggregation: sum
  description: Long-term table storage (unmodified 90+ days)
  dimensions:
  - dataset
  - region
  - billing_model
  name: long_term_storage
  unit: GB-month
- aggregation: sum
  description: Bytes ingested via legacy streaming insert API
  dimensions:
  - dataset
  - region
  name: streaming_inserts
  unit: GB
- aggregation: sum
  description: Bytes ingested via Storage Write API
  dimensions:
  - dataset
  - region
  name: storage_write_api
  unit: GB
- aggregation: sum
  description: Bytes read via Storage Read API
  dimensions:
  - dataset
  - region
  name: storage_read_api
  unit: GB
- aggregation: max
  description: BI Engine reserved memory
  dimensions:
  - region
  name: bi_engine_capacity
  unit: GB-month
name: Google Bigquery Finops
provider_name: Google BigQuery
provider_slug: google-bigquery
publisher_name: Google LLC
service_category: Data Warehouse / Analytics
slug: google-bigquery-finops
source_filename: google-bigquery-finops.yml
source_heading: FinOps Profile
source_url: https://cloud.google.com/bigquery/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Google BigQuery\nproviderId: google-bigquery\npublisherName: Google LLC\nserviceCategory: Data Warehouse / Analytics\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - Data Warehouse\n  - Analytics\n  - Google Cloud\n  - SQL\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps for BigQuery: separate compute (on-demand TB-scanned or capacity slot-hours)\n  and storage (active vs long-term, logical vs physical) meters, billed continuously through Google Cloud\n  Billing. Detailed export to BigQuery itself is the canonical visibility surface.'\nsources:\n  - https://cloud.google.com/bigquery/pricing\n  - https://cloud.google.com/billing/docs/how-to/export-data-bigquery\n\
  \  - https://cloud.google.com/bigquery/docs/information-schema-jobs\nbillingModel:\n  pricingCategory: Pay-As-You-Go + Committed Use\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Adjustment\n    - Credit\nfocusColumns:\n  ServiceName: BigQuery\n  ServiceCategory: Database / Data Warehouse\n  ProviderName: Google Cloud\n  PublisherName: Google LLC\n  InvoiceIssuerName: Google LLC\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: query_bytes_processed\n    description: Bytes processed by on-demand SQL queries\n    unit: TB\n    aggregation: sum\n    dimensions:\n      - project\n      - region\n      - user\n      - job_id\n  - name: slot_hours\n    description: Slot-hours consumed under a capacity reservation (Standard/Enterprise/Enterprise Plus)\n    unit: slot-hour\n    aggregation: sum\n    dimensions:\n      - reservation\n      - edition\n      - region\n  - name: active_storage\n    description:\
  \ Active table storage (modified within 90 days) - logical or physical\n    unit: GB-month\n    aggregation: sum\n    dimensions:\n      - dataset\n      - region\n      - billing_model\n  - name: long_term_storage\n    description: Long-term table storage (unmodified 90+ days)\n    unit: GB-month\n    aggregation: sum\n    dimensions:\n      - dataset\n      - region\n      - billing_model\n  - name: streaming_inserts\n    description: Bytes ingested via legacy streaming insert API\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - dataset\n      - region\n  - name: storage_write_api\n    description: Bytes ingested via Storage Write API\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - dataset\n      - region\n  - name: storage_read_api\n    description: Bytes read via Storage Read API\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - dataset\n      - region\n  - name: bi_engine_capacity\n    description: BI Engine reserved memory\n    unit: GB-month\n\
  \    aggregation: max\n    dimensions:\n      - region\napis:\n  - name: BigQuery API\n    baseURL: https://bigquery.googleapis.com\n    serviceName: BigQuery API\n    serviceCategory: Data Warehouse\n  - name: BigQuery Storage Read API\n    baseURL: https://bigquerystorage.googleapis.com\n    serviceName: BigQuery Storage API\n    serviceCategory: Data Warehouse\n  - name: BigQuery Reservation API\n    baseURL: https://bigqueryreservation.googleapis.com\n    serviceName: BigQuery Reservation API\n    serviceCategory: Data Warehouse\n  - name: BigQuery Connection API\n    baseURL: https://bigqueryconnection.googleapis.com\n    serviceName: BigQuery Connection API\n    serviceCategory: Data Warehouse\nprinciples:\n  - name: Visibility\n    description: Enable Cloud Billing detailed export to BigQuery and query INFORMATION_SCHEMA.JOBS_BY_PROJECT\n      for query-level cost attribution. Use the BigQuery Admin Resource Charts dashboard to see slot utilization\n      per reservation.\n  - name:\
  \ Allocation\n    description: Tag jobs with labels (team, application, environment) and pivot the billing export by\n      label; use reservations + assignments to chargeback capacity to specific projects/folders.\n  - name: Optimization\n    description: Partition and cluster large tables to reduce bytes scanned; use materialized views and\n      BI Engine for hot queries; switch from on-demand to a capacity reservation when sustained slot consumption\n      makes it cheaper; commit 1y/3y for additional discount; switch eligible datasets to physical storage\n      billing when compression ratio is high.\n  - name: Accountability\n    description: Set per-project query bytes-billed daily caps as a hard guardrail; configure Cloud Billing\n      budget alerts at 50/80/100% per project; review the top-spending queries weekly via INFORMATION_SCHEMA.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/google-bigquery/refs/heads/main/finops/google-bigquery-finops.yml
sources:
- https://cloud.google.com/bigquery/pricing
- https://cloud.google.com/billing/docs/how-to/export-data-bigquery
- https://cloud.google.com/bigquery/docs/information-schema-jobs
specification: FinOps Framework
tags:
- Data Warehouse
- Analytics
- Google Cloud
- SQL
- FinOps
- FOCUS
---
