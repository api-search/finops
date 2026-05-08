---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: avalara-avatax-rest-openapi.yml
  format: yaml
  label: AvaTax APIs
  slug: avatax-apis
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/avalara/refs/heads/main/openapi/avalara-avatax-rest-openapi.yml
- filename: avalara-communications-openapi.yml
  format: yaml
  label: Communications Tax API
  slug: communications-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/avalara/refs/heads/main/openapi/avalara-communications-openapi.yml
- filename: avalara-excise-openapi.yml
  format: yaml
  label: Excise Platform API
  slug: excise-tax-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/avalara/refs/heads/main/openapi/avalara-excise-openapi.yml
- filename: avalara-item-classification-openapi.yml
  format: yaml
  label: Item Classification API
  slug: item-classification-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/avalara/refs/heads/main/openapi/avalara-item-classification-openapi.yml
- filename: avalara-avatax-brazil-openapi.yml
  format: yaml
  label: AvaTax Brazil API
  slug: avatax-brazil-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/avalara/refs/heads/main/openapi/avalara-avatax-brazil-openapi.yml
- filename: avalara-vat-reporting-openapi.yml
  format: yaml
  label: VAT Reporting API
  slug: vat-reporting-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/avalara/refs/heads/main/openapi/avalara-vat-reporting-openapi.yml
- filename: avalara-mylodgetax-openapi.yml
  format: yaml
  label: MyLodgeTax API
  slug: mylodgetax-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/avalara/refs/heads/main/openapi/avalara-mylodgetax-openapi.yml
- filename: avalara-certcapture-openapi.yml
  format: yaml
  label: CertCapture API
  slug: certcapture-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/avalara/refs/heads/main/openapi/avalara-certcapture-openapi.yml
- filename: avalara-e-invoicing-openapi.yml
  format: yaml
  label: E-Invoicing REST API
  slug: e-invoicing-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/avalara/refs/heads/main/openapi/avalara-e-invoicing-openapi.yml
- filename: avalara-activation-service-openapi.yml
  format: yaml
  label: Activation Service API
  slug: activation-service-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/avalara/refs/heads/main/openapi/avalara-activation-service-openapi.yml
- filename: avalara-business-openapi.yml
  format: yaml
  label: Avalara Business API
  slug: business-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/avalara/refs/heads/main/openapi/avalara-business-openapi.yml
- filename: avalara-portal-oauth-openapi.yml
  format: yaml
  label: Portal OAuth API
  slug: portal-oauth-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/avalara/refs/heads/main/openapi/avalara-portal-oauth-openapi.yml
- filename: avalara-shared-company-service-openapi.yml
  format: yaml
  label: Shared Company Service API
  slug: shared-company-service-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/avalara/refs/heads/main/openapi/avalara-shared-company-service-openapi.yml
- filename: avalara-hs-code-classification-openapi.yml
  format: yaml
  label: Automated Tariff Code Classification API
  slug: hs-code-classification-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/avalara/refs/heads/main/openapi/avalara-hs-code-classification-openapi.yml
- filename: avalara-1099-w9-openapi.yml
  format: yaml
  label: 1099 & W-9 API
  slug: 1099-w9-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/avalara/refs/heads/main/openapi/avalara-1099-w9-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  - Usage
  - Adjustment
  - Tax
  - Credit
  pricingCategory: Subscription + Pay-As-You-Go
description: 'FOCUS-aligned FinOps for Avalara: subscription + per-transaction tax-compliance billing with separate meters for AvaTax calculations, Returns filings, certificate management, and e-invoicing documents.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Avalara, Inc.
  ProviderName: Avalara
  PublisherName: Avalara, Inc.
  ServiceCategory: Tax Compliance
  ServiceName: Avalara
layout: finops
meters:
- aggregation: sum
  dimensions:
  - jurisdiction
  - country
  - document_type
  name: avatax_transactions
  unit: transaction
- aggregation: max
  dimensions:
  - country
  name: jurisdictions_subscribed
  unit: jurisdiction
- aggregation: sum
  dimensions:
  - jurisdiction
  - return_type
  name: returns_filings
  unit: filing
- aggregation: max
  name: certificate_storage
  unit: certificate
- aggregation: sum
  dimensions:
  - country
  - mandate_type
  name: e_invoice_documents
  unit: document
- aggregation: sum
  dimensions:
  - origin_country
  - destination_country
  name: cross_border_transactions
  unit: transaction
name: Avalara Finops
provider_name: Avalara
provider_slug: avalara
publisher_name: Avalara, Inc.
service_category: Tax Compliance
slug: avalara-finops
source_filename: avalara-finops.yml
source_heading: FinOps Profile
source_url: https://www.avalara.com/us/en/products.html
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Avalara\nproviderId: avalara\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\nnotes: Avalara pricing is quote-based and not publicly posted. This artifact models the FinOps shape\n  of an AvaTax-led tax-compliance subscription with per-transaction and per-filing meters.\ntags:\n  - FinOps\n  - FOCUS\n  - Tax Compliance\n  - Sales Tax\n  - VAT\n  - E-Invoicing\ndescription: 'FOCUS-aligned FinOps for Avalara: subscription + per-transaction tax-compliance billing\n  with separate meters for AvaTax calculations, Returns filings, certificate management, and\n  e-invoicing documents.'\nsources:\n  - https://www.avalara.com/us/en/products.html\n  - https://www.avalara.com/us/en/products/calculations/avatax.html\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion:\
  \ '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Avalara, Inc.\nserviceCategory: Tax Compliance\nbillingModel:\n  pricingCategory: Subscription + Pay-As-You-Go\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\n    - Adjustment\n    - Tax\n    - Credit\nfocusColumns:\n  ServiceName: Avalara\n  ServiceCategory: Tax Compliance\n  ProviderName: Avalara\n  PublisherName: Avalara, Inc.\n  InvoiceIssuerName: Avalara, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: avatax_transactions\n    unit: transaction\n    aggregation: sum\n    dimensions:\n      - jurisdiction\n      - country\n      - document_type\n  - name: jurisdictions_subscribed\n    unit: jurisdiction\n    aggregation: max\n    dimensions:\n      - country\n  - name: returns_filings\n    unit: filing\n    aggregation: sum\n    dimensions:\n      - jurisdiction\n      - return_type\n  - name: certificate_storage\n    unit: certificate\n\
  \    aggregation: max\n  - name: e_invoice_documents\n    unit: document\n    aggregation: sum\n    dimensions:\n      - country\n      - mandate_type\n  - name: cross_border_transactions\n    unit: transaction\n    aggregation: sum\n    dimensions:\n      - origin_country\n      - destination_country\nprinciples:\n  - name: Visibility\n    description: Use the AvaTax admin console and the Reporting API to track transaction counts by\n      company / jurisdiction / document type; reconcile against the annual subscription envelope.\n  - name: Allocation\n    description: Tag CreateTransaction calls with internal company / location / business-unit codes;\n      use those to allocate Avalara spend to the originating ERP entity.\n  - name: Optimization\n    description: Right-size the jurisdiction footprint annually (drop states with no nexus); batch\n      adjustments and avoid voiding-and-reissuing transactions which can double-count meters; consolidate\n      multi-product discounts at\
  \ renewal.\n  - name: Accountability\n    description: Tax / Indirect-Tax team owns the Avalara subscription; engineering owns the integration\n      health; finance reviews jurisdiction footprint annually.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/avalara/refs/heads/main/finops/avalara-finops.yml
sources:
- https://www.avalara.com/us/en/products.html
- https://www.avalara.com/us/en/products/calculations/avatax.html
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Tax Compliance
- Sales Tax
- VAT
- E-Invoicing
---
