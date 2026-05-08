---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: apple-pay-js-openapi.yml
  format: yaml
  label: Apple Pay JS API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/apple-pay/refs/heads/main/openapi/apple-pay-js-openapi.yml
- filename: apple-pay-payment-token-openapi.yml
  format: yaml
  label: Apple Pay Payment Token API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/apple-pay/refs/heads/main/openapi/apple-pay-payment-token-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Annual (Developer Program)
  chargeCategories:
  - Purchase
  - Tax
  pricingCategory: No-Charge (Free for Merchants) + Annual Membership Prerequisite
description: 'FOCUS-aligned FinOps view for Apple Pay: Apple does not charge merchants directly. Direct Apple-billed cost is limited to the annual Apple Developer Program fee ($99/year individual or organization, $299/year enterprise). All transaction-level economics live with the merchant''s payment processor (Stripe, Adyen, Braintree, etc.) — Apple Pay is a tokenization layer on top, not a separately metered service.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Apple Inc.
  PricingCategory: Subscription (prerequisite only)
  ProviderName: Apple
  PublisherName: Apple Inc.
  ServiceCategory: Payments / Digital Wallet
  ServiceName: Apple Pay
layout: finops
meters:
- aggregation: sum
  description: Annual Apple Developer Program membership required for Merchant ID and certificates
  dimensions:
  - membership_type
  - team_id
  name: developer_program_membership
  unit: year
- aggregation: sum
  description: Count of completed Apple Pay transactions (telemetry; billed by underlying processor, not Apple)
  dimensions:
  - merchant_id
  - country
  - card_brand
  name: apple_pay_transactions
  unit: transaction
- aggregation: sum
  description: Calls to apple-pay-gateway.apple.com for merchant session creation
  dimensions:
  - merchant_id
  - environment
  name: merchant_validation_calls
  unit: request
- aggregation: sum
  description: Processor-billed fees on Apple Pay transactions (allocated to the same FinOps domain as other card spend)
  dimensions:
  - processor
  - merchant_id
  name: processor_fees
  unit: transaction
name: Apple Pay Finops
provider_name: Apple Pay
provider_slug: apple-pay
publisher_name: Apple Inc.
service_category: Payments / Digital Wallet
slug: apple-pay-finops
source_filename: apple-pay-finops.yml
source_heading: FinOps Profile
source_url: https://developer.apple.com/apple-pay/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Apple Pay\nproviderId: apple-pay\npublisherName: Apple Inc.\nserviceCategory: Payments / Digital Wallet\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Payments\n  - Apple\ndescription: 'FOCUS-aligned FinOps view for Apple Pay: Apple does not charge merchants directly. Direct\n  Apple-billed cost is limited to the annual Apple Developer Program fee ($99/year individual or organization,\n  $299/year enterprise). All transaction-level economics live with the merchant''s payment processor (Stripe,\n  Adyen, Braintree, etc.) — Apple Pay is a tokenization layer on top, not a separately metered service.'\n\
  sources:\n  - https://developer.apple.com/apple-pay/\n  - https://developer.apple.com/programs/\nbillingModel:\n  pricingCategory: No-Charge (Free for Merchants) + Annual Membership Prerequisite\n  billingFrequency: Annual (Developer Program)\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Tax\nfocusColumns:\n  ServiceName: Apple Pay\n  ServiceCategory: Payments / Digital Wallet\n  ProviderName: Apple\n  PublisherName: Apple Inc.\n  InvoiceIssuerName: Apple Inc.\n  BillingCurrency: USD\n  ChargeCategory: Purchase\n  PricingCategory: Subscription (prerequisite only)\nmeters:\n  - name: developer_program_membership\n    description: Annual Apple Developer Program membership required for Merchant ID and certificates\n    unit: year\n    aggregation: sum\n    dimensions:\n      - membership_type\n      - team_id\n  - name: apple_pay_transactions\n    description: Count of completed Apple Pay transactions (telemetry; billed by underlying processor,\n      not Apple)\n  \
  \  unit: transaction\n    aggregation: sum\n    dimensions:\n      - merchant_id\n      - country\n      - card_brand\n  - name: merchant_validation_calls\n    description: Calls to apple-pay-gateway.apple.com for merchant session creation\n    unit: request\n    aggregation: sum\n    dimensions:\n      - merchant_id\n      - environment\n  - name: processor_fees\n    description: Processor-billed fees on Apple Pay transactions (allocated to the same FinOps domain\n      as other card spend)\n    unit: transaction\n    aggregation: sum\n    dimensions:\n      - processor\n      - merchant_id\nprinciples:\n  - name: Visibility\n    description: Track Apple Pay transaction volume in App Store Connect and via the merchant's payment\n      processor dashboards (Stripe, Adyen, Braintree). Apple-side charges are limited to the developer\n      program invoice.\n  - name: Allocation\n    description: Allocate the developer program fee to the engineering org owning the Apple ecosystem\n      footprint;\
  \ allocate transaction processor fees per merchant ID / business unit.\n  - name: Optimization\n    description: Use the Apple Developer Enterprise Program only when distributing in-house apps; otherwise\n      consolidate teams under a single Organization membership. Negotiate processor blended rates that\n      include Apple Pay token volume.\n  - name: Accountability\n    description: Mobile / Web Engineering owns the Apple Developer Program account and Merchant ID lifecycle;\n      Finance / Payments team owns processor contracts and chargeback monitoring.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/apple-pay/refs/heads/main/finops/apple-pay-finops.yml
sources:
- https://developer.apple.com/apple-pay/
- https://developer.apple.com/programs/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Payments
- Apple
---
