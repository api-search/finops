---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: shopify-storefront-openapi.yml
  format: yaml
  label: Shopify Storefront API
  slug: shopify-storefront-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/shopify-storefront/refs/heads/main/openapi/shopify-storefront-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Purchase
  - Usage
  - Tax
  - Adjustment
  pricingCategory: Subscription + Take Rate
description: FOCUS-aligned FinOps for the Shopify Storefront API. The Storefront API has no per-call fees and no published rate limits; cost flows through the merchant's commerce subscription and the payment processing fees on orders that flow through the Storefront-built checkout.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Shopify Inc.
  ProviderName: Shopify
  PublisherName: Shopify Inc.
  ServiceCategory: Commerce
  ServiceName: Shopify Storefront API
layout: finops
meters:
- aggregation: sum
  description: Monthly commerce plan fee that includes Storefront API entitlement.
  dimensions:
  - plan
  - billing_term
  name: commerce_subscription
  unit: month
- aggregation: sum
  description: Payment processing fees on orders placed through the Storefront-driven checkout.
  dimensions:
  - plan
  - channel
  - card_brand
  - region
  name: card_transactions
  unit: transaction
- aggregation: sum
  description: Per-transaction surcharge applied when using a non-Shopify payment provider.
  dimensions:
  - plan
  - provider
  name: third_party_payment_fee
  unit: transaction
- aggregation: sum
  description: Storefront API requests; not billed per call but useful as a capacity and abuse-detection meter for headless deployments.
  dimensions:
  - shop
  - operation
  name: storefront_requests
  unit: request
name: Shopify Storefront Finops
provider_name: Shopify Storefront API
provider_slug: shopify-storefront
publisher_name: Shopify Inc.
service_category: Commerce
slug: shopify-storefront-finops
source_filename: shopify-storefront-finops.yml
source_heading: FinOps Profile
source_url: https://www.shopify.com/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Shopify Storefront API\nproviderId: shopify-storefront\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - Commerce\n  - Ecommerce\n  - Headless\n  - GraphQL\n  - FinOps\n  - FOCUS\ndescription: FOCUS-aligned FinOps for the Shopify Storefront API. The Storefront API has no per-call\n  fees and no published rate limits; cost flows through the merchant's commerce subscription and the\n  payment processing fees on orders that flow through the Storefront-built checkout.\nsources:\n  - https://www.shopify.com/pricing\n  - https://shopify.dev/docs/api/usage/rate-limits\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Shopify Inc.\nserviceCategory: Commerce\nbillingModel:\n\
  \  pricingCategory: Subscription + Take Rate\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\n    - Tax\n    - Adjustment\nfocusColumns:\n  ServiceName: Shopify Storefront API\n  ServiceCategory: Commerce\n  ProviderName: Shopify\n  PublisherName: Shopify Inc.\n  InvoiceIssuerName: Shopify Inc.\n  BillingCurrency: USD\nmeters:\n  - name: commerce_subscription\n    description: Monthly commerce plan fee that includes Storefront API entitlement.\n    unit: month\n    aggregation: sum\n    dimensions:\n      - plan\n      - billing_term\n  - name: card_transactions\n    description: Payment processing fees on orders placed through the Storefront-driven checkout.\n    unit: transaction\n    aggregation: sum\n    dimensions:\n      - plan\n      - channel\n      - card_brand\n      - region\n  - name: third_party_payment_fee\n    description: Per-transaction surcharge applied when using a non-Shopify payment provider.\n    unit: transaction\n\
  \    aggregation: sum\n    dimensions:\n      - plan\n      - provider\n  - name: storefront_requests\n    description: Storefront API requests; not billed per call but useful as a capacity and abuse-detection\n      meter for headless deployments.\n    unit: request\n    aggregation: sum\n    dimensions:\n      - shop\n      - operation\nprinciples:\n  - name: Visibility\n    description: Subscription, processing fees, and refunds appear on the Shopify monthly invoice and\n      Shopify Payments balance reports. Storefront request counts are observable through the consumer's\n      own client/CDN telemetry, not a Shopify-billed line.\n  - name: Allocation\n    description: Allocate by myshopify domain and channel (Hydrogen storefront, custom headless, Buy\n      SDK embed); attribute card-fee spend to the originating storefront.\n  - name: Optimization\n    description: Cache GraphQL responses at the edge (Hydrogen / Oxygen / CDN) to reduce origin load,\n      and choose the commerce\
  \ plan that matches transaction volume rather than over-paying for Plus\n      when API throughput is unconstrained.\n  - name: Accountability\n    description: Commerce/finance owns subscription and processing-fee spend; engineering owns Storefront\n      request behavior, security signals (430), and checkout throttle handling.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/shopify-storefront/refs/heads/main/finops/shopify-storefront-finops.yml
sources:
- https://www.shopify.com/pricing
- https://shopify.dev/docs/api/usage/rate-limits
specification: FinOps Framework
tags:
- Commerce
- Ecommerce
- Headless
- GraphQL
- FinOps
- FOCUS
---
