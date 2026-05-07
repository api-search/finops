---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: sap-ariba-procurement-api.yml
  format: yaml
  label: SAP Ariba Procurement API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/sap-ariba/refs/heads/main/openapi/sap-ariba-procurement-api.yml
- filename: openapi.json
  format: json
  label: SAP Ariba Sourcing API
  slug: ''
  spec_type: OpenAPI
  url: https://developer.ariba.com/api/sourcing/openapi.json
- filename: openapi.json
  format: json
  label: SAP Ariba Supplier Management API
  slug: ''
  spec_type: OpenAPI
  url: https://developer.ariba.com/api/supplier/openapi.json
- filename: openapi.json
  format: json
  label: SAP Ariba Contract Management API
  slug: ''
  spec_type: OpenAPI
  url: https://developer.ariba.com/api/contracts/openapi.json
- filename: openapi.json
  format: json
  label: SAP Ariba Analytical Reporting API
  slug: ''
  spec_type: OpenAPI
  url: https://developer.ariba.com/api/analytics/openapi.json
- filename: openapi.json
  format: json
  label: SAP Ariba Invoice Management API
  slug: ''
  spec_type: OpenAPI
  url: https://developer.ariba.com/api/invoices/openapi.json
billing_model:
  billingCurrency: USD/EUR/varies
  billingFrequency: Per-Invoice
  chargeCategories:
  - Purchase
  - Usage
  - Tax
  - Adjustment
  pricingCategory: Enterprise Contract
description: FOCUS-aligned FinOps placeholder for SAP Ariba. Module-based subscription plus supplier network transaction fees; specific rates are contract-only.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: SAP SE
  ProviderName: SAP Ariba
  PublisherName: SAP SE
  ServiceCategory: Procurement / B2B Network
  ServiceName: SAP Ariba
layout: finops
meters:
- aggregation: sum
  description: Consumption against the customer's negotiated SAP / Concur contract; reconcile to actual provider-published meters once available.
  dimensions:
  - service
  - region
  name: contracted_consumption
  unit: varies
name: Sap Ariba Finops
provider_name: SAP Ariba
provider_slug: sap-ariba
publisher_name: SAP SE
service_category: Procurement / B2B Network
slug: sap-ariba-finops
source_filename: sap-ariba-finops.yml
source_heading: FinOps Profile
source_url: https://www.ariba.com
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: SAP Ariba\nproviderId: sap-ariba\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - B2B\n  - Contract Management\n  - Procurement\n  - Sourcing\n  - Spend Analysis\n  - Supplier Management\n  - Supply Chain\ndescription: FOCUS-aligned FinOps placeholder for SAP Ariba. Module-based subscription plus supplier network transaction fees; specific rates are contract-only.\nsources:\n  - https://www.ariba.com\n  - https://www.sap.com/products/spend-management/ariba.html\nnotes: Provider does not publish a public, machine-readable rate card; meters and FOCUS columns below are placeholders to be reconciled once contract or partner-portal terms are available.\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl:\
  \ https://focus.finops.org/focus-specification/v1-3/\npublisherName: SAP SE\nserviceCategory: Procurement / B2B Network\nbillingModel:\n  pricingCategory: Enterprise Contract\n  billingFrequency: Per-Invoice\n  billingCurrency: USD/EUR/varies\n  chargeCategories:\n    - Purchase\n    - Usage\n    - Tax\n    - Adjustment\nfocusColumns:\n  ServiceName: SAP Ariba\n  ServiceCategory: Procurement / B2B Network\n  ProviderName: SAP Ariba\n  PublisherName: SAP SE\n  InvoiceIssuerName: SAP SE\n  BillingCurrency: USD\nmeters:\n  - name: contracted_consumption\n    description: Consumption against the customer's negotiated SAP / Concur contract; reconcile to actual\n      provider-published meters once available.\n    unit: varies\n    aggregation: sum\n    dimensions:\n      - service\n      - region\nprinciples:\n  - name: Visibility\n    description: Use SAP for Me, the BTP Cockpit, or the SAP Concur admin console (as applicable) to\n      view consumption against entitlements; line items appear\
  \ on the SAP / Concur invoice.\n  - name: Allocation\n    description: Allocate by SAP global account / subaccount or by Concur entity; map to internal cost\n      centers via the relevant cockpit before chargeback.\n  - name: Optimization\n    description: Track CPEA/BTPEA balance burn or per-employee subscription utilization; right-size service\n      plans and prune unused entitlements at renewal.\n  - name: Accountability\n    description: Designate a single billing owner and reconcile invoices monthly with usage reports from\n      the relevant SAP / Concur cockpit.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/sap-ariba/refs/heads/main/finops/sap-ariba-finops.yml
sources:
- https://www.ariba.com
- https://www.sap.com/products/spend-management/ariba.html
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- B2B
- Contract Management
- Procurement
- Sourcing
- Spend Analysis
- Supplier Management
- Supply Chain
---
