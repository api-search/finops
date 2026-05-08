---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: oracle-database-19c-ords-openapi.yml
  format: yaml
  label: Oracle REST Data Services (ORDS)
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/oracle-database-19c/refs/heads/main/openapi/oracle-database-19c-ords-openapi.yml
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
description: FinOps framework definition for the Oracle Database 19c API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Oracle Database 19c
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Oracle Database 19c
  PublisherName: Oracle Database 19c
  ServiceCategory: Developer Tools / API
  ServiceName: Oracle Database 19c
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
name: Oracle Database 19C Finops
provider_name: Oracle Database 19c
provider_slug: oracle-database-19c
publisher_name: Oracle Database 19c
service_category: API
slug: oracle-database-19c-finops
source_filename: oracle-database-19c-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Oracle Database 19c\nproviderId: oracle-database-19c\npublisherName: Oracle Database 19c\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Database\n  - Enterprise\n  - Json\n  - Machine-Learning\n  - Nosql\n  - Oracle\n  - Rest\n  - Sql\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Oracle Database 19c API surface. Provides a FOCUS-aligned\n  mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name:\
  \ Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  -\
  \ name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Oracle Database 19c\n  ServiceCategory: Developer Tools / API\n  ProviderName: Oracle Database 19c\n  PublisherName: Oracle Database 19c\n  InvoiceIssuerName: Oracle Database 19c\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n\
  \    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Oracle REST Data Services (ORDS)\n    baseURL: https://example.oracle.com:8443/ords/\n    tags:\n      - Database\n      - Oracle\n      - Rest\n      - Sql\n    serviceName: Oracle REST Data Services (ORDS)\n    serviceCategory: API\n  - name: Oracle Database SODA (Simple Oracle Document Access)\n    baseURL: https://example.oracle.com:8443/ords/\n    tags:\n      - Document-Store\n      - Json\n      - Nosql\n      - Oracle\n    serviceName: Oracle Database SODA (Simple Oracle Document Access)\n    serviceCategory: API\n  - name: Oracle SQL Developer Web\n    baseURL: https://example.oracle.com:8443/ords/sql-developer/\n\
  \    tags:\n      - Administration\n      - Development\n      - Sql\n      - Web-Interface\n    serviceName: Oracle SQL Developer Web\n    serviceCategory: API\n  - name: Oracle Database API for MongoDB\n    baseURL: mongodb://example.oracle.com:27017/\n    tags:\n      - Compatibility\n      - Document-Store\n      - Mongodb\n      - Nosql\n    serviceName: Oracle Database API for MongoDB\n    serviceCategory: API\n  - name: Oracle Database JSON Collections API\n    baseURL: https://example.oracle.com:8443/ords/\n    tags:\n      - Collections\n      - Document-Api\n      - Json\n      - Rest\n    serviceName: Oracle Database JSON Collections API\n    serviceCategory: API\n  - name: Oracle Database REST API for AutoML\n    baseURL: https://example.oracle.com:8443/omlmod/\n    tags:\n      - Ai\n      - Analytics\n      - Automl\n      - Machine-Learning\n    serviceName: Oracle Database REST API for AutoML\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n  \
  \  metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/oracle-database-19c/refs/heads/main/finops/oracle-database-19c-finops.yml
sources: []
specification: FinOps Framework
tags:
- Database
- Enterprise
- Json
- Machine-Learning
- Nosql
- Oracle
- Rest
- Sql
- FinOps
- Cost Management
- FOCUS
---
