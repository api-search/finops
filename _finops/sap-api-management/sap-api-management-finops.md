---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: sap-api-management-portal-openapi.yml
  format: yaml
  label: SAP API Management API Portal API
  slug: sap-api-management-api-portal
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/sap-api-management/refs/heads/main/openapi/sap-api-management-portal-openapi.yml
billing_model:
  billingCurrency: USD/EUR/varies
  billingFrequency: Per-Invoice
  chargeCategories:
  - Purchase
  - Usage
  - Tax
  - Adjustment
  pricingCategory: Enterprise Contract
description: FOCUS-aligned FinOps placeholder for SAP API Management. The service is consumed via BTP entitlements and SAP does not publish a public rate card.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: SAP SE
  ProviderName: SAP API Management
  PublisherName: SAP SE
  ServiceCategory: API Management
  ServiceName: SAP API Management
layout: finops
meters:
- aggregation: sum
  description: Consumption against the customer's negotiated SAP / Concur contract; reconcile to actual provider-published meters once available.
  dimensions:
  - service
  - region
  name: contracted_consumption
  unit: varies
name: Sap Api Management Finops
provider_name: SAP API Management
provider_slug: sap-api-management
publisher_name: SAP SE
service_category: API Management
slug: sap-api-management-finops
source_filename: sap-api-management-finops.yml
source_heading: FinOps Profile
source_url: https://help.sap.com/docs/integration-suite
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: SAP API Management\nproviderId: sap-api-management\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - API Management\n  - Developer Portal\n  - Enterprise\n  - SAP\n  - BTP\ndescription: FOCUS-aligned FinOps placeholder for SAP API Management. The service is consumed via BTP entitlements and SAP does not publish a public rate card.\nsources:\n  - https://help.sap.com/docs/integration-suite\n  - https://www.sap.com/products/business-technology-platform/integration-suite/api-management.html\nnotes: Provider does not publish a public, machine-readable rate card; meters and FOCUS columns below are placeholders to be reconciled once contract or partner-portal terms are available.\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion:\
  \ '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: SAP SE\nserviceCategory: API Management\nbillingModel:\n  pricingCategory: Enterprise Contract\n  billingFrequency: Per-Invoice\n  billingCurrency: USD/EUR/varies\n  chargeCategories:\n    - Purchase\n    - Usage\n    - Tax\n    - Adjustment\nfocusColumns:\n  ServiceName: SAP API Management\n  ServiceCategory: API Management\n  ProviderName: SAP API Management\n  PublisherName: SAP SE\n  InvoiceIssuerName: SAP SE\n  BillingCurrency: USD\nmeters:\n  - name: contracted_consumption\n    description: Consumption against the customer's negotiated SAP / Concur contract; reconcile to actual\n      provider-published meters once available.\n    unit: varies\n    aggregation: sum\n    dimensions:\n      - service\n      - region\nprinciples:\n  - name: Visibility\n    description: Use SAP for Me, the BTP Cockpit, or the SAP Concur admin console (as applicable) to\n      view consumption against entitlements;\
  \ line items appear on the SAP / Concur invoice.\n  - name: Allocation\n    description: Allocate by SAP global account / subaccount or by Concur entity; map to internal cost\n      centers via the relevant cockpit before chargeback.\n  - name: Optimization\n    description: Track CPEA/BTPEA balance burn or per-employee subscription utilization; right-size service\n      plans and prune unused entitlements at renewal.\n  - name: Accountability\n    description: Designate a single billing owner and reconcile invoices monthly with usage reports from\n      the relevant SAP / Concur cockpit.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/sap-api-management/refs/heads/main/finops/sap-api-management-finops.yml
sources:
- https://help.sap.com/docs/integration-suite
- https://www.sap.com/products/business-technology-platform/integration-suite/api-management.html
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- API Management
- Developer Portal
- Enterprise
- SAP
- BTP
---
