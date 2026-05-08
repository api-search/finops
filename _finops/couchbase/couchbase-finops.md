---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: couchbase-server-rest-api-openapi.yml
  format: yaml
  label: Couchbase Server REST API
  slug: couchbase-server-rest-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/couchbase/refs/heads/main/openapi/couchbase-server-rest-api-openapi.yml
- filename: couchbase-query-service-rest-api-openapi.yml
  format: yaml
  label: Couchbase Query Service REST API
  slug: couchbase-query-service-rest-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/couchbase/refs/heads/main/openapi/couchbase-query-service-rest-api-openapi.yml
- filename: couchbase-analytics-service-rest-api-openapi.yml
  format: yaml
  label: Couchbase Analytics Service REST API
  slug: couchbase-analytics-service-rest-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/couchbase/refs/heads/main/openapi/couchbase-analytics-service-rest-api-openapi.yml
- filename: couchbase-search-service-rest-api-openapi.yml
  format: yaml
  label: Couchbase Search Service REST API
  slug: couchbase-search-service-rest-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/couchbase/refs/heads/main/openapi/couchbase-search-service-rest-api-openapi.yml
- filename: couchbase-eventing-service-rest-api-openapi.yml
  format: yaml
  label: Couchbase Eventing Service REST API
  slug: couchbase-eventing-service-rest-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/couchbase/refs/heads/main/openapi/couchbase-eventing-service-rest-api-openapi.yml
- filename: couchbase-backup-service-rest-api-openapi.yml
  format: yaml
  label: Couchbase Backup Service REST API
  slug: couchbase-backup-service-rest-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/couchbase/refs/heads/main/openapi/couchbase-backup-service-rest-api-openapi.yml
- filename: couchbase-xdcr-rest-api-openapi.yml
  format: yaml
  label: Couchbase XDCR REST API
  slug: couchbase-xdcr-rest-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/couchbase/refs/heads/main/openapi/couchbase-xdcr-rest-api-openapi.yml
- filename: couchbase-capella-management-api-openapi.yml
  format: yaml
  label: Couchbase Capella Management API
  slug: couchbase-capella-management-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/couchbase/refs/heads/main/openapi/couchbase-capella-management-api-openapi.yml
- filename: couchbase-capella-app-services-public-api-openapi.yml
  format: yaml
  label: Couchbase Capella App Services Public API
  slug: couchbase-capella-app-services-public-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/couchbase/refs/heads/main/openapi/couchbase-capella-app-services-public-api-openapi.yml
- filename: couchbase-capella-app-services-admin-api-openapi.yml
  format: yaml
  label: Couchbase Capella App Services Admin API
  slug: couchbase-capella-app-services-admin-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/couchbase/refs/heads/main/openapi/couchbase-capella-app-services-admin-api-openapi.yml
- filename: couchbase-sync-gateway-public-rest-api-openapi.yml
  format: yaml
  label: Couchbase Sync Gateway Public REST API
  slug: couchbase-sync-gateway-public-rest-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/couchbase/refs/heads/main/openapi/couchbase-sync-gateway-public-rest-api-openapi.yml
- filename: couchbase-sync-gateway-admin-rest-api-openapi.yml
  format: yaml
  label: Couchbase Sync Gateway Admin REST API
  slug: couchbase-sync-gateway-admin-rest-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/couchbase/refs/heads/main/openapi/couchbase-sync-gateway-admin-rest-api-openapi.yml
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
description: FinOps framework definition for the Couchbase API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Couchbase
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Couchbase
  PublisherName: Couchbase
  ServiceCategory: Developer Tools / API
  ServiceName: Couchbase
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
name: Couchbase Finops
provider_name: Couchbase
provider_slug: couchbase
publisher_name: Couchbase
service_category: API
slug: couchbase-finops
source_filename: couchbase-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Couchbase\nproviderId: couchbase\npublisherName: Couchbase\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Analytics\n  - App Services\n  - Backup\n  - Capella\n  - Cloud\n  - Database\n  - DBaaS\n  - Eventing\n  - Full-Text Search\n  - Gateway\n  - JSON\n  - Mobile\n  - NoSQL\n  - Replication\n  - SQL++\n  - Sync\n  - Vector Search\n  - XDCR\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Couchbase API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption\
  \ costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n\
  \      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Couchbase\n  ServiceCategory: Developer Tools / API\n  ProviderName: Couchbase\n  PublisherName: Couchbase\n  InvoiceIssuerName: Couchbase\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n\
  \      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Couchbase Server REST API\n    baseURL: https://localhost:8091\n    tags:\n      - Administration\n      - Buckets\n      - Clusters\n      - Database\n      - NoSQL\n    serviceName: Couchbase Server REST API\n    serviceCategory: API\n  - name: Couchbase Query Service REST API\n    baseURL: https://localhost:8093\n    tags:\n      - Database\n      - N1QL\n      - NoSQL\n      - Query\n      - SQL++\n    serviceName: Couchbase Query Service REST API\n    serviceCategory: API\n  - name: Couchbase Analytics Service REST API\n    baseURL: https://localhost:8095\n\
  \    tags:\n      - Analytics\n      - Database\n      - NoSQL\n      - SQL++\n    serviceName: Couchbase Analytics Service REST API\n    serviceCategory: API\n  - name: Couchbase Search Service REST API\n    baseURL: https://localhost:8094\n    tags:\n      - Database\n      - Full-Text Search\n      - Indexing\n      - NoSQL\n      - Vector Search\n    serviceName: Couchbase Search Service REST API\n    serviceCategory: API\n  - name: Couchbase Eventing Service REST API\n    baseURL: https://localhost:8096\n    tags:\n      - Database\n      - Eventing\n      - NoSQL\n      - Serverless Functions\n    serviceName: Couchbase Eventing Service REST API\n    serviceCategory: API\n  - name: Couchbase Backup Service REST API\n    baseURL: https://localhost:8097\n    tags:\n      - Backup\n      - Database\n      - Disaster Recovery\n      - NoSQL\n    serviceName: Couchbase Backup Service REST API\n    serviceCategory: API\n  - name: Couchbase XDCR REST API\n    baseURL: https://localhost:8091\n\
  \    tags:\n      - Cross Data Center\n      - Database\n      - NoSQL\n      - Replication\n    serviceName: Couchbase XDCR REST API\n    serviceCategory: API\n  - name: Couchbase Capella Management API\n    baseURL: https://cloudapi.cloud.couchbase.com\n    tags:\n      - Capella\n      - Cloud\n      - Database\n      - DBaaS\n      - Management\n      - NoSQL\n    serviceName: Couchbase Capella Management API\n    serviceCategory: API\n  - name: Couchbase Capella App Services Public API\n    baseURL: ''\n    tags:\n      - App Services\n      - Capella\n      - Cloud\n      - Mobile\n      - NoSQL\n      - Sync\n    serviceName: Couchbase Capella App Services Public API\n    serviceCategory: API\n  - name: Couchbase Capella App Services Admin API\n    baseURL: ''\n    tags:\n      - Administration\n      - App Services\n      - Capella\n      - Cloud\n      - Mobile\n      - NoSQL\n    serviceName: Couchbase Capella App Services Admin API\n    serviceCategory: API\n  - name: Couchbase\
  \ Sync Gateway Public REST API\n    baseURL: https://localhost:4984\n    tags:\n      - Database\n      - Gateway\n      - Mobile\n      - NoSQL\n      - Sync\n    serviceName: Couchbase Sync Gateway Public REST API\n    serviceCategory: API\n  - name: Couchbase Sync Gateway Admin REST API\n    baseURL: https://localhost:4985\n    tags:\n      - Administration\n      - Database\n      - Mobile\n      - NoSQL\n      - Sync\n    serviceName: Couchbase Sync Gateway Admin REST API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/couchbase/refs/heads/main/finops/couchbase-finops.yml
sources: []
specification: FinOps Framework
tags:
- Analytics
- App Services
- Backup
- Capella
- Cloud
- Database
- DBaaS
- Eventing
- Full-Text Search
- Gateway
- JSON
- Mobile
- NoSQL
- Replication
- SQL++
- Sync
- Vector Search
- XDCR
- FinOps
- Cost Management
- FOCUS
---
