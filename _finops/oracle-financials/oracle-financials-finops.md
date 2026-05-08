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
  slug: ''
  spec_type: OpenAPI
  url: https://docs.oracle.com/en/cloud/saas/financials/23r3/farfa/openapi-general-ledger.yaml
- filename: openapi-payables.yaml
  format: yaml
  label: Oracle Financials Accounts Payable API
  slug: ''
  spec_type: OpenAPI
  url: https://docs.oracle.com/en/cloud/saas/financials/23r3/farfa/openapi-payables.yaml
- filename: openapi-receivables.yaml
  format: yaml
  label: Oracle Financials Accounts Receivable API
  slug: ''
  spec_type: OpenAPI
  url: https://docs.oracle.com/en/cloud/saas/financials/23r3/farfa/openapi-receivables.yaml
- filename: openapi-cash-management.yaml
  format: yaml
  label: Oracle Financials Cash Management API
  slug: ''
  spec_type: OpenAPI
  url: https://docs.oracle.com/en/cloud/saas/financials/23r3/farfa/openapi-cash-management.yaml
- filename: openapi-expenses.yaml
  format: yaml
  label: Oracle Financials Expense Management API
  slug: ''
  spec_type: OpenAPI
  url: https://docs.oracle.com/en/cloud/saas/financials/23r3/farfa/openapi-expenses.yaml
- filename: openapi-fixed-assets.yaml
  format: yaml
  label: Oracle Financials Fixed Assets API
  slug: ''
  spec_type: OpenAPI
  url: https://docs.oracle.com/en/cloud/saas/financials/23r3/farfa/openapi-fixed-assets.yaml
- filename: openapi-reporting.yaml
  format: yaml
  label: Oracle Financial Reporting API
  slug: ''
  spec_type: OpenAPI
  url: https://docs.oracle.com/en/cloud/saas/financials/23r3/farfa/openapi-reporting.yaml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  - Tax
  - Credit
  - Adjustment
  chargeFrequency: Recurring
  pricingCategory: Usage-Based
description: FinOps framework definition for the Oracle Financials API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Oracle Financials
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Oracle Financials
  PublisherName: Oracle Financials
  ServiceCategory: Developer Tools / API
  ServiceName: Oracle Financials
layout: finops
meters:
- aggregation: sum
  description: Count of billable API requests
  dimensions:
  - api
  - endpoint
  - tier
  - region
  - consumer
  name: api_requests
  unit: request
- aggregation: sum
  description: Bytes returned over the network in API responses
  dimensions:
  - api
  - region
  - consumer
  name: data_egress
  unit: GB
- aggregation: sum
  description: Server-side compute consumed by the request, where applicable
  dimensions:
  - api
  - endpoint
  - tier
  name: compute_seconds
  unit: second
name: Oracle Financials Finops
provider_name: Oracle Financials
provider_slug: oracle-financials
publisher_name: Oracle Financials
service_category: API
slug: oracle-financials-finops
source_filename: oracle-financials-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Oracle Financials\nproviderId: oracle-financials\npublisherName: Oracle Financials\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Accounting\n  - Accounts Payable\n  - Accounts Receivable\n  - Cash Management\n  - ERP\n  - Expense Management\n  - Financial Management\n  - General Ledger\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Oracle Financials API surface. Provides a FOCUS-aligned\n  mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and\
  \ finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud\
  \ Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Oracle Financials\n  ServiceCategory: Developer Tools / API\n  ProviderName: Oracle Financials\n  PublisherName: Oracle Financials\n  InvoiceIssuerName: Oracle Financials\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      -\
  \ region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Oracle Financials General Ledger API\n    baseURL: https://your-instance.fa.us2.oraclecloud.com/fscmRestApi/resources/11.13.18.05\n    tags:\n      - Account Balances\n      - Chart of Accounts\n      - General Ledger\n      - Journals\n    serviceName: Oracle Financials General Ledger API\n    serviceCategory: API\n  - name: Oracle Financials Accounts Payable API\n    baseURL: https://your-instance.fa.us2.oraclecloud.com/fscmRestApi/resources/11.13.18.05\n    tags:\n      - Accounts Payable\n      - Invoices\n      - Payments\n      - Suppliers\n  \
  \  serviceName: Oracle Financials Accounts Payable API\n    serviceCategory: API\n  - name: Oracle Financials Accounts Receivable API\n    baseURL: https://your-instance.fa.us2.oraclecloud.com/fscmRestApi/resources/11.13.18.05\n    tags:\n      - Accounts Receivable\n      - Credit Management\n      - Customer Invoices\n      - Receipts\n    serviceName: Oracle Financials Accounts Receivable API\n    serviceCategory: API\n  - name: Oracle Financials Cash Management API\n    baseURL: https://your-instance.fa.us2.oraclecloud.com/fscmRestApi/resources/11.13.18.05\n    tags:\n      - Bank Accounts\n      - Cash Forecasting\n      - Cash Management\n      - Reconciliation\n    serviceName: Oracle Financials Cash Management API\n    serviceCategory: API\n  - name: Oracle Financials Expense Management API\n    baseURL: https://your-instance.fa.us2.oraclecloud.com/fscmRestApi/resources/11.13.18.05\n    tags:\n      - Corporate Cards\n      - Expense Management\n      - Expense Reports\n      -\
  \ Reimbursements\n    serviceName: Oracle Financials Expense Management API\n    serviceCategory: API\n  - name: Oracle Financials Fixed Assets API\n    baseURL: https://your-instance.fa.us2.oraclecloud.com/fscmRestApi/resources/11.13.18.05\n    tags:\n      - Asset Management\n      - Asset Tracking\n      - Depreciation\n      - Fixed Assets\n    serviceName: Oracle Financials Fixed Assets API\n    serviceCategory: API\n  - name: Oracle Financial Reporting API\n    baseURL: https://your-instance.fa.us2.oraclecloud.com/fscmRestApi/resources/11.13.18.05\n    tags:\n      - Analytics\n      - Business Intelligence\n      - Financial Reports\n      - Reporting\n    serviceName: Oracle Financial Reporting API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/oracle-financials/refs/heads/main/finops/oracle-financials-finops.yml
sources: []
specification: FinOps Framework
tags:
- Accounting
- Accounts Payable
- Accounts Receivable
- Cash Management
- ERP
- Expense Management
- Financial Management
- General Ledger
- FinOps
- Cost Management
- FOCUS
---
