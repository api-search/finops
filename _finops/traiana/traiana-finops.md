---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: traiana-harmony-trade-processing-openapi.yml
  format: yaml
  label: Traiana Harmony Trade Processing API
  slug: harmony-trade-processing
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/traiana/refs/heads/main/openapi/traiana-harmony-trade-processing-openapi.yml
- filename: traiana-harmony-creditlink-openapi.yml
  format: yaml
  label: Traiana Harmony CreditLink API
  slug: harmony-creditlink
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/traiana/refs/heads/main/openapi/traiana-harmony-creditlink-openapi.yml
- filename: traiana-harmony-netlink-openapi.yml
  format: yaml
  label: Traiana Harmony NetLink API
  slug: harmony-netlink
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/traiana/refs/heads/main/openapi/traiana-harmony-netlink-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  - Tax
  - Adjustment
  pricingCategory: Contracted Per-Message + Connectivity Fee
description: 'FinOps shape for Traiana: contracted post-trade network fees billed by CME Group, typically scaled by message volume, asset class, and counterparty connections. No public meter rates are published; this artifact captures structural meters.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: CME Group Inc.
  ProviderName: Traiana
  PublisherName: CME Group Inc.
  ServiceCategory: Post-Trade Network
  ServiceName: Traiana
layout: finops
meters:
- aggregation: sum
  description: Count of post-trade messages (matches, allocations, novations, give-ups) processed through the Traiana network.
  dimensions:
  - asset_class
  - service
  - counterparty
  name: post_trade_messages
  unit: message
- aggregation: avg
  description: Active counterparty connections / sessions enabled on the network for the institution.
  dimensions:
  - asset_class
  - region
  name: counterparty_connections
  unit: connection-month
- aggregation: sum
  description: Recurring network connectivity / membership fee separate from per-message pricing.
  name: connectivity_fee
  unit: month
name: Traiana Finops
provider_name: Traiana
provider_slug: traiana
publisher_name: CME Group Inc.
service_category: Post-Trade Network
slug: traiana-finops
source_filename: traiana-finops.yml
source_heading: FinOps Profile
source_url: https://www.cmegroup.com/services/traiana.html
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Traiana\nproviderId: traiana\npublisherName: CME Group Inc.\nserviceCategory: Post-Trade Network\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Post-Trade Processing\n  - Foreign Exchange\n  - Fintech\n  - FinOps\n  - FOCUS\ndescription: 'FinOps shape for Traiana: contracted post-trade network fees billed by CME Group, typically\n  scaled by message volume, asset class, and counterparty connections. No public meter rates are published;\n  this artifact captures structural meters.'\nsources:\n  - https://www.cmegroup.com/services/traiana.html\nnotes: Pricing not publicly retrievable; meters are descriptive and unpriced.\n\
  billingModel:\n  pricingCategory: Contracted Per-Message + Connectivity Fee\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Adjustment\nfocusColumns:\n  ServiceName: Traiana\n  ServiceCategory: Post-Trade Network\n  ProviderName: Traiana\n  PublisherName: CME Group Inc.\n  InvoiceIssuerName: CME Group Inc.\n  BillingCurrency: USD\nmeters:\n  - name: post_trade_messages\n    description: Count of post-trade messages (matches, allocations, novations, give-ups) processed through\n      the Traiana network.\n    unit: message\n    aggregation: sum\n    dimensions:\n      - asset_class\n      - service\n      - counterparty\n  - name: counterparty_connections\n    description: Active counterparty connections / sessions enabled on the network for the institution.\n    unit: connection-month\n    aggregation: avg\n    dimensions:\n      - asset_class\n      - region\n  - name: connectivity_fee\n    description: Recurring\
  \ network connectivity / membership fee separate from per-message pricing.\n    unit: month\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Reconcile the monthly CME Group invoice against your message logs by service line (FX\n      Match, Harmony, etc.); request a per-asset-class breakdown from the relationship manager.\n  - name: Allocation\n    description: Allocate fees to the trading desk / asset class generating the post-trade volume; tag\n      messages with the originating book or strategy.\n  - name: Optimization\n    description: Right-size connected counterparties to those actually trading; consolidate redundant\n      sessions; review service-line subscriptions (give-up, allocations, risk) annually against active\n      use.\n  - name: Accountability\n    description: Operations / middle-office head owns Traiana costs and the network agreement; trading\n      desks are accountable for the volume they generate.\nmaintainers:\n  - FN: Kin Lane\n   \
  \ email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/traiana/refs/heads/main/finops/traiana-finops.yml
sources:
- https://www.cmegroup.com/services/traiana.html
specification: FinOps Framework
tags:
- Post-Trade Processing
- Foreign Exchange
- Fintech
- FinOps
- FOCUS
---
