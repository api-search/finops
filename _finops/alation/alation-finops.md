---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: alation-data-catalog-openapi.yaml
  format: yaml
  label: Alation Data Catalog API
  slug: data-catalog-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/alation/refs/heads/main/openapi/alation-data-catalog-openapi.yaml
- filename: alation-lineage-openapi.yaml
  format: yaml
  label: Alation Lineage API
  slug: lineage-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/alation/refs/heads/main/openapi/alation-lineage-openapi.yaml
- filename: alation-governance-openapi.yaml
  format: yaml
  label: Alation Governance API
  slug: governance-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/alation/refs/heads/main/openapi/alation-governance-openapi.yaml
- filename: alation-search-openapi.yaml
  format: yaml
  label: Alation Search API
  slug: search-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/alation/refs/heads/main/openapi/alation-search-openapi.yaml
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  - Tax
  - Adjustment
  pricingCategory: Subscription
description: 'FOCUS-aligned FinOps for Alation: enterprise platform subscriptions sold by edition + seats with API access included. Public pricing is gated behind a "Request Pricing" form, so per-seat / per-edition rates are not authoritative until reconciled with the negotiated quote.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Alation, Inc.
  ProviderName: Alation
  PublisherName: Alation, Inc.
  ServiceCategory: Data Intelligence Platform
  ServiceName: Alation Data Intelligence Platform
layout: finops
meters:
- aggregation: sum
  description: Annual platform subscription value
  dimensions:
  - edition
  - deployment
  name: platform_subscription
  unit: contract-year
- aggregation: max
  description: Named user seats (steward / curator / consumer)
  dimensions:
  - role
  - region
  name: seats
  unit: seat
- aggregation: max
  description: Source-system connector licenses where billed separately
  dimensions:
  - source
  name: connectors
  unit: connector
name: Alation Finops
provider_name: Alation
provider_slug: alation
publisher_name: Alation, Inc.
service_category: Data Intelligence Platform
slug: alation-finops
source_filename: alation-finops.yml
source_heading: FinOps Profile
source_url: https://www.alation.com/pricing/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Alation\nproviderId: alation\npublisherName: Alation, Inc.\nserviceCategory: Data Intelligence Platform\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Data Catalog\n  - Data Governance\n  - Data Intelligence\n  - Data Lineage\n  - Data Quality\n  - Metadata Management\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps for Alation: enterprise platform subscriptions sold by edition + seats\n  with API access included. Public pricing is gated behind a \"Request Pricing\" form, so per-seat / per-edition\n  rates are not authoritative until reconciled with the negotiated quote.'\nsources:\n  - https://www.alation.com/pricing/\n\
  \  - https://focus.finops.org/focus-specification/v1-3/\nbillingModel:\n  pricingCategory: Subscription\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Tax\n    - Adjustment\nfocusColumns:\n  ServiceName: Alation Data Intelligence Platform\n  ServiceCategory: Data Intelligence Platform\n  ProviderName: Alation\n  PublisherName: Alation, Inc.\n  InvoiceIssuerName: Alation, Inc.\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: platform_subscription\n    description: Annual platform subscription value\n    unit: contract-year\n    aggregation: sum\n    dimensions:\n      - edition\n      - deployment\n  - name: seats\n    description: Named user seats (steward / curator / consumer)\n    unit: seat\n    aggregation: max\n    dimensions:\n      - role\n      - region\n  - name: connectors\n    description: Source-system connector licenses where billed separately\n    unit: connector\n    aggregation: max\n    dimensions:\n\
  \      - source\nprinciples:\n  - name: Visibility\n    description: Surface Alation seat utilization and connector inventory through the Alation admin console;\n      reconcile against annual invoices.\n  - name: Allocation\n    description: Allocate Alation cost across data domains and stewardship teams using seat assignments\n      and curator workload.\n  - name: Optimization\n    description: Reclaim inactive seats during renewals; consolidate redundant connectors; align edition\n      to actual feature usage.\n  - name: Accountability\n    description: Data governance / chief data office typically owns the Alation contract; integrate spend\n      into the data-platform budget review.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/alation/refs/heads/main/finops/alation-finops.yml
sources:
- https://www.alation.com/pricing/
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Data Catalog
- Data Governance
- Data Intelligence
- Data Lineage
- Data Quality
- Metadata Management
- FinOps
- FOCUS
---
