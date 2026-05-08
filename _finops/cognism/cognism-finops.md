---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Subscription
  - Commitment
  pricingCategory: Subscription
description: 'FOCUS-aligned FinOps profile for Cognism. The cost lever is the annual enterprise contract — typically a fixed seat-based commitment with a bundled credit pool for API enrichment. There is no per-call invoicing. Cost optimization is at renewal: right-size seats and credit allotment based on observed consumption.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Subscription
  InvoiceIssuerName: Cognism
  ProviderName: Cognism
  PublisherName: Cognism
  ServiceCategory: Sales Intelligence
  ServiceName: Cognism Platform
layout: finops
meters:
- aggregation: max
  description: Number of licensed users.
  dimensions:
  - team
  name: platform_seats
  unit: seat-month
- aggregation: sum
  description: API enrichment credits consumed.
  dimensions:
  - endpoint
  name: enrichment_credits
  unit: credit
name: Cognism Finops
provider_name: Cognism
provider_slug: cognism
publisher_name: Cognism
service_category: Sales Intelligence
slug: cognism-finops
source_filename: cognism-finops.yml
source_heading: FinOps Profile
source_url: https://www.cognism.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Cognism\nproviderId: cognism\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: true\ntags:\n- Sales Intelligence\n- B2B\n- Enrichment\n- Contact Data\n- GDPR\n- Intent Data\n- FinOps\n- Cost Management\n- FOCUS\ndescription: >-\n  FOCUS-aligned FinOps profile for Cognism. The cost lever is the annual enterprise contract —\n  typically a fixed seat-based commitment with a bundled credit pool for API enrichment. There is no\n  per-call invoicing. Cost optimization is at renewal: right-size seats and credit allotment based on\n  observed consumption.\nnotes: Annual contract, prepaid; seats and credit pool are the optimization levers at renewal.\nsources:\n- https://www.cognism.com/\n- https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n\
  \  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Cognism\nserviceCategory: Sales Intelligence\nbillingModel:\n  pricingCategory: Subscription\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n  - Subscription\n  - Commitment\nfocusColumns:\n  ServiceName: Cognism Platform\n  ServiceCategory: Sales Intelligence\n  ProviderName: Cognism\n  PublisherName: Cognism\n  InvoiceIssuerName: Cognism\n  BillingCurrency: USD\n  ChargeCategory: Subscription\nmeters:\n- name: platform_seats\n  description: Number of licensed users.\n  unit: seat-month\n  aggregation: max\n  dimensions:\n  - team\n- name: enrichment_credits\n  description: API enrichment credits consumed.\n  unit: credit\n  aggregation: sum\n  dimensions:\n  - endpoint\nprinciples:\n- name: Visibility\n  description: Track API credit consumption monthly against the contracted pool.\n- name: Allocation\n  description: Allocate seats and credits to revenue\
  \ teams (SDR, AE, marketing ops).\n- name: Optimization\n  description: At renewal, right-size seats and the credit pool; consolidate vendors if overlapping (Lusha, Apollo, ZoomInfo).\n- name: Accountability\n  description: RevOps team owns the contract and renewal.\nmaintainers:\n- FN: Kin Lane\n  email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/cognism/refs/heads/main/finops/cognism-finops.yml
sources:
- https://www.cognism.com/
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Sales Intelligence
- B2B
- Enrichment
- Contact Data
- GDPR
- Intent Data
- FinOps
- Cost Management
- FOCUS
---
