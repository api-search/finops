---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: sap-integration-suite-cloud-integration-openapi.yml
  format: yaml
  label: SAP Cloud Integration API
  slug: sap-cloud-integration
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/sap-integration-suite/refs/heads/main/openapi/sap-integration-suite-cloud-integration-openapi.yml
- filename: sap-integration-suite-api-management-openapi.yml
  format: yaml
  label: SAP API Management API
  slug: sap-api-management
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/sap-integration-suite/refs/heads/main/openapi/sap-integration-suite-api-management-openapi.yml
billing_model:
  billingCurrency: USD (varies by contract)
  billingFrequency: Per-Contract
  chargeCategories:
  - Purchase
  - Usage
  - Adjustment
  pricingCategory: Contract / Negotiated
description: 'FOCUS-aligned FinOps shape for SAP Integration Suite: BTP-hosted iPaaS billed under the customer''s SAP BTP commercial agreement (CPEA / Pay-As-You-Go-for-SAP-BTP). No public unit pricing.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: SAP SE
  ProviderName: SAP Integration Suite
  PublisherName: SAP SE
  ServiceCategory: Integration Platform
  ServiceName: SAP Integration Suite
layout: finops
meters:
- aggregation: sum
  name: contracted_consumption
  unit: varies
name: Sap Integration Suite Finops
provider_name: SAP Integration Suite
provider_slug: sap-integration-suite
publisher_name: SAP SE
service_category: Integration Platform
slug: sap-integration-suite-finops
source_filename: sap-integration-suite-finops.yml
source_heading: FinOps Profile
source_url: https://www.sap.com/products/technology-platform/integration-suite.html
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: SAP Integration Suite\nproviderId: sap-integration-suite\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n- FinOps\n- FOCUS\n- iPaaS\n- API Management\n- SAP\ndescription: 'FOCUS-aligned FinOps shape for SAP Integration Suite: BTP-hosted iPaaS billed under the\n  customer''s SAP BTP commercial agreement (CPEA / Pay-As-You-Go-for-SAP-BTP). No public unit pricing.'\nnotes: SAP Integration Suite is sold as part of SAP Business Technology Platform (BTP) and priced via\n  SAP commercial agreements. The public pricing page returns HTTP 403 to anonymous fetches; Discovery\n  Center requires authenticated SAP session. List pricing is not publicly disclosed.\nsources:\n- https://www.sap.com/products/technology-platform/integration-suite.html\n- https://discovery-center.cloud.sap/serviceCatalog/integration-suite\nalignedWith:\n  framework: FinOps\
  \ Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: SAP SE\nserviceCategory: Integration Platform\nbillingModel:\n  pricingCategory: Contract / Negotiated\n  billingFrequency: Per-Contract\n  billingCurrency: USD (varies by contract)\n  chargeCategories:\n  - Purchase\n  - Usage\n  - Adjustment\nfocusColumns:\n  ServiceName: SAP Integration Suite\n  ServiceCategory: Integration Platform\n  ProviderName: SAP Integration Suite\n  PublisherName: SAP SE\n  InvoiceIssuerName: SAP SE\n  BillingCurrency: USD\nmeters:\n- name: contracted_consumption\n  unit: varies\n  aggregation: sum\nprinciples:\n- name: Visibility\n  description: Consumption visibility comes from the SAP Integration Suite account / partner reporting\n    surface (invoices, account dashboards) rather than a public usage API.\n- name: Allocation\n  description: Allocate cost through\
  \ the SAP Integration Suite contract structure (entitlement, project,\n    business unit) and reconcile against internal cost centers.\n- name: Optimization\n  description: 'Optimization levers are commercial: renegotiation cadence, commitment sizing, and consolidation\n    of SAP Integration Suite entitlements.'\n- name: Accountability\n  description: Assign a contract owner who reconciles SAP Integration Suite invoices against contracted\n    entitlements each billing cycle.\nmaintainers:\n- FN: Kin Lane\n  email: kin@apievangelist.com\n  url: https://apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/sap-integration-suite/refs/heads/main/finops/sap-integration-suite-finops.yml
sources:
- https://www.sap.com/products/technology-platform/integration-suite.html
- https://discovery-center.cloud.sap/serviceCatalog/integration-suite
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- iPaaS
- API Management
- SAP
---
