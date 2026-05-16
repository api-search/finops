---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: openapi-general-ledger.yaml
  format: yaml
  label: Oracle Financials General Ledger API
  slug: oracle-financials-general-ledger-api
  spec_type: OpenAPI
  url: https://docs.oracle.com/en/cloud/saas/financials/23r3/farfa/openapi-general-ledger.yaml
- filename: openapi-payables.yaml
  format: yaml
  label: Oracle Financials Accounts Payable API
  slug: oracle-financials-accounts-payable-api
  spec_type: OpenAPI
  url: https://docs.oracle.com/en/cloud/saas/financials/23r3/farfa/openapi-payables.yaml
- filename: openapi-receivables.yaml
  format: yaml
  label: Oracle Financials Accounts Receivable API
  slug: oracle-financials-accounts-receivable-api
  spec_type: OpenAPI
  url: https://docs.oracle.com/en/cloud/saas/financials/23r3/farfa/openapi-receivables.yaml
- filename: openapi-cash-management.yaml
  format: yaml
  label: Oracle Financials Cash Management API
  slug: oracle-financials-cash-management-api
  spec_type: OpenAPI
  url: https://docs.oracle.com/en/cloud/saas/financials/23r3/farfa/openapi-cash-management.yaml
- filename: openapi-expenses.yaml
  format: yaml
  label: Oracle Financials Expense Management API
  slug: oracle-financials-expense-management-api
  spec_type: OpenAPI
  url: https://docs.oracle.com/en/cloud/saas/financials/23r3/farfa/openapi-expenses.yaml
- filename: openapi-fixed-assets.yaml
  format: yaml
  label: Oracle Financials Fixed Assets API
  slug: oracle-financials-fixed-assets-api
  spec_type: OpenAPI
  url: https://docs.oracle.com/en/cloud/saas/financials/23r3/farfa/openapi-fixed-assets.yaml
- filename: openapi-reporting.yaml
  format: yaml
  label: Oracle Financial Reporting API
  slug: oracle-financial-reporting-api
  spec_type: OpenAPI
  url: https://docs.oracle.com/en/cloud/saas/financials/23r3/farfa/openapi-reporting.yaml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Purchase
  - Tax
  - Adjustment
  - Credit
  pricingCategory: Tiered Subscription
description: 'FOCUS-aligned FinOps view for Oracle Financials Cloud: a SaaS subscription billed monthly per Hosted Named User / Hosted Employee. REST API access is bundled with the subscription and does not generate a separate metered charge. FinOps observation focuses on user-license utilization rather than per-call consumption.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Oracle America, Inc.
  PricingCategory: Subscription
  ProviderName: Oracle
  PublisherName: Oracle America, Inc.
  ServiceCategory: ERP / Financials
  ServiceName: Oracle Financials Cloud
layout: finops
meters:
- aggregation: max
  description: Active Hosted Named User seats per month
  dimensions:
  - module
  - business_unit
  name: hosted_named_user_subscription
  unit: seat-month
- aggregation: max
  description: Hosted Employee seats per month for employee-priced modules
  dimensions:
  - module
  - business_unit
  name: hosted_employee_subscription
  unit: employee-month
- aggregation: sum
  description: REST API calls (informational; bundled in the subscription)
  dimensions:
  - api
  - endpoint
  - consumer
  name: rest_api_calls
  unit: request
- aggregation: count
  description: FBDI / BI Publisher bulk extracts (informational)
  dimensions:
  - module
  name: file_based_data_imports
  unit: job
name: Oracle Financials Finops
provider_name: Oracle Financials
provider_slug: oracle-financials
publisher_name: Oracle America, Inc.
service_category: ERP / Financials
slug: oracle-financials-finops
source_filename: oracle-financials-finops.yml
source_heading: FinOps Profile
source_url: https://www.oracle.com/erp/financials/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Oracle Financials\nproviderId: oracle-financials\npublisherName: Oracle America, Inc.\nserviceCategory: ERP / Financials\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - ERP\n  - Financial Management\n  - Oracle Cloud\n  - FinOps\n  - FOCUS\ndescription: >-\n  FOCUS-aligned FinOps view for Oracle Financials Cloud: a SaaS subscription\n  billed monthly per Hosted Named User / Hosted Employee. REST API access is\n  bundled with the subscription and does not generate a separate metered\n  charge. FinOps observation focuses on user-license utilization rather than\n  per-call consumption.\nsources:\n  - https://www.oracle.com/erp/financials/\n\
  \  - https://docs.oracle.com/en/cloud/saas/financials/\nnotes: >-\n  No per-API meter exists. Track license seat utilization through the Fusion\n  Applications usage reports and reconcile against the contractual seat count\n  on the order document.\nbillingModel:\n  pricingCategory: Tiered Subscription\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Tax\n    - Adjustment\n    - Credit\nfocusColumns:\n  ServiceName: Oracle Financials Cloud\n  ServiceCategory: ERP / Financials\n  ProviderName: Oracle\n  PublisherName: Oracle America, Inc.\n  InvoiceIssuerName: Oracle America, Inc.\n  BillingCurrency: USD\n  PricingCategory: Subscription\n  ChargeCategory: Purchase\nmeters:\n  - name: hosted_named_user_subscription\n    description: Active Hosted Named User seats per month\n    unit: seat-month\n    aggregation: max\n    dimensions:\n      - module\n      - business_unit\n  - name: hosted_employee_subscription\n    description: Hosted Employee\
  \ seats per month for employee-priced modules\n    unit: employee-month\n    aggregation: max\n    dimensions:\n      - module\n      - business_unit\n  - name: rest_api_calls\n    description: REST API calls (informational; bundled in the subscription)\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - consumer\n  - name: file_based_data_imports\n    description: FBDI / BI Publisher bulk extracts (informational)\n    unit: job\n    aggregation: count\n    dimensions:\n      - module\nprinciples:\n  - name: Visibility\n    description: >-\n      Review Hosted Named User / Hosted Employee utilization through the\n      Fusion Applications Security Console and Manage Users area; reconcile\n      monthly against the contractual seat count.\n  - name: Allocation\n    description: >-\n      Tag user records with the consuming business unit and cost center so\n      seat cost can be allocated back to finance teams.\n  - name: Optimization\n    description:\
  \ >-\n      Reclaim inactive seats, consolidate duplicate user records, and use the\n      lower-priced Hosted Employee or Hosted Single-Sign-On metrics for\n      light-touch users where the module supports them.\n  - name: Accountability\n    description: >-\n      Assign the Financials applications administrator and the FP&A finance\n      partner joint accountability for seat growth and renewal scoping.\napis:\n  - name: Oracle Financials General Ledger API\n    serviceName: Oracle Financials General Ledger API\n    serviceCategory: ERP / Financials\n  - name: Oracle Financials Accounts Payable API\n    serviceName: Oracle Financials Accounts Payable API\n    serviceCategory: ERP / Financials\n  - name: Oracle Financials Accounts Receivable API\n    serviceName: Oracle Financials Accounts Receivable API\n    serviceCategory: ERP / Financials\n  - name: Oracle Financials Cash Management API\n    serviceName: Oracle Financials Cash Management API\n    serviceCategory: ERP / Financials\n\
  \  - name: Oracle Financials Expense Management API\n    serviceName: Oracle Financials Expense Management API\n    serviceCategory: ERP / Financials\n  - name: Oracle Financials Fixed Assets API\n    serviceName: Oracle Financials Fixed Assets API\n    serviceCategory: ERP / Financials\n  - name: Oracle Financial Reporting API\n    serviceName: Oracle Financial Reporting API\n    serviceCategory: ERP / Financials\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/oracle-financials/refs/heads/main/finops/oracle-financials-finops.yml
sources:
- https://www.oracle.com/erp/financials/
- https://docs.oracle.com/en/cloud/saas/financials/
specification: FinOps Framework
tags:
- ERP
- Financial Management
- Oracle Cloud
- FinOps
- FOCUS
---
