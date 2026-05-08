---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Subscription
  - Usage
  pricingCategory: Subscription with Metered CU Allowance
description: FinOps view of Solscan. Subscription tiers gate a monthly compute-unit (CU) allowance plus a per-second rate cap. Per-call CU cost varies by endpoint. Allocation is by API key.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Subscription
  InvoiceIssuerName: Solscan
  ProviderName: Solscan
  PublisherName: Solscan
  ServiceCategory: Crypto Explorer
  ServiceName: Solscan Pro API
layout: finops
meters:
- aggregation: sum
  description: Monthly Pro subscription per API key.
  dimensions:
  - api_key
  name: subscription
  unit: month
- aggregation: sum
  description: Per-call compute unit consumption against monthly allowance.
  dimensions:
  - api_key
  - endpoint
  name: compute_units
  unit: cu
name: Solscan Finops
provider_name: Solscan
provider_slug: solscan
publisher_name: Solscan
service_category: Crypto Explorer
slug: solscan-finops
source_filename: solscan-finops.yml
source_heading: FinOps Profile
source_url: https://solscan.io/apis
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Solscan\nproviderId: solscan\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: true\ntags:\n  - Solana\n  - Explorer\n  - FinOps\n  - FOCUS\ndescription: >-\n  FinOps view of Solscan. Subscription tiers gate a monthly compute-unit (CU) allowance plus a\n  per-second rate cap. Per-call CU cost varies by endpoint. Allocation is by API key.\nsources:\n  - https://solscan.io/apis\n  - https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Solscan\nserviceCategory: Crypto Explorer\nbillingModel:\n  pricingCategory: Subscription with Metered CU Allowance\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n \
  \   - Subscription\n    - Usage\nfocusColumns:\n  ServiceName: Solscan Pro API\n  ServiceCategory: Crypto Explorer\n  ProviderName: Solscan\n  PublisherName: Solscan\n  InvoiceIssuerName: Solscan\n  BillingCurrency: USD\n  ChargeCategory: Subscription\nmeters:\n  - name: subscription\n    description: Monthly Pro subscription per API key.\n    unit: month\n    aggregation: sum\n    dimensions:\n      - api_key\n  - name: compute_units\n    description: Per-call compute unit consumption against monthly allowance.\n    unit: cu\n    aggregation: sum\n    dimensions:\n      - api_key\n      - endpoint\nprinciples:\n  - name: Visibility\n    description: Track per-endpoint CU consumption to forecast tier sufficiency.\n  - name: Allocation\n    description: Tag each API key to a single owning workload.\n  - name: Optimization\n    description: Cache hot endpoints; bundle queries to reduce CU consumption.\n  - name: Accountability\n    description: Assign a billing owner per API key; review\
  \ monthly CU vs allowance.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/solscan/refs/heads/main/finops/solscan-finops.yml
sources:
- https://solscan.io/apis
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Solana
- Explorer
- FinOps
- FOCUS
---
