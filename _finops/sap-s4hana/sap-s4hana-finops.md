---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: overview
  format: yaml
  label: SAP S/4HANA Business Partner API
  slug: sap-s4hana-business-partner-api
  spec_type: OpenAPI
  url: https://api.sap.com/api/API_BUSINESS_PARTNER/overview
- filename: sap-s4hana-sales-order-openapi.yml
  format: yaml
  label: SAP S/4HANA Sales Order API
  slug: sap-s4hana-sales-order-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/sap-s4hana/refs/heads/main/openapi/sap-s4hana-sales-order-openapi.yml
- filename: overview
  format: yaml
  label: SAP S/4HANA Purchase Order API
  slug: sap-s4hana-purchase-order-api
  spec_type: OpenAPI
  url: https://api.sap.com/api/API_PURCHASEORDER_PROCESS_SRV/overview
- filename: overview
  format: yaml
  label: SAP S/4HANA Material Document API
  slug: sap-s4hana-material-document-api
  spec_type: OpenAPI
  url: https://api.sap.com/api/API_MATERIAL_DOCUMENT_SRV/overview
- filename: overview
  format: yaml
  label: SAP S/4HANA Product Master API
  slug: sap-s4hana-product-master-api
  spec_type: OpenAPI
  url: https://api.sap.com/api/API_PRODUCT_SRV/overview
- filename: overview
  format: yaml
  label: SAP S/4HANA Journal Entry API
  slug: sap-s4hana-journal-entry-api
  spec_type: OpenAPI
  url: https://api.sap.com/api/API_JOURNALENTRY_SRV/overview
- filename: overview
  format: yaml
  label: SAP S/4HANA Billing Document API
  slug: sap-s4hana-billing-document-api
  spec_type: OpenAPI
  url: https://api.sap.com/api/API_BILLING_DOCUMENT_SRV/overview
- filename: overview
  format: yaml
  label: SAP S/4HANA Supplier Invoice API
  slug: sap-s4hana-supplier-invoice-api
  spec_type: OpenAPI
  url: https://api.sap.com/api/API_SUPPLIERINVOICE_PROCESS_SRV/overview
- filename: overview
  format: yaml
  label: SAP S/4HANA Customer Return API
  slug: sap-s4hana-customer-return-api
  spec_type: OpenAPI
  url: https://api.sap.com/api/API_CUSTOMER_RETURN_SRV/overview
- filename: overview
  format: yaml
  label: SAP S/4HANA Purchase Requisition API
  slug: sap-s4hana-purchase-requisition-api
  spec_type: OpenAPI
  url: https://api.sap.com/api/API_PURCHASEREQ_PROCESS_SRV/overview
- filename: overview
  format: yaml
  label: SAP S/4HANA Outbound Delivery API
  slug: sap-s4hana-outbound-delivery-api
  spec_type: OpenAPI
  url: https://api.sap.com/api/API_OUTBOUND_DELIVERY_SRV_0002/overview
- filename: overview
  format: yaml
  label: SAP S/4HANA Inbound Delivery API
  slug: sap-s4hana-inbound-delivery-api
  spec_type: OpenAPI
  url: https://api.sap.com/api/API_INBOUND_DELIVERY_SRV_0002/overview
- filename: overview
  format: yaml
  label: SAP S/4HANA Cost Center API
  slug: sap-s4hana-cost-center-api
  spec_type: OpenAPI
  url: https://api.sap.com/api/API_COSTCENTER_SRV/overview
- filename: overview
  format: yaml
  label: SAP S/4HANA GL Account API
  slug: sap-s4hana-gl-account-api
  spec_type: OpenAPI
  url: https://api.sap.com/api/API_GLACCOUNTINCHARTOFACCOUNTS_SRV/overview
- filename: overview
  format: yaml
  label: SAP S/4HANA Bank Master API
  slug: sap-s4hana-bank-master-api
  spec_type: OpenAPI
  url: https://api.sap.com/api/API_BANKDETAIL_SRV/overview
- filename: overview
  format: yaml
  label: SAP S/4HANA Production Order API
  slug: sap-s4hana-production-order-api
  spec_type: OpenAPI
  url: https://api.sap.com/api/API_PRODUCTION_ORDER_2_SRV/overview
- filename: overview
  format: yaml
  label: SAP S/4HANA Maintenance Order API
  slug: sap-s4hana-maintenance-order-api
  spec_type: OpenAPI
  url: https://api.sap.com/api/API_MAINTENANCEORDER/overview
- filename: overview
  format: yaml
  label: SAP S/4HANA Workforce Timesheet API
  slug: sap-s4hana-workforce-timesheet-api
  spec_type: OpenAPI
  url: https://api.sap.com/api/API_MANAGE_WORKFORCE_TIMESHEET/overview
billing_model:
  billingCurrency: USD (varies by contract)
  billingFrequency: Per-Contract
  chargeCategories:
  - Purchase
  - Usage
  - Adjustment
  pricingCategory: Contract / Negotiated
description: 'FOCUS-aligned FinOps shape for SAP S/4HANA: ERP suite licensed via SAP Enterprise Agreement (Public Cloud Edition, Private Cloud, On-Premise) or RISE with SAP. Cost visibility is via SAP''s commercial contract and BTP cockpit; no public unit pricing.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: SAP SE
  ProviderName: SAP S/4HANA
  PublisherName: SAP SE
  ServiceCategory: ERP
  ServiceName: SAP S/4HANA
layout: finops
meters:
- aggregation: sum
  name: contracted_consumption
  unit: varies
name: Sap S4Hana Finops
provider_name: SAP S/4HANA
provider_slug: sap-s4hana
publisher_name: SAP SE
service_category: ERP
slug: sap-s4hana-finops
source_filename: sap-s4hana-finops.yml
source_heading: FinOps Profile
source_url: https://www.sap.com/products/erp/s4hana.html
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: SAP S/4HANA\nproviderId: sap-s4hana\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n- FinOps\n- FOCUS\n- ERP\n- Enterprise\n- SAP\ndescription: 'FOCUS-aligned FinOps shape for SAP S/4HANA: ERP suite licensed via SAP Enterprise Agreement\n  (Public Cloud Edition, Private Cloud, On-Premise) or RISE with SAP. Cost visibility is via SAP''s commercial\n  contract and BTP cockpit; no public unit pricing.'\nnotes: SAP S/4HANA is sold via SAP enterprise license agreements (Cloud, Private Cloud, On-Premise) and\n  priced based on SAPS / users / modules / RISE-with-SAP commitments. The public pricing page returns\n  HTTP 403; pricing is engaged via SAP sales and partner channels.\nsources:\n- https://www.sap.com/products/erp/s4hana.html\n- https://api.sap.com/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n\
  \  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: SAP SE\nserviceCategory: ERP\nbillingModel:\n  pricingCategory: Contract / Negotiated\n  billingFrequency: Per-Contract\n  billingCurrency: USD (varies by contract)\n  chargeCategories:\n  - Purchase\n  - Usage\n  - Adjustment\nfocusColumns:\n  ServiceName: SAP S/4HANA\n  ServiceCategory: ERP\n  ProviderName: SAP S/4HANA\n  PublisherName: SAP SE\n  InvoiceIssuerName: SAP SE\n  BillingCurrency: USD\nmeters:\n- name: contracted_consumption\n  unit: varies\n  aggregation: sum\nprinciples:\n- name: Visibility\n  description: Consumption visibility comes from the SAP S/4HANA account / partner reporting surface (invoices,\n    account dashboards) rather than a public usage API.\n- name: Allocation\n  description: Allocate cost through the SAP S/4HANA contract structure (entitlement, project, business\n    unit) and reconcile against internal cost centers.\n- name: Optimization\n\
  \  description: 'Optimization levers are commercial: renegotiation cadence, commitment sizing, and consolidation\n    of SAP S/4HANA entitlements.'\n- name: Accountability\n  description: Assign a contract owner who reconciles SAP S/4HANA invoices against contracted entitlements\n    each billing cycle.\nmaintainers:\n- FN: Kin Lane\n  email: kin@apievangelist.com\n  url: https://apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/sap-s4hana/refs/heads/main/finops/sap-s4hana-finops.yml
sources:
- https://www.sap.com/products/erp/s4hana.html
- https://api.sap.com/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- ERP
- Enterprise
- SAP
---
