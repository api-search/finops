---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: uniblock-unified-api-openapi.yml
  format: yaml
  label: Uniblock Unified API
  slug: unified-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/uniblock/refs/heads/main/openapi/uniblock-unified-api-openapi.yml
- filename: uniblock-direct-api-openapi.yml
  format: yaml
  label: Uniblock Direct API
  slug: direct-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/uniblock/refs/heads/main/openapi/uniblock-direct-api-openapi.yml
- filename: uniblock-json-rpc-api-openapi.yml
  format: yaml
  label: Uniblock JSON-RPC API
  slug: json-rpc-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/uniblock/refs/heads/main/openapi/uniblock-json-rpc-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Purchase
  - Usage
  - Adjustment
  - Credit
  pricingCategory: Tiered Subscription with CU Envelope
description: FOCUS-aligned FinOps for Uniblock - monthly subscription tier plus a compute-unit (CU) envelope that meters JSON-RPC and unified-API consumption across providers and chains.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Uniblock
  PricingCategory: Subscription
  ProviderName: Uniblock
  PublisherName: Uniblock
  ServiceCategory: Web3 Infrastructure
  ServiceName: Uniblock
layout: finops
meters:
- aggregation: sum
  description: Monthly Uniblock plan subscription (Growth, Pro, Business).
  dimensions:
  - plan
  - billing_term
  name: plan_subscription
  unit: month
- aggregation: sum
  description: Compute units consumed across JSON-RPC, Unified, and Direct APIs. CU cost per call varies by method.
  dimensions:
  - api
  - method
  - chain
  - project
  name: compute_units
  unit: compute_unit
- aggregation: max
  description: Number of active projects used in the month, capped per plan tier.
  dimensions:
  - plan
  name: projects
  unit: project
name: Uniblock Finops
provider_name: Uniblock
provider_slug: uniblock
publisher_name: Uniblock
service_category: Web3 Infrastructure
slug: uniblock-finops
source_filename: uniblock-finops.yml
source_heading: FinOps Profile
source_url: https://uniblock.dev/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Uniblock\nproviderId: uniblock\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - Blockchain\n  - Web3\n  - FinOps\n  - FOCUS\ndescription: FOCUS-aligned FinOps for Uniblock - monthly subscription tier plus a compute-unit (CU)\n  envelope that meters JSON-RPC and unified-API consumption across providers and chains.\nsources:\n  - https://uniblock.dev/pricing\n  - https://docs.uniblock.dev/guides/uniblock/rate-limits\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Uniblock\nserviceCategory: Web3 Infrastructure\nbillingModel:\n  pricingCategory: Tiered Subscription with CU Envelope\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n\
  \    - Purchase\n    - Usage\n    - Adjustment\n    - Credit\nfocusColumns:\n  ServiceName: Uniblock\n  ServiceCategory: Web3 Infrastructure\n  ProviderName: Uniblock\n  PublisherName: Uniblock\n  InvoiceIssuerName: Uniblock\n  BillingCurrency: USD\n  ChargeCategory: Purchase\n  PricingCategory: Subscription\nmeters:\n  - name: plan_subscription\n    description: Monthly Uniblock plan subscription (Growth, Pro, Business).\n    unit: month\n    aggregation: sum\n    dimensions:\n      - plan\n      - billing_term\n  - name: compute_units\n    description: Compute units consumed across JSON-RPC, Unified, and Direct APIs. CU cost per call\n      varies by method.\n    unit: compute_unit\n    aggregation: sum\n    dimensions:\n      - api\n      - method\n      - chain\n      - project\n  - name: projects\n    description: Number of active projects used in the month, capped per plan tier.\n    unit: project\n    aggregation: max\n    dimensions:\n      - plan\nprinciples:\n  - name: Visibility\n\
  \    description: Track CU consumption per project in the Uniblock dashboard; correlate request volume\n      to method-level CU costs to identify cost-driver endpoints.\n  - name: Allocation\n    description: Use separate Uniblock projects per consuming team, environment, or product line so\n      CU spend can be attributed without invoice splitting.\n  - name: Optimization\n    description: Reduce CU usage with response caching, batching, lower poll frequencies, and selecting\n      cheaper unified methods over high-cost direct provider calls. Switch to annual billing for the\n      built-in discount.\n  - name: Accountability\n    description: Set CU consumption alerts ahead of plan envelope exhaustion to avoid 429s; assign\n      a project owner for each Uniblock project to handle plan upgrades and traffic anomalies.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/uniblock/refs/heads/main/finops/uniblock-finops.yml
sources:
- https://uniblock.dev/pricing
- https://docs.uniblock.dev/guides/uniblock/rate-limits
specification: FinOps Framework
tags:
- Blockchain
- Web3
- FinOps
- FOCUS
---
