---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: squarespace-commerce-api-openapi.yml
  format: yaml
  label: Squarespace Commerce API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/squarespace/refs/heads/main/openapi/squarespace-commerce-api-openapi.yml
- filename: squarespace-orders-api-openapi.yml
  format: yaml
  label: Squarespace Orders API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/squarespace/refs/heads/main/openapi/squarespace-orders-api-openapi.yml
- filename: squarespace-products-api-openapi.yml
  format: yaml
  label: Squarespace Products API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/squarespace/refs/heads/main/openapi/squarespace-products-api-openapi.yml
- filename: squarespace-inventory-api-openapi.yml
  format: yaml
  label: Squarespace Inventory API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/squarespace/refs/heads/main/openapi/squarespace-inventory-api-openapi.yml
- filename: squarespace-profiles-api-openapi.yml
  format: yaml
  label: Squarespace Profiles API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/squarespace/refs/heads/main/openapi/squarespace-profiles-api-openapi.yml
- filename: squarespace-transactions-api-openapi.yml
  format: yaml
  label: Squarespace Transactions API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/squarespace/refs/heads/main/openapi/squarespace-transactions-api-openapi.yml
- filename: squarespace-webhook-subscriptions-api-openapi.yml
  format: yaml
  label: Squarespace Webhook Subscriptions API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/squarespace/refs/heads/main/openapi/squarespace-webhook-subscriptions-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Purchase
  - Usage
  - Tax
  - Refund
  pricingCategory: Subscription + Take Rate
description: Squarespace bills the merchant for a monthly / annual website + commerce subscription; the Commerce API is included at no additional per-call cost. Transaction take-rates layer on top of the subscription on lower commerce tiers (Squarespace's Commerce Advanced removes the per-transaction fee). Concrete subscription prices and transaction-fee percentages are not on a publicly scrapeable page and are not reconciled here.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Squarespace, Inc.
  ProviderName: Squarespace
  PublisherName: Squarespace, Inc.
  ServiceCategory: E-Commerce
  ServiceName: Squarespace Commerce
layout: finops
meters:
- aggregation: sum
  dimensions:
  - plan_tier
  - billing_term
  name: site_subscription
  unit: month
- aggregation: count
  dimensions:
  - plan_tier
  - currency
  name: commerce_transactions
  unit: transaction
- aggregation: sum
  dimensions:
  - plan_tier
  - currency
  name: transaction_volume
  unit: USD
name: Squarespace Finops
provider_name: Squarespace
provider_slug: squarespace
publisher_name: Squarespace, Inc.
service_category: E-Commerce
slug: squarespace-finops
source_filename: squarespace-finops.yml
source_heading: FinOps Profile
source_url: https://www.squarespace.com/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Squarespace\nproviderId: squarespace\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Commerce\n  - E-Commerce\n  - Website Builder\n  - FinOps\n  - FOCUS\ndescription: Squarespace bills the merchant for a monthly / annual website + commerce subscription; the Commerce API is included at no additional per-call cost. Transaction take-rates layer on top of the subscription on lower commerce tiers (Squarespace's Commerce Advanced removes the per-transaction fee). Concrete subscription prices and transaction-fee percentages are not on a publicly scrapeable page and are not reconciled here.\nsources:\n  - https://www.squarespace.com/pricing\n  - https://developers.squarespace.com/commerce-apis/overview\nnotes: Per-tier subscription prices and transaction-fee percentages are gated behind a JS-rendered pricing page. Meter set is anchored to\
  \ the documented billing levers (subscription + take-rate) but exact unit prices are not reconciled.\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Squarespace, Inc.\nserviceCategory: E-Commerce\nbillingModel:\n  pricingCategory: Subscription + Take Rate\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\n    - Tax\n    - Refund\nfocusColumns:\n  ServiceName: Squarespace Commerce\n  ServiceCategory: E-Commerce\n  ProviderName: Squarespace\n  PublisherName: Squarespace, Inc.\n  InvoiceIssuerName: Squarespace, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: site_subscription\n    unit: month\n    aggregation: sum\n    dimensions:\n      - plan_tier\n      - billing_term\n  - name: commerce_transactions\n    unit: transaction\n    aggregation: count\n\
  \    dimensions:\n      - plan_tier\n      - currency\n  - name: transaction_volume\n    unit: USD\n    aggregation: sum\n    dimensions:\n      - plan_tier\n      - currency\nprinciples:\n  - name: Visibility\n    description: Inspect billing in the Squarespace merchant account dashboard; commerce activity (orders, refunds, payouts) is queryable through the Transactions and Orders endpoints of the Commerce API for downstream cost-of-channel analysis.\n  - name: Allocation\n    description: For multi-brand operators, allocate per-site subscription cost to the brand that owns the Squarespace website. Tag transactions in the Orders API by storefront / channel to attribute take-rate spend.\n  - name: Optimization\n    description: Move to Commerce Advanced when transaction-fee savings on lower tiers exceed the subscription delta. Use the Inventory and Products APIs to keep a single source of truth and avoid duplicate-listing fees across channels.\n  - name: Accountability\n    description:\
  \ E-commerce / merchant-ops team owns the Squarespace subscription and renewal; finance owns reconciliation of Squarespace payouts against the Transactions API export.\nmaintainers:\n  - name: Squarespace, Inc.\n    url: https://developers.squarespace.com/\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/squarespace/refs/heads/main/finops/squarespace-finops.yml
sources:
- https://www.squarespace.com/pricing
- https://developers.squarespace.com/commerce-apis/overview
specification: FinOps Framework
tags:
- Commerce
- E-Commerce
- Website Builder
- FinOps
- FOCUS
---
