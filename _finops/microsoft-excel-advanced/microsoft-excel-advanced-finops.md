---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: openapi.yaml
  format: yaml
  label: Microsoft Graph Excel API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/microsoftgraph/msgraph-metadata/master/openapi/v1.0/openapi.yaml
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
description: FinOps framework definition for the Microsoft Excel (Advanced) API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Microsoft Excel (Advanced)
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Microsoft Excel (Advanced)
  PublisherName: Microsoft Excel (Advanced)
  ServiceCategory: Developer Tools / API
  ServiceName: Microsoft Excel (Advanced)
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
name: Microsoft Excel Advanced Finops
provider_name: Microsoft Excel (Advanced)
provider_slug: microsoft-excel-advanced
publisher_name: Microsoft Excel (Advanced)
service_category: API
slug: microsoft-excel-advanced-finops
source_filename: microsoft-excel-advanced-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Microsoft Excel (Advanced)\nproviderId: microsoft-excel-advanced\npublisherName: Microsoft Excel (Advanced)\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Automation\n  - Business Intelligence\n  - Data Analysis\n  - Office\n  - Spreadsheets\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Microsoft Excel (Advanced) API surface. Provides a FOCUS-aligned\n  mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n\
  \  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and\
  \ SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Microsoft Excel (Advanced)\n  ServiceCategory: Developer Tools / API\n  ProviderName: Microsoft Excel (Advanced)\n  PublisherName: Microsoft Excel (Advanced)\n  InvoiceIssuerName: Microsoft Excel (Advanced)\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n\
  \      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Microsoft Graph Excel API\n    baseURL: https://graph.microsoft.com/v1.0\n    tags:\n      - Cloud\n      - REST\n      - Workbooks\n      - Worksheets\n    serviceName: Microsoft Graph Excel API\n    serviceCategory: API\n  - name: Office Scripts API\n    baseURL: https://script.office.com\n    tags:\n      - Automation\n      - Power-Automate\n      - Scripting\n      - Typescript\n    serviceName: Office Scripts API\n    serviceCategory: API\n  - name: Excel JavaScript API\n    baseURL: https://appsforoffice.microsoft.com\n    tags:\n      - Add-Ins\n    \
  \  - Extensions\n      - Javascript\n      - Office-Js\n    serviceName: Excel JavaScript API\n    serviceCategory: API\n  - name: Excel Custom Functions API\n    baseURL: ''\n    tags:\n      - Calculations\n      - Custom-Functions\n      - Formulas\n      - Udf\n    serviceName: Excel Custom Functions API\n    serviceCategory: API\n  - name: Excel REST API (OneDrive)\n    baseURL: https://graph.microsoft.com/v1.0/me/drive\n    tags:\n      - Cloud-Storage\n      - Onedrive\n      - REST\n      - Sharepoint\n    serviceName: Excel REST API (OneDrive)\n    serviceCategory: API\n  - name: Power Automate Excel Connector\n    baseURL: ''\n    tags:\n      - Connector\n      - Low-Code\n      - Power-Automate\n      - Workflow\n    serviceName: Power Automate Excel Connector\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n\
  \    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/microsoft-excel-advanced/refs/heads/main/finops/microsoft-excel-advanced-finops.yml
sources: []
specification: FinOps Framework
tags:
- Automation
- Business Intelligence
- Data Analysis
- Office
- Spreadsheets
- FinOps
- Cost Management
- FOCUS
---
