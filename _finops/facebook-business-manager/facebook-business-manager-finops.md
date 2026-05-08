---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: facebook-marketing-openapi.yml
  format: yaml
  label: Facebook Marketing API
  slug: facebook-marketing-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/facebook-business-manager/refs/heads/main/openapi/facebook-marketing-openapi.yml
- filename: facebook-pages-openapi.yml
  format: yaml
  label: Facebook Pages API
  slug: facebook-pages-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/facebook-business-manager/refs/heads/main/openapi/facebook-pages-openapi.yml
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
description: FinOps framework definition for the Facebook Business Manager API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Facebook Business Manager
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Facebook Business Manager
  PublisherName: Facebook Business Manager
  ServiceCategory: Developer Tools / API
  ServiceName: Facebook Business Manager
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
name: Facebook Business Manager Finops
provider_name: Facebook Business Manager
provider_slug: facebook-business-manager
publisher_name: Facebook Business Manager
service_category: API
slug: facebook-business-manager-finops
source_filename: facebook-business-manager-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Facebook Business Manager\nproviderId: facebook-business-manager\npublisherName: Facebook Business Manager\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Advertising\n  - Analytics\n  - Business Management\n  - Marketing\n  - Social Media\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Facebook Business Manager API surface. Provides a FOCUS-aligned\n  mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n\
  \  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and\
  \ SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Facebook Business Manager\n  ServiceCategory: Developer Tools / API\n  ProviderName: Facebook Business Manager\n  PublisherName: Facebook Business Manager\n  InvoiceIssuerName: Facebook Business Manager\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n\
  \      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Facebook Marketing API\n    baseURL: https://graph.facebook.com/v18.0\n    tags:\n      - Ads\n      - Advertising\n      - Campaigns\n      - Marketing\n    serviceName: Facebook Marketing API\n    serviceCategory: API\n  - name: Facebook Pages API\n    baseURL: https://graph.facebook.com/v18.0\n    tags:\n      - Content\n      - Pages\n      - Publishing\n      - Social Media\n    serviceName: Facebook Pages API\n    serviceCategory: API\n  - name: Facebook Conversions API\n    baseURL: https://graph.facebook.com/v18.0\n    tags:\n      - Attribution\n   \
  \   - Conversions\n      - Events\n      - Tracking\n    serviceName: Facebook Conversions API\n    serviceCategory: API\n  - name: Facebook Business Asset API\n    baseURL: https://graph.facebook.com/v18.0\n    tags:\n      - Assets\n      - Audiences\n      - Catalogs\n      - Pixels\n    serviceName: Facebook Business Asset API\n    serviceCategory: API\n  - name: Facebook Instagram API\n    baseURL: https://graph.facebook.com/v18.0\n    tags:\n      - Content\n      - Instagram\n      - Media\n      - Social Media\n    serviceName: Facebook Instagram API\n    serviceCategory: API\n  - name: Facebook Insights API\n    baseURL: https://graph.facebook.com/v25.0\n    tags:\n      - Analytics\n      - Insights\n      - Metrics\n      - Reporting\n    serviceName: Facebook Insights API\n    serviceCategory: API\n  - name: Facebook Messenger Platform API\n    baseURL: https://graph.facebook.com/v25.0\n    tags:\n      - Bots\n      - Chat\n      - Customer Service\n      - Messaging\n   \
  \ serviceName: Facebook Messenger Platform API\n    serviceCategory: API\n  - name: Facebook Catalog API\n    baseURL: https://graph.facebook.com/v25.0\n    tags:\n      - Catalogs\n      - Commerce\n      - Products\n      - Shopping\n    serviceName: Facebook Catalog API\n    serviceCategory: API\n  - name: Facebook Live Video API\n    baseURL: https://graph.facebook.com/v25.0\n    tags:\n      - Broadcasting\n      - Live Streaming\n      - Media\n      - Video\n    serviceName: Facebook Live Video API\n    serviceCategory: API\n  - name: Facebook Threads API\n    baseURL: https://graph.threads.net/v25.0\n    tags:\n      - Content\n      - Publishing\n      - Social Media\n      - Threads\n    serviceName: Facebook Threads API\n    serviceCategory: API\n  - name: Facebook WhatsApp Business Platform API\n    baseURL: https://graph.facebook.com/v25.0\n    tags:\n      - Customer Service\n      - Messaging\n      - Notifications\n      - WhatsApp\n    serviceName: Facebook WhatsApp Business\
  \ Platform API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/facebook-business-manager/refs/heads/main/finops/facebook-business-manager-finops.yml
sources: []
specification: FinOps Framework
tags:
- Advertising
- Analytics
- Business Management
- Marketing
- Social Media
- FinOps
- Cost Management
- FOCUS
---
