---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: sap-hana-cloud-rest-api.yml
  format: yaml
  label: SAP HANA Cloud REST API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/sap-hana/refs/heads/main/openapi/sap-hana-cloud-rest-api.yml
billing_model:
  billingCurrency: USD (varies by contract)
  billingFrequency: Per-Contract
  chargeCategories:
  - Purchase
  - Usage
  - Adjustment
  pricingCategory: Contract / Negotiated
description: 'FOCUS-aligned FinOps shape for SAP HANA Cloud: enterprise database licensed via SAP Store / SAP sales contract; consumption visibility is via SAP BTP cockpit and Cloud Management Tools. No public unit pricing.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: SAP SE
  ProviderName: SAP HANA
  PublisherName: SAP SE
  ServiceCategory: Database
  ServiceName: SAP HANA
layout: finops
meters:
- aggregation: sum
  name: contracted_consumption
  unit: varies
name: Sap Hana Finops
provider_name: SAP HANA
provider_slug: sap-hana
publisher_name: SAP SE
service_category: Database
slug: sap-hana-finops
source_filename: sap-hana-finops.yml
source_heading: FinOps Profile
source_url: https://www.sap.com/products/technology-platform/hana.html
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: SAP HANA\nproviderId: sap-hana\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n- FinOps\n- FOCUS\n- Database\n- Enterprise\n- SAP\ndescription: 'FOCUS-aligned FinOps shape for SAP HANA Cloud: enterprise database licensed via SAP Store\n  / SAP sales contract; consumption visibility is via SAP BTP cockpit and Cloud Management Tools. No public\n  unit pricing.'\nnotes: SAP HANA Cloud pricing is gated behind the SAP Discovery Center / SAP Store and SAP corporate sales;\n  the public sap.com pricing page returns HTTP 403 to anonymous fetches and Discovery Center requires\n  authenticated session. Pricing is contract-based via SAP Store / sales engagement.\nsources:\n- https://www.sap.com/products/technology-platform/hana.html\n- https://discovery-center.cloud.sap/serviceCatalog/sap-hana-cloud\nalignedWith:\n  framework: FinOps Foundation Framework\n\
  \  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: SAP SE\nserviceCategory: Database\nbillingModel:\n  pricingCategory: Contract / Negotiated\n  billingFrequency: Per-Contract\n  billingCurrency: USD (varies by contract)\n  chargeCategories:\n  - Purchase\n  - Usage\n  - Adjustment\nfocusColumns:\n  ServiceName: SAP HANA\n  ServiceCategory: Database\n  ProviderName: SAP HANA\n  PublisherName: SAP SE\n  InvoiceIssuerName: SAP SE\n  BillingCurrency: USD\nmeters:\n- name: contracted_consumption\n  unit: varies\n  aggregation: sum\nprinciples:\n- name: Visibility\n  description: Consumption visibility comes from the SAP HANA account / partner reporting surface (invoices,\n    account dashboards) rather than a public usage API.\n- name: Allocation\n  description: Allocate cost through the SAP HANA contract structure (entitlement, project, business unit)\n    and reconcile\
  \ against internal cost centers.\n- name: Optimization\n  description: 'Optimization levers are commercial: renegotiation cadence, commitment sizing, and consolidation\n    of SAP HANA entitlements.'\n- name: Accountability\n  description: Assign a contract owner who reconciles SAP HANA invoices against contracted entitlements\n    each billing cycle.\nmaintainers:\n- FN: Kin Lane\n  email: kin@apievangelist.com\n  url: https://apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/sap-hana/refs/heads/main/finops/sap-hana-finops.yml
sources:
- https://www.sap.com/products/technology-platform/hana.html
- https://discovery-center.cloud.sap/serviceCatalog/sap-hana-cloud
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Database
- Enterprise
- SAP
---
