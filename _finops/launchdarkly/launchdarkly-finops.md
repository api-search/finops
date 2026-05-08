---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: launchdarkly-rest-api-openapi.yml
  format: yaml
  label: LaunchDarkly REST API
  slug: rest-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/launchdarkly/refs/heads/main/openapi/launchdarkly-rest-api-openapi.yml
- filename: launchdarkly-webhooks-asyncapi.yml
  format: yaml
  label: LaunchDarkly Webhooks API
  slug: webhooks-api
  spec_type: AsyncAPI
  url: https://raw.githubusercontent.com/api-evangelist/launchdarkly/refs/heads/main/asyncapi/launchdarkly-webhooks-asyncapi.yml
- filename: launchdarkly-relay-proxy-openapi.yml
  format: yaml
  label: LaunchDarkly Relay Proxy
  slug: relay-proxy
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/launchdarkly/refs/heads/main/openapi/launchdarkly-relay-proxy-openapi.yml
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
description: FinOps framework definition for the launchdarkly API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: launchdarkly
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: launchdarkly
  PublisherName: launchdarkly
  ServiceCategory: Developer Tools / API
  ServiceName: launchdarkly
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
name: Launchdarkly Finops
provider_name: launchdarkly
provider_slug: launchdarkly
publisher_name: launchdarkly
service_category: API
slug: launchdarkly-finops
source_filename: launchdarkly-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: launchdarkly\nproviderId: launchdarkly\npublisherName: launchdarkly\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the launchdarkly API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so\
  \ cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n\
  \      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: launchdarkly\n  ServiceCategory: Developer Tools / API\n  ProviderName: launchdarkly\n  PublisherName: launchdarkly\n  InvoiceIssuerName: launchdarkly\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n\
  \      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: LaunchDarkly REST API\n    baseURL: https://app.launchdarkly.com/api/v2\n    tags:\n      - Environments\n      - Experimentation\n      - Feature Flags\n      - Feature Management\n      - Segments\n      - Toggles\n    serviceName: LaunchDarkly REST API\n    serviceCategory: API\n  - name: LaunchDarkly Webhooks API\n    baseURL: https://app.launchdarkly.com/api/v2\n    tags:\n      - Events\n      - Integrations\n      - Notifications\n      - Webhooks\n    serviceName: LaunchDarkly Webhooks API\n    serviceCategory: API\n  - name: LaunchDarkly Relay Proxy\n    baseURL: https://api.example.com\n    tags:\n      - Edge\n      - Infrastructure\n      - Performance\n      - Proxy\n      - Streaming\n    serviceName: LaunchDarkly Relay Proxy\n   \
  \ serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers: []\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/launchdarkly/refs/heads/main/finops/launchdarkly-finops.yml
sources: []
specification: FinOps Framework
tags:
- FinOps
- Cost Management
- FOCUS
---
