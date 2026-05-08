---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: nasdaq-omx-group-openapi.yml
  format: yaml
  label: Nasdaq Data Link Time-series API
  slug: data-link-time-series
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/nasdaq-omx-group/refs/heads/main/openapi/nasdaq-omx-group-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly / Annual (per dataset)
  chargeCategories:
  - Purchase
  - Adjustment
  - Tax
  pricingCategory: Per-Dataset Subscription
description: 'FOCUS-aligned FinOps for Nasdaq Data Link APIs: free for community / open datasets and metered by a la carte premium dataset subscriptions. Cost is dataset-driven rather than call-volume-driven — the meaningful FinOps levers are which datasets are subscribed and which API keys are entitled.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Nasdaq, Inc.
  ProviderName: Nasdaq
  PublisherName: Nasdaq, Inc.
  ServiceCategory: Market Data
  ServiceName: Nasdaq Data Link
layout: finops
meters:
- aggregation: max
  dimensions:
  - dataset
  - account
  name: dataset_subscription
  unit: dataset-month
- aggregation: sum
  dimensions:
  - api_key
  - api
  - dataset
  name: api_calls
  unit: request
- aggregation: count
  dimensions:
  - api_key
  - dataset
  name: bulk_exports
  unit: export
- aggregation: count
  dimensions:
  - api_key
  - table
  name: bulk_downloads
  unit: download
name: Nasdaq Omx Group Finops
provider_name: Nasdaq
provider_slug: nasdaq-omx-group
publisher_name: Nasdaq, Inc.
service_category: Market Data / Financial Data
slug: nasdaq-omx-group-finops
source_filename: nasdaq-omx-group-finops.yml
source_heading: FinOps Profile
source_url: https://data.nasdaq.com/sign-up
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Nasdaq\nproviderId: nasdaq-omx-group\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Financial Data\n  - Capital Markets\n  - Market Data\ndescription: 'FOCUS-aligned FinOps for Nasdaq Data Link APIs: free for community / open datasets and metered\n  by a la carte premium dataset subscriptions. Cost is dataset-driven rather than call-volume-driven —\n  the meaningful FinOps levers are which datasets are subscribed and which API keys are entitled.'\nsources:\n  - https://data.nasdaq.com/sign-up\n  - https://docs.data.nasdaq.com/docs/in-depth-usage\n  - https://docs.data.nasdaq.com/docs/rate-limits-1\n  - https://help.data.nasdaq.com/article/464-what-is-included-with-my-premium-data-subscription\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec:\
  \ FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Nasdaq, Inc.\nserviceCategory: Market Data / Financial Data\nbillingModel:\n  pricingCategory: Per-Dataset Subscription\n  billingFrequency: Monthly / Annual (per dataset)\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Adjustment\n    - Tax\nfocusColumns:\n  ServiceName: Nasdaq Data Link\n  ServiceCategory: Market Data\n  ProviderName: Nasdaq\n  PublisherName: Nasdaq, Inc.\n  InvoiceIssuerName: Nasdaq, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: dataset_subscription\n    unit: dataset-month\n    aggregation: max\n    dimensions:\n      - dataset\n      - account\n  - name: api_calls\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api_key\n      - api\n      - dataset\n  - name: bulk_exports\n    unit: export\n    aggregation: count\n    dimensions:\n      - api_key\n      - dataset\n  - name: bulk_downloads\n    unit: download\n\
  \    aggregation: count\n    dimensions:\n      - api_key\n      - table\nprinciples:\n  - name: Visibility\n    description: Track Data Link subscription invoices per dataset; use the API key as the allocation\n      handle (one key per consuming application or research workstream) and read the rate-limit headers\n      to monitor headroom.\n  - name: Allocation\n    description: Map datasets to research / trading / data-science cost centers; tag each Data Link API\n      key with its owning team so subscription cost rolls up cleanly.\n  - name: Optimization\n    description: Cancel premium datasets that are not actively queried; consolidate research workloads\n      onto a smaller number of premium keys; cache historical time-series locally rather than re-pulling\n      static slices.\n  - name: Accountability\n    description: The data-platform / quant-research lead owns the dataset portfolio decision; engineering\n      owns the consumption pattern (rate-limit-friendly, cached); procurement\
  \ owns the renewal cadence.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/nasdaq-omx-group/refs/heads/main/finops/nasdaq-omx-group-finops.yml
sources:
- https://data.nasdaq.com/sign-up
- https://docs.data.nasdaq.com/docs/in-depth-usage
- https://docs.data.nasdaq.com/docs/rate-limits-1
- https://help.data.nasdaq.com/article/464-what-is-included-with-my-premium-data-subscription
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Financial Data
- Capital Markets
- Market Data
---
