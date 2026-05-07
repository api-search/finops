---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: woocommerce-rest-api-openapi.yml
  format: yaml
  label: WooCommerce REST API
  slug: rest-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/woocommerce/refs/heads/main/openapi/woocommerce-rest-api-openapi.yml
- filename: woocommerce-store-api-openapi.yml
  format: yaml
  label: WooCommerce Store API
  slug: store-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/woocommerce/refs/heads/main/openapi/woocommerce-store-api-openapi.yml
- filename: woocommerce-webhooks-asyncapi.yml
  format: yaml
  label: WooCommerce Webhook Events
  slug: webhook-events
  spec_type: AsyncAPI
  url: https://raw.githubusercontent.com/api-evangelist/woocommerce/refs/heads/main/asyncapi/woocommerce-webhooks-asyncapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  pricingCategory: Free Core + Hosting + Extensions + Payment Fees
description: FOCUS-aligned FinOps for WooCommerce.
focus_columns:
  BillingCurrency: USD
  ProviderName: WooCommerce
  PublisherName: WooCommerce
  ServiceCategory: E-Commerce
  ServiceName: WooCommerce
layout: finops
meters:
- aggregation: sum
  name: hosting_costs
  unit: month
- aggregation: sum
  name: payment_processing_fees
  unit: USD
- aggregation: max
  name: extension_subscriptions
  unit: extension-year
- aggregation: sum
  name: transactions
  unit: transaction
- aggregation: sum
  name: transaction_volume
  unit: USD
name: Woocommerce Finops
provider_name: WooCommerce
provider_slug: woocommerce
publisher_name: WooCommerce
service_category: E-Commerce
slug: woocommerce-finops
source_filename: woocommerce-finops.yml
source_heading: FinOps Profile
source_url: https://woocommerce.com/pricing/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: WooCommerce\nproviderId: woocommerce\ncreated: '2026-05-04'\nmodified: '2026-05-04'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - E-Commerce\ndescription: FOCUS-aligned FinOps for WooCommerce.\nsources:\n  - https://woocommerce.com/pricing/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: WooCommerce\nserviceCategory: E-Commerce\nbillingModel:\n  pricingCategory: Free Core + Hosting + Extensions + Payment Fees\n  billingFrequency: Monthly\n  billingCurrency: USD\nfocusColumns:\n  ServiceName: WooCommerce\n  ServiceCategory: E-Commerce\n  ProviderName: WooCommerce\n  PublisherName: WooCommerce\n  BillingCurrency: USD\nmeters:\n  - name: hosting_costs\n    unit: month\n   \
  \ aggregation: sum\n  - name: payment_processing_fees\n    unit: USD\n    aggregation: sum\n  - name: extension_subscriptions\n    unit: extension-year\n    aggregation: max\n  - name: transactions\n    unit: transaction\n    aggregation: sum\n  - name: transaction_volume\n    unit: USD\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Track WooCommerce consumption monthly.\n  - name: Allocation\n    description: Tag usage to teams/cost centers.\n  - name: Optimization\n    description: Right-size; reclaim unused entitlements.\n  - name: Accountability\n    description: Set spend alerts; quarterly review.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/woocommerce/refs/heads/main/finops/woocommerce-finops.yml
sources:
- https://woocommerce.com/pricing/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- E-Commerce
---
