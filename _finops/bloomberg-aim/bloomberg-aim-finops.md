---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: bloomberg-data-license-api.yml
  format: yaml
  label: Bloomberg Data License API
  slug: bloomberg-data-license-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/bloomberg-aim/refs/heads/main/openapi/bloomberg-data-license-api.yml
- filename: bloomberg-emsx-api.yml
  format: yaml
  label: Bloomberg EMSX API
  slug: bloomberg-emsx-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/bloomberg-aim/refs/heads/main/openapi/bloomberg-emsx-api.yml
- filename: bloomberg-http-api.yml
  format: yaml
  label: Bloomberg HTTP API
  slug: bloomberg-http-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/bloomberg-aim/refs/heads/main/openapi/bloomberg-http-api.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  - Tax
  - Adjustment
  pricingCategory: Enterprise Subscription (Negotiated)
description: 'FOCUS-aligned FinOps placeholder for Bloomberg AIM: enterprise buy-side OMS / IBOR platform billed under a contract-negotiated annual subscription typically combined with named-user seats and Bloomberg market-data feeds.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Bloomberg L.P.
  ProviderName: Bloomberg
  PublisherName: Bloomberg L.P.
  ServiceCategory: Buy-side OMS / IBOR
  ServiceName: Bloomberg AIM
layout: finops
meters:
- aggregation: sum
  dimensions:
  - module
  - tenant
  name: aim_subscription
  unit: year
- aggregation: max
  dimensions:
  - tenant
  - role
  name: aim_named_users
  unit: seat
- aggregation: sum
  dimensions:
  - asset_class
  - venue
  name: aim_orders
  unit: order
- aggregation: sum
  dimensions:
  - feed
  - exchange
  name: market_data_passthrough
  unit: record
name: Bloomberg Aim Finops
provider_name: Bloomberg AIM
provider_slug: bloomberg-aim
publisher_name: Bloomberg L.P.
service_category: Buy-side OMS / IBOR
slug: bloomberg-aim-finops
source_filename: bloomberg-aim-finops.yml
source_heading: FinOps Profile
source_url: https://www.bloomberg.com/professional/products/bloomberg-terminal/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Bloomberg AIM\nproviderId: bloomberg-aim\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Order Management\n  - Portfolio Management\n  - Trading\ndescription: 'FOCUS-aligned FinOps placeholder for Bloomberg AIM: enterprise buy-side OMS / IBOR\n  platform billed under a contract-negotiated annual subscription typically combined with named-user\n  seats and Bloomberg market-data feeds.'\nsources:\n  - https://www.bloomberg.com/professional/products/bloomberg-terminal/\nnotes: AIM commercial terms are bundled into the Bloomberg Enterprise contract; reconcile against\n  the active subscription for actual fee structure.\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\n\
  publisherName: Bloomberg L.P.\nserviceCategory: Buy-side OMS / IBOR\nbillingModel:\n  pricingCategory: Enterprise Subscription (Negotiated)\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Tax\n    - Adjustment\nfocusColumns:\n  ServiceName: Bloomberg AIM\n  ServiceCategory: Buy-side OMS / IBOR\n  ProviderName: Bloomberg\n  PublisherName: Bloomberg L.P.\n  InvoiceIssuerName: Bloomberg L.P.\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: aim_subscription\n    unit: year\n    aggregation: sum\n    dimensions:\n      - module\n      - tenant\n  - name: aim_named_users\n    unit: seat\n    aggregation: max\n    dimensions:\n      - tenant\n      - role\n  - name: aim_orders\n    unit: order\n    aggregation: sum\n    dimensions:\n      - asset_class\n      - venue\n  - name: market_data_passthrough\n    unit: record\n    aggregation: sum\n    dimensions:\n      - feed\n      - exchange\nprinciples:\n  - name: Visibility\n\
  \    description: Use AIM administration and Bloomberg client-services usage reports to track\n      module activation, named-user counts, and order throughput.\n  - name: Allocation\n    description: Map AIM tenants and modules to the consuming desk / strategy for chargeback;\n      reconcile against the bundled Bloomberg Enterprise invoice.\n  - name: Optimization\n    description: Reclaim unused AIM seats during annual renewal; align AIM module mix with\n      portfolio strategy; consolidate market-data passthrough into shared B-PIPE rather than\n      per-AIM-tenant feeds where possible.\n  - name: Accountability\n    description: Designate an AIM contract owner per legal entity; review utilization quarterly\n      with Bloomberg Enterprise client services.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/bloomberg-aim/refs/heads/main/finops/bloomberg-aim-finops.yml
sources:
- https://www.bloomberg.com/professional/products/bloomberg-terminal/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Order Management
- Portfolio Management
- Trading
---
