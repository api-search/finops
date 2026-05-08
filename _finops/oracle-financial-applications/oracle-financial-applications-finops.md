---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: op-version-latest-get.html
  format: yaml
  label: Oracle ERP Cloud REST API
  slug: ''
  spec_type: OpenAPI
  url: https://docs.oracle.com/en/cloud/saas/financials/24d/farfa/op-version-latest-get.html
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
description: FinOps framework definition for the Oracle Financial Applications API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Oracle Financial Applications
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Oracle Financial Applications
  PublisherName: Oracle Financial Applications
  ServiceCategory: Developer Tools / API
  ServiceName: Oracle Financial Applications
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
name: Oracle Financial Applications Finops
provider_name: Oracle Financial Applications
provider_slug: oracle-financial-applications
publisher_name: Oracle Financial Applications
service_category: API
slug: oracle-financial-applications-finops
source_filename: oracle-financial-applications-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Oracle Financial Applications\nproviderId: oracle-financial-applications\npublisherName: Oracle Financial Applications\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Accounting\n  - Cloud Applications\n  - Enterprise Performance Management\n  - Enterprise Resource Planning\n  - EPM\n  - ERP\n  - Financial Management\n  - Financial Reporting\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Oracle Financial Applications API surface. Provides a\n  FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the\n  provider's APIs.\nprinciples:\n  - name: Visibility\n    description:\
  \ Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n   \
  \   - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Oracle Financial Applications\n  ServiceCategory: Developer Tools / API\n  ProviderName: Oracle Financial Applications\n  PublisherName: Oracle Financial Applications\n  InvoiceIssuerName: Oracle Financial Applications\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n\
  \    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Oracle ERP Cloud REST API\n    baseURL: ''\n    tags:\n      - Accounts Payable\n      - Accounts Receivable\n      - ERP\n      - General Ledger\n      - REST\n    serviceName: Oracle ERP Cloud REST API\n    serviceCategory: API\n  - name: Oracle General Ledger REST API\n    baseURL: ''\n    tags:\n      - Budgets\n      - Chart of Accounts\n      - General Ledger\n      - Journals\n    serviceName: Oracle General Ledger REST API\n    serviceCategory:\
  \ API\n  - name: Oracle Accounts Payable REST API\n    baseURL: ''\n    tags:\n      - Accounts Payable\n      - Invoices\n      - Payments\n      - Suppliers\n    serviceName: Oracle Accounts Payable REST API\n    serviceCategory: API\n  - name: Oracle Accounts Receivable REST API\n    baseURL: ''\n    tags:\n      - Accounts Receivable\n      - Customers\n      - Invoices\n      - Receipts\n    serviceName: Oracle Accounts Receivable REST API\n    serviceCategory: API\n  - name: Oracle Cash Management REST API\n    baseURL: ''\n    tags:\n      - Bank Accounts\n      - Cash Management\n      - Reconciliation\n      - Treasury\n    serviceName: Oracle Cash Management REST API\n    serviceCategory: API\n  - name: Oracle Fixed Assets REST API\n    baseURL: ''\n    tags:\n      - Asset Management\n      - Depreciation\n      - Fixed Assets\n    serviceName: Oracle Fixed Assets REST API\n    serviceCategory: API\n  - name: Oracle EPM Cloud REST API\n    baseURL: ''\n    tags:\n      - Account\
  \ Reconciliation\n      - Budgeting\n      - EPM\n      - Financial Consolidation\n      - Planning\n    serviceName: Oracle EPM Cloud REST API\n    serviceCategory: API\n  - name: Oracle Financial Reporting REST API\n    baseURL: ''\n    tags:\n      - Analytics\n      - Financial Reporting\n      - Reports\n    serviceName: Oracle Financial Reporting REST API\n    serviceCategory: API\n  - name: Oracle FCCS REST API\n    baseURL: ''\n    tags:\n      - Close Management\n      - Consolidation\n      - Currency Translation\n      - Eliminations\n    serviceName: Oracle FCCS REST API\n    serviceCategory: API\n  - name: Oracle ARCS REST API\n    baseURL: ''\n    tags:\n      - Account Reconciliation\n      - Certifications\n      - Compliance\n    serviceName: Oracle ARCS REST API\n    serviceCategory: API\n  - name: Oracle Planning REST API\n    baseURL: ''\n    tags:\n      - Budgeting\n      - Forecasting\n      - Planning\n      - Workforce Planning\n    serviceName: Oracle Planning\
  \ REST API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/oracle-financial-applications/refs/heads/main/finops/oracle-financial-applications-finops.yml
sources: []
specification: FinOps Framework
tags:
- Accounting
- Cloud Applications
- Enterprise Performance Management
- Enterprise Resource Planning
- EPM
- ERP
- Financial Management
- Financial Reporting
- FinOps
- Cost Management
- FOCUS
---
