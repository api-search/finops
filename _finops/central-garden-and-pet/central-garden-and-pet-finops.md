---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: Per-Contract
  chargeCategories:
  - Purchase
  - Adjustment
  pricingCategory: Custom (Partner Contract)
description: FOCUS-aligned FinOps scaffold for Central Garden & Pet. No public API pricing exists; meters capture integration telemetry against retailer / distributor contracts that are the actual cost surface.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Central Garden & Pet Company
  ProviderName: Central Garden and Pet
  PublisherName: Central Garden & Pet Company
  ServiceCategory: Consumer Goods Distribution
  ServiceName: Central Garden and Pet API
layout: finops
meters:
- aggregation: sum
  dimensions:
  - endpoint
  - partner
  name: api_requests
  unit: request
- aggregation: count
  dimensions:
  - retailer
  name: orders_synchronized
  unit: order
- aggregation: count
  dimensions:
  - document_type
  - partner
  name: edi_documents_exchanged
  unit: document
name: Central Garden And Pet Finops
provider_name: Central Garden and Pet
provider_slug: central-garden-and-pet
publisher_name: Central Garden & Pet Company
service_category: Consumer Goods (Pet + Garden)
slug: central-garden-and-pet-finops
source_filename: central-garden-and-pet-finops.yml
source_heading: FinOps Profile
source_url: https://www.central.com
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Central Garden and Pet\nproviderId: central-garden-and-pet\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Pet Products\n  - Garden\n  - Consumer\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps scaffold for Central Garden & Pet. No public API pricing exists; meters\n  capture integration telemetry against retailer / distributor contracts that are the actual cost surface.'\nnotes: Cost surface is contract-driven; no per-call invoicing.\nsources:\n  - https://www.central.com\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Central Garden & Pet Company\nserviceCategory: Consumer Goods (Pet + Garden)\nbillingModel:\n  pricingCategory: Custom\
  \ (Partner Contract)\n  billingFrequency: Per-Contract\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Adjustment\nfocusColumns:\n  ServiceName: Central Garden and Pet API\n  ServiceCategory: Consumer Goods Distribution\n  ProviderName: Central Garden and Pet\n  PublisherName: Central Garden & Pet Company\n  InvoiceIssuerName: Central Garden & Pet Company\n  BillingCurrency: USD\nmeters:\n  - name: api_requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - endpoint\n      - partner\n  - name: orders_synchronized\n    unit: order\n    aggregation: count\n    dimensions:\n      - retailer\n  - name: edi_documents_exchanged\n    unit: document\n    aggregation: count\n    dimensions:\n      - document_type\n      - partner\nprinciples:\n  - name: Visibility\n    description: Track partner integration via the negotiated reporting surface delivered with the retailer\n      / distributor contract; no public usage API.\n  - name: Allocation\n    description:\
  \ Tag integration costs to the retailer / distributor relationship and the originating\n      product line (pet vs. garden).\n  - name: Optimization\n    description: Batch order / inventory / shipment EDI documents on the agreed cadence; consolidate\n      redundant SKU master data calls.\n  - name: Accountability\n    description: A retail-channel owner reconciles partner fees against contracts; IT owns EDI / API\n      integration uptime.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/central-garden-and-pet/refs/heads/main/finops/central-garden-and-pet-finops.yml
sources:
- https://www.central.com
specification: FinOps Framework
tags:
- Pet Products
- Garden
- Consumer
- FinOps
- FOCUS
---
