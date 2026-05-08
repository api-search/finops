---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: beehiiv-openapi.yml
  format: yaml
  label: beehiiv Publications API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/beehiiv/refs/heads/main/openapi/beehiiv-openapi.yml
- filename: beehiiv-openapi.yml
  format: yaml
  label: beehiiv Subscriptions API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/beehiiv/refs/heads/main/openapi/beehiiv-openapi.yml
- filename: beehiiv-openapi.yml
  format: yaml
  label: beehiiv Posts API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/beehiiv/refs/heads/main/openapi/beehiiv-openapi.yml
- filename: beehiiv-openapi.yml
  format: yaml
  label: beehiiv Automations API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/beehiiv/refs/heads/main/openapi/beehiiv-openapi.yml
- filename: beehiiv-openapi.yml
  format: yaml
  label: beehiiv Custom Fields API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/beehiiv/refs/heads/main/openapi/beehiiv-openapi.yml
- filename: beehiiv-openapi.yml
  format: yaml
  label: beehiiv Segments API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/beehiiv/refs/heads/main/openapi/beehiiv-openapi.yml
- filename: beehiiv-openapi.yml
  format: yaml
  label: beehiiv Tiers API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/beehiiv/refs/heads/main/openapi/beehiiv-openapi.yml
- filename: beehiiv-openapi.yml
  format: yaml
  label: beehiiv Polls API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/beehiiv/refs/heads/main/openapi/beehiiv-openapi.yml
- filename: beehiiv-openapi.yml
  format: yaml
  label: beehiiv Webhooks API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/beehiiv/refs/heads/main/openapi/beehiiv-openapi.yml
- filename: beehiiv-openapi.yml
  format: yaml
  label: beehiiv OAuth2 API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/beehiiv/refs/heads/main/openapi/beehiiv-openapi.yml
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
description: FinOps framework definition for the beehiiv API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: beehiiv
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: beehiiv
  PublisherName: beehiiv
  ServiceCategory: Developer Tools / API
  ServiceName: beehiiv
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
name: Beehiiv Finops
provider_name: beehiiv
provider_slug: beehiiv
publisher_name: beehiiv
service_category: API
slug: beehiiv-finops
source_filename: beehiiv-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: beehiiv\nproviderId: beehiiv\npublisherName: beehiiv\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Newsletter\n  - Creator\n  - Email\n  - Subscription\n  - Publishing\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the beehiiv API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming\
  \ team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice\
  \ Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: beehiiv\n  ServiceCategory: Developer Tools / API\n  ProviderName: beehiiv\n  PublisherName: beehiiv\n  InvoiceIssuerName: beehiiv\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n\
  \      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: beehiiv Publications API\n    baseURL: https://api.beehiiv.com/v2\n    tags:\n      - Publications\n    serviceName: beehiiv Publications API\n    serviceCategory: API\n  - name: beehiiv Subscriptions API\n    baseURL: https://api.beehiiv.com/v2\n    tags:\n      - Subscribers\n    serviceName: beehiiv Subscriptions API\n    serviceCategory: API\n  - name: beehiiv Posts API\n    baseURL: https://api.beehiiv.com/v2\n    tags:\n      - Posts\n      - Content\n    serviceName: beehiiv Posts API\n    serviceCategory: API\n  - name: beehiiv Automations API\n    baseURL: https://api.beehiiv.com/v2\n    tags:\n      - Automations\n    serviceName: beehiiv Automations API\n    serviceCategory: API\n  - name: beehiiv Custom Fields\
  \ API\n    baseURL: https://api.beehiiv.com/v2\n    tags:\n      - Custom Fields\n    serviceName: beehiiv Custom Fields API\n    serviceCategory: API\n  - name: beehiiv Segments API\n    baseURL: https://api.beehiiv.com/v2\n    tags:\n      - Segments\n    serviceName: beehiiv Segments API\n    serviceCategory: API\n  - name: beehiiv Tiers API\n    baseURL: https://api.beehiiv.com/v2\n    tags:\n      - Tiers\n      - Paid Subscriptions\n    serviceName: beehiiv Tiers API\n    serviceCategory: API\n  - name: beehiiv Polls API\n    baseURL: https://api.beehiiv.com/v2\n    tags:\n      - Polls\n    serviceName: beehiiv Polls API\n    serviceCategory: API\n  - name: beehiiv Webhooks API\n    baseURL: https://api.beehiiv.com/v2\n    tags:\n      - Webhooks\n      - Events\n    serviceName: beehiiv Webhooks API\n    serviceCategory: API\n  - name: beehiiv OAuth2 API\n    baseURL: https://api.beehiiv.com/v2\n    tags:\n      - OAuth\n      - Authentication\n    serviceName: beehiiv OAuth2 API\n\
  \    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/beehiiv/refs/heads/main/finops/beehiiv-finops.yml
sources: []
specification: FinOps Framework
tags:
- Newsletter
- Creator
- Email
- Subscription
- Publishing
- FinOps
- Cost Management
- FOCUS
---
