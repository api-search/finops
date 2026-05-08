---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: datafiniti-api.yml
  format: yaml
  label: Datafiniti API
  slug: datafiniti-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/datafiniti/refs/heads/main/openapi/datafiniti-api.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  - Adjustment
  pricingCategory: Subscription + Usage
description: 'FOCUS-aligned FinOps for Datafiniti: subscription billing scaled by record volume across four data products (Property, People, Business, Product). The primary billable unit is a delivered record. Specific per-record rates are gated behind portal sign-up.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Datafiniti, LLC
  PricingCategory: Subscription + Usage
  PricingUnit: record
  ProviderName: Datafiniti
  PublisherName: Datafiniti, LLC
  ServiceCategory: Data as a Service
  ServiceName: Datafiniti
  ServiceSubcategory: Web Data Aggregation
layout: finops
meters:
- aggregation: sum
  description: Count of unique records returned via search, download, or bulk export. The primary billable line.
  dimensions:
  - dataset
  - api_key
  - consumer
  name: records_delivered
  unit: record
- aggregation: count
  description: Count of API requests issued against the search and download endpoints.
  dimensions:
  - endpoint
  - api_key
  name: api_requests
  unit: request
- aggregation: count
  description: Bulk download exports requested through the portal or API.
  dimensions:
  - dataset
  - api_key
  name: bulk_downloads
  unit: download
name: Datafiniti Finops
provider_name: Datafiniti
provider_slug: datafiniti
publisher_name: Datafiniti, LLC
service_category: Data as a Service
slug: datafiniti-finops
source_filename: datafiniti-finops.yml
source_heading: FinOps Profile
source_url: https://datafiniti.co
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Datafiniti\nproviderId: datafiniti\npublisherName: Datafiniti, LLC\nserviceCategory: Data as a Service\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Business Data\n  - Data as a Service\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps for Datafiniti: subscription billing scaled by record volume\n  across four data products (Property, People, Business, Product). The primary billable unit is a\n  delivered record. Specific per-record rates are gated behind portal sign-up.'\nsources:\n  - https://datafiniti.co\n  - https://portal.datafiniti.co\nnotes: No public per-unit pricing; reconciled false. Meter shape\
  \ is correct (records-as-unit) but\n  the dollar values must be sourced from the customer's portal.\nbillingModel:\n  pricingCategory: Subscription + Usage\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Adjustment\nfocusColumns:\n  ServiceName: Datafiniti\n  ServiceCategory: Data as a Service\n  ServiceSubcategory: Web Data Aggregation\n  ProviderName: Datafiniti\n  PublisherName: Datafiniti, LLC\n  InvoiceIssuerName: Datafiniti, LLC\n  PricingCategory: Subscription + Usage\n  PricingUnit: record\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: records_delivered\n    description: Count of unique records returned via search, download, or bulk export. The primary\n      billable line.\n    unit: record\n    aggregation: sum\n    dimensions:\n      - dataset\n      - api_key\n      - consumer\n  - name: api_requests\n    description: Count of API requests issued against the search and download endpoints.\n\
  \    unit: request\n    aggregation: count\n    dimensions:\n      - endpoint\n      - api_key\n  - name: bulk_downloads\n    description: Bulk download exports requested through the portal or API.\n    unit: download\n    aggregation: count\n    dimensions:\n      - dataset\n      - api_key\nprinciples:\n  - name: Visibility\n    description: Use the Datafiniti portal usage dashboard plus per-response record counts to track\n      consumption. Aggregate API responses into internal observability since record volume drives\n      cost.\n  - name: Allocation\n    description: Issue separate API keys per consuming product or team so record consumption can\n      be sliced. Datafiniti does not provide cost-allocation tags natively.\n  - name: Optimization\n    description: Filter aggressively server-side, request only required fields, and prefer search\n      over download for exploration so you do not pay for records you do not retain. Cache stable\n      records locally to avoid re-pulling.\n\
  \  - name: Accountability\n    description: Set monthly record-budget alerts in the portal, designate a budget owner per\n      dataset, and review consumption against business-value metrics (records-converted-to-leads,\n      records-per-listing).\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/datafiniti/refs/heads/main/finops/datafiniti-finops.yml
sources:
- https://datafiniti.co
- https://portal.datafiniti.co
specification: FinOps Framework
tags:
- Business Data
- Data as a Service
- FinOps
- FOCUS
---
