---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: shopify-api-openapi.yml
  format: yaml
  label: Shopify Admin REST API
  slug: shopify-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/shopify/refs/heads/main/openapi/shopify-api-openapi.yml
- filename: shopify-ajax-api-openapi.yml
  format: yaml
  label: Shopify Ajax API
  slug: ajax-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/shopify/refs/heads/main/openapi/shopify-ajax-api-openapi.yml
- filename: shopify-webhooks-api-openapi.yml
  format: yaml
  label: Shopify Webhooks API
  slug: webhooks-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/shopify/refs/heads/main/openapi/shopify-webhooks-api-openapi.yml
- filename: shopify-multipass-api-openapi.yml
  format: yaml
  label: Shopify Multipass API
  slug: multipass-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/shopify/refs/heads/main/openapi/shopify-multipass-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  pricingCategory: Subscription + Take Rate
description: 'FOCUS-aligned FinOps for Shopify: monthly subscription + per-transaction take rate.'
focus_columns:
  BillingCurrency: USD
  ProviderName: Shopify
  PublisherName: Shopify Inc.
  ServiceCategory: E-Commerce Platform
  ServiceName: Shopify
layout: finops
meters:
- aggregation: sum
  dimensions:
  - plan
  name: subscription_months
  unit: month
- aggregation: sum
  dimensions:
  - card_present
  - currency
  name: card_transactions
  unit: transaction
- aggregation: sum
  name: transaction_volume
  unit: USD
- aggregation: sum
  name: third_party_gateway_volume
  unit: USD
- aggregation: sum
  name: shopify_shipping
  unit: label
name: Shopify Finops
provider_name: Shopify
provider_slug: shopify
publisher_name: Shopify Inc.
service_category: E-Commerce Platform
slug: shopify-finops
source_filename: shopify-finops.yml
source_heading: FinOps Profile
source_url: https://www.shopify.com/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Shopify\nproviderId: shopify\ncreated: '2026-05-04'\nmodified: '2026-05-04'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Commerce\ndescription: 'FOCUS-aligned FinOps for Shopify: monthly subscription + per-transaction take rate.'\nsources:\n  - https://www.shopify.com/pricing\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Shopify Inc.\nserviceCategory: E-Commerce Platform\nbillingModel:\n  pricingCategory: Subscription + Take Rate\n  billingFrequency: Monthly\n  billingCurrency: USD\nfocusColumns:\n  ServiceName: Shopify\n  ServiceCategory: E-Commerce Platform\n  ProviderName: Shopify\n  PublisherName: Shopify Inc.\n  BillingCurrency: USD\nmeters:\n  - name: subscription_months\n\
  \    unit: month\n    aggregation: sum\n    dimensions:\n      - plan\n  - name: card_transactions\n    unit: transaction\n    aggregation: sum\n    dimensions:\n      - card_present\n      - currency\n  - name: transaction_volume\n    unit: USD\n    aggregation: sum\n  - name: third_party_gateway_volume\n    unit: USD\n    aggregation: sum\n  - name: shopify_shipping\n    unit: label\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Pull payouts and Orders API daily; reconcile Shopify Payments fees against ledger.\n  - name: Allocation\n    description: Tag orders with channel/source for per-channel margin reporting.\n  - name: Optimization\n    description: Upgrade to Advanced/Plus when third-party gateway fees outweigh subscription delta.\n  - name: Accountability\n    description: Review monthly fee report; renegotiate gateway rates above $1M GMV.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/shopify/refs/heads/main/finops/shopify-finops.yml
sources:
- https://www.shopify.com/pricing
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Commerce
---
