---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: shopify-admin-rest-openapi.yml
  format: yaml
  label: Shopify Admin REST API
  slug: shopify-admin-rest-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/shopify-admin/refs/heads/main/openapi/shopify-admin-rest-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Purchase
  - Usage
  - Tax
  - Adjustment
  pricingCategory: Subscription + Take Rate
description: FOCUS-aligned FinOps for the Shopify Admin API. The Admin API is bundled with a Shopify commerce subscription; cost surfaces are the monthly plan fee, payment processing take rates, and third-party payment provider fees. API throughput is governed by GraphQL points budgets that scale with the commerce plan rather than priced per call.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Shopify Inc.
  ProviderName: Shopify
  PublisherName: Shopify Inc.
  ServiceCategory: Commerce
  ServiceName: Shopify Admin API
layout: finops
meters:
- aggregation: sum
  description: Monthly commerce plan fee (Basic, Grow, Advanced, Plus, Enterprise).
  dimensions:
  - plan
  - billing_term
  name: commerce_subscription
  unit: month
- aggregation: sum
  description: Payment processing fees on cards processed via Shopify Payments.
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
  description: GraphQL Admin API query points consumed against the per-second leak-bucket budget; not a billed line, but the primary throughput-cost meter for capacity planning.
  dimensions:
  - shop
  - api
  - operation
  name: graphql_points_consumed
  unit: point
name: Shopify Admin Finops
provider_name: Shopify Admin API
provider_slug: shopify-admin
publisher_name: Shopify Inc.
service_category: Commerce
slug: shopify-admin-finops
source_filename: shopify-admin-finops.yml
source_heading: FinOps Profile
source_url: https://www.shopify.com/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Shopify Admin API\nproviderId: shopify-admin\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - Commerce\n  - Ecommerce\n  - Admin\n  - FinOps\n  - FOCUS\ndescription: FOCUS-aligned FinOps for the Shopify Admin API. The Admin API is bundled with a Shopify\n  commerce subscription; cost surfaces are the monthly plan fee, payment processing take rates, and\n  third-party payment provider fees. API throughput is governed by GraphQL points budgets that scale\n  with the commerce plan rather than priced per call.\nsources:\n  - https://www.shopify.com/pricing\n  - https://shopify.dev/docs/api/usage/rate-limits\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName:\
  \ Shopify Inc.\nserviceCategory: Commerce\nbillingModel:\n  pricingCategory: Subscription + Take Rate\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\n    - Tax\n    - Adjustment\nfocusColumns:\n  ServiceName: Shopify Admin API\n  ServiceCategory: Commerce\n  ProviderName: Shopify\n  PublisherName: Shopify Inc.\n  InvoiceIssuerName: Shopify Inc.\n  BillingCurrency: USD\nmeters:\n  - name: commerce_subscription\n    description: Monthly commerce plan fee (Basic, Grow, Advanced, Plus, Enterprise).\n    unit: month\n    aggregation: sum\n    dimensions:\n      - plan\n      - billing_term\n  - name: card_transactions\n    description: Payment processing fees on cards processed via Shopify Payments.\n    unit: transaction\n    aggregation: sum\n    dimensions:\n      - plan\n      - channel\n      - card_brand\n      - region\n  - name: third_party_payment_fee\n    description: Per-transaction surcharge applied when using a non-Shopify\
  \ payment provider.\n    unit: transaction\n    aggregation: sum\n    dimensions:\n      - plan\n      - provider\n  - name: graphql_points_consumed\n    description: GraphQL Admin API query points consumed against the per-second leak-bucket budget;\n      not a billed line, but the primary throughput-cost meter for capacity planning.\n    unit: point\n    aggregation: sum\n    dimensions:\n      - shop\n      - api\n      - operation\nprinciples:\n  - name: Visibility\n    description: Subscription and processing fees appear on the Shopify monthly invoice and Shopify\n      Payments balance reports. API throughput is observable via GraphQL response extensions.cost\n      (requestedQueryCost, actualQueryCost, throttleStatus).\n  - name: Allocation\n    description: Allocate by shop (myshopify domain), commerce plan, and channel (online vs POS); for\n      multi-store Plus deployments, attribute by store.\n  - name: Optimization\n    description: Reduce GraphQL query cost by selecting only\
  \ needed fields, batching mutations, and\n      using bulk operations for large reads. Choose the commerce plan that matches transaction volume\n      and required GraphQL points budget rather than over-provisioning Plus.\n  - name: Accountability\n    description: Commerce/finance owns the subscription and processing-fee line; engineering owns API\n      cost via query design and leak-bucket headroom.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/shopify-admin/refs/heads/main/finops/shopify-admin-finops.yml
sources:
- https://www.shopify.com/pricing
- https://shopify.dev/docs/api/usage/rate-limits
specification: FinOps Framework
tags:
- Commerce
- Ecommerce
- Admin
- FinOps
- FOCUS
---
