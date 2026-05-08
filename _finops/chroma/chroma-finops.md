---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: chroma-server-api-openapi.yml
  format: yaml
  label: Chroma Server API
  slug: server-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/chroma/refs/heads/main/openapi/chroma-server-api-openapi.yml
- filename: chroma-cloud-api-openapi.yml
  format: yaml
  label: Chroma Cloud API
  slug: cloud-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/chroma/refs/heads/main/openapi/chroma-cloud-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  - Credit
  - Tax
  - Adjustment
  pricingCategory: Subscription + Pay-As-You-Go
description: 'FOCUS-aligned FinOps for Chroma Cloud: hybrid Subscription + Pay-As-You-Go on four primitives (Write, Storage, Query, Network) with monthly credits on Starter and Team, and custom-priced Enterprise (including BYOC).'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Chroma, Inc.
  PricingCategory: Pay-As-You-Go
  ProviderName: Chroma
  PublisherName: Chroma, Inc.
  ServiceCategory: AI Infrastructure / Vector Database
  ServiceName: Chroma Cloud
layout: finops
meters:
- aggregation: sum
  description: GiB written into Chroma Cloud collections
  dimensions:
  - database
  - collection
  - tenant
  name: write
  unit: GiB
- aggregation: sum
  description: GiB-month of vector and metadata storage
  dimensions:
  - database
  - tenant
  name: storage
  unit: GiB-month
- aggregation: sum
  description: TiB scanned by similarity, full-text, and metadata queries
  dimensions:
  - database
  - collection
  - tenant
  name: query
  unit: TiB
- aggregation: sum
  description: GiB of response data returned over the network
  dimensions:
  - database
  - tenant
  name: network
  unit: GiB
- aggregation: sum
  description: Monthly Team / Enterprise plan fee
  dimensions:
  - plan
  name: plan_fee
  unit: month
- aggregation: max
  description: Team member seats consumed (Team / Enterprise)
  dimensions:
  - plan
  name: seats
  unit: seat
name: Chroma Finops
provider_name: Chroma
provider_slug: chroma
publisher_name: Chroma, Inc.
service_category: AI Infrastructure / Vector Database
slug: chroma-finops
source_filename: chroma-finops.yml
source_heading: FinOps Profile
source_url: https://www.trychroma.com/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Chroma\nproviderId: chroma\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - AI\n  - Vector Database\n  - Retrieval\n  - Serverless\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps for Chroma Cloud: hybrid Subscription + Pay-As-You-Go on four\n  primitives (Write, Storage, Query, Network) with monthly credits on Starter and Team, and\n  custom-priced Enterprise (including BYOC).'\nsources:\n  - https://www.trychroma.com/pricing\n  - https://docs.trychroma.com/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Chroma, Inc.\nserviceCategory: AI Infrastructure / Vector Database\nbillingModel:\n  pricingCategory: Subscription + Pay-As-You-Go\n  billingFrequency:\
  \ Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Credit\n    - Tax\n    - Adjustment\nfocusColumns:\n  ServiceName: Chroma Cloud\n  ServiceCategory: AI Infrastructure / Vector Database\n  ProviderName: Chroma\n  PublisherName: Chroma, Inc.\n  InvoiceIssuerName: Chroma, Inc.\n  BillingCurrency: USD\n  ChargeCategory: Usage\n  PricingCategory: Pay-As-You-Go\nmeters:\n  - name: write\n    description: GiB written into Chroma Cloud collections\n    unit: GiB\n    aggregation: sum\n    dimensions:\n      - database\n      - collection\n      - tenant\n  - name: storage\n    description: GiB-month of vector and metadata storage\n    unit: GiB-month\n    aggregation: sum\n    dimensions:\n      - database\n      - tenant\n  - name: query\n    description: TiB scanned by similarity, full-text, and metadata queries\n    unit: TiB\n    aggregation: sum\n    dimensions:\n      - database\n      - collection\n      - tenant\n  - name: network\n    description:\
  \ GiB of response data returned over the network\n    unit: GiB\n    aggregation: sum\n    dimensions:\n      - database\n      - tenant\n  - name: plan_fee\n    description: Monthly Team / Enterprise plan fee\n    unit: month\n    aggregation: sum\n    dimensions:\n      - plan\n  - name: seats\n    description: Team member seats consumed (Team / Enterprise)\n    unit: seat\n    aggregation: max\n    dimensions:\n      - plan\nprinciples:\n  - name: Visibility\n    description: Track Chroma Cloud spend through the in-product usage dashboard (Write GiB, Storage\n      GiB-month, Query TiB, Network GiB) and the credit-burn ledger.\n  - name: Allocation\n    description: Tag spend by database and tenant — Chroma's primitives align naturally with\n      database / collection boundaries for showback to AI features.\n  - name: Optimization\n    description: Reduce dimensionality, batch writes, prune stale collections, cache frequent queries\n      upstream, and right-size embeddings to lower\
  \ Storage and Query meters.\n  - name: Accountability\n    description: AI / ML teams own collection design and recall quality; platform engineering owns\n      Chroma cost dashboards; finance reconciles invoices and credit consumption.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/chroma/refs/heads/main/finops/chroma-finops.yml
sources:
- https://www.trychroma.com/pricing
- https://docs.trychroma.com/
specification: FinOps Framework
tags:
- AI
- Vector Database
- Retrieval
- Serverless
- FinOps
- FOCUS
---
