---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
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
description: FinOps framework definition for the Oracle General Ledger API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Oracle General Ledger
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Oracle General Ledger
  PublisherName: Oracle General Ledger
  ServiceCategory: Developer Tools / API
  ServiceName: Oracle General Ledger
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
name: Oracle General Ledger Finops
provider_name: Oracle General Ledger
provider_slug: oracle-general-ledger
publisher_name: Oracle General Ledger
service_category: API
slug: oracle-general-ledger-finops
source_filename: oracle-general-ledger-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Oracle General Ledger\nproviderId: oracle-general-ledger\npublisherName: Oracle General Ledger\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Accounting\n  - Balances\n  - Cloud\n  - ERP\n  - Finance\n  - General Ledger\n  - Journals\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Oracle General Ledger API surface. Provides a FOCUS-aligned\n  mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name:\
  \ Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  -\
  \ name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Oracle General Ledger\n  ServiceCategory: Developer Tools / API\n  ProviderName: Oracle General Ledger\n  PublisherName: Oracle General Ledger\n  InvoiceIssuerName: Oracle General Ledger\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name:\
  \ data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Oracle General Ledger Journal Batches REST API\n    baseURL: https://{instance}.oraclecloud.com/fscmRestApi/resources/11.13.18.05\n    tags:\n      - Accounting\n      - General Ledger\n      - Journal Batches\n      - Journals\n    serviceName: Oracle General Ledger Journal Batches REST API\n    serviceCategory: API\n  - name: Oracle General Ledger Ledger Balances REST API\n    baseURL: https://{instance}.oraclecloud.com/fscmRestApi/resources/11.13.18.05\n    tags:\n      - Account Balances\n      - Balances\n      - Financial Reporting\n      - General Ledger\n    serviceName: Oracle\
  \ General Ledger Ledger Balances REST API\n    serviceCategory: API\n  - name: Oracle General Ledger Accounting Period Status REST API\n    baseURL: https://{instance}.oraclecloud.com/fscmRestApi/resources/11.13.18.05\n    tags:\n      - Accounting Periods\n      - Financial Close\n      - General Ledger\n      - Period Close\n    serviceName: Oracle General Ledger Accounting Period Status REST API\n    serviceCategory: API\n  - name: Oracle General Ledger Currency Rates REST API\n    baseURL: https://{instance}.oraclecloud.com/fscmRestApi/resources/11.13.18.05\n    tags:\n      - Currency Rates\n      - Exchange Rates\n      - Foreign Currency\n      - General Ledger\n    serviceName: Oracle General Ledger Currency Rates REST API\n    serviceCategory: API\n  - name: Oracle General Ledger Ledger Options REST API\n    baseURL: https://{instance}.oraclecloud.com/fscmRestApi/resources/11.13.18.05\n    tags:\n      - Chart of Accounts\n      - General Ledger\n      - Ledger Options\n     \
  \ - Ledger Setup\n    serviceName: Oracle General Ledger Ledger Options REST API\n    serviceCategory: API\n  - name: Oracle General Ledger Budgetary Control REST API\n    baseURL: https://{instance}.oraclecloud.com/fscmRestApi/resources/11.13.18.05\n    tags:\n      - Appropriations\n      - Budgetary Control\n      - Budgets\n      - General Ledger\n    serviceName: Oracle General Ledger Budgetary Control REST API\n    serviceCategory: API\n  - name: Oracle General Ledger Chart of Accounts Filters REST API\n    baseURL: https://{instance}.oraclecloud.com/fscmRestApi/resources/11.13.18.05\n    tags:\n      - Account Combinations\n      - Account Filters\n      - Chart of Accounts\n      - General Ledger\n    serviceName: Oracle General Ledger Chart of Accounts Filters REST API\n    serviceCategory: API\n  - name: Oracle Intercompany Transactions REST API\n    baseURL: https://{instance}.oraclecloud.com/fscmRestApi/resources/11.13.18.05\n    tags:\n      - Cross-Charge\n      - General\
  \ Ledger\n      - Intercompany\n      - Transfer Pricing\n    serviceName: Oracle Intercompany Transactions REST API\n    serviceCategory: API\n  - name: Oracle Joint Venture General Ledger Transactions REST API\n    baseURL: https://{instance}.oraclecloud.com/fscmRestApi/resources/11.13.18.05\n    tags:\n      - General Ledger\n      - Joint Venture\n      - Partnership Accounting\n      - Subledger Accounting\n    serviceName: Oracle Joint Venture General Ledger Transactions REST API\n    serviceCategory: API\n  - name: Oracle General Ledger ERP Integrations REST API\n    baseURL: https://{instance}.oraclecloud.com/fscmRestApi/resources/11.13.18.05\n    tags:\n      - Data Import\n      - ERP Integration\n      - General Ledger\n      - Journal Import\n    serviceName: Oracle General Ledger ERP Integrations REST API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n\
  \    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/oracle-general-ledger/refs/heads/main/finops/oracle-general-ledger-finops.yml
sources: []
specification: FinOps Framework
tags:
- Accounting
- Balances
- Cloud
- ERP
- Finance
- General Ledger
- Journals
- FinOps
- Cost Management
- FOCUS
---
