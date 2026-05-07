---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: redfin-stingray-api-openapi.yml
  format: yaml
  label: Redfin Stingray API
  slug: redfin-stingray-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/redfin/refs/heads/main/openapi/redfin-stingray-api-openapi.yml
- filename: redfin-gis-csv-api-openapi.yml
  format: yaml
  label: Redfin GIS CSV Export API
  slug: redfin-gis-csv-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/redfin/refs/heads/main/openapi/redfin-gis-csv-api-openapi.yml
- filename: redfin-data-center-openapi.yml
  format: yaml
  label: Redfin Data Center
  slug: redfin-data-center
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/redfin/refs/heads/main/openapi/redfin-data-center-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Per-Invoice
  chargeCategories:
  - Purchase
  pricingCategory: Contact Sales
description: FinOps shape for Redfin programmatic data partnerships. Redfin does not publish self-serve API pricing; spend is governed by the partner contract and any FinOps allocation must be derived from invoices supplied by Redfin under that contract.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Redfin Corporation
  ProviderName: Redfin
  PublisherName: Redfin Corporation
  ServiceCategory: Real Estate Data
  ServiceName: Redfin
layout: finops
meters:
- aggregation: sum
  name: contract_term
  unit: month
name: Redfin Finops
provider_name: Redfin
provider_slug: redfin
publisher_name: Redfin Corporation
service_category: Real Estate Data
slug: redfin-finops
source_filename: redfin-finops.yml
source_heading: FinOps Profile
source_url: https://www.redfin.com/news/data-center-metrics-definitions/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Redfin\nproviderId: redfin\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Real Estate\n  - Property Data\ndescription: FinOps shape for Redfin programmatic data partnerships. Redfin does not publish self-serve\n  API pricing; spend is governed by the partner contract and any FinOps allocation must be derived from\n  invoices supplied by Redfin under that contract.\nsources:\n  - https://www.redfin.com/news/data-center-metrics-definitions/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Redfin Corporation\nserviceCategory: Real Estate Data\nbillingModel:\n  pricingCategory: Contact Sales\n  billingFrequency: Per-Invoice\n  billingCurrency:\
  \ USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: Redfin\n  ServiceCategory: Real Estate Data\n  ProviderName: Redfin\n  PublisherName: Redfin Corporation\n  InvoiceIssuerName: Redfin Corporation\n  BillingCurrency: USD\nmeters:\n  - name: contract_term\n    unit: month\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Track Redfin partnership invoices and any agreed usage reports; no public usage API\n      exists, so visibility relies on contractual reporting.\n  - name: Allocation\n    description: Allocate Redfin partnership cost to the consuming product line; without per-call telemetry\n      use the contract's negotiated unit (per-feed, per-region) as the allocation key.\n  - name: Optimization\n    description: Optimization is contractual — renegotiate scope, geography, and refresh cadence at renewal\n      rather than tuning request volume.\n  - name: Accountability\n    description: Owner is the partnership/data team that signed\
  \ the Redfin contract; renewals and scope\n      changes go through that owner.\nnotes: No public pricing or usage API; FinOps shape reflects a contract-driven data partnership rather\n  than a metered API. Generic meters/columns removed.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/redfin/refs/heads/main/finops/redfin-finops.yml
sources:
- https://www.redfin.com/news/data-center-metrics-definitions/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Real Estate
- Property Data
---
