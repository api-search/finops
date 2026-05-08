---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: wikidata-mediawiki-openapi.yml
  format: yaml
  label: Wikibase REST API
  slug: wikibase-rest-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/wikidata/refs/heads/main/openapi/wikidata-mediawiki-openapi.yml
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
description: FinOps framework definition for the Wikidata API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Wikidata
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Wikidata
  PublisherName: Wikidata
  ServiceCategory: Developer Tools / API
  ServiceName: Wikidata
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
name: Wikidata Finops
provider_name: Wikidata
provider_slug: wikidata
publisher_name: Wikidata
service_category: API
slug: wikidata-finops
source_filename: wikidata-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Wikidata\nproviderId: wikidata\npublisherName: Wikidata\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Knowledge Graph\n  - Linked Data\n  - Open Data\n  - Semantic Web\n  - SPARQL\n  - Wikipedia\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Wikidata API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable\
  \ API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n\
  \      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Wikidata\n  ServiceCategory: Developer Tools / API\n  ProviderName: Wikidata\n  PublisherName: Wikidata\n  InvoiceIssuerName: Wikidata\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation:\
  \ sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Wikibase REST API\n    baseURL: https://www.wikidata.org/w/rest.php/wikibase/v0\n    tags:\n      - Knowledge Graph\n      - Entities\n      - Items\n      - Properties\n      - Statements\n      - Linked Data\n    serviceName: Wikibase REST API\n    serviceCategory: API\n  - name: MediaWiki Action API\n    baseURL: https://www.wikidata.org/w/api.php\n    tags:\n      - MediaWiki\n      - Batch Operations\n      - Entity Retrieval\n      - Search\n    serviceName: MediaWiki Action API\n    serviceCategory: API\n  - name: SPARQL Query Service\n    baseURL: https://query.wikidata.org/sparql\n    tags:\n      - SPARQL\n      - Graph Query\n      - Linked Data\n      - Open Data\n    serviceName: SPARQL\
  \ Query Service\n    serviceCategory: API\n  - name: Linked Data Interface\n    baseURL: https://www.wikidata.org/entity\n    tags:\n      - Linked Data\n      - RDF\n      - JSON-LD\n      - Content Negotiation\n    serviceName: Linked Data Interface\n    serviceCategory: API\n  - name: Recent Changes Event Stream\n    baseURL: https://stream.wikimedia.org/v2/stream\n    tags:\n      - Event Streaming\n      - Real-time\n      - Server-Sent Events\n      - Change Detection\n    serviceName: Recent Changes Event Stream\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/wikidata/refs/heads/main/finops/wikidata-finops.yml
sources: []
specification: FinOps Framework
tags:
- Knowledge Graph
- Linked Data
- Open Data
- Semantic Web
- SPARQL
- Wikipedia
- FinOps
- Cost Management
- FOCUS
---
