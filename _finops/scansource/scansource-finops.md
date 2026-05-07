---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: scansource-product-openapi.yml
  format: yaml
  label: ScanSource Product API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/scansource/refs/heads/main/openapi/scansource-product-openapi.yml
- filename: scansource-sales-order-openapi.yml
  format: yaml
  label: ScanSource Sales Order API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/scansource/refs/heads/main/openapi/scansource-sales-order-openapi.yml
- filename: scansource-invoice-openapi.yml
  format: yaml
  label: ScanSource Invoice API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/scansource/refs/heads/main/openapi/scansource-invoice-openapi.yml
billing_model:
  billingCurrency: USD (varies by contract)
  billingFrequency: Per-Contract
  chargeCategories:
  - Purchase
  - Usage
  - Adjustment
  pricingCategory: Contract / Negotiated
description: 'FOCUS-aligned FinOps shape for ScanSource: B2B distributor APIs (product, pricing, inventory, orders) provided to channel partners under their existing partner agreement. No standalone API fee; consumption is operational support to the distribution relationship.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: ScanSource, Inc.
  ProviderName: ScanSource
  PublisherName: ScanSource, Inc.
  ServiceCategory: B2B Distribution
  ServiceName: ScanSource
layout: finops
meters:
- aggregation: sum
  name: contracted_consumption
  unit: varies
name: Scansource Finops
provider_name: ScanSource
provider_slug: scansource
publisher_name: ScanSource, Inc.
service_category: B2B Distribution
slug: scansource-finops
source_filename: scansource-finops.yml
source_heading: FinOps Profile
source_url: https://www.scansource.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: ScanSource\nproviderId: scansource\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n- FinOps\n- FOCUS\n- Distribution\n- B2B\ndescription: 'FOCUS-aligned FinOps shape for ScanSource: B2B distributor APIs (product, pricing, inventory,\n  orders) provided to channel partners under their existing partner agreement. No standalone API fee;\n  consumption is operational support to the distribution relationship.'\nnotes: ScanSource is a B2B technology distributor; its Product API is provisioned for authorized channel\n  partners under a partner agreement. There is no self-service pricing page or public plan tier, and access\n  requires a ScanSource partner account.\nsources:\n- https://www.scansource.com/\n- https://services.scansource.com/api/Help\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n\
  \  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: ScanSource, Inc.\nserviceCategory: B2B Distribution\nbillingModel:\n  pricingCategory: Contract / Negotiated\n  billingFrequency: Per-Contract\n  billingCurrency: USD (varies by contract)\n  chargeCategories:\n  - Purchase\n  - Usage\n  - Adjustment\nfocusColumns:\n  ServiceName: ScanSource\n  ServiceCategory: B2B Distribution\n  ProviderName: ScanSource\n  PublisherName: ScanSource, Inc.\n  InvoiceIssuerName: ScanSource, Inc.\n  BillingCurrency: USD\nmeters:\n- name: contracted_consumption\n  unit: varies\n  aggregation: sum\nprinciples:\n- name: Visibility\n  description: Consumption visibility comes from the ScanSource account / partner reporting surface (invoices,\n    account dashboards) rather than a public usage API.\n- name: Allocation\n  description: Allocate cost through the ScanSource contract structure (entitlement, project, business\n    unit) and\
  \ reconcile against internal cost centers.\n- name: Optimization\n  description: 'Optimization levers are commercial: renegotiation cadence, commitment sizing, and consolidation\n    of ScanSource entitlements.'\n- name: Accountability\n  description: Assign a contract owner who reconciles ScanSource invoices against contracted entitlements\n    each billing cycle.\nmaintainers:\n- FN: Kin Lane\n  email: kin@apievangelist.com\n  url: https://apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/scansource/refs/heads/main/finops/scansource-finops.yml
sources:
- https://www.scansource.com/
- https://services.scansource.com/api/Help
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Distribution
- B2B
---
