---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: sap-sd-sales-order-openapi.yml
  format: yaml
  label: Sales Order API
  slug: sales-order
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/sap-sales-and-distribution-sd/refs/heads/main/openapi/sap-sd-sales-order-openapi.yml
- filename: sap-sd-customer-master-data-openapi.yml
  format: yaml
  label: Customer Master Data API
  slug: customer-master-data
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/sap-sales-and-distribution-sd/refs/heads/main/openapi/sap-sd-customer-master-data-openapi.yml
- filename: sap-sd-outbound-delivery-openapi.yml
  format: yaml
  label: Outbound Delivery API
  slug: outbound-delivery
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/sap-sales-and-distribution-sd/refs/heads/main/openapi/sap-sd-outbound-delivery-openapi.yml
- filename: sap-sd-billing-document-openapi.yml
  format: yaml
  label: Billing Document API
  slug: billing-document
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/sap-sales-and-distribution-sd/refs/heads/main/openapi/sap-sd-billing-document-openapi.yml
- filename: sap-sd-pricing-openapi.yml
  format: yaml
  label: Pricing API
  slug: pricing
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/sap-sales-and-distribution-sd/refs/heads/main/openapi/sap-sd-pricing-openapi.yml
- filename: sap-sd-sales-quotation-openapi.yml
  format: yaml
  label: Sales Quotation API
  slug: sales-quotation
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/sap-sales-and-distribution-sd/refs/heads/main/openapi/sap-sd-sales-quotation-openapi.yml
- filename: sap-sd-credit-management-openapi.yml
  format: yaml
  label: Credit Management API
  slug: credit-management
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/sap-sales-and-distribution-sd/refs/heads/main/openapi/sap-sd-credit-management-openapi.yml
- filename: sap-sd-material-master-openapi.yml
  format: yaml
  label: Material Master API
  slug: material-master
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/sap-sales-and-distribution-sd/refs/heads/main/openapi/sap-sd-material-master-openapi.yml
- filename: sap-sd-credit-memo-request-openapi.yml
  format: yaml
  label: Credit Memo Request API
  slug: credit-memo-request
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/sap-sales-and-distribution-sd/refs/heads/main/openapi/sap-sd-credit-memo-request-openapi.yml
- filename: sap-sd-debit-memo-request-openapi.yml
  format: yaml
  label: Debit Memo Request API
  slug: debit-memo-request
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/sap-sales-and-distribution-sd/refs/heads/main/openapi/sap-sd-debit-memo-request-openapi.yml
- filename: sap-sd-sales-contract-openapi.yml
  format: yaml
  label: Sales Contract API
  slug: sales-contract
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/sap-sales-and-distribution-sd/refs/heads/main/openapi/sap-sd-sales-contract-openapi.yml
- filename: sap-sd-sales-inquiry-openapi.yml
  format: yaml
  label: Sales Inquiry API
  slug: sales-inquiry
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/sap-sales-and-distribution-sd/refs/heads/main/openapi/sap-sd-sales-inquiry-openapi.yml
- filename: sap-sd-sales-scheduling-agreement-openapi.yml
  format: yaml
  label: Sales Scheduling Agreement API
  slug: sales-scheduling-agreement
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/sap-sales-and-distribution-sd/refs/heads/main/openapi/sap-sd-sales-scheduling-agreement-openapi.yml
- filename: sap-sd-customer-return-openapi.yml
  format: yaml
  label: Customer Return API
  slug: customer-return
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/sap-sales-and-distribution-sd/refs/heads/main/openapi/sap-sd-customer-return-openapi.yml
- filename: sap-sd-customer-returns-delivery-openapi.yml
  format: yaml
  label: Customer Returns Delivery API
  slug: customer-returns-delivery
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/sap-sales-and-distribution-sd/refs/heads/main/openapi/sap-sd-customer-returns-delivery-openapi.yml
- filename: sap-sd-customer-material-openapi.yml
  format: yaml
  label: Customer Material API
  slug: customer-material
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/sap-sales-and-distribution-sd/refs/heads/main/openapi/sap-sd-customer-material-openapi.yml
- filename: sap-sd-inbound-delivery-openapi.yml
  format: yaml
  label: Inbound Delivery API
  slug: inbound-delivery
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/sap-sales-and-distribution-sd/refs/heads/main/openapi/sap-sd-inbound-delivery-openapi.yml
billing_model:
  billingCurrency: USD (varies by contract)
  billingFrequency: Per-Contract
  chargeCategories:
  - Purchase
  - Usage
  - Adjustment
  pricingCategory: Contract / Negotiated
description: 'FOCUS-aligned FinOps shape for SAP Sales and Distribution (SD): module of SAP S/4HANA, licensed under the customer''s S/4HANA / RISE-with-SAP agreement. Costs are absorbed into the parent S/4HANA contract; no per-API pricing.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: SAP SE
  ProviderName: SAP Sales and Distribution (SD)
  PublisherName: SAP SE
  ServiceCategory: ERP Module
  ServiceName: SAP Sales and Distribution (SD)
layout: finops
meters:
- aggregation: sum
  name: contracted_consumption
  unit: varies
name: Sap Sales And Distribution Sd Finops
provider_name: SAP Sales and Distribution (SD)
provider_slug: sap-sales-and-distribution-sd
publisher_name: SAP SE
service_category: ERP Module
slug: sap-sales-and-distribution-sd-finops
source_filename: sap-sales-and-distribution-sd-finops.yml
source_heading: FinOps Profile
source_url: https://www.sap.com/products/scm/sales-distribution.html
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: SAP Sales and Distribution (SD)\nproviderId: sap-sales-and-distribution-sd\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n- FinOps\n- FOCUS\n- ERP\n- Sales\n- SAP\ndescription: 'FOCUS-aligned FinOps shape for SAP Sales and Distribution (SD): module of SAP S/4HANA, licensed\n  under the customer''s S/4HANA / RISE-with-SAP agreement. Costs are absorbed into the parent S/4HANA\n  contract; no per-API pricing.'\nnotes: SAP Sales and Distribution (SD) is a module of SAP S/4HANA / ECC and is licensed as part of the\n  customer's broader S/4HANA agreement; it is not sold or priced as a standalone API product. No public\n  pricing exists.\nsources:\n- https://www.sap.com/products/scm/sales-distribution.html\n- https://api.sap.com/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec:\
  \ FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: SAP SE\nserviceCategory: ERP Module\nbillingModel:\n  pricingCategory: Contract / Negotiated\n  billingFrequency: Per-Contract\n  billingCurrency: USD (varies by contract)\n  chargeCategories:\n  - Purchase\n  - Usage\n  - Adjustment\nfocusColumns:\n  ServiceName: SAP Sales and Distribution (SD)\n  ServiceCategory: ERP Module\n  ProviderName: SAP Sales and Distribution (SD)\n  PublisherName: SAP SE\n  InvoiceIssuerName: SAP SE\n  BillingCurrency: USD\nmeters:\n- name: contracted_consumption\n  unit: varies\n  aggregation: sum\nprinciples:\n- name: Visibility\n  description: Consumption visibility comes from the SAP Sales and Distribution (SD) account / partner\n    reporting surface (invoices, account dashboards) rather than a public usage API.\n- name: Allocation\n  description: Allocate cost through the SAP Sales and Distribution (SD) contract structure (entitlement,\n\
  \    project, business unit) and reconcile against internal cost centers.\n- name: Optimization\n  description: 'Optimization levers are commercial: renegotiation cadence, commitment sizing, and consolidation\n    of SAP Sales and Distribution (SD) entitlements.'\n- name: Accountability\n  description: Assign a contract owner who reconciles SAP Sales and Distribution (SD) invoices against\n    contracted entitlements each billing cycle.\nmaintainers:\n- FN: Kin Lane\n  email: kin@apievangelist.com\n  url: https://apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/sap-sales-and-distribution-sd/refs/heads/main/finops/sap-sales-and-distribution-sd-finops.yml
sources:
- https://www.sap.com/products/scm/sales-distribution.html
- https://api.sap.com/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- ERP
- Sales
- SAP
---
