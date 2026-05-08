---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: sap-concur-expense-report-openapi.yml
  format: yaml
  label: Expense Report v3 API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/sap-concur-expense/refs/heads/main/openapi/sap-concur-expense-report-openapi.yml
- filename: sap-concur-expense-report-openapi.yml
  format: yaml
  label: Expense Entry v3 API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/sap-concur-expense/refs/heads/main/openapi/sap-concur-expense-report-openapi.yml
- filename: sap-concur-expense-report-openapi.yml
  format: yaml
  label: Quick Expense v3 API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/sap-concur-expense/refs/heads/main/openapi/sap-concur-expense-report-openapi.yml
- filename: sap-concur-expense-report-openapi.yml
  format: yaml
  label: Receipt Image v3 API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/sap-concur-expense/refs/heads/main/openapi/sap-concur-expense-report-openapi.yml
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
description: FinOps framework definition for the SAP Concur Expense API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: SAP Concur Expense
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: SAP Concur Expense
  PublisherName: SAP Concur Expense
  ServiceCategory: Developer Tools / API
  ServiceName: SAP Concur Expense
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
name: Sap Concur Expense Finops
provider_name: SAP Concur Expense
provider_slug: sap-concur-expense
publisher_name: SAP Concur Expense
service_category: API
slug: sap-concur-expense-finops
source_filename: sap-concur-expense-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: SAP Concur Expense\nproviderId: sap-concur-expense\npublisherName: SAP Concur Expense\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Expense Management\n  - Financial Management\n  - Receipts\n  - Reimbursement\n  - Reporting\n  - SAP\n  - Travel\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the SAP Concur Expense API surface. Provides a FOCUS-aligned\n  mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n\
  \  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and\
  \ SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: SAP Concur Expense\n  ServiceCategory: Developer Tools / API\n  ProviderName: SAP Concur Expense\n  PublisherName: SAP Concur Expense\n  InvoiceIssuerName: SAP Concur Expense\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name:\
  \ data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Expense Report v3 API\n    baseURL: https://us.api.concursolutions.com/api/v3.0\n    tags:\n      - Approval\n      - Expenses\n      - Financial\n      - Reports\n      - Workflow\n    serviceName: Expense Report v3 API\n    serviceCategory: API\n  - name: Expense Entry v3 API\n    baseURL: https://us.api.concursolutions.com/api/v3.0\n    tags:\n      - Expense Entries\n      - Itemization\n      - Line Items\n    serviceName: Expense Entry v3 API\n    serviceCategory: API\n  - name: Quick Expense v3 API\n    baseURL: https://us.api.concursolutions.com/api/v3.0\n    tags:\n      - Expenses\n\
  \      - Mobile\n      - Quick Expense\n    serviceName: Quick Expense v3 API\n    serviceCategory: API\n  - name: Receipt Image v3 API\n    baseURL: https://us.api.concursolutions.com/api/v3.0\n    tags:\n      - Documents\n      - Images\n      - Receipts\n    serviceName: Receipt Image v3 API\n    serviceCategory: API\n  - name: Digital Tax Invoice API\n    baseURL: https://us.api.concursolutions.com/api/v3.0\n    tags:\n      - Compliance\n      - Invoice\n      - Tax\n    serviceName: Digital Tax Invoice API\n    serviceCategory: API\n  - name: Expense Group Configuration API\n    baseURL: https://us.api.concursolutions.com/api/v3.0\n    tags:\n      - Configuration\n      - Policies\n      - Settings\n    serviceName: Expense Group Configuration API\n    serviceCategory: API\n  - name: Expense Allocations API\n    baseURL: https://us.api.concursolutions.com/api/v3.0\n    tags:\n      - Accounting\n      - Allocations\n      - Cost Centers\n    serviceName: Expense Allocations API\n\
  \    serviceCategory: API\n  - name: Payment Batch v1 API\n    baseURL: https://us.api.concursolutions.com/api/v1.1\n    tags:\n      - Batch Processing\n      - Payments\n      - Reimbursement\n    serviceName: Payment Batch v1 API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - name: Kin Lane\n    email: kin@apievangelist.com\n    url: https://apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/sap-concur-expense/refs/heads/main/finops/sap-concur-expense-finops.yml
sources: []
specification: FinOps Framework
tags:
- Expense Management
- Financial Management
- Receipts
- Reimbursement
- Reporting
- SAP
- Travel
- FinOps
- Cost Management
- FOCUS
---
