---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: nasdaq-data-link-timeseries-openapi.yml
  format: yaml
  label: Nasdaq Data Link REST API (Time-Series)
  slug: nasdaq-data-link-timeseries-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/quandl/refs/heads/main/openapi/nasdaq-data-link-timeseries-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Purchase
  - Usage
  pricingCategory: Subscription (Per-Dataset)
description: FOCUS-aligned FinOps for Nasdaq Data Link (Quandl) - per-dataset subscription fees plus enterprise multi-dataset contracts; pricing is set inside the catalog rather than a published tier table.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Nasdaq, Inc.
  ProviderName: Nasdaq Data Link
  PublisherName: Nasdaq, Inc.
  ServiceCategory: Market Data
  ServiceName: Nasdaq Data Link
layout: finops
meters:
- aggregation: sum
  description: Per-dataset subscription fee for premium Nasdaq Data Link content; rate is set on the data.nasdaq.com product page for each dataset.
  dimensions:
  - dataset
  - account
  name: dataset_subscription
  unit: month
- aggregation: sum
  description: REST and Streaming API requests against the subscribed datasets; subject to per-account throttling rather than per-call billing.
  dimensions:
  - dataset
  - api_key
  name: api_requests
  unit: request
name: Quandl Finops
provider_name: Quandl (Nasdaq Data Link)
provider_slug: quandl
publisher_name: Nasdaq, Inc.
service_category: Market Data
slug: quandl-finops
source_filename: quandl-finops.yml
source_heading: FinOps Profile
source_url: https://data.nasdaq.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Quandl (Nasdaq Data Link)\nproviderId: quandl\npublisherName: Nasdaq, Inc.\nserviceCategory: Market Data\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Finance\n  - Market Data\n  - FinOps\n  - FOCUS\nnotes: Nasdaq Data Link does not publish a public per-dataset price list or a usage telemetry API;\n  premium dataset prices are surfaced inside the data.nasdaq.com catalog and enterprise pricing is\n  contracted via Nasdaq sales. FOCUS columns are populated at the publisher level; per-dataset meters\n  are listed but rates are intentionally left unreconciled.\ndescription: FOCUS-aligned FinOps for Nasdaq Data Link (Quandl)\
  \ - per-dataset subscription fees plus\n  enterprise multi-dataset contracts; pricing is set inside the catalog rather than a published tier\n  table.\nsources:\n  - https://data.nasdaq.com/\n  - https://docs.data.nasdaq.com/\nbillingModel:\n  pricingCategory: Subscription (Per-Dataset)\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\nfocusColumns:\n  ServiceName: Nasdaq Data Link\n  ServiceCategory: Market Data\n  ProviderName: Nasdaq Data Link\n  PublisherName: Nasdaq, Inc.\n  InvoiceIssuerName: Nasdaq, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: dataset_subscription\n    description: Per-dataset subscription fee for premium Nasdaq Data Link content; rate is set on\n      the data.nasdaq.com product page for each dataset.\n    unit: month\n    aggregation: sum\n    dimensions:\n      - dataset\n      - account\n  - name: api_requests\n    description: REST and Streaming API requests against the subscribed datasets; subject to\
  \ per-account\n      throttling rather than per-call billing.\n    unit: request\n    aggregation: sum\n    dimensions:\n      - dataset\n      - api_key\nprinciples:\n  - name: Visibility\n    description: Track subscribed datasets and per-account API key usage through the data.nasdaq.com\n      account dashboard; export invoice line items into the internal cost-management system.\n  - name: Allocation\n    description: Allocate per-dataset subscription fees against the analytics or trading desk consuming\n      each dataset; tag API keys per consuming application.\n  - name: Optimization\n    description: Audit subscribed datasets quarterly; cancel datasets that no longer drive analyses,\n      and consolidate access against an enterprise contract when multiple desks subscribe to the same\n      provider.\n  - name: Accountability\n    description: Data leadership owns the dataset catalog; finance reviews per-dataset spend at renewal.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/quandl/refs/heads/main/finops/quandl-finops.yml
sources:
- https://data.nasdaq.com/
- https://docs.data.nasdaq.com/
specification: FinOps Framework
tags:
- Finance
- Market Data
- FinOps
- FOCUS
---
