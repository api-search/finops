---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  - Tax
  - Adjustment
  - Credit
  pricingCategory: Enterprise Subscription
description: 'FOCUS-aligned FinOps for SAP Concur: enterprise SaaS subscription where API consumption is bundled with the customer''s SAP Concur (Expense / Travel / Invoice / Request) contract; spend allocation follows the SAP enterprise invoice rather than per-API-call billing.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: SAP America, Inc.
  ProviderName: SAP Concur
  PublisherName: SAP Concur Technologies, Inc.
  ServiceCategory: Travel & Expense Management
  ServiceName: SAP Concur
layout: finops
meters:
- aggregation: max
  description: Annual SAP Concur subscription fee (Expense / Travel / Invoice / Request modules)
  dimensions:
  - module
  - tenant
  name: concur_subscription
  unit: month
- aggregation: sum
  description: Internal-only meter — count of API calls per consuming application for chargeback within the customer organization. Not billed externally by SAP.
  dimensions:
  - api
  - consumer_app
  - environment
  name: api_calls_internal
  unit: request
- aggregation: avg
  description: Per-user (employee) component of the SAP Concur subscription
  dimensions:
  - module
  - tenant
  name: active_users
  unit: seat
name: Concur Finops
provider_name: SAP Concur
provider_slug: concur
publisher_name: SAP Concur Technologies, Inc.
service_category: Travel & Expense Management
slug: concur-finops
source_filename: concur-finops.yml
source_heading: FinOps Profile
source_url: https://developer.concur.com/api-reference/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: SAP Concur\nproviderId: concur\npublisherName: SAP Concur Technologies, Inc.\nserviceCategory: Travel & Expense Management\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Expense Management\n  - Finance\n  - Invoice\n  - SAP\n  - Travel\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps for SAP Concur: enterprise SaaS subscription where API consumption\n  is bundled with the customer''s SAP Concur (Expense / Travel / Invoice / Request) contract; spend allocation\n  follows the SAP enterprise invoice rather than per-API-call billing.'\nnotes: SAP Concur does not publish per-call API pricing; spend rolls up under\
  \ the customer's enterprise\n  Concur subscription. Meters here describe what consumers should track internally for chargeback even\n  though SAP does not bill per-call externally.\nsources:\n  - https://developer.concur.com/api-reference/\n  - https://www.concur.com/\nbillingModel:\n  pricingCategory: Enterprise Subscription\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Tax\n    - Adjustment\n    - Credit\nfocusColumns:\n  ServiceName: SAP Concur\n  ServiceCategory: Travel & Expense Management\n  ProviderName: SAP Concur\n  PublisherName: SAP Concur Technologies, Inc.\n  InvoiceIssuerName: SAP America, Inc.\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: concur_subscription\n    description: Annual SAP Concur subscription fee (Expense / Travel / Invoice / Request modules)\n    unit: month\n    aggregation: max\n    dimensions:\n      - module\n      - tenant\n  - name: api_calls_internal\n    description: Internal-only\
  \ meter — count of API calls per consuming application for chargeback within\n      the customer organization. Not billed externally by SAP.\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - consumer_app\n      - environment\n  - name: active_users\n    description: Per-user (employee) component of the SAP Concur subscription\n    unit: seat\n    aggregation: avg\n    dimensions:\n      - module\n      - tenant\nprinciples:\n  - name: Visibility\n    description: SAP does not bill API calls separately; for internal cost allocation use the Concur Audit\n      / Reporting APIs and the partner application credential identifiers to attribute consumption to\n      consuming apps and teams.\n  - name: Allocation\n    description: Tag SAP Concur OAuth2 application credentials and entity IDs (companyId) per consuming\n      product; allocate the overall Concur subscription across business units using employee headcount\n      and module activation.\n  - name: Optimization\n\
  \    description: Optimize the SAP contract by reviewing module activation (Expense vs Travel vs Invoice\n      vs Request) annually and pruning unused integration apps; reduce API churn via batch endpoints\n      and webhook-driven sync rather than polling.\n  - name: Accountability\n    description: Travel & expense ops typically owns the Concur subscription line; integration owners\n      (HR / IT / partner integrations) are accountable for API usage patterns within the bundled allowance.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/concur/refs/heads/main/finops/concur-finops.yml
sources:
- https://developer.concur.com/api-reference/
- https://www.concur.com/
specification: FinOps Framework
tags:
- Expense Management
- Finance
- Invoice
- SAP
- Travel
- FinOps
- FOCUS
---
