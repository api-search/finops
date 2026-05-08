---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: envestnet-account-aggregation-openapi-original.yml
  format: yaml
  label: Envestnet Account Aggregation API
  slug: envestnet-account-aggregation-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/envestnet/refs/heads/main/openapi/envestnet-account-aggregation-openapi-original.yml
- filename: envestnet-account-token-openapi-original.yml
  format: yaml
  label: Envestnet Account Token APIs
  slug: envestnet-account-token-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/envestnet/refs/heads/main/openapi/envestnet-account-token-openapi-original.yml
- filename: envestnet-verification-openapi-original.yml
  format: yaml
  label: Envestnet Account Verification APIs
  slug: envestnet-account-verification-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/envestnet/refs/heads/main/openapi/envestnet-verification-openapi-original.yml
- filename: envestnet-credit-accelerator-openapi-original.yml
  format: yaml
  label: Envestnet Credit Accelerator API
  slug: envestnet-credit-accelerator-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/envestnet/refs/heads/main/openapi/envestnet-credit-accelerator-openapi-original.yml
- filename: envestnet-insights-openapi-original.yml
  format: yaml
  label: Envestnet Insights API
  slug: envestnet-insights-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/envestnet/refs/heads/main/openapi/envestnet-insights-openapi-original.yml
- filename: envestnet-personalized-views-openapi-original.yml
  format: yaml
  label: Envestnet Personalized View API
  slug: envestnet-personalized-view-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/envestnet/refs/heads/main/openapi/envestnet-personalized-views-openapi-original.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  - Adjustment
  pricingCategory: Subscription + Usage
description: FOCUS-aligned FinOps view for Envestnet | Yodlee. Yodlee bills FIs and FinTechs under enterprise subscription contracts, typically combining product subscriptions with usage components such as connected end-users, account refreshes, and verification calls. List pricing is not published; FinOps tracks contracted fees and per-product usage against the customer agreement.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Envestnet, Inc.
  ProviderName: Envestnet
  PublisherName: Envestnet, Inc.
  ServiceCategory: Financial Data / Open Banking
  ServiceName: Envestnet | Yodlee APIs
layout: finops
meters:
- aggregation: max
  dimensions:
  - product
  - customer
  name: connected_end_users
  unit: user-month
- aggregation: sum
  dimensions:
  - product
  - data_source
  - customer
  name: account_refreshes
  unit: refresh
- aggregation: sum
  dimensions:
  - verification_type
  - customer
  name: verification_calls
  unit: call
- aggregation: sum
  dimensions:
  - customer
  name: credit_accelerator_files
  unit: file
- aggregation: sum
  dimensions:
  - product
  - customer
  name: insights_calls
  unit: call
- aggregation: sum
  dimensions:
  - product
  - customer
  name: subscription_fee
  unit: month
name: Envestnet Finops
provider_name: Envestnet
provider_slug: envestnet
publisher_name: Envestnet, Inc.
service_category: Financial Data / Open Banking
slug: envestnet-finops
source_filename: envestnet-finops.yml
source_heading: FinOps Profile
source_url: https://www.envestnet.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Envestnet\nproviderId: envestnet\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Financial\n  - Open Banking\n  - Account Aggregation\n  - FinOps\n  - FOCUS\ndescription: FOCUS-aligned FinOps view for Envestnet | Yodlee. Yodlee bills FIs and FinTechs under enterprise\n  subscription contracts, typically combining product subscriptions with usage components such as connected\n  end-users, account refreshes, and verification calls. List pricing is not published; FinOps tracks contracted\n  fees and per-product usage against the customer agreement.\nnotes: List prices are not published on developer.envestnet.com. Reconcile FinOps against the executed\n  Yodlee agreement and the per-product usage statements provided to the customer.\nsources:\n  - https://www.envestnet.com/\n  - https://developer.envestnet.com/\nalignedWith:\n  framework:\
  \ FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Envestnet, Inc.\nserviceCategory: Financial Data / Open Banking\nbillingModel:\n  pricingCategory: Subscription + Usage\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Adjustment\nfocusColumns:\n  ServiceName: Envestnet | Yodlee APIs\n  ServiceCategory: Financial Data / Open Banking\n  ProviderName: Envestnet\n  PublisherName: Envestnet, Inc.\n  InvoiceIssuerName: Envestnet, Inc.\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: connected_end_users\n    unit: user-month\n    aggregation: max\n    dimensions:\n      - product\n      - customer\n  - name: account_refreshes\n    unit: refresh\n    aggregation: sum\n    dimensions:\n      - product\n      - data_source\n      - customer\n  - name: verification_calls\n\
  \    unit: call\n    aggregation: sum\n    dimensions:\n      - verification_type\n      - customer\n  - name: credit_accelerator_files\n    unit: file\n    aggregation: sum\n    dimensions:\n      - customer\n  - name: insights_calls\n    unit: call\n    aggregation: sum\n    dimensions:\n      - product\n      - customer\n  - name: subscription_fee\n    unit: month\n    aggregation: sum\n    dimensions:\n      - product\n      - customer\nprinciples:\n  - name: Visibility\n    description: Track per-product usage (aggregation, verification, token, credit, insights, views) against\n      the contract and reconcile to monthly Yodlee usage statements.\n  - name: Allocation\n    description: Allocate spend by FinTech product line, end-user cohort, and Yodlee product family.\n  - name: Optimization\n    description: Optimization levers include refresh-cadence tuning, deduplicated aggregation across products,\n      and selective verification (not every aggregation flow needs a verification\
  \ call).\n  - name: Accountability\n    description: The FI/FinTech product owner reconciles spend against the Yodlee agreement and engages\n      Envestnet account management for renewal and tier changes.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/envestnet/refs/heads/main/finops/envestnet-finops.yml
sources:
- https://www.envestnet.com/
- https://developer.envestnet.com/
specification: FinOps Framework
tags:
- Financial
- Open Banking
- Account Aggregation
- FinOps
- FOCUS
---
