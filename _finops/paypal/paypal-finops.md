---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: paypal-billing-subscriptions-openapi-original.yml
  format: yaml
  label: PayPal Billing Subscriptions API
  slug: paypal-billing-subscriptions-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/paypal/refs/heads/main/openapi/paypal-billing-subscriptions-openapi-original.yml
- filename: paypal-catalog-products-openapi-original.yml
  format: yaml
  label: PayPal Catalog Products API
  slug: paypal-products-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/paypal/refs/heads/main/openapi/paypal-catalog-products-openapi-original.yml
- filename: paypal-checkout-orders-openapi-original.yml
  format: yaml
  label: PayPal Orders API
  slug: paypal-orders-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/paypal/refs/heads/main/openapi/paypal-checkout-orders-openapi-original.yml
- filename: paypal-customer-disputes-openapi-original.yml
  format: yaml
  label: PayPal Customer Disputes API
  slug: paypal-disputes-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/paypal/refs/heads/main/openapi/paypal-customer-disputes-openapi-original.yml
- filename: paypal-customer-partner-referrals-openapi-original.yml
  format: yaml
  label: PayPal Partner Referrals API
  slug: paypal-partner-referrals-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/paypal/refs/heads/main/openapi/paypal-customer-partner-referrals-openapi-original.yml
- filename: paypal-invoicing-openapi-original.yml
  format: yaml
  label: PayPal Invoicing API
  slug: paypal-invoicing-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/paypal/refs/heads/main/openapi/paypal-invoicing-openapi-original.yml
- filename: paypal-notification-webhooks-openapi-original.yml
  format: yaml
  label: PayPal Notification Webhooks API
  slug: paypal-notification-webhooks-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/paypal/refs/heads/main/openapi/paypal-notification-webhooks-openapi-original.yml
- filename: paypal-payment-experience-openapi-original.yml
  format: yaml
  label: PayPal Payment Experience API
  slug: paypal-payment-experience-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/paypal/refs/heads/main/openapi/paypal-payment-experience-openapi-original.yml
- filename: paypal-payments-openapi-original.yml
  format: yaml
  label: PayPal Payments API
  slug: paypal-payments-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/paypal/refs/heads/main/openapi/paypal-payments-openapi-original.yml
- filename: paypal-payouts-openapi-original.yml
  format: yaml
  label: PayPal Payouts API
  slug: paypal-payouts-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/paypal/refs/heads/main/openapi/paypal-payouts-openapi-original.yml
- filename: paypal-reporting-transactions-openapi-original.yml
  format: yaml
  label: PayPal Transaction Search (Reporting) API
  slug: paypal-reporting-transactions-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/paypal/refs/heads/main/openapi/paypal-reporting-transactions-openapi-original.yml
- filename: paypal-shipping-tracking-openapi-original.yml
  format: yaml
  label: PayPal Shipping Tracking API
  slug: paypal-shipping-tracking-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/paypal/refs/heads/main/openapi/paypal-shipping-tracking-openapi-original.yml
- filename: paypal-vault-payment-tokens-openapi-original.yml
  format: yaml
  label: PayPal Vault Payment Tokens API
  slug: paypal-payment-tokens-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/paypal/refs/heads/main/openapi/paypal-vault-payment-tokens-openapi-original.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  pricingCategory: Per-Transaction Take Rate
description: FOCUS-aligned FinOps for PayPal.
focus_columns:
  BillingCurrency: USD
  ProviderName: PayPal
  PublisherName: PayPal
  ServiceCategory: Payments
  ServiceName: PayPal
layout: finops
meters:
- aggregation: sum
  dimensions:
  - channel
  - currency
  - country
  name: checkout_transactions
  unit: transaction
- aggregation: sum
  name: transaction_volume
  unit: USD
- aggregation: sum
  name: ach_transactions
  unit: transaction
- aggregation: sum
  name: international_transactions
  unit: transaction
name: Paypal Finops
provider_name: PayPal
provider_slug: paypal
publisher_name: PayPal
service_category: Payments
slug: paypal-finops
source_filename: paypal-finops.yml
source_heading: FinOps Profile
source_url: https://www.paypal.com/us/business/paypal-business-fees
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: PayPal\nproviderId: paypal\ncreated: '2026-05-04'\nmodified: '2026-05-04'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Payments\ndescription: FOCUS-aligned FinOps for PayPal.\nsources:\n  - https://www.paypal.com/us/business/paypal-business-fees\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: PayPal\nserviceCategory: Payments\nbillingModel:\n  pricingCategory: Per-Transaction Take Rate\n  billingFrequency: Monthly\n  billingCurrency: USD\nfocusColumns:\n  ServiceName: PayPal\n  ServiceCategory: Payments\n  ProviderName: PayPal\n  PublisherName: PayPal\n  BillingCurrency: USD\nmeters:\n  - name: checkout_transactions\n    unit: transaction\n    aggregation: sum\n    dimensions:\n\
  \      - channel\n      - currency\n      - country\n  - name: transaction_volume\n    unit: USD\n    aggregation: sum\n  - name: ach_transactions\n    unit: transaction\n    aggregation: sum\n  - name: international_transactions\n    unit: transaction\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Track PayPal consumption monthly.\n  - name: Allocation\n    description: Tag usage to teams/cost centers.\n  - name: Optimization\n    description: Right-size; reclaim unused entitlements.\n  - name: Accountability\n    description: Set spend alerts; quarterly review.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/paypal/refs/heads/main/finops/paypal-finops.yml
sources:
- https://www.paypal.com/us/business/paypal-business-fees
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Payments
---
