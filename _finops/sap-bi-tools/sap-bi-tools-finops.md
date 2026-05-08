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
  label: SAP Analytics Cloud API
  slug: ''
  spec_type: OpenAPI
  url: https://api.sap.com/api/SACOpenAPI/overview
- filename: overview
  format: yaml
  label: SAP HANA Cloud Data Lake Files REST API
  slug: ''
  spec_type: OpenAPI
  url: https://api.sap.com/api/HanaCloudDataLake/overview
- filename: overview
  format: yaml
  label: SAP Datasphere API
  slug: ''
  spec_type: OpenAPI
  url: https://api.sap.com/api/Datasphere/overview
billing_model:
  billingCurrency: USD/EUR/varies
  billingFrequency: Per-Invoice
  chargeCategories:
  - Purchase
  - Usage
  - Tax
  - Adjustment
  pricingCategory: Enterprise Contract
description: FOCUS-aligned FinOps placeholder for SAP BI Tools. Per-user / per-session licensing under the BusinessObjects BI Suite.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: SAP SE
  ProviderName: SAP BI Tools
  PublisherName: SAP SE
  ServiceCategory: Business Intelligence / Reporting
  ServiceName: SAP BI Tools
layout: finops
meters:
- aggregation: sum
  description: Consumption against the customer's negotiated SAP / Concur contract; reconcile to actual provider-published meters once available.
  dimensions:
  - service
  - region
  name: contracted_consumption
  unit: varies
name: Sap Bi Tools Finops
provider_name: SAP BI Tools
provider_slug: sap-bi-tools
publisher_name: SAP SE
service_category: Business Intelligence / Reporting
slug: sap-bi-tools-finops
source_filename: sap-bi-tools-finops.yml
source_heading: FinOps Profile
source_url: https://api.sap.com/bi-tools
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: SAP BI Tools\nproviderId: sap-bi-tools\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Analytics\n  - Business Intelligence\n  - Data Visualization\n  - Reporting\n  - SAP\ndescription: FOCUS-aligned FinOps placeholder for SAP BI Tools. Per-user / per-session licensing under the BusinessObjects BI Suite.\nsources:\n  - https://api.sap.com/bi-tools\n  - https://help.sap.com/docs/SAP_BUSINESSOBJECTS_BUSINESS_INTELLIGENCE_PLATFORM\nnotes: Provider does not publish a public, machine-readable rate card; meters and FOCUS columns below are placeholders to be reconciled once contract or partner-portal terms are available.\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\n\
  publisherName: SAP SE\nserviceCategory: Business Intelligence / Reporting\nbillingModel:\n  pricingCategory: Enterprise Contract\n  billingFrequency: Per-Invoice\n  billingCurrency: USD/EUR/varies\n  chargeCategories:\n    - Purchase\n    - Usage\n    - Tax\n    - Adjustment\nfocusColumns:\n  ServiceName: SAP BI Tools\n  ServiceCategory: Business Intelligence / Reporting\n  ProviderName: SAP BI Tools\n  PublisherName: SAP SE\n  InvoiceIssuerName: SAP SE\n  BillingCurrency: USD\nmeters:\n  - name: contracted_consumption\n    description: Consumption against the customer's negotiated SAP / Concur contract; reconcile to actual\n      provider-published meters once available.\n    unit: varies\n    aggregation: sum\n    dimensions:\n      - service\n      - region\nprinciples:\n  - name: Visibility\n    description: Use SAP for Me, the BTP Cockpit, or the SAP Concur admin console (as applicable) to\n      view consumption against entitlements; line items appear on the SAP / Concur invoice.\n\
  \  - name: Allocation\n    description: Allocate by SAP global account / subaccount or by Concur entity; map to internal cost\n      centers via the relevant cockpit before chargeback.\n  - name: Optimization\n    description: Track CPEA/BTPEA balance burn or per-employee subscription utilization; right-size service\n      plans and prune unused entitlements at renewal.\n  - name: Accountability\n    description: Designate a single billing owner and reconcile invoices monthly with usage reports from\n      the relevant SAP / Concur cockpit.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/sap-bi-tools/refs/heads/main/finops/sap-bi-tools-finops.yml
sources:
- https://api.sap.com/bi-tools
- https://help.sap.com/docs/SAP_BUSINESSOBJECTS_BUSINESS_INTELLIGENCE_PLATFORM
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Analytics
- Business Intelligence
- Data Visualization
- Reporting
- SAP
---
