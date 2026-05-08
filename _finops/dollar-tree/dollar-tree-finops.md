---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: Not Applicable
  chargeCategories: []
  pricingCategory: Not Applicable (No Public API)
description: FOCUS-aligned FinOps shape for Dollar Tree vendor integrations. Dollar Tree does not invoice for API consumption; FinOps focus is on the consumer-side cost of running EDI/SAP integration with the Vendor Portal.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Not Applicable
  ProviderName: Dollar Tree
  PublisherName: Dollar Tree, Inc.
  ServiceCategory: Retail / Vendor Integration
  ServiceName: Dollar Tree Vendor Portal
layout: finops
meters:
- aggregation: count
  description: EDI documents exchanged with Dollar Tree
  dimensions:
  - document_type
  - direction
  name: edi_documents
  unit: document
name: Dollar Tree Finops
provider_name: Dollar Tree
provider_slug: dollar-tree
publisher_name: Dollar Tree, Inc.
service_category: Retail / Vendor Integration
slug: dollar-tree-finops
source_filename: dollar-tree-finops.yml
source_heading: FinOps Profile
source_url: https://www.dollartree.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Dollar Tree\nproviderId: dollar-tree\npublisherName: Dollar Tree, Inc.\nserviceCategory: Retail / Vendor Integration\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Retail\n  - Discount Retail\n  - EDI\n  - Vendor Management\n  - FinOps\n  - FOCUS\ndescription: FOCUS-aligned FinOps shape for Dollar Tree vendor integrations. Dollar Tree does not invoice\n  for API consumption; FinOps focus is on the consumer-side cost of running EDI/SAP integration with the\n  Vendor Portal.\nnotes: No public API or invoiced consumption; reconciled=false. Meters describe internal integration cost.\nsources:\n  - https://www.dollartree.com/\n\
  billingModel:\n  pricingCategory: Not Applicable (No Public API)\n  billingFrequency: Not Applicable\n  billingCurrency: USD\n  chargeCategories: []\nfocusColumns:\n  ServiceName: Dollar Tree Vendor Portal\n  ServiceCategory: Retail / Vendor Integration\n  ProviderName: Dollar Tree\n  PublisherName: Dollar Tree, Inc.\n  InvoiceIssuerName: Not Applicable\n  BillingCurrency: USD\nmeters:\n  - name: edi_documents\n    description: EDI documents exchanged with Dollar Tree\n    unit: document\n    aggregation: count\n    dimensions:\n      - document_type\n      - direction\nprinciples:\n  - name: Visibility\n    description: Track EDI volumes and acknowledgement latency in the consumer's integration platform;\n      Dollar Tree does not invoice for API access.\n  - name: Allocation\n    description: Allocate EDI/SAP integration cost to the vendor program that owns the trading-partner\n      relationship.\n  - name: Optimization\n    description: Batch EDI transmissions where the trading-partner\
  \ agreement permits; minimise duplicated\n      vendor portal sessions.\n  - name: Accountability\n    description: Vendor program owner is accountable for the trading-partner agreement and integration\n      uptime.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/dollar-tree/refs/heads/main/finops/dollar-tree-finops.yml
sources:
- https://www.dollartree.com/
specification: FinOps Framework
tags:
- Retail
- Discount Retail
- EDI
- Vendor Management
- FinOps
- FOCUS
---
