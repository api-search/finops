---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: scotiabank-tranxact-openapi.yml
  format: yaml
  label: Scotia TranXact APIs
  slug: scotia-tranxact
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/scotiabank/refs/heads/main/openapi/scotiabank-tranxact-openapi.yml
billing_model:
  billingCurrency: USD (varies by contract)
  billingFrequency: Per-Contract
  chargeCategories:
  - Purchase
  - Usage
  - Adjustment
  pricingCategory: Contract / Negotiated
description: 'FOCUS-aligned FinOps shape for Scotiabank: corporate-banking APIs (Scotia TranXact: wire, EFT, INTERAC e-Transfer, account info) priced under the customer''s corporate-banking relationship; transaction-level fees apply per the Treasury Services agreement.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: The Bank of Nova Scotia
  ProviderName: Scotiabank
  PublisherName: The Bank of Nova Scotia
  ServiceCategory: Banking
  ServiceName: Scotiabank
layout: finops
meters:
- aggregation: sum
  name: contracted_consumption
  unit: varies
name: Scotiabank Finops
provider_name: Scotiabank
provider_slug: scotiabank
publisher_name: The Bank of Nova Scotia
service_category: Banking
slug: scotiabank-finops
source_filename: scotiabank-finops.yml
source_heading: FinOps Profile
source_url: https://developer.scotiabank.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Scotiabank\nproviderId: scotiabank\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n- FinOps\n- FOCUS\n- Banking\n- Payments\ndescription: 'FOCUS-aligned FinOps shape for Scotiabank: corporate-banking APIs (Scotia TranXact: wire,\n  EFT, INTERAC e-Transfer, account info) priced under the customer''s corporate-banking relationship;\n  transaction-level fees apply per the Treasury Services agreement.'\nnotes: Scotiabank's Scotia TranXact developer portal is a B2B partner-only API marketplace for corporate\n  / commercial customers. There is no public pricing page; access and pricing are negotiated as part of\n  the broader corporate-banking relationship through Scotiabank Treasury and Cash Management.\nsources:\n- https://developer.scotiabank.com/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n\
  \  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: The Bank of Nova Scotia\nserviceCategory: Banking\nbillingModel:\n  pricingCategory: Contract / Negotiated\n  billingFrequency: Per-Contract\n  billingCurrency: USD (varies by contract)\n  chargeCategories:\n  - Purchase\n  - Usage\n  - Adjustment\nfocusColumns:\n  ServiceName: Scotiabank\n  ServiceCategory: Banking\n  ProviderName: Scotiabank\n  PublisherName: The Bank of Nova Scotia\n  InvoiceIssuerName: The Bank of Nova Scotia\n  BillingCurrency: USD\nmeters:\n- name: contracted_consumption\n  unit: varies\n  aggregation: sum\nprinciples:\n- name: Visibility\n  description: Consumption visibility comes from the Scotiabank account / partner reporting surface (invoices,\n    account dashboards) rather than a public usage API.\n- name: Allocation\n  description: Allocate cost through the Scotiabank contract structure (entitlement, project, business\n    unit)\
  \ and reconcile against internal cost centers.\n- name: Optimization\n  description: 'Optimization levers are commercial: renegotiation cadence, commitment sizing, and consolidation\n    of Scotiabank entitlements.'\n- name: Accountability\n  description: Assign a contract owner who reconciles Scotiabank invoices against contracted entitlements\n    each billing cycle.\nmaintainers:\n- FN: Kin Lane\n  email: kin@apievangelist.com\n  url: https://apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/scotiabank/refs/heads/main/finops/scotiabank-finops.yml
sources:
- https://developer.scotiabank.com/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Banking
- Payments
---
