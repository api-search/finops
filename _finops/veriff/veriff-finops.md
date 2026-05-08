---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: veriff-openapi.yml
  format: yaml
  label: Veriff Sessions API
  slug: sessions
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/veriff/refs/heads/main/openapi/veriff-openapi.yml
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
description: FinOps framework definition for the Veriff API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Veriff
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Veriff
  PublisherName: Veriff
  ServiceCategory: Developer Tools / API
  ServiceName: Veriff
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
name: Veriff Finops
provider_name: Veriff
provider_slug: veriff
publisher_name: Veriff
service_category: API
slug: veriff-finops
source_filename: veriff-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Veriff\nproviderId: veriff\npublisherName: Veriff\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - KYC\n  - Identity Verification\n  - Biometrics\n  - Fraud Prevention\n  - AML\n  - SaaS\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Veriff API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with\
  \ the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps\
  \ Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Veriff\n  ServiceCategory: Developer Tools / API\n  ProviderName: Veriff\n  PublisherName: Veriff\n  InvoiceIssuerName: Veriff\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n\
  \      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Veriff Sessions API\n    baseURL: https://stationapi.veriff.com/v1\n    tags:\n      - Sessions\n      - Verification\n      - Onboarding\n    serviceName: Veriff Sessions API\n    serviceCategory: API\n  - name: Veriff Media API\n    baseURL: https://stationapi.veriff.com/v1\n    tags:\n      - Media\n      - Uploads\n      - Documents\n    serviceName: Veriff Media API\n    serviceCategory: API\n  - name: Veriff Decisions API\n    baseURL: https://stationapi.veriff.com/v1\n    tags:\n      - Decisions\n      - Verification Results\n    serviceName: Veriff Decisions API\n    serviceCategory: API\n  - name: Veriff Attempts API\n    baseURL: https://stationapi.veriff.com/v1\n    tags:\n      - Attempts\n      - Resubmission\n\
  \    serviceName: Veriff Attempts API\n    serviceCategory: API\n  - name: Veriff Persons API\n    baseURL: https://stationapi.veriff.com/v1\n    tags:\n      - Persons\n      - Identity Data\n    serviceName: Veriff Persons API\n    serviceCategory: API\n  - name: Veriff Watchlist Screening API\n    baseURL: https://stationapi.veriff.com/v1\n    tags:\n      - AML\n      - Sanctions\n      - PEP\n      - Watchlist\n    serviceName: Veriff Watchlist Screening API\n    serviceCategory: API\n  - name: Veriff Webhook Delivery\n    baseURL: customer-configured\n    tags:\n      - Webhooks\n      - Events\n      - HMAC\n    serviceName: Veriff Webhook Delivery\n    serviceCategory: API\n  - name: Veriff Web (InContext / Hosted) SDK\n    baseURL: https://github.com/Veriff\n    tags:\n      - Web SDK\n      - JavaScript\n      - Capture\n    serviceName: Veriff Web (InContext / Hosted) SDK\n    serviceCategory: API\n  - name: Veriff iOS SDK\n    baseURL: https://github.com/Veriff/veriff-ios\n\
  \    tags:\n      - iOS SDK\n      - Mobile\n      - Capture\n    serviceName: Veriff iOS SDK\n    serviceCategory: API\n  - name: Veriff Android SDK\n    baseURL: https://github.com/Veriff/veriff-android\n    tags:\n      - Android SDK\n      - Mobile\n      - Capture\n    serviceName: Veriff Android SDK\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/veriff/refs/heads/main/finops/veriff-finops.yml
sources: []
specification: FinOps Framework
tags:
- KYC
- Identity Verification
- Biometrics
- Fraud Prevention
- AML
- SaaS
- FinOps
- Cost Management
- FOCUS
---
