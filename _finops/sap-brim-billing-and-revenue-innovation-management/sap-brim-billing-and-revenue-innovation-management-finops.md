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
  label: SAP Convergent Charging API
  slug: ''
  spec_type: OpenAPI
  url: https://api.sap.com/api/convergent_charging/overview
- filename: overview
  format: yaml
  label: SAP Convergent Invoicing API
  slug: ''
  spec_type: OpenAPI
  url: https://api.sap.com/api/convergent_invoicing/overview
- filename: overview
  format: yaml
  label: SAP Subscription Billing API
  slug: ''
  spec_type: OpenAPI
  url: https://api.sap.com/api/subscription_billing/overview
- filename: overview
  format: yaml
  label: SAP Contract Accounts Receivable and Payable API
  slug: ''
  spec_type: OpenAPI
  url: https://api.sap.com/api/fica/overview
- filename: overview
  format: yaml
  label: SAP BRIM Usage Data Intake API
  slug: ''
  spec_type: OpenAPI
  url: https://api.sap.com/api/usage_data_intake/overview
- filename: overview
  format: yaml
  label: SAP Revenue Accounting and Reporting API
  slug: ''
  spec_type: OpenAPI
  url: https://api.sap.com/api/revenue_accounting/overview
billing_model:
  billingCurrency: USD/EUR/varies
  billingFrequency: Per-Invoice
  chargeCategories:
  - Purchase
  - Usage
  - Tax
  - Adjustment
  pricingCategory: Enterprise Contract
description: FOCUS-aligned FinOps placeholder for SAP BRIM. Module-based S/4HANA licensing.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: SAP SE
  ProviderName: SAP BRIM (Billing and Revenue Innovation Management)
  PublisherName: SAP SE
  ServiceCategory: Billing / Revenue Management
  ServiceName: SAP BRIM (Billing and Revenue Innovation Management)
layout: finops
meters:
- aggregation: sum
  description: Consumption against the customer's negotiated SAP / Concur contract; reconcile to actual provider-published meters once available.
  dimensions:
  - service
  - region
  name: contracted_consumption
  unit: varies
name: Sap Brim Billing And Revenue Innovation Management Finops
provider_name: SAP BRIM (Billing and Revenue Innovation Management)
provider_slug: sap-brim-billing-and-revenue-innovation-management
publisher_name: SAP SE
service_category: Billing / Revenue Management
slug: sap-brim-billing-and-revenue-innovation-management-finops
source_filename: sap-brim-billing-and-revenue-innovation-management-finops.yml
source_heading: FinOps Profile
source_url: https://www.sap.com/products/financial-management/billing-revenue-innovation-mgmt.html
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: SAP BRIM (Billing and Revenue Innovation Management)\nproviderId: sap-brim-billing-and-revenue-innovation-management\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Billing\n  - Enterprise\n  - Order to Cash\n  - Revenue Management\n  - SAP\n  - Subscription Management\n  - Usage-Based Pricing\ndescription: FOCUS-aligned FinOps placeholder for SAP BRIM. Module-based S/4HANA licensing.\nsources:\n  - https://www.sap.com/products/financial-management/billing-revenue-innovation-mgmt.html\n  - https://help.sap.com/docs/SAP_S4HANA_CLOUD/0fa84c9d9c634132b7c4abb9ffdd8f06\nnotes: Provider does not publish a public, machine-readable rate card; meters and FOCUS columns below are placeholders to be reconciled once contract or partner-portal terms are available.\nalignedWith:\n  framework: FinOps Foundation Framework\n \
  \ frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: SAP SE\nserviceCategory: Billing / Revenue Management\nbillingModel:\n  pricingCategory: Enterprise Contract\n  billingFrequency: Per-Invoice\n  billingCurrency: USD/EUR/varies\n  chargeCategories:\n    - Purchase\n    - Usage\n    - Tax\n    - Adjustment\nfocusColumns:\n  ServiceName: SAP BRIM (Billing and Revenue Innovation Management)\n  ServiceCategory: Billing / Revenue Management\n  ProviderName: SAP BRIM (Billing and Revenue Innovation Management)\n  PublisherName: SAP SE\n  InvoiceIssuerName: SAP SE\n  BillingCurrency: USD\nmeters:\n  - name: contracted_consumption\n    description: Consumption against the customer's negotiated SAP / Concur contract; reconcile to actual\n      provider-published meters once available.\n    unit: varies\n    aggregation: sum\n    dimensions:\n      - service\n      - region\n\
  principles:\n  - name: Visibility\n    description: Use SAP for Me, the BTP Cockpit, or the SAP Concur admin console (as applicable) to\n      view consumption against entitlements; line items appear on the SAP / Concur invoice.\n  - name: Allocation\n    description: Allocate by SAP global account / subaccount or by Concur entity; map to internal cost\n      centers via the relevant cockpit before chargeback.\n  - name: Optimization\n    description: Track CPEA/BTPEA balance burn or per-employee subscription utilization; right-size service\n      plans and prune unused entitlements at renewal.\n  - name: Accountability\n    description: Designate a single billing owner and reconcile invoices monthly with usage reports from\n      the relevant SAP / Concur cockpit.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/sap-brim-billing-and-revenue-innovation-management/refs/heads/main/finops/sap-brim-billing-and-revenue-innovation-management-finops.yml
sources:
- https://www.sap.com/products/financial-management/billing-revenue-innovation-mgmt.html
- https://help.sap.com/docs/SAP_S4HANA_CLOUD/0fa84c9d9c634132b7c4abb9ffdd8f06
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Billing
- Enterprise
- Order to Cash
- Revenue Management
- SAP
- Subscription Management
- Usage-Based Pricing
---
