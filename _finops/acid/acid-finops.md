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
  label: Google Spanner API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/APIs-guru/openapi-directory/main/APIs/googleapis.com/spanner/v1/openapi.yaml
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
description: FinOps framework definition for the ACID API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: ACID
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: ACID
  PublisherName: ACID
  ServiceCategory: Developer Tools / API
  ServiceName: ACID
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
name: Acid Finops
provider_name: ACID
provider_slug: acid
publisher_name: ACID
service_category: API
slug: acid-finops
source_filename: acid-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: ACID\nproviderId: acid\npublisherName: ACID\nserviceCategory: API\ncreated: '2026-05-04'\nmodified: '2026-05-04'\ntags:\n  - ACID\n  - Database\n  - Transactions\n  - Atomicity\n  - Consistency\n  - Isolation\n  - Durability\n  - Distributed Systems\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the ACID API surface. Provides a FOCUS-aligned mapping for\n  cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every\
  \ chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n   \
  \ capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: ACID\n  ServiceCategory: Developer Tools / API\n  ProviderName: ACID\n  PublisherName: ACID\n  InvoiceIssuerName: ACID\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation:\
  \ sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: PostgreSQL Transaction API\n    baseURL: https://www.postgresql.org/\n    tags:\n      - PostgreSQL\n      - RDBMS\n      - MVCC\n      - ACID\n      - SQL\n    serviceName: PostgreSQL Transaction API\n    serviceCategory: API\n  - name: CockroachDB Distributed SQL API\n    baseURL: https://cockroachlabs.cloud/\n    tags:\n      - CockroachDB\n      - Distributed SQL\n      - ACID\n      - Serializable\n      - Cloud Native\n    serviceName: CockroachDB Distributed SQL API\n    serviceCategory: API\n  - name: Google Spanner API\n    baseURL: https://spanner.googleapis.com/\n    tags:\n      - Google Spanner\n      - Distributed Database\n      - Global Scale\n      - ACID\n      - TrueTime\n  \
  \  serviceName: Google Spanner API\n    serviceCategory: API\n  - name: Amazon Aurora Transactions API\n    baseURL: https://rds.amazonaws.com/\n    tags:\n      - AWS Aurora\n      - MySQL\n      - PostgreSQL\n      - ACID\n      - Serverless\n    serviceName: Amazon Aurora Transactions API\n    serviceCategory: API\n  - name: Atomikos Transaction API\n    baseURL: https://www.atomikos.com/\n    tags:\n      - Atomikos\n      - Distributed Transactions\n      - TCC Pattern\n      - Microservices\n      - XA\n    serviceName: Atomikos Transaction API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/acid/refs/heads/main/finops/acid-finops.yml
sources: []
specification: FinOps Framework
tags:
- ACID
- Database
- Transactions
- Atomicity
- Consistency
- Isolation
- Durability
- Distributed Systems
- FinOps
- Cost Management
- FOCUS
---
