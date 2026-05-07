---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: enterprise-products-partners-pipeline-operations-api-openapi.yml
  format: yaml
  label: Enterprise Products Partners Pipeline Operations API
  slug: pipeline-operations-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/enterprise-products-partners/refs/heads/main/openapi/enterprise-products-partners-pipeline-operations-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  - Adjustment
  pricingCategory: Tariff / Contract
description: FOCUS-aligned FinOps placeholder for Enterprise Products Partners. The economic surface here is pipeline transportation, NGL fractionation, and storage services governed by FERC-filed tariffs and bilateral service agreements rather than per-API-call billing. FinOps practice attaches to the underlying logistics service, not to API metering.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Enterprise Products Partners L.P.
  ProviderName: Enterprise Products Partners
  PublisherName: Enterprise Products Partners L.P.
  ServiceCategory: Pipeline & Midstream Services
  ServiceName: Enterprise Products Partners Pipeline Operations API
layout: finops
meters:
- aggregation: sum
  dimensions:
  - endpoint
  - shipper
  name: api_requests
  unit: request
- aggregation: sum
  dimensions:
  - pipeline
  - shipper
  - product
  name: pipeline_throughput
  unit: barrel
- aggregation: sum
  dimensions:
  - terminal
  - shipper
  name: storage_capacity
  unit: barrel-month
- aggregation: sum
  dimensions:
  - contract
  name: contract_fee
  unit: month
name: Enterprise Products Partners Finops
provider_name: Enterprise Products Partners
provider_slug: enterprise-products-partners
publisher_name: Enterprise Products Partners L.P.
service_category: Pipeline & Midstream Services
slug: enterprise-products-partners-finops
source_filename: enterprise-products-partners-finops.yml
source_heading: FinOps Profile
source_url: https://www.enterpriseproducts.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Enterprise Products Partners\nproviderId: enterprise-products-partners\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Energy\n  - Midstream\n  - Pipelines\n  - FinOps\n  - FOCUS\ndescription: FOCUS-aligned FinOps placeholder for Enterprise Products Partners. The economic surface here\n  is pipeline transportation, NGL fractionation, and storage services governed by FERC-filed tariffs and\n  bilateral service agreements rather than per-API-call billing. FinOps practice attaches to the underlying\n  logistics service, not to API metering.\nnotes: No public usage/billing API was located. The relevant cost lines are pipeline tariff charges, NGL\n  processing fees, and contracted storage; reconcile against the executed Transportation/Service Agreement.\nsources:\n  - https://www.enterpriseproducts.com/\n  - https://www.enterpriseproducts.com/operations\n\
  alignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Enterprise Products Partners L.P.\nserviceCategory: Pipeline & Midstream Services\nbillingModel:\n  pricingCategory: Tariff / Contract\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Adjustment\nfocusColumns:\n  ServiceName: Enterprise Products Partners Pipeline Operations API\n  ServiceCategory: Pipeline & Midstream Services\n  ProviderName: Enterprise Products Partners\n  PublisherName: Enterprise Products Partners L.P.\n  InvoiceIssuerName: Enterprise Products Partners L.P.\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - endpoint\n      - shipper\n  - name: pipeline_throughput\n    unit: barrel\n\
  \    aggregation: sum\n    dimensions:\n      - pipeline\n      - shipper\n      - product\n  - name: storage_capacity\n    unit: barrel-month\n    aggregation: sum\n    dimensions:\n      - terminal\n      - shipper\n  - name: contract_fee\n    unit: month\n    aggregation: sum\n    dimensions:\n      - contract\nprinciples:\n  - name: Visibility\n    description: Visibility into pipeline usage and charges flows through monthly transportation/storage\n      invoices and shipper portals rather than an API-billing dashboard.\n  - name: Allocation\n    description: Allocate charges by shipper contract, pipeline segment, terminal, and product category\n      (crude/NGL/natural gas/refined).\n  - name: Optimization\n    description: Optimization is achieved through nomination accuracy, capacity contract structuring, and\n      multi-product bundling; there are no API-level discount programs.\n  - name: Accountability\n    description: The shipper's commercial/operations team owns spend and\
  \ reconciles against the executed\n      service agreement and FERC-filed tariff.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/enterprise-products-partners/refs/heads/main/finops/enterprise-products-partners-finops.yml
sources:
- https://www.enterpriseproducts.com/
- https://www.enterpriseproducts.com/operations
specification: FinOps Framework
tags:
- Energy
- Midstream
- Pipelines
- FinOps
- FOCUS
---
