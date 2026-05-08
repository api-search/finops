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
description: FinOps framework definition for the CData API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: CData
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: CData
  PublisherName: CData
  ServiceCategory: Developer Tools / API
  ServiceName: CData
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
name: Cdata Finops
provider_name: CData
provider_slug: cdata
publisher_name: CData
service_category: API
slug: cdata-finops
source_filename: cdata-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: CData\nproviderId: cdata\npublisherName: CData\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Data\n  - Data Access\n  - Data Connectivity\n  - Databases\n  - NoSQL\n  - SQL\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the CData API surface. Provides a FOCUS-aligned mapping for\n  cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming\
  \ team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice\
  \ Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: CData\n  ServiceCategory: Developer Tools / API\n  ProviderName: CData\n  PublisherName: CData\n  InvoiceIssuerName: CData\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n  \
  \    - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: CData SQL API\n    baseURL: ''\n    tags:\n      - Data Access\n      - Query\n      - REST\n      - SQL\n    serviceName: CData SQL API\n    serviceCategory: API\n  - name: CData Metadata API\n    baseURL: ''\n    tags:\n      - Catalog\n      - Data Access\n      - Metadata\n      - Schemas\n    serviceName: CData Metadata API\n    serviceCategory: API\n  - name: CData Log API\n    baseURL: ''\n    tags:\n      - Audit\n      - Logs\n      - Observability\n    serviceName: CData Log API\n    serviceCategory: API\n  - name: CData Connection API\n    baseURL: ''\n    tags:\n      - Administration\n      - Connections\n      - Data Sources\n    serviceName: CData Connection API\n    serviceCategory: API\n  - name: CData\
  \ Job API\n    baseURL: ''\n    tags:\n      - Background Jobs\n      - Monitoring\n      - Replication\n    serviceName: CData Job API\n    serviceCategory: API\n  - name: CData Account API\n    baseURL: ''\n    tags:\n      - Account Management\n      - Administration\n      - Users\n    serviceName: CData Account API\n    serviceCategory: API\n  - name: CData Audit API\n    baseURL: ''\n    tags:\n      - Audit\n      - Compliance\n      - Security\n    serviceName: CData Audit API\n    serviceCategory: API\n  - name: CData OData API\n    baseURL: ''\n    tags:\n      - Data Access\n      - OData\n      - REST\n    serviceName: CData OData API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: info@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/cdata/refs/heads/main/finops/cdata-finops.yml
sources: []
specification: FinOps Framework
tags:
- Data
- Data Access
- Data Connectivity
- Databases
- NoSQL
- SQL
- FinOps
- Cost Management
- FOCUS
---
