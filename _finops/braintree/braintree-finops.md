---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: braintree-payments-openapi.yml
  format: yaml
  label: Braintree Payments API
  slug: payments-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/braintree/refs/heads/main/openapi/braintree-payments-openapi.yml
- filename: braintree-webhooks-asyncapi.yml
  format: yaml
  label: Braintree Webhooks
  slug: webhooks
  spec_type: AsyncAPI
  url: https://raw.githubusercontent.com/api-evangelist/braintree/refs/heads/main/asyncapi/braintree-webhooks-asyncapi.yml
- filename: braintree-payments-openapi.yml
  format: yaml
  label: Braintree Vault API
  slug: vault-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/braintree/refs/heads/main/openapi/braintree-payments-openapi.yml
- filename: braintree-subscriptions-openapi.yml
  format: yaml
  label: Braintree Subscriptions API
  slug: subscriptions-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/braintree/refs/heads/main/openapi/braintree-subscriptions-openapi.yml
billing_model:
  billingCurrency: USD (settlement varies)
  billingFrequency: Continuous Settlement
  chargeCategories:
  - Usage
  - Adjustment
  - Refund
  - Tax
  pricingCategory: Take Rate
description: 'FOCUS-aligned FinOps for Braintree: pure take-rate per-transaction pricing across cards, digital wallets, Venmo and ACH, with surcharges for non-USD presentment and non-US issued cards plus per-incident chargeback fees and optional Chargeback Protection / Fraud Protection Lite.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: PayPal, Inc.
  PricingCategory: Standard
  PricingUnit: transaction
  ProviderName: Braintree
  PublisherName: PayPal, Inc.
  ServiceCategory: Payments
  ServiceName: Braintree
layout: finops
meters:
- aggregation: sum
  description: Card and digital wallet transactions priced at 2.89% + $0.29.
  dimensions:
  - card_brand
  - country
  - currency
  - merchant_account
  name: card_transactions
  unit: transaction
- aggregation: sum
  description: Venmo transactions priced at 3.49% + $0.49 (US only).
  dimensions:
  - merchant_account
  name: venmo_transactions
  unit: transaction
- aggregation: sum
  description: ACH Direct Debit transactions priced at 0.75% capped at $5.00.
  dimensions:
  - merchant_account
  name: ach_transactions
  unit: transaction
- aggregation: sum
  description: $0.15 per transaction pass-through fee for merchants with a direct American Express account.
  dimensions:
  - merchant_account
  name: amex_passthrough
  unit: transaction
- aggregation: sum
  description: $15.00 per disputed transaction.
  dimensions:
  - merchant_account
  - reason_code
  name: chargebacks
  unit: dispute
- aggregation: sum
  description: $5.00 per ACH return / unauthorized claim.
  dimensions:
  - merchant_account
  name: ach_returns
  unit: incident
- aggregation: sum
  description: Add-on rate (starting at 0.4%) on transactions covered by Chargeback Protection.
  dimensions:
  - merchant_account
  name: chargeback_protection
  unit: transaction
- aggregation: sum
  description: Fraud Protection Lite inquiries at $0.05 each.
  dimensions:
  - merchant_account
  name: fraud_protection_inquiries
  unit: inquiry
name: Braintree Finops
provider_name: braintree
provider_slug: braintree
publisher_name: PayPal, Inc.
service_category: Payments
slug: braintree-finops
source_filename: braintree-finops.yml
source_heading: FinOps Profile
source_url: https://www.paypal.com/us/enterprise/paypal-braintree-fees
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Braintree\nproviderId: braintree\npublisherName: PayPal, Inc.\nserviceCategory: Payments\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - Payments\n  - Credit Cards\n  - PayPal\n  - Venmo\n  - ACH\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps for Braintree: pure take-rate per-transaction pricing across cards,\n  digital wallets, Venmo and ACH, with surcharges for non-USD presentment and non-US issued cards plus\n  per-incident chargeback fees and optional Chargeback Protection / Fraud Protection Lite.'\nsources:\n  - https://www.paypal.com/us/enterprise/paypal-braintree-fees\n  - https://developer.paypal.com/braintree/docs\n\
  billingModel:\n  pricingCategory: Take Rate\n  billingFrequency: Continuous Settlement\n  billingCurrency: USD (settlement varies)\n  chargeCategories:\n    - Usage\n    - Adjustment\n    - Refund\n    - Tax\nfocusColumns:\n  ServiceName: Braintree\n  ServiceCategory: Payments\n  ProviderName: Braintree\n  PublisherName: PayPal, Inc.\n  InvoiceIssuerName: PayPal, Inc.\n  BillingCurrency: USD\n  PricingCategory: Standard\n  PricingUnit: transaction\nmeters:\n  - name: card_transactions\n    description: Card and digital wallet transactions priced at 2.89% + $0.29.\n    unit: transaction\n    aggregation: sum\n    dimensions:\n      - card_brand\n      - country\n      - currency\n      - merchant_account\n  - name: venmo_transactions\n    description: Venmo transactions priced at 3.49% + $0.49 (US only).\n    unit: transaction\n    aggregation: sum\n    dimensions:\n      - merchant_account\n  - name: ach_transactions\n    description: ACH Direct Debit transactions priced at 0.75% capped\
  \ at $5.00.\n    unit: transaction\n    aggregation: sum\n    dimensions:\n      - merchant_account\n  - name: amex_passthrough\n    description: $0.15 per transaction pass-through fee for merchants with a direct American Express\n      account.\n    unit: transaction\n    aggregation: sum\n    dimensions:\n      - merchant_account\n  - name: chargebacks\n    description: $15.00 per disputed transaction.\n    unit: dispute\n    aggregation: sum\n    dimensions:\n      - merchant_account\n      - reason_code\n  - name: ach_returns\n    description: $5.00 per ACH return / unauthorized claim.\n    unit: incident\n    aggregation: sum\n    dimensions:\n      - merchant_account\n  - name: chargeback_protection\n    description: Add-on rate (starting at 0.4%) on transactions covered by Chargeback Protection.\n    unit: transaction\n    aggregation: sum\n    dimensions:\n      - merchant_account\n  - name: fraud_protection_inquiries\n    description: Fraud Protection Lite inquiries at $0.05 each.\n\
  \    unit: inquiry\n    aggregation: sum\n    dimensions:\n      - merchant_account\nprinciples:\n  - name: Visibility\n    description: Pull transaction-level data via the Transaction Search API and the Braintree Control\n      Panel reports; reconcile gross volume, fees, refunds, and disputes daily.\n  - name: Allocation\n    description: Use sub-merchant accounts and order metadata to attribute revenue and fees to product\n      lines, brands, or marketplaces.\n  - name: Optimization\n    description: Negotiate custom interchange-plus / volume rates as processing history matures, route\n      eligible volume through preferred payment methods, mitigate disputes early with Chargeback Protection,\n      and minimize cross-border surcharges via local presentment currencies.\n  - name: Accountability\n    description: Designate a payments owner; review effective take rate, dispute rate, and refund rate\n      monthly; alert on variance against modeled cost-of-payments.\nmaintainers:\n  -\
  \ FN: Kin Lane\n    email: info@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/braintree/refs/heads/main/finops/braintree-finops.yml
sources:
- https://www.paypal.com/us/enterprise/paypal-braintree-fees
- https://developer.paypal.com/braintree/docs
specification: FinOps Framework
tags:
- Payments
- Credit Cards
- PayPal
- Venmo
- ACH
- FinOps
- FOCUS
---
