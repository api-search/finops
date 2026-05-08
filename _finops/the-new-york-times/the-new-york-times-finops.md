---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: new-york-times-archive-openapi-original.yml
  format: yaml
  label: The New York Times Archive API
  slug: archive-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/the-new-york-times/refs/heads/main/openapi/new-york-times-archive-openapi-original.yml
- filename: new-york-times-article-search-openapi-original.yml
  format: yaml
  label: The New York Times Article Search API
  slug: article-search-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/the-new-york-times/refs/heads/main/openapi/new-york-times-article-search-openapi-original.yml
- filename: new-york-times-books-openapi-original.yml
  format: yaml
  label: The New York Times Books API
  slug: books-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/the-new-york-times/refs/heads/main/openapi/new-york-times-books-openapi-original.yml
- filename: new-york-times-most-popular-openapi-original.yml
  format: yaml
  label: The New York Times Most Popular API
  slug: most-popular
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/the-new-york-times/refs/heads/main/openapi/new-york-times-most-popular-openapi-original.yml
- filename: new-york-times-movie-review-openapi-original.yml
  format: yaml
  label: The New York Times Movie Reviews API
  slug: movie-reviews-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/the-new-york-times/refs/heads/main/openapi/new-york-times-movie-review-openapi-original.yml
- filename: new-york-times-semantic-openapi-original.yml
  format: yaml
  label: The New York Times Semantic API
  slug: semantic-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/the-new-york-times/refs/heads/main/openapi/new-york-times-semantic-openapi-original.yml
- filename: new-york-times-times-tags-openapi-original.yml
  format: yaml
  label: The New York Times TimesTags API
  slug: timestags-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/the-new-york-times/refs/heads/main/openapi/new-york-times-times-tags-openapi-original.yml
- filename: new-york-times-times-newswire-openapi-original.yml
  format: yaml
  label: The New York Times Times Newswire API
  slug: times-newswire-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/the-new-york-times/refs/heads/main/openapi/new-york-times-times-newswire-openapi-original.yml
- filename: new-york-times-top-stories-openapi-original.yml
  format: yaml
  label: The New York Times Top Stories API
  slug: top-stories
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/the-new-york-times/refs/heads/main/openapi/new-york-times-top-stories-openapi-original.yml
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
description: FinOps framework definition for the The New York Times API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: The New York Times
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: The New York Times
  PublisherName: The New York Times
  ServiceCategory: Developer Tools / API
  ServiceName: The New York Times
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
name: The New York Times Finops
provider_name: The New York Times
provider_slug: the-new-york-times
publisher_name: The New York Times
service_category: API
slug: the-new-york-times-finops
source_filename: the-new-york-times-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: The New York Times\nproviderId: the-new-york-times\npublisherName: The New York Times\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Articles\n  - Books\n  - Movies\n  - News\n  - Media\n  - Publishing\n  - Journalism\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the The New York Times API surface. Provides a FOCUS-aligned\n  mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description:\
  \ Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n\
  \    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: The New York Times\n  ServiceCategory: Developer Tools / API\n  ProviderName: The New York Times\n  PublisherName: The New York Times\n  InvoiceIssuerName: The New York Times\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned\
  \ over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: The New York Times Archive API\n    baseURL: https://api.nytimes.com/svc/archive/v1\n    tags:\n      - Archive\n      - Articles\n      - Months\n      - Years\n      - History\n    serviceName: The New York Times Archive API\n    serviceCategory: API\n  - name: The New York Times Article Search API\n    baseURL: https://api.nytimes.com/svc/search/v2\n    tags:\n      - Articles\n      - Search\n      - Keywords\n      - Facets\n    serviceName: The New York Times Article Search API\n    serviceCategory: API\n  - name: The New York Times Books API\n    baseURL: https://api.nytimes.com/svc/books/v3\n    tags:\n      - Books\n   \
  \   - Best Sellers\n      - Reviews\n      - Lists\n    serviceName: The New York Times Books API\n    serviceCategory: API\n  - name: The New York Times Most Popular API\n    baseURL: https://api.nytimes.com/svc/mostpopular/v2\n    tags:\n      - Articles\n      - Popular\n      - Social Sharing\n      - Trending\n    serviceName: The New York Times Most Popular API\n    serviceCategory: API\n  - name: The New York Times Movie Reviews API\n    baseURL: https://api.nytimes.com/svc/movies/v2\n    tags:\n      - Movies\n      - Reviews\n      - Critics\n      - Film\n    serviceName: The New York Times Movie Reviews API\n    serviceCategory: API\n  - name: The New York Times Semantic API\n    baseURL: https://api.nytimes.com/svc/semantic/v2\n    tags:\n      - Concepts\n      - Semantics\n      - Metadata\n      - Entities\n      - People\n      - Organizations\n    serviceName: The New York Times Semantic API\n    serviceCategory: API\n  - name: The New York Times TimesTags API\n    baseURL:\
  \ https://api.nytimes.com/svc/suggest/v1\n    tags:\n      - Tags\n      - Autocomplete\n      - Metadata\n      - Search\n    serviceName: The New York Times TimesTags API\n    serviceCategory: API\n  - name: The New York Times Times Newswire API\n    baseURL: https://api.nytimes.com/svc/news/v3\n    tags:\n      - News\n      - Wire\n      - Streaming\n      - Articles\n      - Sections\n    serviceName: The New York Times Times Newswire API\n    serviceCategory: API\n  - name: The New York Times Top Stories API\n    baseURL: https://api.nytimes.com/svc/topstories/v2\n    tags:\n      - Articles\n      - Top Stories\n      - Sections\n      - News\n    serviceName: The New York Times Top Stories API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/the-new-york-times/refs/heads/main/finops/the-new-york-times-finops.yml
sources: []
specification: FinOps Framework
tags:
- Articles
- Books
- Movies
- News
- Media
- Publishing
- Journalism
- FinOps
- Cost Management
- FOCUS
---
