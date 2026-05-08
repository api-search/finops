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
  - Usage
  - Purchase
  - Adjustment
  pricingCategory: Subscription + Usage (page overage)
description: FOCUS-aligned FinOps profile for Rossum. Billing is annual subscription contract (Starter from $18,000/yr; Business / Enterprise / Ultimate by sales) with a negotiated document-or-page bundle and per-page overage if the bundle is exceeded. One-year minimum.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Rossum
  PricingUnit: page
  ProviderName: Rossum
  PublisherName: Rossum
  ServiceCategory: AI / IDP
  ServiceName: Rossum
layout: finops
meters:
- aggregation: sum
  description: Annual contract fee.
  dimensions:
  - account
  - tier
  name: subscription_contract
  unit: contract-year
- aggregation: sum
  description: Pages processed against the negotiated bundle.
  dimensions:
  - workspace
  - queue
  name: pages_processed
  unit: page
- aggregation: sum
  description: Pages above the contract bundle.
  dimensions:
  - workspace
  - queue
  name: page_overage
  unit: page
- aggregation: sum
  description: Documents processed (informational; pricing is per-page).
  dimensions:
  - queue
  name: documents_processed
  unit: document
- aggregation: sum
  description: REST API calls consumed (informational; not directly billed).
  dimensions:
  - account
  name: api_calls
  unit: request
name: Rossum Finops
provider_name: Rossum
provider_slug: rossum
publisher_name: Rossum
service_category: Document AI / AP Automation
slug: rossum-finops
source_filename: rossum-finops.yml
source_heading: FinOps Profile
source_url: https://rossum.ai/pricing/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Rossum\nproviderId: rossum\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: true\ntags:\n- AI\n- Document AI\n- IDP\n- Invoices\n- OCR\n- FinOps\n- Cost Management\n- FOCUS\ndescription: >-\n  FOCUS-aligned FinOps profile for Rossum. Billing is annual subscription\n  contract (Starter from $18,000/yr; Business / Enterprise / Ultimate by\n  sales) with a negotiated document-or-page bundle and per-page overage if\n  the bundle is exceeded. One-year minimum.\nnotes: >-\n  Annotation lifecycle (importing → to_review → confirmed → exported) gives\n  granular allocation hooks. Queue-level chargeback is the cleanest mapping\n  to teams / business units.\nsources:\n- https://rossum.ai/pricing/\n- https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec:\
  \ FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Rossum\nserviceCategory: Document AI / AP Automation\nbillingModel:\n  pricingCategory: Subscription + Usage (page overage)\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n  - Usage\n  - Purchase\n  - Adjustment\nfocusColumns:\n  ServiceName: Rossum\n  ServiceCategory: AI / IDP\n  ProviderName: Rossum\n  PublisherName: Rossum\n  InvoiceIssuerName: Rossum\n  BillingCurrency: USD\n  ChargeCategory: Purchase\n  PricingUnit: page\nmeters:\n- name: subscription_contract\n  description: Annual contract fee.\n  unit: contract-year\n  aggregation: sum\n  dimensions:\n  - account\n  - tier\n- name: pages_processed\n  description: Pages processed against the negotiated bundle.\n  unit: page\n  aggregation: sum\n  dimensions:\n  - workspace\n  - queue\n- name: page_overage\n  description: Pages above the contract bundle.\n  unit: page\n  aggregation: sum\n\
  \  dimensions:\n  - workspace\n  - queue\n- name: documents_processed\n  description: Documents processed (informational; pricing is per-page).\n  unit: document\n  aggregation: sum\n  dimensions:\n  - queue\n- name: api_calls\n  description: REST API calls consumed (informational; not directly billed).\n  unit: request\n  aggregation: sum\n  dimensions:\n  - account\nprinciples:\n- name: Visibility\n  description: Use queue-level annotation counts for chargeback; reconcile against monthly usage exports.\n- name: Allocation\n  description: One queue per business unit / vendor / channel; map queues to FOCUS ResourceTag.\n- name: Optimization\n  description: Tune extraction schemas to reduce review touches; right-size the contract bundle annually.\n- name: Accountability\n  description: Assign queue owners; monitor approaching bundle exhaustion to renegotiate vs. pay overage.\nmaintainers:\n- FN: Kin Lane\n  email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/rossum/refs/heads/main/finops/rossum-finops.yml
sources:
- https://rossum.ai/pricing/
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- AI
- Document AI
- IDP
- Invoices
- OCR
- FinOps
- Cost Management
- FOCUS
---
