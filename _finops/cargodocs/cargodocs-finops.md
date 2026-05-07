---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: cargodocs-partner-openapi.yml
  format: yaml
  label: CargoDocs Partner API
  slug: partner-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/cargodocs/refs/heads/main/openapi/cargodocs-partner-openapi.yml
- filename: cargodocs-issuer-openapi.yml
  format: yaml
  label: CargoDocs Issuer API
  slug: issuer-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/cargodocs/refs/heads/main/openapi/cargodocs-issuer-openapi.yml
- filename: cargodocs-customer-openapi.yml
  format: yaml
  label: CargoDocs Customer Data/Docs API
  slug: customer-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/cargodocs/refs/heads/main/openapi/cargodocs-customer-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  - Usage
  - Adjustment
  pricingCategory: Subscription + Per-Document
description: 'FOCUS-aligned FinOps for CargoDocs (EssDocs): enterprise license + per-document fees on electronic bills of lading and trade documents; billing is contract-based.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Electronic Shipping Solutions Limited
  ProviderName: CargoDocs
  PublisherName: Electronic Shipping Solutions Limited
  ServiceCategory: Trade Documentation Platform
  ServiceName: CargoDocs DocEx
layout: finops
meters:
- aggregation: sum
  dimensions:
  - module
  name: enterprise_license
  unit: year
- aggregation: sum
  dimensions:
  - document_type
  - issuer
  - geography
  name: document_issuance
  unit: document
- aggregation: sum
  dimensions:
  - document_type
  name: document_transfers
  unit: event
- aggregation: max
  dimensions:
  - role
  name: named_users
  unit: seat-month
name: Cargodocs Finops
provider_name: CargoDocs
provider_slug: cargodocs
publisher_name: Electronic Shipping Solutions Limited
service_category: Trade Documentation Platform
slug: cargodocs-finops
source_filename: cargodocs-finops.yml
source_heading: FinOps Profile
source_url: https://www.essdocs.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: CargoDocs\nproviderId: cargodocs\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Trade Documentation\n  - Shipping\n  - Supply Chain\ndescription: 'FOCUS-aligned FinOps for CargoDocs (EssDocs): enterprise license + per-document fees on\n  electronic bills of lading and trade documents; billing is contract-based.'\nnotes: CargoDocs/EssDocs does not publish public API or document-volume pricing. FinOps mapping is provisional\n  pending enterprise-contract reconciliation.\nsources:\n  - https://www.essdocs.com/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Electronic Shipping Solutions Limited\nserviceCategory: Trade Documentation\
  \ Platform\nbillingModel:\n  pricingCategory: Subscription + Per-Document\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\n    - Adjustment\nfocusColumns:\n  ServiceName: CargoDocs DocEx\n  ServiceCategory: Trade Documentation Platform\n  ProviderName: CargoDocs\n  PublisherName: Electronic Shipping Solutions Limited\n  InvoiceIssuerName: Electronic Shipping Solutions Limited\n  BillingCurrency: USD\nmeters:\n  - name: enterprise_license\n    unit: year\n    aggregation: sum\n    dimensions:\n      - module\n  - name: document_issuance\n    unit: document\n    aggregation: sum\n    dimensions:\n      - document_type\n      - issuer\n      - geography\n  - name: document_transfers\n    unit: event\n    aggregation: sum\n    dimensions:\n      - document_type\n  - name: named_users\n    unit: seat-month\n    aggregation: max\n    dimensions:\n      - role\nprinciples:\n  - name: Visibility\n    description: Visibility into document-volume\
  \ costs is via EssDocs customer reports; the platform\n      audit log identifies issuance, transfer, and surrender events for cost attribution.\n  - name: Allocation\n    description: Allocate by issuer entity (carrier/NVOCC), trade lane, and document type; multi-business-unit\n      customers should configure separate issuer codes.\n  - name: Optimization\n    description: Consolidate document issuance windows, retire unused user seats, and align module selection\n      to active document types.\n  - name: Accountability\n    description: Trade-operations / digital-trade lead owns the relationship; quarterly volume reviews\n      with EssDocs are typical.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/cargodocs/refs/heads/main/finops/cargodocs-finops.yml
sources:
- https://www.essdocs.com/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Trade Documentation
- Shipping
- Supply Chain
---
