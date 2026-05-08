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
  label: Oracle REST Data Services (ORDS)
  slug: ''
  spec_type: OpenAPI
  url: https://docs.oracle.com/en/database/oracle/oracle-rest-data-services/
- filename: openapi.yaml
  format: yaml
  label: Oracle Cloud Infrastructure Database API
  slug: ''
  spec_type: OpenAPI
  url: https://docs.oracle.com/iaas/api/#/en/database/
- filename: oracle-database-soda-openapi.yml
  format: yaml
  label: Oracle SODA (Simple Oracle Document Access)
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/oracle-database/refs/heads/main/openapi/oracle-database-soda-openapi.yml
- filename: oracle-database-txeventq-asyncapi.yml
  format: yaml
  label: Oracle Transactional Event Queues (TxEventQ)
  slug: ''
  spec_type: AsyncAPI
  url: https://raw.githubusercontent.com/api-evangelist/oracle-database/refs/heads/main/asyncapi/oracle-database-txeventq-asyncapi.yml
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
description: FinOps framework definition for the Oracle Database API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Oracle Database
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Oracle Database
  PublisherName: Oracle Database
  ServiceCategory: Developer Tools / API
  ServiceName: Oracle Database
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
name: Oracle Database Finops
provider_name: Oracle Database
provider_slug: oracle-database
publisher_name: Oracle Database
service_category: API
slug: oracle-database-finops
source_filename: oracle-database-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Oracle Database\nproviderId: oracle-database\npublisherName: Oracle Database\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Cloud\n  - Database\n  - Enterprise\n  - Oracle\n  - REST API\n  - SQL\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Oracle Database API surface. Provides a FOCUS-aligned\n  mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable\
  \ API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n\
  \      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Oracle Database\n  ServiceCategory: Developer Tools / API\n  ProviderName: Oracle Database\n  PublisherName: Oracle Database\n  InvoiceIssuerName: Oracle Database\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n\
  \    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Oracle REST Data Services (ORDS)\n    baseURL: ''\n    tags:\n      - Data Access\n      - Database\n      - REST\n      - SQL\n    serviceName: Oracle REST Data Services (ORDS)\n    serviceCategory: API\n  - name: Oracle Database API for MongoDB\n    baseURL: ''\n    tags:\n      - Database\n      - JSON\n      - MongoDB\n      - NoSQL\n    serviceName: Oracle Database API for MongoDB\n    serviceCategory: API\n  - name: Oracle Cloud Infrastructure Database API\n    baseURL: ''\n    tags:\n      - Autonomous Database\n      - Cloud\n      - Database Management\n      - Infrastructure\n    serviceName: Oracle Cloud Infrastructure Database API\n    serviceCategory:\
  \ API\n  - name: Oracle Database JDBC\n    baseURL: ''\n    tags:\n      - Database Driver\n      - Java\n      - JDBC\n      - SQL\n    serviceName: Oracle Database JDBC\n    serviceCategory: API\n  - name: Oracle Call Interface (OCI)\n    baseURL: ''\n    tags:\n      - C\n      - C++\n      - Database Driver\n      - Native API\n    serviceName: Oracle Call Interface (OCI)\n    serviceCategory: API\n  - name: Oracle SQL Developer REST API\n    baseURL: ''\n    tags:\n      - Development Tools\n      - REST\n      - SQL\n    serviceName: Oracle SQL Developer REST API\n    serviceCategory: API\n  - name: Oracle SODA (Simple Oracle Document Access)\n    baseURL: ''\n    tags:\n      - Document Database\n      - JSON\n      - NoSQL\n      - REST\n    serviceName: Oracle SODA (Simple Oracle Document Access)\n    serviceCategory: API\n  - name: Oracle Transactional Event Queues (TxEventQ)\n    baseURL: ''\n    tags:\n      - Event Streaming\n      - Kafka\n      - Messaging\n      - Pub/Sub\n\
  \      - Queues\n    serviceName: Oracle Transactional Event Queues (TxEventQ)\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/oracle-database/refs/heads/main/finops/oracle-database-finops.yml
sources: []
specification: FinOps Framework
tags:
- Cloud
- Database
- Enterprise
- Oracle
- REST API
- SQL
- FinOps
- Cost Management
- FOCUS
---
