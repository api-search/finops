---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: eodhd-eod-historical-data-openapi.yml
  format: yaml
  label: EODHD End-Of-Day Historical Data API
  slug: eod-historical-data-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/eodhd/refs/heads/main/openapi/eodhd-eod-historical-data-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Purchase
  - Usage
  - Refund
  - Credit
  pricingCategory: Subscription
description: 'FOCUS-aligned FinOps for EODHD: flat per-product subscriptions (monthly or annual) plus a custom-priced commercial-use plan; usage is bounded by daily/per-minute call quotas rather than per-call charges.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: EOD Historical Data Ltd
  ProviderName: EODHD
  PublisherName: EOD Historical Data Ltd
  ServiceCategory: Market Data
  ServiceName: EODHD
layout: finops
meters:
- aggregation: sum
  dimensions:
  - product
  - billing_period
  name: subscription_fees
  unit: month
- aggregation: sum
  dimensions:
  - api_token
  - endpoint
  name: api_calls_daily
  unit: request
- aggregation: count
  name: api_tokens_active
  unit: token
name: Eodhd Finops
provider_name: EODHD
provider_slug: eodhd
publisher_name: EOD Historical Data Ltd
service_category: Market Data
slug: eodhd-finops
source_filename: eodhd-finops.yml
source_heading: FinOps Profile
source_url: https://eodhd.com/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: EODHD\nproviderId: eodhd\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Financial\n  - Market Data\ndescription: 'FOCUS-aligned FinOps for EODHD: flat per-product subscriptions (monthly or annual) plus\n  a custom-priced commercial-use plan; usage is bounded by daily/per-minute call quotas rather than per-call\n  charges.'\nsources:\n  - https://eodhd.com/pricing\n  - https://eodhd.com/financial-apis/api-for-historical-data-and-volumes\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: EOD Historical Data Ltd\nserviceCategory: Market Data\nbillingModel:\n  pricingCategory: Subscription\n  billingFrequency: Monthly\n  billingCurrency:\
  \ USD\n  chargeCategories:\n    - Purchase\n    - Usage\n    - Refund\n    - Credit\nfocusColumns:\n  ServiceName: EODHD\n  ServiceCategory: Market Data\n  ProviderName: EODHD\n  PublisherName: EOD Historical Data Ltd\n  InvoiceIssuerName: EOD Historical Data Ltd\n  BillingCurrency: USD\nmeters:\n  - name: subscription_fees\n    unit: month\n    aggregation: sum\n    dimensions:\n      - product\n      - billing_period\n  - name: api_calls_daily\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api_token\n      - endpoint\n  - name: api_tokens_active\n    unit: token\n    aggregation: count\nprinciples:\n  - name: Visibility\n    description: Track per-token call usage against the 100,000/day and 1,000/min ceilings via the EODHD\n      account dashboard; export billing receipts monthly.\n  - name: Allocation\n    description: Issue a separate API token per consuming application or team so daily call usage is\n      attributable.\n  - name: Optimization\n    description:\
  \ Use the bulk historical-series endpoint (one call covers a full ticker history) to minimize\n      call count; cache static fundamentals locally; choose annual billing for ~17% discount.\n  - name: Accountability\n    description: A single account owner pays the subscription; usage and renewal cadence should be reviewed\n      against ticker coverage actually consumed.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/eodhd/refs/heads/main/finops/eodhd-finops.yml
sources:
- https://eodhd.com/pricing
- https://eodhd.com/financial-apis/api-for-historical-data-and-volumes
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Financial
- Market Data
---
