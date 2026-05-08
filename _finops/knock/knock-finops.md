---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: knock-openapi.json
  format: json
  label: Knock Workflows API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/knock/refs/heads/main/openapi/knock-openapi.json
- filename: knock-openapi.json
  format: json
  label: Knock Messages API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/knock/refs/heads/main/openapi/knock-openapi.json
- filename: knock-openapi.json
  format: json
  label: Knock Users API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/knock/refs/heads/main/openapi/knock-openapi.json
- filename: knock-openapi.json
  format: json
  label: Knock Objects API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/knock/refs/heads/main/openapi/knock-openapi.json
- filename: knock-openapi.json
  format: json
  label: Knock Feeds API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/knock/refs/heads/main/openapi/knock-openapi.json
- filename: knock-openapi.json
  format: json
  label: Knock Guides API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/knock/refs/heads/main/openapi/knock-openapi.json
- filename: knock-openapi.json
  format: json
  label: Knock Schedules API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/knock/refs/heads/main/openapi/knock-openapi.json
- filename: knock-openapi.json
  format: json
  label: Knock Preferences API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/knock/refs/heads/main/openapi/knock-openapi.json
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
description: FinOps framework definition for the Knock API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Knock
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Knock
  PublisherName: Knock
  ServiceCategory: Developer Tools / API
  ServiceName: Knock
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
name: Knock Finops
provider_name: Knock
provider_slug: knock
publisher_name: Knock
service_category: API
slug: knock-finops
source_filename: knock-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Knock\nproviderId: knock\npublisherName: Knock\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Notifications\n  - Email\n  - SMS\n  - Push\n  - Workflows\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Knock API surface. Provides a FOCUS-aligned mapping for\n  cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment,\
  \ application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      -\
  \ FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Knock\n  ServiceCategory: Developer Tools / API\n  ProviderName: Knock\n  PublisherName: Knock\n  InvoiceIssuerName: Knock\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n\
  \      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Knock Workflows API\n    baseURL: https://api.knock.app/v1\n    tags:\n      - Workflows\n      - Orchestration\n    serviceName: Knock Workflows API\n    serviceCategory: API\n  - name: Knock Messages API\n    baseURL: https://api.knock.app/v1\n    tags:\n      - Messages\n      - Delivery\n    serviceName: Knock Messages API\n    serviceCategory: API\n  - name: Knock Users API\n    baseURL: https://api.knock.app/v1\n    tags:\n      - Users\n      - Recipients\n    serviceName: Knock Users API\n    serviceCategory: API\n  - name: Knock Objects API\n    baseURL: https://api.knock.app/v1\n    tags:\n      - Objects\n    serviceName: Knock Objects API\n    serviceCategory: API\n  - name: Knock Feeds API\n    baseURL: https://api.knock.app/v1\n  \
  \  tags:\n      - Feeds\n      - In-App\n    serviceName: Knock Feeds API\n    serviceCategory: API\n  - name: Knock Guides API\n    baseURL: https://api.knock.app/v1\n    tags:\n      - Guides\n      - Onboarding\n    serviceName: Knock Guides API\n    serviceCategory: API\n  - name: Knock Schedules API\n    baseURL: https://api.knock.app/v1\n    tags:\n      - Schedules\n    serviceName: Knock Schedules API\n    serviceCategory: API\n  - name: Knock Preferences API\n    baseURL: https://api.knock.app/v1\n    tags:\n      - Preferences\n    serviceName: Knock Preferences API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/knock/refs/heads/main/finops/knock-finops.yml
sources: []
specification: FinOps Framework
tags:
- Notifications
- Email
- SMS
- Push
- Workflows
- FinOps
- Cost Management
- FOCUS
---
