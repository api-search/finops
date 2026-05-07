---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: Per-Tariff / Per-Volume
  chargeCategories:
  - Usage
  - Purchase
  pricingCategory: Regulated Tariff
description: FOCUS-aligned FinOps placeholder for Plains All American Pipeline. The provider's monetization is pipeline transportation and storage tariffs, not metered API consumption. There is no public per-call price book to model.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Plains All American Pipeline, L.P.
  ProviderName: Plains All American Pipeline
  PublisherName: Plains All American Pipeline, L.P.
  ServiceCategory: Midstream Energy
  ServiceName: Plains Pipeline Transportation
  ServiceSubcategory: Crude Oil and NGL Pipeline / Storage
layout: finops
meters:
- aggregation: sum
  description: Volume transported through Plains pipelines under a shipper contract; billed via FERC tariff.
  dimensions:
  - pipeline
  - origin
  - destination
  - product
  name: barrels_transported
  unit: barrel
- aggregation: max
  description: Contracted storage capacity at Plains terminals.
  dimensions:
  - terminal
  name: storage_capacity
  unit: barrel-month
- aggregation: sum
  description: FERC-tariff per-barrel transportation charge.
  dimensions:
  - tariff_id
  - route
  name: tariff_charge
  unit: USD
name: Plains All American Pipeline Finops
provider_name: Plains All American Pipeline
provider_slug: plains-all-american-pipeline
publisher_name: Plains All American Pipeline, L.P.
service_category: Midstream Energy
slug: plains-all-american-pipeline-finops
source_filename: plains-all-american-pipeline-finops.yml
source_heading: FinOps Profile
source_url: https://www.plains.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Plains All American Pipeline\nproviderId: plains-all-american-pipeline\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Energy\n  - Pipeline\n  - Midstream\nnotes: Plains All American Pipeline is a midstream energy operator, not a software / API vendor.\n  There is no public metered API to model. This artifact captures the FinOps shape only at the\n  shipper-contract level under FERC tariffs.\ndescription: FOCUS-aligned FinOps placeholder for Plains All American Pipeline. The provider's\n  monetization is pipeline transportation and storage tariffs, not metered API consumption. There\n  is no public per-call price book to model.\nsources:\n  - https://www.plains.com/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion:\
  \ '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Plains All American Pipeline, L.P.\nserviceCategory: Midstream Energy\nbillingModel:\n  pricingCategory: Regulated Tariff\n  billingFrequency: Per-Tariff / Per-Volume\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\nfocusColumns:\n  ServiceName: Plains Pipeline Transportation\n  ServiceCategory: Midstream Energy\n  ServiceSubcategory: Crude Oil and NGL Pipeline / Storage\n  ProviderName: Plains All American Pipeline\n  PublisherName: Plains All American Pipeline, L.P.\n  InvoiceIssuerName: Plains All American Pipeline, L.P.\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: barrels_transported\n    description: Volume transported through Plains pipelines under a shipper contract; billed via\n      FERC tariff.\n    unit: barrel\n    aggregation: sum\n    dimensions:\n      - pipeline\n      - origin\n      - destination\n      - product\n  - name: storage_capacity\n\
  \    description: Contracted storage capacity at Plains terminals.\n    unit: barrel-month\n    aggregation: max\n    dimensions:\n      - terminal\n  - name: tariff_charge\n    description: FERC-tariff per-barrel transportation charge.\n    unit: USD\n    aggregation: sum\n    dimensions:\n      - tariff_id\n      - route\nprinciples:\n  - name: Visibility\n    description: Track shipper nominations and actual movements via the Plains shipper portal /\n      EDI; reconcile against monthly tariff invoices.\n  - name: Allocation\n    description: Allocate barrels and tariff cost to the producing field, trading desk, or refining\n      cost center on the shipper side.\n  - name: Optimization\n    description: Optimize routing and committed volume against tariff structure; review committed\n      capacity vs. actual nominations quarterly.\n  - name: Accountability\n    description: Shipper-side scheduling and commercial team own the contract; finance reviews\n      tariff invoices monthly.\n\
  maintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/plains-all-american-pipeline/refs/heads/main/finops/plains-all-american-pipeline-finops.yml
sources:
- https://www.plains.com/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Energy
- Pipeline
- Midstream
---
