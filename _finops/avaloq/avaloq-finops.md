---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: avaloq-banking-openapi.yml
  format: yaml
  label: Avaloq Banking API
  slug: avaloq-banking-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/avaloq/refs/heads/main/openapi/avaloq-banking-openapi.yml
- filename: avaloq-wealth-management-openapi.yml
  format: yaml
  label: Avaloq Wealth Management API
  slug: avaloq-wealth-management-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/avaloq/refs/heads/main/openapi/avaloq-wealth-management-openapi.yml
- filename: avaloq-payments-openapi.yml
  format: yaml
  label: Avaloq Payments API
  slug: avaloq-payments-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/avaloq/refs/heads/main/openapi/avaloq-payments-openapi.yml
- filename: avaloq-client-management-openapi.yml
  format: yaml
  label: Avaloq Client Management API
  slug: avaloq-client-management-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/avaloq/refs/heads/main/openapi/avaloq-client-management-openapi.yml
- filename: avaloq-trading-openapi.yml
  format: yaml
  label: Avaloq Trading API
  slug: avaloq-trading-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/avaloq/refs/heads/main/openapi/avaloq-trading-openapi.yml
- filename: avaloq-compliance-openapi.yml
  format: yaml
  label: Avaloq Compliance & Risk API
  slug: avaloq-compliance-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/avaloq/refs/heads/main/openapi/avaloq-compliance-openapi.yml
billing_model:
  billingCurrency: USD/EUR/CHF
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  - Usage
  - Adjustment
  - Tax
  - Credit
  pricingCategory: Enterprise Subscription
description: 'FOCUS-aligned FinOps for Avaloq: enterprise subscription core-banking platform with optional BPO services. Cost is dominated by platform license + per-AUM / per-account scale fees and BPO operations charges; not by per-API-call usage.'
focus_columns:
  BillingCurrency: CHF
  InvoiceIssuerName: Avaloq Group AG
  ProviderName: Avaloq
  PublisherName: Avaloq Group AG
  ServiceCategory: Core Banking / Wealth Management
  ServiceName: Avaloq
layout: finops
meters:
- aggregation: sum
  dimensions:
  - module
  - deployment
  name: banking_suite_license
  unit: month
- aggregation: max
  name: client_accounts
  unit: account
- aggregation: max
  name: assets_under_management
  unit: USD
- aggregation: sum
  dimensions:
  - service
  name: bpo_operations
  unit: month
- aggregation: sum
  dimensions:
  - module
  name: api_invocations
  unit: invocation
name: Avaloq Finops
provider_name: Avaloq
provider_slug: avaloq
publisher_name: Avaloq Group AG
service_category: Core Banking / Wealth Management
slug: avaloq-finops
source_filename: avaloq-finops.yml
source_heading: FinOps Profile
source_url: https://www.avaloq.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Avaloq\nproviderId: avaloq\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\nnotes: Avaloq pricing is enterprise-quote and not publicly posted. This artifact models the FinOps\n  shape of an Avaloq deployment (subscription + BPO + optional on-prem).\ntags:\n  - FinOps\n  - FOCUS\n  - Banking\n  - Wealth Management\n  - Core Banking\ndescription: 'FOCUS-aligned FinOps for Avaloq: enterprise subscription core-banking platform with\n  optional BPO services. Cost is dominated by platform license + per-AUM / per-account scale fees and\n  BPO operations charges; not by per-API-call usage.'\nsources:\n  - https://www.avaloq.com/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName:\
  \ Avaloq Group AG\nserviceCategory: Core Banking / Wealth Management\nbillingModel:\n  pricingCategory: Enterprise Subscription\n  billingFrequency: Annual\n  billingCurrency: USD/EUR/CHF\n  chargeCategories:\n    - Purchase\n    - Usage\n    - Adjustment\n    - Tax\n    - Credit\nfocusColumns:\n  ServiceName: Avaloq\n  ServiceCategory: Core Banking / Wealth Management\n  ProviderName: Avaloq\n  PublisherName: Avaloq Group AG\n  InvoiceIssuerName: Avaloq Group AG\n  BillingCurrency: CHF\nmeters:\n  - name: banking_suite_license\n    unit: month\n    aggregation: sum\n    dimensions:\n      - module\n      - deployment\n  - name: client_accounts\n    unit: account\n    aggregation: max\n  - name: assets_under_management\n    unit: USD\n    aggregation: max\n  - name: bpo_operations\n    unit: month\n    aggregation: sum\n    dimensions:\n      - service\n  - name: api_invocations\n    unit: invocation\n    aggregation: sum\n    dimensions:\n      - module\nprinciples:\n  - name: Visibility\n\
  \    description: Visibility comes from the institution's own Avaloq instance — operations dashboards,\n      Banking Suite reporting, and contractual scale reports tied to AUM / account counts.\n  - name: Allocation\n    description: Allocate by business unit (private banking, wealth, corporate), legal entity, and\n      booking center. Avaloq supports multi-entity bookkeeping for chargeback.\n  - name: Optimization\n    description: Optimization levers are module mix (only license modules used), retiring legacy\n      country / module deployments, and renegotiating BPO scope. API call patterns matter less than\n      module footprint.\n  - name: Accountability\n    description: COO / Head of Operations or CIO typically owns the Avaloq relationship; multi-year\n      contract reviews involve procurement and risk.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/avaloq/refs/heads/main/finops/avaloq-finops.yml
sources:
- https://www.avaloq.com/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Banking
- Wealth Management
- Core Banking
---
