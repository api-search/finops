---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: codat-platform-openapi.json
  format: json
  label: Codat Platform API
  slug: platform-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/codat/refs/heads/main/openapi/codat-platform-openapi.json
- filename: codat-lending-openapi.json
  format: json
  label: Codat Lending API
  slug: lending-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/codat/refs/heads/main/openapi/codat-lending-openapi.json
- filename: codat-bank-feeds-openapi.json
  format: json
  label: Codat Bank Feeds API
  slug: bank-feeds-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/codat/refs/heads/main/openapi/codat-bank-feeds-openapi.json
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Purchase
  - Usage
  - Tax
  - Adjustment
  pricingCategory: Subscription
description: 'FOCUS-aligned FinOps for Codat: ACC-priced enterprise subscription with daily API call quotas derived from the ACC count. Codat does not publish a public price list, so principles below focus on ACC lifecycle hygiene and module-level allocation.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Codat
  PricingCategory: Subscription
  PricingUnit: connected-company-month
  ProviderName: Codat
  PublisherName: Codat
  ServiceCategory: Unified API
  ServiceName: Codat
layout: finops
meters:
- aggregation: max
  description: Count of Active Connected Companies (ACCs) over the billing period.
  dimensions:
  - product_module
  - integration
  - environment
  name: active_connected_companies
  unit: account-month
- aggregation: sum
  description: API calls made against the Codat platform; counts against the daily ACC-derived quota.
  dimensions:
  - product_module
  - integration
  - company
  name: api_calls
  unit: request
- aggregation: max
  description: Active integration connections to upstream platforms (accounting, banking, commerce).
  dimensions:
  - integration
  - environment
  name: integration_connections
  unit: connection
- aggregation: sum
  description: Webhook events delivered (data sync notifications, rate-limit signals, etc.).
  dimensions:
  - event_type
  name: webhook_events
  unit: event
name: Codat Finops
provider_name: Codat
provider_slug: codat
publisher_name: Codat
service_category: Unified API
slug: codat-finops
source_filename: codat-finops.yml
source_heading: FinOps Profile
source_url: https://www.codat.io/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Codat\nproviderId: codat\npublisherName: Codat\nserviceCategory: Unified API\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Unified API\n  - Accounting\n  - Banking\n  - Cost Management\nnotes: Codat does not publish public pricing; the FOCUS-aligned shape below assumes an Active-Connected-Company-priced\n  subscription with optional product modules, which is consistent with how Codat positions commercial discussions.\n  Validate exact billing line-items against your signed order form.\ndescription: 'FOCUS-aligned FinOps for Codat: ACC-priced enterprise subscription with daily API call quotas\n\
  \  derived from the ACC count. Codat does not publish a public price list, so principles below focus on\n  ACC lifecycle hygiene and module-level allocation.'\nsources:\n  - https://www.codat.io/\n  - https://docs.codat.io/using-the-api/rate-limits\nbillingModel:\n  pricingCategory: Subscription\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\n    - Tax\n    - Adjustment\nfocusColumns:\n  ServiceName: Codat\n  ServiceCategory: Unified API\n  ProviderName: Codat\n  PublisherName: Codat\n  InvoiceIssuerName: Codat\n  PricingCategory: Subscription\n  PricingUnit: connected-company-month\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: active_connected_companies\n    description: Count of Active Connected Companies (ACCs) over the billing period.\n    unit: account-month\n    aggregation: max\n    dimensions:\n      - product_module\n      - integration\n      - environment\n  - name: api_calls\n    description:\
  \ API calls made against the Codat platform; counts against the daily ACC-derived quota.\n    unit: request\n    aggregation: sum\n    dimensions:\n      - product_module\n      - integration\n      - company\n  - name: integration_connections\n    description: Active integration connections to upstream platforms (accounting, banking, commerce).\n    unit: connection\n    aggregation: max\n    dimensions:\n      - integration\n      - environment\n  - name: webhook_events\n    description: Webhook events delivered (data sync notifications, rate-limit signals, etc.).\n    unit: event\n    aggregation: sum\n    dimensions:\n      - event_type\nprinciples:\n  - name: Visibility\n    description: Use the Codat dashboard to monitor ACC counts, daily quota burn-down (X-Rate-Limit headers),\n      and webhook delivery. Subscribe to `client.rateLimit.reached` to alert before quota exhaustion.\n  - name: Allocation\n    description: Tag ACCs and product modules to the consuming business line; reconcile\
  \ module utilization\n      against the order form quarterly.\n  - name: Optimization\n    description: Off-board inactive ACCs to free up daily quota (which scales linearly with ACC count);\n      cache idempotent reads and rely on incremental sync rather than full refreshes; coalesce per-company\n      polling to stay within the 10-concurrent-request-per-ACC ceiling.\n  - name: Accountability\n    description: Assign an integration owner per product module and review ACC growth against contract\n      commitments before each renewal.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/codat/refs/heads/main/finops/codat-finops.yml
sources:
- https://www.codat.io/
- https://docs.codat.io/using-the-api/rate-limits
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Unified API
- Accounting
- Banking
- Cost Management
---
