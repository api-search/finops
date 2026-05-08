---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: workday-finance-financial-management-openapi.yml
  format: yaml
  label: Workday Financial Management API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/workday-finance/refs/heads/main/openapi/workday-finance-financial-management-openapi.yml
- filename: workday-finance-procurement-openapi.yml
  format: yaml
  label: Workday Resource Management API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/workday-finance/refs/heads/main/openapi/workday-finance-procurement-openapi.yml
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
description: FinOps framework definition for the Workday Finance API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Workday Finance
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Workday Finance
  PublisherName: Workday Finance
  ServiceCategory: Developer Tools / API
  ServiceName: Workday Finance
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
name: Workday Finance Finops
provider_name: Workday Finance
provider_slug: workday-finance
publisher_name: Workday Finance
service_category: API
slug: workday-finance-finops
source_filename: workday-finance-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Workday Finance\nproviderId: workday-finance\npublisherName: Workday Finance\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Accounting\n  - Cloud\n  - Enterprise\n  - ERP\n  - Finance\n  - Financial Management\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Workday Finance API surface. Provides a FOCUS-aligned\n  mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description:\
  \ Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n\
  \    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Workday Finance\n  ServiceCategory: Developer Tools / API\n  ProviderName: Workday Finance\n  PublisherName: Workday Finance\n  InvoiceIssuerName: Workday Finance\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the\
  \ network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Workday Financial Management API\n    baseURL: https://wd2-impl-services1.workday.com/ccx/service\n    tags:\n      - Accounting\n      - Banking\n      - Finance\n      - General Ledger\n    serviceName: Workday Financial Management API\n    serviceCategory: API\n  - name: Workday Revenue Management API\n    baseURL: https://wd2-impl-services1.workday.com/ccx/service\n    tags:\n      - Billing\n      - Contracts\n      - Revenue\n    serviceName: Workday Revenue Management API\n    serviceCategory: API\n  - name: Workday Expenses API\n    baseURL: https://wd2-impl-services1.workday.com/ccx/service\n    tags:\n      - Expenses\n      - Reimbursement\n\
  \      - Spend Management\n    serviceName: Workday Expenses API\n    serviceCategory: API\n  - name: Workday Cash Management API\n    baseURL: https://wd2-impl-services1.workday.com/ccx/service\n    tags:\n      - Banking\n      - Cash Management\n      - Treasury\n    serviceName: Workday Cash Management API\n    serviceCategory: API\n  - name: Workday Budgets API\n    baseURL: https://wd2-impl-services1.workday.com/ccx/service\n    tags:\n      - Budgets\n      - Financial Planning\n      - Planning\n    serviceName: Workday Budgets API\n    serviceCategory: API\n  - name: Workday Projects API\n    baseURL: https://wd2-impl-services1.workday.com/ccx/service\n    tags:\n      - Cost Tracking\n      - Project Management\n      - Projects\n    serviceName: Workday Projects API\n    serviceCategory: API\n  - name: Workday Resource Management API\n    baseURL: https://wd2-impl-services1.workday.com/ccx/service\n    tags:\n      - Business Assets\n      - Invoicing\n      - Procurement\n\
  \      - Resource Management\n      - Suppliers\n    serviceName: Workday Resource Management API\n    serviceCategory: API\n  - name: Workday Settlement Services API\n    baseURL: https://wd2-impl-services1.workday.com/ccx/service\n    tags:\n      - Banking\n      - Direct Debit\n      - Payments\n      - Settlements\n    serviceName: Workday Settlement Services API\n    serviceCategory: API\n  - name: Workday Inventory API\n    baseURL: https://wd2-impl-services1.workday.com/ccx/service\n    tags:\n      - Goods Delivery\n      - Inventory\n      - Stock Management\n      - Supply Chain\n    serviceName: Workday Inventory API\n    serviceCategory: API\n  - name: Workday Professional Services Automation API\n    baseURL: https://wd2-impl-services1.workday.com/ccx/service\n    tags:\n      - Professional Services\n      - PSA\n      - Resource Staffing\n      - Services Billing\n    serviceName: Workday Professional Services Automation API\n    serviceCategory: API\nunitEconomics:\n \
  \ - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/workday-finance/refs/heads/main/finops/workday-finance-finops.yml
sources: []
specification: FinOps Framework
tags:
- Accounting
- Cloud
- Enterprise
- ERP
- Finance
- Financial Management
- FinOps
- Cost Management
- FOCUS
---
