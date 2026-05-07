---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: alchemy-gas-manager-api-openapi.yml
  format: yaml
  label: Alchemy Gas Manager API
  slug: alchemy-gas-manager-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/alchemy/refs/heads/main/openapi/alchemy-gas-manager-api-openapi.yml
- filename: alchemy-token-api-openapi.yml
  format: yaml
  label: Alchemy Token API
  slug: alchemy-token-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/alchemy/refs/heads/main/openapi/alchemy-token-api-openapi.yml
- filename: alchemy-transfers-api-openapi.yml
  format: yaml
  label: Alchemy Transfers API
  slug: alchemy-transfers-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/alchemy/refs/heads/main/openapi/alchemy-transfers-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  - Tax
  - Credit
  - Adjustment
  pricingCategory: Pay-As-You-Go + Tiered + Custom Enterprise
description: 'FOCUS-aligned FinOps for Alchemy: Compute-Unit-based metered usage with a free quota, tiered per-1M-CU pricing on Pay-as-you-go ($0.45/1M up to 300M, $0.40/1M after), and custom-quoted Enterprise with volume discounts. Throughput is provisioned in CU/s and RPS.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Alchemy Insights, Inc.
  PricingUnit: 1M Compute Units
  ProviderName: Alchemy
  PublisherName: Alchemy Insights, Inc.
  ServiceCategory: Web3 / Blockchain Infrastructure
  ServiceName: Alchemy
layout: finops
meters:
- aggregation: sum
  description: Compute Units consumed across all Alchemy APIs
  dimensions:
  - chain
  - method
  - app
  - environment
  name: compute_units
  unit: compute-unit
- aggregation: sum
  description: Raw API requests (averages ~27 CUs per request)
  dimensions:
  - chain
  - method
  - app
  name: requests
  unit: request
- aggregation: max
  description: Purchased CU/s throughput add-ons beyond the plan's included throughput
  dimensions:
  - app
  name: throughput_addons
  unit: CU/s-month
- aggregation: max
  description: Configured Alchemy apps in the account
  dimensions:
  - chain
  name: apps
  unit: app
- aggregation: max
  description: Configured webhooks
  dimensions:
  - app
  name: webhooks
  unit: webhook
name: Alchemy Finops
provider_name: Alchemy
provider_slug: alchemy
publisher_name: Alchemy Insights, Inc.
service_category: Web3 / Blockchain Infrastructure
slug: alchemy-finops
source_filename: alchemy-finops.yml
source_heading: FinOps Profile
source_url: https://www.alchemy.com/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Alchemy\nproviderId: alchemy\npublisherName: Alchemy Insights, Inc.\nserviceCategory: Web3 / Blockchain Infrastructure\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - Blockchain\n  - Cryptocurrency\n  - Web3\n  - Account Abstraction\n  - Ethereum\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps for Alchemy: Compute-Unit-based metered usage with a free quota, tiered\n  per-1M-CU pricing on Pay-as-you-go ($0.45/1M up to 300M, $0.40/1M after), and custom-quoted Enterprise\n  with volume discounts. Throughput is provisioned in CU/s and RPS.'\nsources:\n  - https://www.alchemy.com/pricing\n  - https://www.alchemy.com/docs/reference/throughput\n\
  \  - https://focus.finops.org/focus-specification/v1-3/\nbillingModel:\n  pricingCategory: Pay-As-You-Go + Tiered + Custom Enterprise\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\nfocusColumns:\n  ServiceName: Alchemy\n  ServiceCategory: Web3 / Blockchain Infrastructure\n  ProviderName: Alchemy\n  PublisherName: Alchemy Insights, Inc.\n  InvoiceIssuerName: Alchemy Insights, Inc.\n  BillingCurrency: USD\n  ChargeCategory: Usage\n  PricingUnit: 1M Compute Units\nmeters:\n  - name: compute_units\n    description: Compute Units consumed across all Alchemy APIs\n    unit: compute-unit\n    aggregation: sum\n    dimensions:\n      - chain\n      - method\n      - app\n      - environment\n  - name: requests\n    description: Raw API requests (averages ~27 CUs per request)\n    unit: request\n    aggregation: sum\n    dimensions:\n      - chain\n      - method\n      - app\n  - name: throughput_addons\n\
  \    description: Purchased CU/s throughput add-ons beyond the plan's included throughput\n    unit: CU/s-month\n    aggregation: max\n    dimensions:\n      - app\n  - name: apps\n    description: Configured Alchemy apps in the account\n    unit: app\n    aggregation: max\n    dimensions:\n      - chain\n  - name: webhooks\n    description: Configured webhooks\n    unit: webhook\n    aggregation: max\n    dimensions:\n      - app\nprinciples:\n  - name: Visibility\n    description: Use the Alchemy dashboard's compute-unit, request-volume, and throughput-utilization views\n      per app to see consumption in near-real-time. Export usage via the Alchemy account API for ingestion\n      into FOCUS-formatted billing pipelines.\n  - name: Allocation\n    description: Allocate cost by app and team using Alchemy's per-app reporting; tag environments (dev/staging/prod)\n      via separate apps to keep prod CU spend isolated.\n  - name: Optimization\n    description: Reduce CU spend by batching\
  \ JSON-RPC calls, caching read-heavy methods, choosing CU-cheaper\n      methods (e.g. eth_getLogs over alchemy_getAssetTransfers when applicable), and using free-tier mainnets\n      for prototyping. Consider Pay-as-you-go's $0.40/1M CU tier kicking in after 300M CUs.\n  - name: Accountability\n    description: Assign budget owners per app; configure usage alerts in the Alchemy dashboard; review\n      CU and throughput trends monthly against feature roadmap and on-chain volume.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/alchemy/refs/heads/main/finops/alchemy-finops.yml
sources:
- https://www.alchemy.com/pricing
- https://www.alchemy.com/docs/reference/throughput
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Blockchain
- Cryptocurrency
- Web3
- Account Abstraction
- Ethereum
- FinOps
- FOCUS
---
