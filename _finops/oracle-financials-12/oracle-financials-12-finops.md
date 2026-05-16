---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: gl-api.json
  format: json
  label: Oracle General Ledger API
  slug: oracle-general-ledger-api
  spec_type: OpenAPI
  url: https://docs.oracle.com/en/cloud/saas/financials/openapi/gl-api.json
- filename: ap-api.json
  format: json
  label: Oracle Accounts Payable API
  slug: oracle-accounts-payable-api
  spec_type: OpenAPI
  url: https://docs.oracle.com/en/cloud/saas/financials/openapi/ap-api.json
- filename: ar-api.json
  format: json
  label: Oracle Accounts Receivable API
  slug: oracle-accounts-receivable-api
  spec_type: OpenAPI
  url: https://docs.oracle.com/en/cloud/saas/financials/openapi/ar-api.json
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
description: FinOps framework definition for the Oracle Financials 12 API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Oracle Financials 12
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Oracle Financials 12
  PublisherName: Oracle Financials 12
  ServiceCategory: Developer Tools / API
  ServiceName: Oracle Financials 12
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
name: Oracle Financials 12 Finops
provider_name: Oracle Financials 12
provider_slug: oracle-financials-12
publisher_name: Oracle Financials 12
service_category: API
slug: oracle-financials-12-finops
source_filename: oracle-financials-12-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Oracle Financials 12\nproviderId: oracle-financials-12\npublisherName: Oracle Financials 12\nserviceCategory: API\ncreated: '2026-05-04'\nmodified: '2026-05-04'\ntags:\n  - Accounting\n  - E-Business Suite\n  - Enterprise\n  - ERP\n  - Financial Management\n  - Oracle\n  - Release 12\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Oracle Financials 12 API surface. Provides a FOCUS-aligned\n  mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n\
  \  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and\
  \ SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Oracle Financials 12\n  ServiceCategory: Developer Tools / API\n  ProviderName: Oracle Financials 12\n  PublisherName: Oracle Financials 12\n  InvoiceIssuerName: Oracle Financials 12\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n\
  \  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Oracle General Ledger API\n    baseURL: ''\n    tags:\n      - Accounting\n      - Financial Reporting\n      - General Ledger\n      - Journals\n    serviceName: Oracle General Ledger API\n    serviceCategory: API\n  - name: Oracle Accounts Payable API\n    baseURL: ''\n    tags:\n      - Accounts Payable\n      - Invoices\n      - Payments\n      - Suppliers\n    serviceName: Oracle Accounts Payable API\n    serviceCategory: API\n  - name: Oracle Accounts Receivable API\n    baseURL: ''\n    tags:\n      - Accounts Receivable\n      - Collections\n      - Customer Invoices\n\
  \      - Receipts\n    serviceName: Oracle Accounts Receivable API\n    serviceCategory: API\n  - name: Oracle Cash Management API\n    baseURL: ''\n    tags:\n      - Bank Accounts\n      - Cash Management\n      - Reconciliation\n      - Treasury\n    serviceName: Oracle Cash Management API\n    serviceCategory: API\n  - name: Oracle Fixed Assets API\n    baseURL: ''\n    tags:\n      - Asset Management\n      - Capital Assets\n      - Depreciation\n      - Fixed Assets\n    serviceName: Oracle Fixed Assets API\n    serviceCategory: API\n  - name: Oracle Purchasing API\n    baseURL: ''\n    tags:\n      - Procurement\n      - Purchase Orders\n      - Purchasing\n      - Requisitions\n    serviceName: Oracle Purchasing API\n    serviceCategory: API\n  - name: Oracle Expenses API\n    baseURL: ''\n    tags:\n      - Expense Reports\n      - Expenses\n      - Reimbursements\n      - Travel\n    serviceName: Oracle Expenses API\n    serviceCategory: API\n  - name: Oracle Projects API\n \
  \   baseURL: ''\n    tags:\n      - Contracts\n      - Project Billing\n      - Project Costing\n      - Projects\n    serviceName: Oracle Projects API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/oracle-financials-12/refs/heads/main/finops/oracle-financials-12-finops.yml
sources: []
specification: FinOps Framework
tags:
- Accounting
- E-Business Suite
- Enterprise
- ERP
- Financial Management
- Oracle
- Release 12
- FinOps
- Cost Management
- FOCUS
---
