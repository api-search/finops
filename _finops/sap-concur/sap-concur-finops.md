---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: expense-report.json
  format: json
  label: Concur Expense API
  slug: concur-expense-api
  spec_type: OpenAPI
  url: https://developer.concur.com/api-reference/expense/expense-report/expense-report.json
- filename: itinerary.json
  format: json
  label: Concur Travel API
  slug: concur-travel-api
  spec_type: OpenAPI
  url: https://developer.concur.com/api-reference/travel/itinerary/itinerary.json
- filename: v3.invoice.json
  format: json
  label: Concur Invoice API
  slug: concur-invoice-api
  spec_type: OpenAPI
  url: https://developer.concur.com/api-reference/invoice/v3.invoice.json
- filename: v4.request.json
  format: json
  label: Concur Request API
  slug: concur-request-api
  spec_type: OpenAPI
  url: https://developer.concur.com/api-reference/request/v4.request.json
billing_model:
  billingCurrency: USD/EUR/varies
  billingFrequency: Per-Invoice
  chargeCategories:
  - Purchase
  - Usage
  - Tax
  - Adjustment
  pricingCategory: Enterprise Contract
description: FOCUS-aligned FinOps placeholder for SAP Concur. Per-employee subscription with transaction-based usage fees.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: SAP Concur (Concur Technologies, Inc.)
  ProviderName: SAP Concur
  PublisherName: SAP Concur (Concur Technologies, Inc.)
  ServiceCategory: Travel & Expense Management
  ServiceName: SAP Concur
layout: finops
meters:
- aggregation: sum
  description: Consumption against the customer's negotiated SAP / Concur contract; reconcile to actual provider-published meters once available.
  dimensions:
  - service
  - region
  name: contracted_consumption
  unit: varies
name: Sap Concur Finops
provider_name: SAP Concur
provider_slug: sap-concur
publisher_name: SAP Concur (Concur Technologies, Inc.)
service_category: Travel & Expense Management
slug: sap-concur-finops
source_filename: sap-concur-finops.yml
source_heading: FinOps Profile
source_url: https://www.concur.com
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: SAP Concur\nproviderId: sap-concur\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Business Travel\n  - Expense Management\n  - Financial Services\n  - Invoice Management\n  - Travel Management\ndescription: FOCUS-aligned FinOps placeholder for SAP Concur. Per-employee subscription with transaction-based usage fees.\nsources:\n  - https://www.concur.com\n  - https://developer.concur.com/api-reference/\nnotes: Provider does not publish a public, machine-readable rate card; meters and FOCUS columns below are placeholders to be reconciled once contract or partner-portal terms are available.\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName:\
  \ SAP Concur (Concur Technologies, Inc.)\nserviceCategory: Travel & Expense Management\nbillingModel:\n  pricingCategory: Enterprise Contract\n  billingFrequency: Per-Invoice\n  billingCurrency: USD/EUR/varies\n  chargeCategories:\n    - Purchase\n    - Usage\n    - Tax\n    - Adjustment\nfocusColumns:\n  ServiceName: SAP Concur\n  ServiceCategory: Travel & Expense Management\n  ProviderName: SAP Concur\n  PublisherName: SAP Concur (Concur Technologies, Inc.)\n  InvoiceIssuerName: SAP Concur (Concur Technologies, Inc.)\n  BillingCurrency: USD\nmeters:\n  - name: contracted_consumption\n    description: Consumption against the customer's negotiated SAP / Concur contract; reconcile to actual\n      provider-published meters once available.\n    unit: varies\n    aggregation: sum\n    dimensions:\n      - service\n      - region\nprinciples:\n  - name: Visibility\n    description: Use SAP for Me, the BTP Cockpit, or the SAP Concur admin console (as applicable) to\n      view consumption against\
  \ entitlements; line items appear on the SAP / Concur invoice.\n  - name: Allocation\n    description: Allocate by SAP global account / subaccount or by Concur entity; map to internal cost\n      centers via the relevant cockpit before chargeback.\n  - name: Optimization\n    description: Track CPEA/BTPEA balance burn or per-employee subscription utilization; right-size service\n      plans and prune unused entitlements at renewal.\n  - name: Accountability\n    description: Designate a single billing owner and reconcile invoices monthly with usage reports from\n      the relevant SAP / Concur cockpit.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/sap-concur/refs/heads/main/finops/sap-concur-finops.yml
sources:
- https://www.concur.com
- https://developer.concur.com/api-reference/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Business Travel
- Expense Management
- Financial Services
- Invoice Management
- Travel Management
---
