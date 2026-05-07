---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: checkpoint-management-api-openapi.yml
  format: yaml
  label: Check Point Management API
  slug: management-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/checkpoint/refs/heads/main/openapi/checkpoint-management-api-openapi.yml
- filename: checkpoint-gaia-api-openapi.yml
  format: yaml
  label: Check Point Gaia API
  slug: gaia-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/checkpoint/refs/heads/main/openapi/checkpoint-gaia-api-openapi.yml
- filename: checkpoint-cloudguard-api-openapi.yml
  format: yaml
  label: Check Point CloudGuard API
  slug: cloudguard-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/checkpoint/refs/heads/main/openapi/checkpoint-cloudguard-api-openapi.yml
- filename: checkpoint-identity-awareness-api-openapi.yml
  format: yaml
  label: Check Point Identity Awareness API
  slug: identity-awareness-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/checkpoint/refs/heads/main/openapi/checkpoint-identity-awareness-api-openapi.yml
- filename: checkpoint-harmony-email-api-openapi.yml
  format: yaml
  label: Check Point Harmony Email API
  slug: harmony-email-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/checkpoint/refs/heads/main/openapi/checkpoint-harmony-email-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  - Usage
  - Tax
  - Adjustment
  pricingCategory: Subscription
description: 'FOCUS-aligned FinOps for Check Point: enterprise license + subscription model where API access is bundled into the underlying product license. Spend is tracked as discrete contractual line items (term subscriptions, support, professional services) rather than per-API-request usage.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Check Point Software Technologies Ltd.
  PricingCategory: Subscription
  ProviderName: Check Point
  PublisherName: Check Point Software Technologies Ltd.
  ServiceCategory: Security
  ServiceName: Check Point
layout: finops
meters:
- aggregation: sum
  description: Per-product term subscription line (Quantum, CloudGuard, Harmony, Infinity, Spark)
  dimensions:
  - product
  - sku
  - region
  name: product_subscription
  unit: month
- aggregation: max
  description: Throughput tier (Mbps / Gbps) attached to a Quantum gateway license
  dimensions:
  - gateway
  - blade_set
  name: gateway_throughput
  unit: Mbps
- aggregation: sum
  description: Endpoints, mailboxes, cloud assets, or users covered under Harmony / CloudGuard subscriptions
  dimensions:
  - product
  - environment
  name: protected_assets
  unit: asset
- aggregation: sum
  description: Premium / Diamond / Elite support contract line
  dimensions:
  - tier
  name: support_subscription
  unit: month
name: Checkpoint Finops
provider_name: Check Point
provider_slug: checkpoint
publisher_name: Check Point Software Technologies Ltd.
service_category: Security
slug: checkpoint-finops
source_filename: checkpoint-finops.yml
source_heading: FinOps Profile
source_url: https://www.checkpoint.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Check Point\nproviderId: checkpoint\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Cloud Security\n  - Cybersecurity\n  - Network Security\n  - Security\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps for Check Point: enterprise license + subscription model where API\n  access is bundled into the underlying product license. Spend is tracked as discrete contractual line\n  items (term subscriptions, support, professional services) rather than per-API-request usage.'\nnotes: Check Point does not expose a metered usage API for billing. FinOps shape below reflects the\n  channel-quoted enterprise license model.\nsources:\n  - https://www.checkpoint.com/\n  - https://www.checkpoint.com/products/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion:\
  \ '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Check Point Software Technologies Ltd.\nserviceCategory: Security\nbillingModel:\n  pricingCategory: Subscription\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\n    - Tax\n    - Adjustment\nfocusColumns:\n  ServiceName: Check Point\n  ServiceCategory: Security\n  ProviderName: Check Point\n  PublisherName: Check Point Software Technologies Ltd.\n  InvoiceIssuerName: Check Point Software Technologies Ltd.\n  BillingCurrency: USD\n  ChargeCategory: Purchase\n  PricingCategory: Subscription\nmeters:\n  - name: product_subscription\n    description: Per-product term subscription line (Quantum, CloudGuard, Harmony, Infinity, Spark)\n    unit: month\n    aggregation: sum\n    dimensions:\n      - product\n      - sku\n      - region\n  - name: gateway_throughput\n    description: Throughput tier (Mbps / Gbps) attached to a Quantum gateway license\n\
  \    unit: Mbps\n    aggregation: max\n    dimensions:\n      - gateway\n      - blade_set\n  - name: protected_assets\n    description: Endpoints, mailboxes, cloud assets, or users covered under Harmony / CloudGuard\n      subscriptions\n    unit: asset\n    aggregation: sum\n    dimensions:\n      - product\n      - environment\n  - name: support_subscription\n    description: Premium / Diamond / Elite support contract line\n    unit: month\n    aggregation: sum\n    dimensions:\n      - tier\nprinciples:\n  - name: Visibility\n    description: Track Check Point spend through Infinity Portal license inventory and the Check Point\n      User Center; reconcile against partner invoices for term renewals.\n  - name: Allocation\n    description: Tag licenses by gateway, business unit, and environment in the Infinity Portal so\n      cyber-security spend can be charged back to consuming organizations.\n  - name: Optimization\n    description: Right-size gateways before renewal, consolidate\
  \ blades into Infinity bundles where\n      eligible, and align license terms (1Y vs 3Y) with refresh cycles to capture multi-year discounts.\n  - name: Accountability\n    description: Security architecture owns license posture; finance owns renewal calendar; SOC owns\n      consumption telemetry and ensures unused entitlements are surfaced before renewal.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/checkpoint/refs/heads/main/finops/checkpoint-finops.yml
sources:
- https://www.checkpoint.com/
- https://www.checkpoint.com/products/
specification: FinOps Framework
tags:
- Cloud Security
- Cybersecurity
- Network Security
- Security
- FinOps
- FOCUS
---
