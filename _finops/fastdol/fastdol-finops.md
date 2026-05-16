---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: fastdol-openapi.yml
  format: yaml
  label: FastDOL API
  slug: fastdol-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/fastdol/main/openapi/fastdol-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly (Free) / Custom (Enterprise contract)
  chargeCategories:
  - Usage
  - Purchase
  pricingCategory: Freemium + Custom Enterprise
description: 'FOCUS-aligned FinOps shape for FastDOL: a free per-key monthly lookup quota plus an enterprise / data-licensing motion priced through direct sales. Public unit pricing is not posted on the website, so the commercial line items are captured as contracted values and `reconciled` is `false` until the provider publishes a unit-priced surface.

  '
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: FastDOL
  ProviderName: FastDOL
  PublisherName: FastDOL
  RegionId: US
  ServiceCategory: Public Records / Compliance Data
  ServiceName: FastDOL API
  ServiceSubcategory: Federal Workplace Enforcement
layout: finops
meters:
- aggregation: sum
  description: Each successful API lookup, counted against the per-key monthly quota. Batch items count individually.
  dimensions:
  - api_key_id
  - endpoint_family
  name: api_lookups
  unit: request
- aggregation: sum
  description: Number of items submitted across POST /v1/employers/batch requests.
  dimensions:
  - api_key_id
  name: batch_items
  unit: item
- aggregation: sum
  description: CSV upload rows processed via POST /v1/employers/upload-csv.
  dimensions:
  - api_key_id
  name: csv_upload_rows
  unit: row
- aggregation: sum
  description: Rows materialized by enterprise async export jobs.
  dimensions:
  - account_id
  - export_job_id
  - format
  name: export_rows
  unit: row
- aggregation: sum
  description: PDF compliance reports claimed through /v1/usage/pdf-report-claim.
  dimensions:
  - account_id
  - employer_id
  name: pdf_report_claims
  unit: report
- aggregation: sum
  description: Bulk dataset licenses (e.g. OSHA construction enforcement, WHD wage theft, cross-agency violations) priced under enterprise contracts.
  dimensions:
  - dataset_id
  name: dataset_licenses
  unit: dataset-year
name: Fastdol Finops
provider_name: FastDOL
provider_slug: fastdol
publisher_name: FastDOL
service_category: Public Records / Compliance Data
slug: fastdol-finops
source_filename: fastdol-finops.yml
source_heading: FinOps Profile
source_url: https://fastdol.com/docs
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: FastDOL\nproviderId: fastdol\ncreated: '2026-05-16'\nmodified: '2026-05-16'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Federal Enforcement\n  - Public Records\n  - Data Licensing\ndescription: >\n  FOCUS-aligned FinOps shape for FastDOL: a free per-key monthly lookup quota plus an\n  enterprise / data-licensing motion priced through direct sales. Public unit pricing is not\n  posted on the website, so the commercial line items are captured as contracted values and\n  `reconciled` is `false` until the provider publishes a unit-priced surface.\nsources:\n  - https://fastdol.com/docs\n  - https://fastdol.com/enterprise\n  - https://fastdol.com/datasets\n  - https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n\
  \  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: FastDOL\nserviceCategory: Public Records / Compliance Data\nbillingModel:\n  pricingCategory: Freemium + Custom Enterprise\n  billingFrequency: Monthly (Free) / Custom (Enterprise contract)\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\nfocusColumns:\n  ServiceName: FastDOL API\n  ServiceCategory: Public Records / Compliance Data\n  ServiceSubcategory: Federal Workplace Enforcement\n  ProviderName: FastDOL\n  PublisherName: FastDOL\n  InvoiceIssuerName: FastDOL\n  BillingCurrency: USD\n  ChargeCategory: Usage\n  RegionId: US\nmeters:\n  - name: api_lookups\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api_key_id\n      - endpoint_family\n    description: Each successful API lookup, counted against the per-key monthly quota. Batch items count individually.\n  - name: batch_items\n    unit: item\n    aggregation: sum\n    dimensions:\n      - api_key_id\n  \
  \  description: Number of items submitted across POST /v1/employers/batch requests.\n  - name: csv_upload_rows\n    unit: row\n    aggregation: sum\n    dimensions:\n      - api_key_id\n    description: CSV upload rows processed via POST /v1/employers/upload-csv.\n  - name: export_rows\n    unit: row\n    aggregation: sum\n    dimensions:\n      - account_id\n      - export_job_id\n      - format\n    description: Rows materialized by enterprise async export jobs.\n  - name: pdf_report_claims\n    unit: report\n    aggregation: sum\n    dimensions:\n      - account_id\n      - employer_id\n    description: PDF compliance reports claimed through /v1/usage/pdf-report-claim.\n  - name: dataset_licenses\n    unit: dataset-year\n    aggregation: sum\n    dimensions:\n      - dataset_id\n    description: Bulk dataset licenses (e.g. OSHA construction enforcement, WHD wage theft, cross-agency violations) priced under enterprise contracts.\nprinciples:\n  - name: Visibility\n    description: GET\
  \ /v1/usage and the dashboard expose per-key consumption; `X-RateLimit-*` response headers surface real-time quota state on every request.\n  - name: Allocation\n    description: Issue one API key per workload (up to 5 active per account) so quota and 429 events can be attributed cleanly to a team or pipeline.\n  - name: Optimization\n    description: Use POST /v1/employers/batch (up to 100 items per request) and CSV upload (up to 500 rows) to amortize HTTP overhead; cache hot employer profiles client-side; move large backfills to async /v1/export.\n  - name: Operation\n    description: Run automated key rotation taking advantage of the 48-hour grace window; alert when X-RateLimit-Remaining falls below a threshold; back off on 429 with the Retry-After header.\npractices:\n  - name: Inform\n    description: Use GET /v1/usage and X-RateLimit-* headers to publish per-key spend and quota dashboards.\n  - name: Optimize\n    description: Prefer batch and CSV-upload endpoints over loops of single\
  \ GETs; downscope research workloads to specific NAICS / states.\n  - name: Operate\n    description: Wire async export downloads to S3/GCS sinks; monitor 5xx and 429 rates and auto-rotate compromised keys.\nnotes:\n  - Reconciled is false because FastDOL has not published a unit-priced rate card; commercial pricing is negotiated through ben@fastdol.com.\n  - Update this artifact once FastDOL exposes a public pricing page with per-call, per-row, or per-dataset rates.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/fastdol/refs/heads/main/finops/fastdol-finops.yml
sources:
- https://fastdol.com/docs
- https://fastdol.com/enterprise
- https://fastdol.com/datasets
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Federal Enforcement
- Public Records
- Data Licensing
---
