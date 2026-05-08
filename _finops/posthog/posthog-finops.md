---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: posthog-openapi.yml
  format: yaml
  label: PostHog API
  slug: posthog
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/posthog/refs/heads/main/openapi/posthog-openapi.yml
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
description: FinOps framework definition for the PostHog API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: PostHog
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: PostHog
  PublisherName: PostHog
  ServiceCategory: Developer Tools / API
  ServiceName: PostHog
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
name: Posthog Finops
provider_name: PostHog
provider_slug: posthog
publisher_name: PostHog
service_category: API
slug: posthog-finops
source_filename: posthog-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: PostHog\nproviderId: posthog\npublisherName: PostHog\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - A/B Testing\n  - Analytics\n  - Feature Flags\n  - Open Source\n  - Product Analytics\n  - Session Recording\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the PostHog API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every\
  \ chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n   \
  \ capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: PostHog\n  ServiceCategory: Developer Tools / API\n  ProviderName: PostHog\n  PublisherName: PostHog\n  InvoiceIssuerName: PostHog\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit:\
  \ GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: PostHog API\n    baseURL: https://app.posthog.com/api\n    tags:\n      - Analytics\n      - Annotations\n      - Cohorts\n      - Dashboards\n      - Events\n      - Experimentation\n      - Feature Flags\n      - HogQL\n      - Insights\n      - Persons\n      - Product Analytics\n      - Surveys\n    serviceName: PostHog API\n    serviceCategory: API\n  - name: PostHog Capture API\n    baseURL: ''\n    tags:\n      - Analytics\n      - Events\n      - Ingestion\n      - Tracking\n    serviceName: PostHog Capture API\n    serviceCategory: API\n  - name: PostHog Query API\n    baseURL: ''\n    tags:\n      - Analytics\n      - HogQL\n      - Queries\n      - Reporting\n  \
  \  serviceName: PostHog Query API\n    serviceCategory: API\n  - name: PostHog Persons API\n    baseURL: ''\n    tags:\n      - Analytics\n      - Identity\n      - Profiles\n      - Users\n    serviceName: PostHog Persons API\n    serviceCategory: API\n  - name: PostHog Feature Flags API\n    baseURL: ''\n    tags:\n      - A/B Testing\n      - Experimentation\n      - Feature Flags\n      - Rollouts\n    serviceName: PostHog Feature Flags API\n    serviceCategory: API\n  - name: PostHog Experiments API\n    baseURL: ''\n    tags:\n      - A/B Testing\n      - Experimentation\n      - Metrics\n      - Variants\n    serviceName: PostHog Experiments API\n    serviceCategory: API\n  - name: PostHog Insights API\n    baseURL: ''\n    tags:\n      - Analytics\n      - Dashboards\n      - Insights\n      - Reporting\n    serviceName: PostHog Insights API\n    serviceCategory: API\n  - name: PostHog Cohorts API\n    baseURL: ''\n    tags:\n      - Analytics\n      - Cohorts\n      - Segmentation\n\
  \      - Users\n    serviceName: PostHog Cohorts API\n    serviceCategory: API\n  - name: PostHog Annotations API\n    baseURL: ''\n    tags:\n      - Analytics\n      - Annotations\n      - Charts\n    serviceName: PostHog Annotations API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/posthog/refs/heads/main/finops/posthog-finops.yml
sources: []
specification: FinOps Framework
tags:
- A/B Testing
- Analytics
- Feature Flags
- Open Source
- Product Analytics
- Session Recording
- FinOps
- Cost Management
- FOCUS
---
