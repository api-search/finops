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
  - Adjustment
  pricingCategory: Subscription with Metered Credit Allowance
description: FinOps view of Dune. Subscription tier governs monthly credit allowance; credits are consumed by query executions, data exports, and writes. Plan-tier export rate (e.g. 20 vs 2 credits/MB) materially changes effective cost. Failed executions still count.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Subscription
  InvoiceIssuerName: Dune
  ProviderName: Dune
  PublisherName: Dune
  ServiceCategory: Crypto Analytics
  ServiceName: Dune API
layout: finops
meters:
- aggregation: sum
  description: Monthly subscription per workspace.
  dimensions:
  - workspace
  name: subscription
  unit: month
- aggregation: sum
  description: Credits consumed by query executions.
  dimensions:
  - workspace
  - query_id
  - performance_tier
  name: query_execution_credits
  unit: credit
- aggregation: sum
  description: Credits consumed by exporting data (per MB).
  dimensions:
  - workspace
  name: export_credits
  unit: credit
name: Dune Analytics Finops
provider_name: Dune Analytics
provider_slug: dune-analytics
publisher_name: Dune
service_category: Crypto Analytics
slug: dune-analytics-finops
source_filename: dune-analytics-finops.yml
source_heading: FinOps Profile
source_url: https://docs.dune.com/api-reference/overview/billing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Dune Analytics\nproviderId: dune-analytics\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: true\ntags:\n  - Web3\n  - Analytics\n  - FinOps\n  - FOCUS\ndescription: >-\n  FinOps view of Dune. Subscription tier governs monthly credit allowance; credits are consumed\n  by query executions, data exports, and writes. Plan-tier export rate (e.g. 20 vs 2 credits/MB)\n  materially changes effective cost. Failed executions still count.\nsources:\n  - https://docs.dune.com/api-reference/overview/billing\n  - https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Dune\nserviceCategory: Crypto Analytics\nbillingModel:\n  pricingCategory:\
  \ Subscription with Metered Credit Allowance\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Subscription\n    - Usage\n    - Adjustment\nfocusColumns:\n  ServiceName: Dune API\n  ServiceCategory: Crypto Analytics\n  ProviderName: Dune\n  PublisherName: Dune\n  InvoiceIssuerName: Dune\n  BillingCurrency: USD\n  ChargeCategory: Subscription\nmeters:\n  - name: subscription\n    description: Monthly subscription per workspace.\n    unit: month\n    aggregation: sum\n    dimensions:\n      - workspace\n  - name: query_execution_credits\n    description: Credits consumed by query executions.\n    unit: credit\n    aggregation: sum\n    dimensions:\n      - workspace\n      - query_id\n      - performance_tier\n  - name: export_credits\n    description: Credits consumed by exporting data (per MB).\n    unit: credit\n    aggregation: sum\n    dimensions:\n      - workspace\nprinciples:\n  - name: Visibility\n    description: Track credit usage per query and per\
  \ consumer to forecast tier sufficiency.\n  - name: Allocation\n    description: Tag queries with consumer team to allocate credit usage on chargeback.\n  - name: Optimization\n    description: Right-size performance tier; cache results to avoid re-execution; gate retries.\n  - name: Accountability\n    description: Assign a billing owner per workspace; review monthly credit-vs-allowance.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/dune-analytics/refs/heads/main/finops/dune-analytics-finops.yml
sources:
- https://docs.dune.com/api-reference/overview/billing
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Web3
- Analytics
- FinOps
- FOCUS
---
