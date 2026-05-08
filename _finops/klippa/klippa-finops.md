---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: EUR / USD
  billingFrequency: Annual
  chargeCategories:
  - Usage
  - Purchase
  - Adjustment
  pricingCategory: Subscription + Usage (per document)
description: FOCUS-aligned FinOps profile for Klippa. Billing is annual sales-led contracts denominated in monthly document/page buckets per API surface (DocHorizon, Financial OCR, Identity Verification). Charges typically bill in EUR for EU customers / USD for US customers; can include EU data-residency and on-prem clauses.
focus_columns:
  BillingCurrency: EUR
  ChargeCategory: Usage
  InvoiceIssuerName: Klippa
  PricingUnit: document / verification
  ProviderName: Klippa
  PublisherName: Klippa
  ServiceCategory: AI / IDP
  ServiceName: Klippa DocHorizon
layout: finops
meters:
- aggregation: sum
  description: Documents processed via DocHorizon platform.
  dimensions:
  - account
  - api_key
  - document_type
  name: documents_processed_dochorizon
  unit: document
- aggregation: sum
  description: Receipts / invoices / bank statements parsed.
  dimensions:
  - account
  name: financial_documents
  unit: document
- aggregation: sum
  description: Identity verifications (KIV) performed.
  dimensions:
  - account
  name: identity_verifications
  unit: verification
- aggregation: sum
  description: Annual contract subscription.
  dimensions:
  - account
  name: subscription_contract
  unit: contract-year
name: Klippa Finops
provider_name: Klippa
provider_slug: klippa
publisher_name: Klippa
service_category: Document AI
slug: klippa-finops
source_filename: klippa-finops.yml
source_heading: FinOps Profile
source_url: https://www.klippa.com/en/pricing/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Klippa\nproviderId: klippa\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: true\ntags:\n- AI\n- Document AI\n- IDP\n- OCR\n- Verification\n- FinOps\n- Cost Management\n- FOCUS\ndescription: >-\n  FOCUS-aligned FinOps profile for Klippa. Billing is annual sales-led\n  contracts denominated in monthly document/page buckets per API surface\n  (DocHorizon, Financial OCR, Identity Verification). Charges typically\n  bill in EUR for EU customers / USD for US customers; can include EU\n  data-residency and on-prem clauses.\nnotes: >-\n  Klippa's strength as a FinOps subject is per-API-surface allocation —\n  invoices, receipts and identity verifications can be tracked separately\n  through different API keys.\nsources:\n- https://www.klippa.com/en/pricing/\n- https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n\
  \  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Klippa\nserviceCategory: Document AI\nbillingModel:\n  pricingCategory: Subscription + Usage (per document)\n  billingFrequency: Annual\n  billingCurrency: EUR / USD\n  chargeCategories:\n  - Usage\n  - Purchase\n  - Adjustment\nfocusColumns:\n  ServiceName: Klippa DocHorizon\n  ServiceCategory: AI / IDP\n  ProviderName: Klippa\n  PublisherName: Klippa\n  InvoiceIssuerName: Klippa\n  BillingCurrency: EUR\n  ChargeCategory: Usage\n  PricingUnit: document / verification\nmeters:\n- name: documents_processed_dochorizon\n  description: Documents processed via DocHorizon platform.\n  unit: document\n  aggregation: sum\n  dimensions:\n  - account\n  - api_key\n  - document_type\n- name: financial_documents\n  description: Receipts / invoices / bank statements parsed.\n  unit: document\n  aggregation: sum\n  dimensions:\n\
  \  - account\n- name: identity_verifications\n  description: Identity verifications (KIV) performed.\n  unit: verification\n  aggregation: sum\n  dimensions:\n  - account\n- name: subscription_contract\n  description: Annual contract subscription.\n  unit: contract-year\n  aggregation: sum\n  dimensions:\n  - account\nprinciples:\n- name: Visibility\n  description: Use Klippa portal usage page; group by API key for per-product breakdown.\n- name: Allocation\n  description: One API key per business unit / product line; map to FOCUS ResourceTag.\n- name: Optimization\n  description: Right-size annual document buckets; renegotiate at renewal; combine receipts/invoices into DocHorizon if volume warrants consolidated platform pricing.\n- name: Accountability\n  description: Assign API-key owners; review monthly burn-down.\nmaintainers:\n- FN: Kin Lane\n  email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/klippa/refs/heads/main/finops/klippa-finops.yml
sources:
- https://www.klippa.com/en/pricing/
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- AI
- Document AI
- IDP
- OCR
- Verification
- FinOps
- Cost Management
- FOCUS
---
