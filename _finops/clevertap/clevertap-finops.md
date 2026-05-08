---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
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
description: FinOps framework definition for the CleverTap API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: CleverTap
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: CleverTap
  PublisherName: CleverTap
  ServiceCategory: Developer Tools / API
  ServiceName: CleverTap
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
name: Clevertap Finops
provider_name: CleverTap
provider_slug: clevertap
publisher_name: CleverTap
service_category: API
slug: clevertap-finops
source_filename: clevertap-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: CleverTap\nproviderId: clevertap\npublisherName: CleverTap\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Audiences\n  - Customer Engagement\n  - Customer Retention\n  - Marketing Automation\n  - Mobile Engagement\n  - Push Notifications\n  - User Behavior\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the CleverTap API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n\
  \  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and\
  \ SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: CleverTap\n  ServiceCategory: Developer Tools / API\n  ProviderName: CleverTap\n  PublisherName: CleverTap\n  InvoiceIssuerName: CleverTap\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes\
  \ returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: CleverTap Profile API\n    baseURL: ''\n    tags:\n      - Profiles\n      - User Data\n    serviceName: CleverTap Profile API\n    serviceCategory: API\n  - name: CleverTap Event API\n    baseURL: ''\n    tags:\n      - Events\n      - Tracking\n    serviceName: CleverTap Event API\n    serviceCategory: API\n  - name: CleverTap Campaign API\n    baseURL: ''\n    tags:\n      - Campaigns\n      - Messaging\n    serviceName: CleverTap Campaign API\n    serviceCategory: API\n  - name: CleverTap Bulletins API\n    baseURL: ''\n    tags:\n      - Bulletins\n      - Triggers\n    serviceName: CleverTap Bulletins API\n    serviceCategory:\
  \ API\n  - name: CleverTap Catalog API\n    baseURL: ''\n    tags:\n      - Catalog\n      - Product Data\n    serviceName: CleverTap Catalog API\n    serviceCategory: API\n  - name: CleverTap Custom List API\n    baseURL: ''\n    tags:\n      - Audiences\n      - Lists\n    serviceName: CleverTap Custom List API\n    serviceCategory: API\n  - name: CleverTap Remote Config API\n    baseURL: ''\n    tags:\n      - Feature Flags\n      - Remote Config\n    serviceName: CleverTap Remote Config API\n    serviceCategory: API\n  - name: CleverTap Real-Time Counts API\n    baseURL: ''\n    tags:\n      - Analytics\n      - Counts\n    serviceName: CleverTap Real-Time Counts API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kinlane@gmail.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/clevertap/refs/heads/main/finops/clevertap-finops.yml
sources: []
specification: FinOps Framework
tags:
- Audiences
- Customer Engagement
- Customer Retention
- Marketing Automation
- Mobile Engagement
- Push Notifications
- User Behavior
- FinOps
- Cost Management
- FOCUS
---
