---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: apollo-io-openapi.yml
  format: yaml
  label: Apollo People Search API
  slug: apollo-people-search-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/apollo-io/refs/heads/main/openapi/apollo-io-openapi.yml
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
description: FinOps framework definition for the Apollo.io API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Apollo.io
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Apollo.io
  PublisherName: Apollo.io
  ServiceCategory: Developer Tools / API
  ServiceName: Apollo.io
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
name: Apollo Io Finops
provider_name: Apollo.io
provider_slug: apollo-io
publisher_name: Apollo.io
service_category: API
slug: apollo-io-finops
source_filename: apollo-io-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Apollo.io\nproviderId: apollo-io\npublisherName: Apollo.io\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Sales Intelligence\n  - Prospecting\n  - Engagement\n  - B2B Data\n  - Enrichment\n  - SaaS\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Apollo.io API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable\
  \ API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n\
  \      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Apollo.io\n  ServiceCategory: Developer Tools / API\n  ProviderName: Apollo.io\n  PublisherName: Apollo.io\n  InvoiceIssuerName: Apollo.io\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n  \
  \  aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Apollo People Search API\n    baseURL: ''\n    tags:\n      - People\n      - Search\n      - Prospecting\n    serviceName: Apollo People Search API\n    serviceCategory: API\n  - name: Apollo Organization Search API\n    baseURL: ''\n    tags:\n      - Organizations\n      - Companies\n      - Search\n    serviceName: Apollo Organization Search API\n    serviceCategory: API\n  - name: Apollo People Enrichment API\n    baseURL: ''\n    tags:\n      - People\n      - Enrichment\n    serviceName: Apollo People Enrichment API\n    serviceCategory: API\n  - name: Apollo Organization Enrichment API\n    baseURL: ''\n    tags:\n      - Organizations\n      - Enrichment\n    serviceName:\
  \ Apollo Organization Enrichment API\n    serviceCategory: API\n  - name: Apollo Bulk People Enrichment API\n    baseURL: ''\n    tags:\n      - Bulk Enrichment\n      - People\n    serviceName: Apollo Bulk People Enrichment API\n    serviceCategory: API\n  - name: Apollo Bulk Organization Enrichment API\n    baseURL: ''\n    tags:\n      - Bulk Enrichment\n      - Organizations\n    serviceName: Apollo Bulk Organization Enrichment API\n    serviceCategory: API\n  - name: Apollo Contacts API\n    baseURL: ''\n    tags:\n      - Contacts\n      - CRM\n    serviceName: Apollo Contacts API\n    serviceCategory: API\n  - name: Apollo Accounts API\n    baseURL: ''\n    tags:\n      - Accounts\n      - CRM\n    serviceName: Apollo Accounts API\n    serviceCategory: API\n  - name: Apollo Deals API\n    baseURL: ''\n    tags:\n      - Deals\n      - Opportunities\n      - Pipeline\n    serviceName: Apollo Deals API\n    serviceCategory: API\n  - name: Apollo Sequences API\n    baseURL: ''\n  \
  \  tags:\n      - Sequences\n      - Cadences\n      - Outreach\n    serviceName: Apollo Sequences API\n    serviceCategory: API\n  - name: Apollo Email Accounts API\n    baseURL: ''\n    tags:\n      - Email Accounts\n      - SMTP\n    serviceName: Apollo Email Accounts API\n    serviceCategory: API\n  - name: Apollo Emails API\n    baseURL: ''\n    tags:\n      - Emails\n      - Tracking\n    serviceName: Apollo Emails API\n    serviceCategory: API\n  - name: Apollo Calls API\n    baseURL: ''\n    tags:\n      - Calls\n      - Telephony\n    serviceName: Apollo Calls API\n    serviceCategory: API\n  - name: Apollo Tasks API\n    baseURL: ''\n    tags:\n      - Tasks\n    serviceName: Apollo Tasks API\n    serviceCategory: API\n  - name: Apollo Meetings API\n    baseURL: ''\n    tags:\n      - Meetings\n      - Scheduling\n    serviceName: Apollo Meetings API\n    serviceCategory: API\n  - name: Apollo Custom Fields API\n    baseURL: ''\n    tags:\n      - Custom Fields\n      - Metadata\n\
  \    serviceName: Apollo Custom Fields API\n    serviceCategory: API\n  - name: Apollo Lists API\n    baseURL: ''\n    tags:\n      - Lists\n      - Segments\n    serviceName: Apollo Lists API\n    serviceCategory: API\n  - name: Apollo Tags API\n    baseURL: ''\n    tags:\n      - Tags\n    serviceName: Apollo Tags API\n    serviceCategory: API\n  - name: Apollo Users API\n    baseURL: ''\n    tags:\n      - Users\n    serviceName: Apollo Users API\n    serviceCategory: API\n  - name: Apollo Analytics API\n    baseURL: ''\n    tags:\n      - Analytics\n      - Reporting\n    serviceName: Apollo Analytics API\n    serviceCategory: API\n  - name: Apollo API Usage API\n    baseURL: ''\n    tags:\n      - Usage\n      - Credits\n    serviceName: Apollo API Usage API\n    serviceCategory: API\n  - name: Apollo Webhooks API\n    baseURL: ''\n    tags:\n      - Webhooks\n      - Events\n    serviceName: Apollo Webhooks API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n\
  \    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/apollo-io/refs/heads/main/finops/apollo-io-finops.yml
sources: []
specification: FinOps Framework
tags:
- Sales Intelligence
- Prospecting
- Engagement
- B2B Data
- Enrichment
- SaaS
- FinOps
- Cost Management
- FOCUS
---
