---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: courier-openapi.yml
  format: yaml
  label: Courier Send API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/courier/refs/heads/main/openapi/courier-openapi.yml
- filename: courier-openapi.yml
  format: yaml
  label: Courier User Profiles API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/courier/refs/heads/main/openapi/courier-openapi.yml
- filename: courier-openapi.yml
  format: yaml
  label: Courier Lists API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/courier/refs/heads/main/openapi/courier-openapi.yml
- filename: courier-openapi.yml
  format: yaml
  label: Courier Events API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/courier/refs/heads/main/openapi/courier-openapi.yml
- filename: courier-openapi.yml
  format: yaml
  label: Courier Brands API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/courier/refs/heads/main/openapi/courier-openapi.yml
- filename: courier-openapi.yml
  format: yaml
  label: Courier Authentication API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/courier/refs/heads/main/openapi/courier-openapi.yml
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
description: FinOps framework definition for the Courier API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Courier
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Courier
  PublisherName: Courier
  ServiceCategory: Developer Tools / API
  ServiceName: Courier
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
name: Courier Finops
provider_name: Courier
provider_slug: courier
publisher_name: Courier
service_category: API
slug: courier-finops
source_filename: courier-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Courier\nproviderId: courier\npublisherName: Courier\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Notifications\n  - Email\n  - SMS\n  - Push\n  - API\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Courier API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment,\
  \ application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      -\
  \ FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Courier\n  ServiceCategory: Developer Tools / API\n  ProviderName: Courier\n  PublisherName: Courier\n  InvoiceIssuerName: Courier\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n \
  \     - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Courier Send API\n    baseURL: https://api.courier.com\n    tags:\n      - Send\n      - Multi-Channel\n    serviceName: Courier Send API\n    serviceCategory: API\n  - name: Courier User Profiles API\n    baseURL: https://api.courier.com\n    tags:\n      - Users\n      - Profiles\n    serviceName: Courier User Profiles API\n    serviceCategory: API\n  - name: Courier Lists API\n    baseURL: https://api.courier.com\n    tags:\n      - Lists\n      - Subscriptions\n    serviceName: Courier Lists API\n    serviceCategory: API\n  - name: Courier Events API\n    baseURL: https://api.courier.com\n    tags:\n      - Events\n    serviceName: Courier Events API\n    serviceCategory: API\n  - name: Courier Brands API\n    baseURL: https://api.courier.com\n\
  \    tags:\n      - Brands\n      - Branding\n    serviceName: Courier Brands API\n    serviceCategory: API\n  - name: Courier Authentication API\n    baseURL: https://api.courier.com\n    tags:\n      - Authentication\n      - JWT\n    serviceName: Courier Authentication API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/courier/refs/heads/main/finops/courier-finops.yml
sources: []
specification: FinOps Framework
tags:
- Notifications
- Email
- SMS
- Push
- API
- FinOps
- Cost Management
- FOCUS
---
