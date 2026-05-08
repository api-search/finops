---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: energy-transfer-messenger-api-openapi.yml
  format: yaml
  label: Energy Transfer Messenger+ API
  slug: messenger-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/energy-transfer/refs/heads/main/openapi/energy-transfer-messenger-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  - Adjustment
  pricingCategory: Tariff / Contract
description: FOCUS-aligned FinOps placeholder for Energy Transfer's Messenger+ platform. The economic surface here is pipeline transportation and storage services governed by FERC-filed tariffs, not per-API-call billing; FinOps practice attaches to the underlying logistics service rather than developer metering.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Energy Transfer LP
  ProviderName: Energy Transfer
  PublisherName: Energy Transfer LP
  ServiceCategory: Pipeline & Midstream Services
  ServiceName: Energy Transfer Messenger+ API
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
  - cycle
  name: scheduled_volume
  unit: MMBtu
- aggregation: sum
  dimensions:
  - contract
  name: contract_fee
  unit: month
name: Energy Transfer Finops
provider_name: Energy Transfer
provider_slug: energy-transfer
publisher_name: Energy Transfer LP
service_category: Pipeline & Midstream Services
slug: energy-transfer-finops
source_filename: energy-transfer-finops.yml
source_heading: FinOps Profile
source_url: https://dev.messenger.energytransfer.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Energy Transfer\nproviderId: energy-transfer\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Energy\n  - Pipelines\n  - Midstream\n  - FinOps\n  - FOCUS\ndescription: FOCUS-aligned FinOps placeholder for Energy Transfer's Messenger+ platform. The economic\n  surface here is pipeline transportation and storage services governed by FERC-filed tariffs, not per-API-call\n  billing; FinOps practice attaches to the underlying logistics service rather than developer metering.\nnotes: No public usage/billing API was located. The relevant cost lines are pipeline tariff charges and\n  contracted services; reconcile against the executed Transportation Service Agreement.\nsources:\n  - https://dev.messenger.energytransfer.com/\n  - https://www.energytransfer.com/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n\
  \  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Energy Transfer LP\nserviceCategory: Pipeline & Midstream Services\nbillingModel:\n  pricingCategory: Tariff / Contract\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Adjustment\nfocusColumns:\n  ServiceName: Energy Transfer Messenger+ API\n  ServiceCategory: Pipeline & Midstream Services\n  ProviderName: Energy Transfer\n  PublisherName: Energy Transfer LP\n  InvoiceIssuerName: Energy Transfer LP\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - endpoint\n      - shipper\n  - name: scheduled_volume\n    unit: MMBtu\n    aggregation: sum\n    dimensions:\n      - pipeline\n      - shipper\n      - cycle\n  - name: contract_fee\n    unit: month\n    aggregation: sum\n    dimensions:\n      - contract\n\
  principles:\n  - name: Visibility\n    description: Visibility into pipeline usage and charges flows through Messenger+ statements and the\n      monthly transportation invoice rather than an API-billing dashboard.\n  - name: Allocation\n    description: Allocate charges by shipper contract, pipeline, and nomination cycle.\n  - name: Optimization\n    description: Optimization is achieved through nomination accuracy, cycle scheduling, and capacity contract\n      structuring; there are no API-level discount programs.\n  - name: Accountability\n    description: The shipper's commercial/operations team owns spend and reconciles against the Transportation\n      Service Agreement and FERC-filed tariff.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/energy-transfer/refs/heads/main/finops/energy-transfer-finops.yml
sources:
- https://dev.messenger.energytransfer.com/
- https://www.energytransfer.com/
specification: FinOps Framework
tags:
- Energy
- Pipelines
- Midstream
- FinOps
- FOCUS
---
