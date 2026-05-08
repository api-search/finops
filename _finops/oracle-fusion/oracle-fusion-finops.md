---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: api-rest-api.html
  format: yaml
  label: Oracle Fusion ERP REST API
  slug: ''
  spec_type: OpenAPI
  url: https://docs.oracle.com/en/cloud/saas/financials/22r3/farfa/api-rest-api.html
- filename: api-rest-api.html
  format: yaml
  label: Oracle Fusion HCM REST API
  slug: ''
  spec_type: OpenAPI
  url: https://docs.oracle.com/en/cloud/saas/human-resources/22r3/farws/api-rest-api.html
- filename: api-rest-api.html
  format: yaml
  label: Oracle Fusion SCM REST API
  slug: ''
  spec_type: OpenAPI
  url: https://docs.oracle.com/en/cloud/saas/supply-chain-management/22r3/fasrs/api-rest-api.html
- filename: rest-api.html
  format: yaml
  label: Oracle Fusion CX Sales and Fusion Service REST API
  slug: ''
  spec_type: OpenAPI
  url: https://docs.oracle.com/en/cloud/saas/cx-sales/rest-api.html
- filename: oracle-fusion-common-openapi.yml
  format: yaml
  label: Oracle Fusion Common Features REST API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/oracle-fusion/refs/heads/main/openapi/oracle-fusion-common-openapi.yml
- filename: oracle-fusion-project-management-openapi.yml
  format: yaml
  label: Oracle Fusion Project Management REST API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/oracle-fusion/refs/heads/main/openapi/oracle-fusion-project-management-openapi.yml
- filename: oracle-fusion-epm-openapi.yml
  format: yaml
  label: Oracle Fusion EPM REST API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/oracle-fusion/refs/heads/main/openapi/oracle-fusion-epm-openapi.yml
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
description: FinOps framework definition for the Oracle Fusion Cloud Applications API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Oracle Fusion Cloud Applications
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Oracle Fusion Cloud Applications
  PublisherName: Oracle Fusion Cloud Applications
  ServiceCategory: Developer Tools / API
  ServiceName: Oracle Fusion Cloud Applications
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
name: Oracle Fusion Finops
provider_name: Oracle Fusion Cloud Applications
provider_slug: oracle-fusion
publisher_name: Oracle Fusion Cloud Applications
service_category: API
slug: oracle-fusion-finops
source_filename: oracle-fusion-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Oracle Fusion Cloud Applications\nproviderId: oracle-fusion\npublisherName: Oracle Fusion Cloud Applications\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Cloud\n  - CX\n  - Enterprise\n  - EPM\n  - ERP\n  - HCM\n  - Project Management\n  - REST API\n  - SaaS\n  - SCM\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Oracle Fusion Cloud Applications API surface. Provides\n  a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across\n  the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and\
  \ finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud\
  \ Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Oracle Fusion Cloud Applications\n  ServiceCategory: Developer Tools / API\n  ProviderName: Oracle Fusion Cloud Applications\n  PublisherName: Oracle Fusion Cloud Applications\n  InvoiceIssuerName: Oracle Fusion Cloud Applications\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n\
  \      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Oracle Fusion ERP REST API\n    baseURL: https://{instance}.oraclecloud.com/fscmRestApi/\n    tags:\n      - ERP\n      - Financials\n      - Procurement\n      - Projects\n      - Risk Management\n    serviceName: Oracle Fusion ERP REST API\n    serviceCategory: API\n  - name: Oracle Fusion HCM REST API\n    baseURL: https://{instance}.oraclecloud.com/hcmRestApi/\n    tags:\n      - HCM\n      - Human Resources\n      - Payroll\n      - Talent Management\n      - Workforce\n    serviceName: Oracle\
  \ Fusion HCM REST API\n    serviceCategory: API\n  - name: Oracle Fusion SCM REST API\n    baseURL: https://{instance}.oraclecloud.com/fscmRestApi/\n    tags:\n      - Inventory\n      - Logistics\n      - Manufacturing\n      - Order Management\n      - SCM\n      - Supply Chain\n    serviceName: Oracle Fusion SCM REST API\n    serviceCategory: API\n  - name: Oracle Fusion CX Sales and Fusion Service REST API\n    baseURL: https://{instance}.oraclecloud.com/crmRestApi/\n    tags:\n      - Commerce\n      - Customer Experience\n      - CX\n      - Marketing\n      - Sales\n    serviceName: Oracle Fusion CX Sales and Fusion Service REST API\n    serviceCategory: API\n  - name: Oracle Fusion Common Features REST API\n    baseURL: https://{instance}.oraclecloud.com/fscmRestApi/\n    tags:\n      - Attachments\n      - Common\n      - Flexfields\n      - Roles\n      - Security\n      - Users\n    serviceName: Oracle Fusion Common Features REST API\n    serviceCategory: API\n  - name: Oracle\
  \ Fusion Project Management REST API\n    baseURL: https://{instance}.oraclecloud.com/fscmRestApi/\n    tags:\n      - Grants\n      - Project Billing\n      - Project Costing\n      - Project Management\n    serviceName: Oracle Fusion Project Management REST API\n    serviceCategory: API\n  - name: Oracle Fusion EPM REST API\n    baseURL: https://{instance}.oraclecloud.com/HyperionPlanning/rest/\n    tags:\n      - Budgeting\n      - Consolidation\n      - EPM\n      - Financial Close\n      - Planning\n    serviceName: Oracle Fusion EPM REST API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/oracle-fusion/refs/heads/main/finops/oracle-fusion-finops.yml
sources: []
specification: FinOps Framework
tags:
- Cloud
- CX
- Enterprise
- EPM
- ERP
- HCM
- Project Management
- REST API
- SaaS
- SCM
- FinOps
- Cost Management
- FOCUS
---
