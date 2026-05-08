---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: openapi.json
  format: json
  label: Microsoft Access Database Engine API
  slug: ''
  spec_type: OpenAPI
  url: https://example.com/openapi.json
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
description: FinOps framework definition for the Microsoft Access API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Microsoft Access
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Microsoft Access
  PublisherName: Microsoft Access
  ServiceCategory: Developer Tools / API
  ServiceName: Microsoft Access
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
name: Microsoft Access Finops
provider_name: Microsoft Access
provider_slug: microsoft-access
publisher_name: Microsoft Access
service_category: API
slug: microsoft-access-finops
source_filename: microsoft-access-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Microsoft Access\nproviderId: microsoft-access\npublisherName: Microsoft Access\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Access Database\n  - Database\n  - Desktop Database\n  - Microsoft\n  - Relational Database\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Microsoft Access API surface. Provides a FOCUS-aligned\n  mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description:\
  \ Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n\
  \    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Microsoft Access\n  ServiceCategory: Developer Tools / API\n  ProviderName: Microsoft Access\n  PublisherName: Microsoft Access\n  InvoiceIssuerName: Microsoft Access\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over\
  \ the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Microsoft Access Database Engine API\n    baseURL: ''\n    tags:\n      - DAO\n      - Database\n      - ODBC\n      - OLE DB\n    serviceName: Microsoft Access Database Engine API\n    serviceCategory: API\n  - name: Microsoft Graph API (for Access Online)\n    baseURL: ''\n    tags:\n      - Cloud Database\n      - Microsoft Graph\n      - SharePoint\n    serviceName: Microsoft Graph API (for Access Online)\n    serviceCategory: API\n  - name: Microsoft Access VBA API\n    baseURL: ''\n    tags:\n      - Automation\n      - Macros\n      - Object Model\n      - VBA\n    serviceName: Microsoft Access VBA API\n    serviceCategory: API\n\
  \  - name: Microsoft Data Access Objects (DAO) API\n    baseURL: ''\n    tags:\n      - DAO\n      - Data Access\n      - QueryDef\n      - Recordset\n      - TableDef\n    serviceName: Microsoft Data Access Objects (DAO) API\n    serviceCategory: API\n  - name: Microsoft ActiveX Data Objects (ADO) API\n    baseURL: ''\n    tags:\n      - ActiveX\n      - ADO\n      - Data Access\n      - OLE DB\n    serviceName: Microsoft ActiveX Data Objects (ADO) API\n    serviceCategory: API\n  - name: Microsoft Access SQL API\n    baseURL: ''\n    tags:\n      - DDL\n      - DML\n      - Query\n      - SQL\n    serviceName: Microsoft Access SQL API\n    serviceCategory: API\n  - name: Microsoft Access Macro Actions API\n    baseURL: ''\n    tags:\n      - Actions\n      - Automation\n      - Macros\n      - No-Code\n    serviceName: Microsoft Access Macro Actions API\n    serviceCategory: API\n  - name: Power Automate Access Actions API\n    baseURL: ''\n    tags:\n      - Automation\n      - Desktop\
  \ Flows\n      - Power Automate\n      - RPA\n    serviceName: Power Automate Access Actions API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n    url: https://apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/microsoft-access/refs/heads/main/finops/microsoft-access-finops.yml
sources: []
specification: FinOps Framework
tags:
- Access Database
- Database
- Desktop Database
- Microsoft
- Relational Database
- FinOps
- Cost Management
- FOCUS
---
