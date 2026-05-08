---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: adobe-pdf-services-api-openapi.yml
  format: yaml
  label: Adobe PDF Services API
  slug: adobe-pdf-services-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/adobe/refs/heads/main/openapi/adobe-pdf-services-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly / Annual
  chargeCategories:
  - Usage
  - Purchase
  - Tax
  - Adjustment
  - Credit
  pricingCategory: Subscription + Pay-As-You-Go + Enterprise Contract
description: 'FOCUS-aligned FinOps shape for Adobe: hybrid per-seat subscription plus per-transaction usage plus generative-credit metering plus enterprise contract licensing across the Experience Cloud portfolio.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Adobe Inc.
  ProviderName: Adobe
  PublisherName: Adobe Inc.
  ServiceCategory: Creative + Marketing + Document SaaS
  ServiceName: Adobe
layout: finops
meters:
- aggregation: sum
  description: Per-seat monthly Creative Cloud subscription
  dimensions:
  - plan
  - geography
  name: cc_seat_subscription
  unit: seat-month
- aggregation: sum
  description: Billable PDF Services / Acrobat Sign transactions
  dimensions:
  - api
  - tier
  name: document_transactions
  unit: transaction
- aggregation: sum
  description: Firefly generative-credit consumption
  dimensions:
  - model
  - api
  name: generative_credits
  unit: credit
- aggregation: sum
  description: Experience Cloud contract licensing
  dimensions:
  - product
  - sku
  name: enterprise_subscription
  unit: month
name: Adobe Finops
provider_name: Adobe
provider_slug: adobe
publisher_name: Adobe Inc.
service_category: Creative + Marketing + Document SaaS
slug: adobe-finops
source_filename: adobe-finops.yml
source_heading: FinOps Profile
source_url: https://www.adobe.com/plans
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Adobe\nproviderId: adobe\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Creative Cloud\n  - Document Services\n  - Experience Cloud\n  - Generative AI\nnotes: >-\n  Adobe spans multiple billing models: per-seat subscription (Creative Cloud,\n  Acrobat), per-transaction (Document Services API), generative-credit-metered\n  (Firefly), and contract-priced enterprise SaaS (Experience Cloud). Per-product\n  prices were not reconciled here; consult per-product repos for exact meters.\ndescription: >-\n  FOCUS-aligned FinOps shape for Adobe: hybrid per-seat subscription plus\n  per-transaction usage plus generative-credit metering plus enterprise\n  contract licensing across the Experience Cloud portfolio.\nsources:\n  - https://www.adobe.com/plans\n  - https://developer.adobe.com/document-services/pricing/\n  - https://business.adobe.com/products/\n\
  alignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Adobe Inc.\nserviceCategory: Creative + Marketing + Document SaaS\nbillingModel:\n  pricingCategory: Subscription + Pay-As-You-Go + Enterprise Contract\n  billingFrequency: Monthly / Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Adjustment\n    - Credit\nfocusColumns:\n  ServiceName: Adobe\n  ServiceCategory: Creative + Marketing + Document SaaS\n  ProviderName: Adobe\n  PublisherName: Adobe Inc.\n  InvoiceIssuerName: Adobe Inc.\n  BillingCurrency: USD\nmeters:\n  - name: cc_seat_subscription\n    description: Per-seat monthly Creative Cloud subscription\n    unit: seat-month\n    aggregation: sum\n    dimensions:\n      - plan\n      - geography\n  - name: document_transactions\n    description: Billable\
  \ PDF Services / Acrobat Sign transactions\n    unit: transaction\n    aggregation: sum\n    dimensions:\n      - api\n      - tier\n  - name: generative_credits\n    description: Firefly generative-credit consumption\n    unit: credit\n    aggregation: sum\n    dimensions:\n      - model\n      - api\n  - name: enterprise_subscription\n    description: Experience Cloud contract licensing\n    unit: month\n    aggregation: sum\n    dimensions:\n      - product\n      - sku\nprinciples:\n  - name: Visibility\n    description: >-\n      Use the Adobe Admin Console for seat-level Creative Cloud usage; the\n      Document Services usage dashboard for PDF/Sign API transactions; the\n      Firefly Services credits dashboard for generative-credit burn; and the\n      Experience Cloud contract dashboard for SKU consumption.\n  - name: Allocation\n    description: >-\n      Tag Creative Cloud seats with department in the Admin Console; pass\n      x-api-key per integration so PDF/Firefly traffic\
  \ can be attributed to\n      a consuming team via API analytics.\n  - name: Optimization\n    description: >-\n      Right-size Creative Cloud SKUs (single-app vs All Apps); cache PDF\n      Extract output where idempotent; use lower-credit Firefly models for\n      drafts and reserve full-credit calls for final renders; negotiate\n      Experience Cloud bundles for SKU overlap.\n  - name: Accountability\n    description: >-\n      Adobe Admin Console roles route invoices to a single billing owner;\n      enterprise contracts have named technical account managers who run\n      quarterly business reviews on consumption versus commit.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/adobe/refs/heads/main/finops/adobe-finops.yml
sources:
- https://www.adobe.com/plans
- https://developer.adobe.com/document-services/pricing/
- https://business.adobe.com/products/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Creative Cloud
- Document Services
- Experience Cloud
- Generative AI
---
