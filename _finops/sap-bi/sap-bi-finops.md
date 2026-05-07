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
  url: https://api.sap.com/api/API_ANALYTICS_CLOUD/overview
- filename: overview
  format: yaml
  label: SAP BusinessObjects BI Platform REST API
  slug: ''
  spec_type: OpenAPI
  url: https://api.sap.com/api/BOBJ_BIPLATFORM/overview
- filename: sap-bi-bw4hana-odata-openapi.yml
  format: yaml
  label: SAP BW/4HANA OData API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/sap-bi/refs/heads/main/openapi/sap-bi-bw4hana-odata-openapi.yml
- filename: overview
  format: yaml
  label: SAP Datasphere API
  slug: ''
  spec_type: OpenAPI
  url: https://api.sap.com/api/datasphere/overview
billing_model:
  billingCurrency: USD/EUR/varies
  billingFrequency: Per-Invoice
  chargeCategories:
  - Purchase
  - Usage
  - Tax
  - Adjustment
  pricingCategory: Enterprise Contract
description: FOCUS-aligned FinOps placeholder for SAP Business Intelligence. Per-user subscription and/or BTP capacity unit billing.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: SAP SE
  ProviderName: SAP Business Intelligence
  PublisherName: SAP SE
  ServiceCategory: Business Intelligence / Analytics
  ServiceName: SAP Business Intelligence
layout: finops
meters:
- aggregation: sum
  description: Consumption against the customer's negotiated SAP / Concur contract; reconcile to actual provider-published meters once available.
  dimensions:
  - service
  - region
  name: contracted_consumption
  unit: varies
name: Sap Bi Finops
provider_name: SAP Business Intelligence
provider_slug: sap-bi
publisher_name: SAP SE
service_category: Business Intelligence / Analytics
slug: sap-bi-finops
source_filename: sap-bi-finops.yml
source_heading: FinOps Profile
source_url: https://api.sap.com/business-intelligence
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: SAP Business Intelligence\nproviderId: sap-bi\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Analytics\n  - Business Intelligence\n  - Data Visualization\n  - Reporting\n  - SAP\n  - BTP\ndescription: FOCUS-aligned FinOps placeholder for SAP Business Intelligence. Per-user subscription and/or BTP capacity unit billing.\nsources:\n  - https://api.sap.com/business-intelligence\n  - https://help.sap.com/docs/SAP_ANALYTICS_CLOUD\nnotes: Provider does not publish a public, machine-readable rate card; meters and FOCUS columns below are placeholders to be reconciled once contract or partner-portal terms are available.\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\n\
  publisherName: SAP SE\nserviceCategory: Business Intelligence / Analytics\nbillingModel:\n  pricingCategory: Enterprise Contract\n  billingFrequency: Per-Invoice\n  billingCurrency: USD/EUR/varies\n  chargeCategories:\n    - Purchase\n    - Usage\n    - Tax\n    - Adjustment\nfocusColumns:\n  ServiceName: SAP Business Intelligence\n  ServiceCategory: Business Intelligence / Analytics\n  ProviderName: SAP Business Intelligence\n  PublisherName: SAP SE\n  InvoiceIssuerName: SAP SE\n  BillingCurrency: USD\nmeters:\n  - name: contracted_consumption\n    description: Consumption against the customer's negotiated SAP / Concur contract; reconcile to actual\n      provider-published meters once available.\n    unit: varies\n    aggregation: sum\n    dimensions:\n      - service\n      - region\nprinciples:\n  - name: Visibility\n    description: Use SAP for Me, the BTP Cockpit, or the SAP Concur admin console (as applicable) to\n      view consumption against entitlements; line items appear on\
  \ the SAP / Concur invoice.\n  - name: Allocation\n    description: Allocate by SAP global account / subaccount or by Concur entity; map to internal cost\n      centers via the relevant cockpit before chargeback.\n  - name: Optimization\n    description: Track CPEA/BTPEA balance burn or per-employee subscription utilization; right-size service\n      plans and prune unused entitlements at renewal.\n  - name: Accountability\n    description: Designate a single billing owner and reconcile invoices monthly with usage reports from\n      the relevant SAP / Concur cockpit.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/sap-bi/refs/heads/main/finops/sap-bi-finops.yml
sources:
- https://api.sap.com/business-intelligence
- https://help.sap.com/docs/SAP_ANALYTICS_CLOUD
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Analytics
- Business Intelligence
- Data Visualization
- Reporting
- SAP
- BTP
---
