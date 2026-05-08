---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: synchrony-financial-credit-authorization-openapi.yml
  format: yaml
  label: Synchrony Credit Authorization API
  slug: credit-authorization
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/synchrony-financial/refs/heads/main/openapi/synchrony-financial-credit-authorization-openapi.yml
- filename: synchrony-financial-quickscreen-apply-openapi.yml
  format: yaml
  label: Synchrony Quickscreen Apply API
  slug: quickscreen-apply
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/synchrony-financial/refs/heads/main/openapi/synchrony-financial-quickscreen-apply-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Per-Program Settlement
  chargeCategories:
  - Purchase
  - Adjustment
  - Refund
  pricingCategory: Program-Attached (Retail Credit)
description: Synchrony's APIs are program-attached (retail credit, Quickscreen, account management); revenue moves through retail-credit program economics rather than a per-call API invoice, so FinOps mapping aligns to program-level merchant settlement rather than usage telemetry.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Synchrony Bank
  ProviderName: Synchrony Financial
  PublisherName: Synchrony Bank
  ServiceCategory: Consumer Credit / Retail Finance
  ServiceName: Synchrony APIs
layout: finops
meters:
- aggregation: sum
  description: Credit authorization transactions submitted through the Authorization API.
  dimensions:
  - merchant
  - channel
  name: credit_authorizations
  unit: transaction
- aggregation: sum
  description: Quickscreen preapproval decisions returned (soft credit pulls).
  dimensions:
  - merchant
  name: quickscreen_decisions
  unit: decision
- aggregation: sum
  description: Account-management API calls supporting cardholder servicing.
  dimensions:
  - merchant
  name: account_servicing_calls
  unit: request
name: Synchrony Financial Finops
provider_name: Synchrony Financial
provider_slug: synchrony-financial
publisher_name: Synchrony Bank
service_category: Consumer Credit / Retail Finance
slug: synchrony-financial-finops
source_filename: synchrony-financial-finops.yml
source_heading: FinOps Profile
source_url: https://developer.syf.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Synchrony Financial\nproviderId: synchrony-financial\npublisherName: Synchrony Bank\nserviceCategory: Consumer Credit / Retail Finance\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Financial Services\n  - Credit\n  - Payments\n  - FinOps\n  - FOCUS\ndescription: Synchrony's APIs are program-attached (retail credit, Quickscreen, account management); revenue moves through retail-credit program economics rather than a per-call API invoice, so FinOps mapping aligns to program-level merchant settlement rather than usage telemetry.\nsources:\n  - https://developer.syf.com/\n  - https://www.synchrony.com\nnotes: No FOCUS-aligned\
  \ per-call billing surface. Cost/revenue is reconciled at the retail-credit program level (interchange, merchant servicing, promotional financing terms) by the merchant's finance team.\nbillingModel:\n  pricingCategory: Program-Attached (Retail Credit)\n  billingFrequency: Per-Program Settlement\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Adjustment\n    - Refund\nfocusColumns:\n  ServiceName: Synchrony APIs\n  ServiceCategory: Consumer Credit / Retail Finance\n  ProviderName: Synchrony Financial\n  PublisherName: Synchrony Bank\n  InvoiceIssuerName: Synchrony Bank\n  BillingCurrency: USD\nmeters:\n  - name: credit_authorizations\n    description: Credit authorization transactions submitted through the Authorization API.\n    unit: transaction\n    aggregation: sum\n    dimensions:\n      - merchant\n      - channel\n  - name: quickscreen_decisions\n    description: Quickscreen preapproval decisions returned (soft credit pulls).\n    unit: decision\n    aggregation:\
  \ sum\n    dimensions:\n      - merchant\n  - name: account_servicing_calls\n    description: Account-management API calls supporting cardholder servicing.\n    unit: request\n    aggregation: sum\n    dimensions:\n      - merchant\nprinciples:\n  - name: Visibility\n    description: Merchants reconcile API-driven activity against Synchrony program reporting; there is no FOCUS export, but transaction- and decision-level reports are available through partner reporting.\n  - name: Allocation\n    description: Allocate by merchant, channel (e-commerce / POS / mobile), and program; the natural unit is the credit program rather than a per-call line.\n  - name: Optimization\n    description: Optimize by routing eligible customers through Quickscreen first to reduce hard-pull costs, batching servicing calls, and tuning checkout flow to maximize approved authorization rates.\n  - name: Accountability\n    description: Merchant program owner and Synchrony partner-management team jointly own commercial\
  \ reviews and program performance.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/synchrony-financial/refs/heads/main/finops/synchrony-financial-finops.yml
sources:
- https://developer.syf.com/
- https://www.synchrony.com
specification: FinOps Framework
tags:
- Financial Services
- Credit
- Payments
- FinOps
- FOCUS
---
