---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly / Annual
  chargeCategories:
  - Usage
  - Purchase
  - Adjustment
  pricingCategory: Subscription + Usage (overage)
description: FOCUS-aligned FinOps profile for Sensible. Costs are a flat monthly tier fee (Growth $499 / Scale $1,499 / Enterprise custom) plus per-document overage ($0.50/document on Growth/Scale, tiered on Enterprise). Charge is per document — not per page — which makes long documents (up to ~100 pages) highly cost-efficient.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Sensible
  PricingUnit: document
  ProviderName: Sensible
  PublisherName: Sensible
  ServiceCategory: AI / IDP
  ServiceName: Sensible
layout: finops
meters:
- aggregation: sum
  description: Flat monthly tier fee.
  dimensions:
  - account
  - tier
  name: plan_subscription
  unit: month
- aggregation: sum
  description: Documents extracted in the billing month.
  dimensions:
  - account
  - environment
  - extractor
  name: documents_processed
  unit: document
- aggregation: sum
  description: Documents above the included monthly bundle.
  dimensions:
  - account
  name: document_overage
  unit: document
- aggregation: sum
  description: Manual review interactions (Scale/Enterprise).
  dimensions:
  - account
  - reviewer
  name: human_review_touches
  unit: review
name: Sensible Io Finops
provider_name: Sensible
provider_slug: sensible-io
publisher_name: Sensible
service_category: Document AI
slug: sensible-io-finops
source_filename: sensible-io-finops.yml
source_heading: FinOps Profile
source_url: https://www.sensible.so/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Sensible\nproviderId: sensible-io\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: true\ntags:\n- AI\n- Document AI\n- IDP\n- Extraction\n- FinOps\n- Cost Management\n- FOCUS\ndescription: >-\n  FOCUS-aligned FinOps profile for Sensible. Costs are a flat monthly tier fee\n  (Growth $499 / Scale $1,499 / Enterprise custom) plus per-document overage\n  ($0.50/document on Growth/Scale, tiered on Enterprise). Charge is per\n  document — not per page — which makes long documents (up to ~100 pages)\n  highly cost-efficient.\nnotes: >-\n  Optimisation focuses on right-sizing the monthly bundle to actual document\n  volume; switching to annual billing for ~10% effective discount; minimising\n  human-review touches on Scale/Enterprise.\nsources:\n- https://www.sensible.so/pricing\n- https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework:\
  \ FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Sensible\nserviceCategory: Document AI\nbillingModel:\n  pricingCategory: Subscription + Usage (overage)\n  billingFrequency: Monthly / Annual\n  billingCurrency: USD\n  chargeCategories:\n  - Usage\n  - Purchase\n  - Adjustment\nfocusColumns:\n  ServiceName: Sensible\n  ServiceCategory: AI / IDP\n  ProviderName: Sensible\n  PublisherName: Sensible\n  InvoiceIssuerName: Sensible\n  BillingCurrency: USD\n  ChargeCategory: Usage\n  PricingUnit: document\nmeters:\n- name: plan_subscription\n  description: Flat monthly tier fee.\n  unit: month\n  aggregation: sum\n  dimensions:\n  - account\n  - tier\n- name: documents_processed\n  description: Documents extracted in the billing month.\n  unit: document\n  aggregation: sum\n  dimensions:\n  - account\n  - environment\n  - extractor\n\
  - name: document_overage\n  description: Documents above the included monthly bundle.\n  unit: document\n  aggregation: sum\n  dimensions:\n  - account\n- name: human_review_touches\n  description: Manual review interactions (Scale/Enterprise).\n  unit: review\n  aggregation: sum\n  dimensions:\n  - account\n  - reviewer\nprinciples:\n- name: Visibility\n  description: Use the Sensible portal Usage page; export per-extractor / per-environment counts for chargeback.\n- name: Allocation\n  description: Use environments and extractor naming conventions to map to teams / cost centres.\n- name: Optimization\n  description: Right-size monthly bundle; consolidate similar templates; avoid unnecessary re-runs; switch to annual.\n- name: Accountability\n  description: Assign extractor owners; alert at 75% of monthly bundle.\nmaintainers:\n- FN: Kin Lane\n  email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/sensible-io/refs/heads/main/finops/sensible-io-finops.yml
sources:
- https://www.sensible.so/pricing
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- AI
- Document AI
- IDP
- Extraction
- FinOps
- Cost Management
- FOCUS
---
