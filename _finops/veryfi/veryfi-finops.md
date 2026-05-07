---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: veryfi-ocr-openapi.yml
  format: yaml
  label: Veryfi OCR API
  slug: ocr-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/veryfi/refs/heads/main/openapi/veryfi-ocr-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  - Tax
  - Adjustment
  pricingCategory: Pay-As-You-Go + Subscription Minimum
description: 'FOCUS-aligned FinOps shape for Veryfi: per-document metered pricing on the Starter plan ($500/mo minimum, document-type-specific unit prices) and a Free quota tier; Growth plan is custom-quoted with volume discounts. The dominant unit of consumption is the processed document.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Veryfi, Inc.
  ProviderName: Veryfi
  PublisherName: Veryfi, Inc.
  ServiceCategory: Document AI / OCR
  ServiceName: Veryfi OCR API
layout: finops
meters:
- aggregation: sum
  dimensions:
  - document_type
  - plan
  name: documents_processed
  unit: document
- aggregation: sum
  dimensions:
  - plan
  name: receipts_processed
  unit: document
- aggregation: sum
  dimensions:
  - plan
  name: invoices_processed
  unit: document
- aggregation: sum
  dimensions:
  - subtype
  name: bank_documents_processed
  unit: document
- aggregation: sum
  dimensions:
  - form_type
  name: tax_forms_processed
  unit: document
- aggregation: max
  dimensions:
  - plan
  name: monthly_minimum
  unit: month
name: Veryfi Finops
provider_name: Veryfi
provider_slug: veryfi
publisher_name: Veryfi, Inc.
service_category: Document AI / OCR
slug: veryfi-finops
source_filename: veryfi-finops.yml
source_heading: FinOps Profile
source_url: https://www.veryfi.com/pricing/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Veryfi\nproviderId: veryfi\npublisherName: Veryfi, Inc.\nserviceCategory: Document AI / OCR\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - OCR\n  - Document AI\n  - Data Extraction\ndescription: 'FOCUS-aligned FinOps shape for Veryfi: per-document metered pricing on the Starter\n  plan ($500/mo minimum, document-type-specific unit prices) and a Free quota tier; Growth plan is\n  custom-quoted with volume discounts. The dominant unit of consumption is the processed document.'\nsources:\n  - https://www.veryfi.com/pricing/\nbillingModel:\n  pricingCategory: Pay-As-You-Go + Subscription Minimum\n  billingFrequency: Monthly\n  billingCurrency:\
  \ USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Adjustment\nfocusColumns:\n  ServiceName: Veryfi OCR API\n  ServiceCategory: Document AI / OCR\n  ProviderName: Veryfi\n  PublisherName: Veryfi, Inc.\n  InvoiceIssuerName: Veryfi, Inc.\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: documents_processed\n    unit: document\n    aggregation: sum\n    dimensions:\n      - document_type\n      - plan\n  - name: receipts_processed\n    unit: document\n    aggregation: sum\n    dimensions:\n      - plan\n  - name: invoices_processed\n    unit: document\n    aggregation: sum\n    dimensions:\n      - plan\n  - name: bank_documents_processed\n    unit: document\n    aggregation: sum\n    dimensions:\n      - subtype\n  - name: tax_forms_processed\n    unit: document\n    aggregation: sum\n    dimensions:\n      - form_type\n  - name: monthly_minimum\n    unit: month\n    aggregation: max\n    dimensions:\n      - plan\nprinciples:\n  - name: Visibility\n\
  \    description: Track per-document consumption via the Veryfi Hub usage views and the API Hub\n      account page; document-type rates are itemized on the monthly invoice.\n  - name: Allocation\n    description: Tag uploads with the originating tenant / business unit at the API request layer\n      (e.g. category or external_id) so document-type cost can be attributed downstream.\n  - name: Optimization\n    description: Right-size the document mix toward lower-priced types (receipts at $0.08 vs invoices\n      at $0.16, checks/statements at $0.25); commit to the 12-month Starter plan for the\n      one-cent-per-document discount; aggregate volume into the Growth plan when usage justifies it.\n  - name: Accountability\n    description: Assign the Veryfi account owner from the integrating product team; finance reconciles\n      monthly against the $500 plan minimum and per-document overage lines on the invoice.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/veryfi/refs/heads/main/finops/veryfi-finops.yml
sources:
- https://www.veryfi.com/pricing/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- OCR
- Document AI
- Data Extraction
---
