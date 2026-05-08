---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: sap-business-one-service-layer-openapi.yml
  format: yaml
  label: SAP Business One Service Layer API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/sap/refs/heads/main/openapi/sap-business-one-service-layer-openapi.yml
- filename: sap-s4hana-cloud-business-partner-openapi.yml
  format: yaml
  label: SAP S/4HANA Cloud API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/sap/refs/heads/main/openapi/sap-s4hana-cloud-business-partner-openapi.yml
- filename: sap-event-mesh-asyncapi.yml
  format: yaml
  label: SAP Event Mesh API
  slug: ''
  spec_type: AsyncAPI
  url: https://raw.githubusercontent.com/api-evangelist/sap/refs/heads/main/asyncapi/sap-event-mesh-asyncapi.yml
- filename: sap-ai-core-openapi.yml
  format: yaml
  label: SAP AI Core API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/sap/refs/heads/main/openapi/sap-ai-core-openapi.yml
billing_model:
  billingCurrency: USD/EUR/varies
  billingFrequency: Per-Invoice
  chargeCategories:
  - Purchase
  - Usage
  - Tax
  - Adjustment
  pricingCategory: Enterprise Contract (CPEA / BTPEA / PAYG)
description: FOCUS-aligned FinOps placeholder for SAP. SAP markets a contract- and partner-mediated portfolio (CPEA, BTPEA, pay-as-you-go consumption units) without a public, machine-readable rate card; meters and billing model below are intentionally generic until per-service billing terms can be sourced.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: SAP SE
  ProviderName: SAP
  PublisherName: SAP SE
  ServiceCategory: Enterprise Software
  ServiceName: SAP
layout: finops
meters:
- aggregation: sum
  description: Consumption against the customer's CPEA/BTPEA contract or pay-as-you-go entitlement; reconcile to actual SAP-published meters per service.
  dimensions:
  - service
  - region
  name: contracted_consumption
  unit: varies
name: Sap Finops
provider_name: SAP
provider_slug: sap
publisher_name: SAP SE
service_category: Enterprise Software / Cloud Platform
slug: sap-finops
source_filename: sap-finops.yml
source_heading: FinOps Profile
source_url: https://www.sap.com
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: SAP\nproviderId: sap\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - SAP\n  - Enterprise\n  - BTP\ndescription: FOCUS-aligned FinOps placeholder for SAP. SAP markets a contract- and partner-mediated portfolio\n  (CPEA, BTPEA, pay-as-you-go consumption units) without a public, machine-readable rate card; meters\n  and billing model below are intentionally generic until per-service billing terms can be sourced.\nsources:\n  - https://www.sap.com\n  - https://store.sap.com\nnotes: SAP corporate pricing and BTP Discovery Center pages are gated against automated fetches; meters\n  and FOCUS columns should be reconciled per product (S/4HANA Cloud, BTP, Ariba, SuccessFactors, Concur,\n  etc.) once published terms are available.\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n\
  \  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: SAP SE\nserviceCategory: Enterprise Software / Cloud Platform\nbillingModel:\n  pricingCategory: Enterprise Contract (CPEA / BTPEA / PAYG)\n  billingFrequency: Per-Invoice\n  billingCurrency: USD/EUR/varies\n  chargeCategories:\n    - Purchase\n    - Usage\n    - Tax\n    - Adjustment\nfocusColumns:\n  ServiceName: SAP\n  ServiceCategory: Enterprise Software\n  ProviderName: SAP\n  PublisherName: SAP SE\n  InvoiceIssuerName: SAP SE\n  BillingCurrency: USD\nmeters:\n  - name: contracted_consumption\n    description: Consumption against the customer's CPEA/BTPEA contract or pay-as-you-go entitlement;\n      reconcile to actual SAP-published meters per service.\n    unit: varies\n    aggregation: sum\n    dimensions:\n      - service\n      - region\nprinciples:\n  - name: Visibility\n    description: Use SAP for Me and the BTP Cockpit (where applicable) to view\
  \ consumption against entitlements;\n      detailed line items appear on the SAP invoice and CPEA balance reports.\n  - name: Allocation\n    description: Allocate by SAP global account, subaccount, and directory; map subaccounts to internal\n      cost centers in the BTP cockpit.\n  - name: Optimization\n    description: Track CPEA/BTPEA balance burn, right-size BTP service plans, and prefer reserved capacity\n      where SAP offers it; verify per-service through SAP sales since published rates are limited.\n  - name: Accountability\n    description: Designate a SAP global-account billing owner; reconcile invoices monthly with SAP for\n      Me reports and contract entitlements.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/sap/refs/heads/main/finops/sap-finops.yml
sources:
- https://www.sap.com
- https://store.sap.com
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- SAP
- Enterprise
- BTP
---
