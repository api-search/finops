---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: meta-openapi.yml
  format: yaml
  label: Facebook Graph API - User
  slug: facebook-graph-api-user
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/meta/refs/heads/main/openapi/meta-openapi.yml
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
description: FinOps framework definition for the Meta API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Meta
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Meta
  PublisherName: Meta
  ServiceCategory: Developer Tools / API
  ServiceName: Meta
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
name: Meta Finops
provider_name: Meta
provider_slug: meta
publisher_name: Meta
service_category: API
slug: meta-finops
source_filename: meta-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Meta\nproviderId: meta\npublisherName: Meta\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Advertising\n  - Analytics\n  - Artificial Intelligence\n  - Messaging\n  - Social\n  - Social Media\n  - Virtual Reality\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Meta API surface. Provides a FOCUS-aligned mapping for\n  cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every\
  \ chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n   \
  \ capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Meta\n  ServiceCategory: Developer Tools / API\n  ProviderName: Meta\n  PublisherName: Meta\n  InvoiceIssuerName: Meta\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation:\
  \ sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Facebook Graph API - User\n    baseURL: ''\n    tags:\n      - Facebook\n      - Social\n      - Users\n    serviceName: Facebook Graph API - User\n    serviceCategory: API\n  - name: Instagram Graph API - User\n    baseURL: ''\n    tags:\n      - Instagram\n      - Social\n      - Users\n    serviceName: Instagram Graph API - User\n    serviceCategory: API\n  - name: Facebook Graph API - Page\n    baseURL: ''\n    tags:\n      - Facebook\n      - Pages\n      - Social\n    serviceName: Facebook Graph API - Page\n    serviceCategory: API\n  - name: Facebook Graph API - Post\n    baseURL: ''\n    tags:\n      - Facebook\n      - Posts\n      - Social\n    serviceName: Facebook Graph API - Post\n\
  \    serviceCategory: API\n  - name: Facebook Graph API - Group\n    baseURL: ''\n    tags:\n      - Facebook\n      - Groups\n      - Social\n    serviceName: Facebook Graph API - Group\n    serviceCategory: API\n  - name: Facebook Graph API - Event\n    baseURL: ''\n    tags:\n      - Events\n      - Facebook\n      - Social\n    serviceName: Facebook Graph API - Event\n    serviceCategory: API\n  - name: Facebook Marketing API\n    baseURL: ''\n    tags:\n      - Advertising\n      - Facebook\n      - Marketing\n    serviceName: Facebook Marketing API\n    serviceCategory: API\n  - name: Meta Conversions API\n    baseURL: ''\n    tags:\n      - Advertising\n      - Analytics\n      - Conversions\n    serviceName: Meta Conversions API\n    serviceCategory: API\n  - name: Meta Ad Library API\n    baseURL: ''\n    tags:\n      - Advertising\n      - Research\n      - Transparency\n    serviceName: Meta Ad Library API\n    serviceCategory: API\n  - name: WhatsApp Cloud API\n    baseURL:\
  \ ''\n    tags:\n      - Cloud\n      - Messaging\n      - WhatsApp\n    serviceName: WhatsApp Cloud API\n    serviceCategory: API\n  - name: WhatsApp Business Management API\n    baseURL: ''\n    tags:\n      - Business\n      - Messaging\n      - WhatsApp\n    serviceName: WhatsApp Business Management API\n    serviceCategory: API\n  - name: Messenger Platform API\n    baseURL: ''\n    tags:\n      - Chatbots\n      - Messaging\n      - Social\n    serviceName: Messenger Platform API\n    serviceCategory: API\n  - name: Threads API\n    baseURL: ''\n    tags:\n      - Social\n      - Social Media\n      - Threads\n    serviceName: Threads API\n    serviceCategory: API\n  - name: Instagram Graph API - Content Publishing\n    baseURL: ''\n    tags:\n      - Media\n      - Publishing\n      - Social\n    serviceName: Instagram Graph API - Content Publishing\n    serviceCategory: API\n  - name: Instagram Messaging API\n    baseURL: ''\n    tags:\n      - Instagram\n      - Messaging\n  \
  \    - Social\n    serviceName: Instagram Messaging API\n    serviceCategory: API\n  - name: Meta Content Library API\n    baseURL: ''\n    tags:\n      - Analytics\n      - Content\n      - Research\n    serviceName: Meta Content Library API\n    serviceCategory: API\n  - name: Meta Llama API\n    baseURL: ''\n    tags:\n      - Artificial Intelligence\n      - Large Language Models\n      - Machine Learning\n    serviceName: Meta Llama API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - name: Kin Lane\n    email: kin@apievangelist.com\n    url: http://apievangelist.com\n  - name: Meta Platforms Inc.\n    email: developer-support@meta.com\n    url: https://about.meta.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/meta/refs/heads/main/finops/meta-finops.yml
sources: []
specification: FinOps Framework
tags:
- Advertising
- Analytics
- Artificial Intelligence
- Messaging
- Social
- Social Media
- Virtual Reality
- FinOps
- Cost Management
- FOCUS
---
