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
  label: Oracle Planning REST API
  slug: ''
  spec_type: OpenAPI
  url: https://docs.oracle.com/en/cloud/saas/planning-budgeting-cloud/rest/openapi.json
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
description: FinOps framework definition for the Oracle Planning API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Oracle Planning
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Oracle Planning
  PublisherName: Oracle Planning
  ServiceCategory: Developer Tools / API
  ServiceName: Oracle Planning
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
name: Oracle Planning Finops
provider_name: Oracle Planning
provider_slug: oracle-planning
publisher_name: Oracle Planning
service_category: API
slug: oracle-planning-finops
source_filename: oracle-planning-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Oracle Planning\nproviderId: oracle-planning\npublisherName: Oracle Planning\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Budgeting\n  - Cloud\n  - Consolidation\n  - Enterprise\n  - EPM\n  - Financial Close\n  - Financial Planning\n  - Forecasting\n  - Oracle\n  - Planning\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Oracle Planning API surface. Provides a FOCUS-aligned\n  mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams\
  \ in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n\
  \      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Oracle Planning\n  ServiceCategory: Developer Tools / API\n  ProviderName: Oracle Planning\n  PublisherName: Oracle Planning\n  InvoiceIssuerName: Oracle Planning\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n\
  \  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Oracle Planning REST API\n    baseURL: https://{serviceHost}/HyperionPlanning/rest\n    tags:\n      - Budgeting\n      - Cloud\n      - EPM\n      - Forecasting\n      - Planning\n    serviceName: Oracle Planning REST API\n    serviceCategory: API\n  - name: Oracle EPM Automate\n    baseURL: https://{serviceHost}\n    tags:\n      - Administration\n      - Automation\n      - CLI\n      - EPM\n    serviceName: Oracle EPM Automate\n    serviceCategory: API\n  - name: Oracle Planning Smart View API\n    baseURL: https://{serviceHost}\n    tags:\n      - Excel\n      - Office Integration\n\
  \      - Reporting\n      - Smart View\n    serviceName: Oracle Planning Smart View API\n    serviceCategory: API\n  - name: Oracle Planning Data Management API\n    baseURL: https://{serviceHost}/aif/rest\n    tags:\n      - Data Load\n      - Data Management\n      - ETL\n      - Integration\n    serviceName: Oracle Planning Data Management API\n    serviceCategory: API\n  - name: Oracle EPM Migration REST API\n    baseURL: https://{serviceHost}/interop/rest\n    tags:\n      - Backup\n      - Lifecycle Management\n      - Migration\n      - Snapshots\n    serviceName: Oracle EPM Migration REST API\n    serviceCategory: API\n  - name: Oracle EPM Security REST API\n    baseURL: https://{serviceHost}/interop/rest/security\n    tags:\n      - Groups\n      - Roles\n      - Security\n      - Users\n    serviceName: Oracle EPM Security REST API\n    serviceCategory: API\n  - name: Oracle Financial Consolidation and Close REST API\n    baseURL: https://{serviceHost}/HyperionPlanning/rest\n\
  \    tags:\n      - Close Management\n      - Eliminations\n      - Financial Consolidation\n      - Journals\n    serviceName: Oracle Financial Consolidation and Close REST API\n    serviceCategory: API\n  - name: Oracle Account Reconciliation REST API\n    baseURL: https://{serviceHost}/armARCS/rest\n    tags:\n      - Account Reconciliation\n      - Compliance\n      - Financial Close\n      - Transaction Matching\n    serviceName: Oracle Account Reconciliation REST API\n    serviceCategory: API\n  - name: Oracle Tax Reporting REST API\n    baseURL: https://{serviceHost}/HyperionPlanning/rest\n    tags:\n      - Compliance\n      - EPM\n      - Tax Provisioning\n      - Tax Reporting\n    serviceName: Oracle Tax Reporting REST API\n    serviceCategory: API\n  - name: Oracle Narrative Reporting REST API\n    baseURL: https://{serviceHost}/epm/rest\n    tags:\n      - EPM\n      - Management Reporting\n      - Narrative Reporting\n      - Reports\n    serviceName: Oracle Narrative Reporting\
  \ REST API\n    serviceCategory: API\n  - name: Oracle Enterprise Profitability and Cost Management REST API\n    baseURL: https://{serviceHost}/HyperionPlanning/rest/v3\n    tags:\n      - Allocations\n      - Cost Management\n      - EPM\n      - Profitability\n    serviceName: Oracle Enterprise Profitability and Cost Management REST API\n    serviceCategory: API\n  - name: Oracle Profitability and Cost Management REST API\n    baseURL: https://{serviceHost}/epm/rest\n    tags:\n      - Cost Allocation\n      - Cost Management\n      - EPM\n      - Profitability\n    serviceName: Oracle Profitability and Cost Management REST API\n    serviceCategory: API\n  - name: Oracle FreeForm REST API\n    baseURL: https://{serviceHost}/HyperionPlanning/rest\n    tags:\n      - EPM\n      - Flexible Modeling\n      - FreeForm\n      - Planning\n    serviceName: Oracle FreeForm REST API\n    serviceCategory: API\n  - name: Oracle Enterprise Data Management REST API\n    baseURL: https://{serviceHost}/epm/rest\n\
  \    tags:\n      - Data Governance\n      - Enterprise Data Management\n      - EPM\n      - Master Data\n    serviceName: Oracle Enterprise Data Management REST API\n    serviceCategory: API\n  - name: Oracle EPM Task Manager REST API\n    baseURL: https://{serviceHost}/HyperionPlanning/rest/cmapi\n    tags:\n      - Close Management\n      - EPM\n      - Task Manager\n      - Workflow\n    serviceName: Oracle EPM Task Manager REST API\n    serviceCategory: API\n  - name: Oracle EPM Enterprise Journals REST API\n    baseURL: https://{serviceHost}/HyperionPlanning/rest/ej\n    tags:\n      - Enterprise Journals\n      - EPM\n      - Financial Close\n      - Journals\n    serviceName: Oracle EPM Enterprise Journals REST API\n    serviceCategory: API\n  - name: Oracle EPM Groovy Scripting API\n    baseURL: https://{serviceHost}\n    tags:\n      - Business Rules\n      - Calculation\n      - Groovy\n      - Scripting\n    serviceName: Oracle EPM Groovy Scripting API\n    serviceCategory:\
  \ API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/oracle-planning/refs/heads/main/finops/oracle-planning-finops.yml
sources: []
specification: FinOps Framework
tags:
- Budgeting
- Cloud
- Consolidation
- Enterprise
- EPM
- Financial Close
- Financial Planning
- Forecasting
- Oracle
- Planning
- FinOps
- Cost Management
- FOCUS
---
