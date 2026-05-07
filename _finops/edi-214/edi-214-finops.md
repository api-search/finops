---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: stedi-edi214-openapi.yml
  format: yaml
  label: EDI 214 Transportation Carrier Shipment Status Message
  slug: edi-214-standard
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/edi-214/refs/heads/main/openapi/stedi-edi214-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  - Adjustment
  pricingCategory: Subscription + Usage
description: 'FOCUS-aligned FinOps for EDI 214 implementations: cost falls on the EDI platform vendor (Stedi, Flexport, SPS Commerce, VAN providers) and is billed per-document, per-trading-partner, or via subscription. The standard itself is governed by ASC X12 membership.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: vendor of choice
  ProviderName: ASC X12 / vendor of choice
  PublisherName: ASC X12 / vendor of choice
  ServiceCategory: EDI
  ServiceName: EDI 214 Shipment Status
layout: finops
meters:
- aggregation: sum
  dimensions:
  - direction
  - trading_partner
  - vendor
  name: edi_214_documents
  unit: document
- aggregation: sum
  dimensions:
  - vendor
  name: trading_partner_connections
  unit: partner
- aggregation: sum
  dimensions:
  - vendor
  name: kc_kilo_characters
  unit: KC
name: Edi 214 Finops
provider_name: edi-214
provider_slug: edi-214
publisher_name: ASC X12 (standard) / VAN or EDI-platform vendor (commercial)
service_category: EDI
slug: edi-214-finops
source_filename: edi-214-finops.yml
source_heading: FinOps Profile
source_url: https://x12.org/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: EDI 214 (Transportation Carrier Shipment Status)\nproviderId: edi-214\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - EDI\n  - X12\n  - Logistics\ndescription: 'FOCUS-aligned FinOps for EDI 214 implementations: cost falls on the EDI platform vendor\n  (Stedi, Flexport, SPS Commerce, VAN providers) and is billed per-document, per-trading-partner, or\n  via subscription. The standard itself is governed by ASC X12 membership.'\nnotes: EDI 214 is a standard. FinOps mapping should be reconciled per chosen vendor invoice (Stedi, SPS,\n  Flexport, etc.).\nsources:\n  - https://x12.org/\n  - https://www.stedi.com/pricing\n  - https://www.spscommerce.com/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl:\
  \ https://focus.finops.org/focus-specification/v1-3/\npublisherName: ASC X12 (standard) / VAN or EDI-platform vendor (commercial)\nserviceCategory: EDI\nbillingModel:\n  pricingCategory: Subscription + Usage\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Adjustment\nfocusColumns:\n  ServiceName: EDI 214 Shipment Status\n  ServiceCategory: EDI\n  ProviderName: ASC X12 / vendor of choice\n  PublisherName: ASC X12 / vendor of choice\n  InvoiceIssuerName: vendor of choice\n  BillingCurrency: USD\nmeters:\n  - name: edi_214_documents\n    unit: document\n    aggregation: sum\n    dimensions:\n      - direction\n      - trading_partner\n      - vendor\n  - name: trading_partner_connections\n    unit: partner\n    aggregation: sum\n    dimensions:\n      - vendor\n  - name: kc_kilo_characters\n    unit: KC\n    aggregation: sum\n    dimensions:\n      - vendor\nprinciples:\n  - name: Visibility\n    description: Pull document counts\
  \ from the chosen EDI vendor (e.g., Stedi usage report, SPS dashboard);\n      reconcile against monthly invoice.\n  - name: Allocation\n    description: Tag 214 traffic by trading partner, mode (truckload, ocean, air), and originating supply-chain\n      node.\n  - name: Optimization\n    description: Consolidate trading partners onto a single VAN/platform to qualify for volume tiers;\n      avoid duplicate document submissions on retry; cache reference data.\n  - name: Accountability\n    description: Logistics IT owns the EDI vendor relationship; finance reviews per-document fees vs.\n      forecast.\nmaintainers:\n  - name: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/edi-214/refs/heads/main/finops/edi-214-finops.yml
sources:
- https://x12.org/
- https://www.stedi.com/pricing
- https://www.spscommerce.com/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- EDI
- X12
- Logistics
---
