---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: neo4j-http-api-openapi.yml
  format: yaml
  label: Neo4j HTTP API
  slug: http-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/neo4j/refs/heads/main/openapi/neo4j-http-api-openapi.yml
- filename: neo4j-query-api-openapi.yml
  format: yaml
  label: Neo4j Query API
  slug: query-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/neo4j/refs/heads/main/openapi/neo4j-query-api-openapi.yml
- filename: neo4j-aura-api-openapi.yml
  format: yaml
  label: Neo4j Aura API
  slug: aura-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/neo4j/refs/heads/main/openapi/neo4j-aura-api-openapi.yml
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
description: FinOps framework definition for the Neo4j API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Neo4j
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Neo4j
  PublisherName: Neo4j
  ServiceCategory: Developer Tools / API
  ServiceName: Neo4j
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
name: Neo4J Finops
provider_name: Neo4j
provider_slug: neo4j
publisher_name: Neo4j
service_category: API
slug: neo4j-finops
source_filename: neo4j-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Neo4j\nproviderId: neo4j\npublisherName: Neo4j\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Graph Database\n  - Cypher\n  - Cloud\n  - GraphQL\n  - Drivers\n  - APIs\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Neo4j API surface. Provides a FOCUS-aligned mapping for\n  cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team,\
  \ environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n\
  \      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Neo4j\n  ServiceCategory: Developer Tools / API\n  ProviderName: Neo4j\n  PublisherName: Neo4j\n  InvoiceIssuerName: Neo4j\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n  \
  \    - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Neo4j HTTP API\n    baseURL: ''\n    tags:\n      - Graph Database\n      - Cypher\n      - HTTP\n      - Transactions\n      - Database\n    serviceName: Neo4j HTTP API\n    serviceCategory: API\n  - name: Neo4j Query API\n    baseURL: ''\n    tags:\n      - Graph Database\n      - Cypher\n      - Query\n      - HTTP\n      - Database\n    serviceName: Neo4j Query API\n    serviceCategory: API\n  - name: Neo4j Aura API\n    baseURL: ''\n    tags:\n      - Cloud\n      - Graph Database\n      - Database Management\n      - Instances\n      - Snapshots\n    serviceName: Neo4j Aura API\n    serviceCategory: API\n  - name: Neo4j GraphQL Library\n    baseURL: ''\n    tags:\n      - GraphQL\n      - Graph Database\n      - JavaScript\n\
  \      - Low-Code\n      - API Development\n    serviceName: Neo4j GraphQL Library\n    serviceCategory: API\n  - name: Neo4j Bolt Protocol\n    baseURL: ''\n    tags:\n      - Binary Protocol\n      - Graph Database\n      - Drivers\n      - Connectivity\n      - Networking\n    serviceName: Neo4j Bolt Protocol\n    serviceCategory: API\n  - name: Neo4j Python Driver\n    baseURL: ''\n    tags:\n      - Python\n      - SDK\n      - Driver\n      - Graph Database\n      - Bolt\n    serviceName: Neo4j Python Driver\n    serviceCategory: API\n  - name: Neo4j Java Driver\n    baseURL: ''\n    tags:\n      - Java\n      - SDK\n      - Driver\n      - Graph Database\n      - Bolt\n    serviceName: Neo4j Java Driver\n    serviceCategory: API\n  - name: Neo4j JavaScript Driver\n    baseURL: ''\n    tags:\n      - JavaScript\n      - SDK\n      - Driver\n      - Graph Database\n      - Bolt\n      - Node.js\n    serviceName: Neo4j JavaScript Driver\n    serviceCategory: API\nunitEconomics:\n \
  \ - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: API Evangelist\n    email: info@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/neo4j/refs/heads/main/finops/neo4j-finops.yml
sources: []
specification: FinOps Framework
tags:
- Graph Database
- Cypher
- Cloud
- GraphQL
- Drivers
- APIs
- FinOps
- Cost Management
- FOCUS
---
