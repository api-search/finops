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
description: FinOps framework definition for the Jumio API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Jumio
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Jumio
  PublisherName: Jumio
  ServiceCategory: Developer Tools / API
  ServiceName: Jumio
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
name: Jumio Finops
provider_name: Jumio
provider_slug: jumio
publisher_name: Jumio
service_category: API
slug: jumio-finops
source_filename: jumio-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Jumio\nproviderId: jumio\npublisherName: Jumio\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - KYC\n  - Identity Verification\n  - Biometrics\n  - AML\n  - Fraud Prevention\n  - KYX\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Jumio API surface. Provides a FOCUS-aligned mapping for\n  cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the\
  \ consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps\
  \ Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Jumio\n  ServiceCategory: Developer Tools / API\n  ProviderName: Jumio\n  PublisherName: Jumio\n  InvoiceIssuerName: Jumio\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n\
  \      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Jumio ID Verification API\n    baseURL: https://account.amer-1.jumio.ai\n    tags:\n      - ID Verification\n      - KYC\n      - Onboarding\n    serviceName: Jumio ID Verification API\n    serviceCategory: API\n  - name: Jumio Document Verification API\n    baseURL: https://account.amer-1.jumio.ai\n    tags:\n      - Document Verification\n      - Proof of Address\n    serviceName: Jumio Document Verification API\n    serviceCategory: API\n  - name: Jumio Authentication API\n    baseURL: https://account.amer-1.jumio.ai\n    tags:\n      - Biometrics\n      - Liveness\n      - Authentication\n    serviceName: Jumio Authentication API\n    serviceCategory: API\n  - name: Jumio selfie.DONE API\n    baseURL: https://account.amer-1.jumio.ai\n\
  \    tags:\n      - Reusable Identity\n      - Biometrics\n      - Selfie\n    serviceName: Jumio selfie.DONE API\n    serviceCategory: API\n  - name: Jumio Screening API (AML / Watchlist)\n    baseURL: https://account.amer-1.jumio.ai\n    tags:\n      - AML\n      - Sanctions\n      - PEP\n      - Watchlist\n    serviceName: Jumio Screening API (AML / Watchlist)\n    serviceCategory: API\n  - name: Jumio Risk Signals API\n    baseURL: https://account.amer-1.jumio.ai\n    tags:\n      - Risk\n      - Fraud Prevention\n      - Signals\n    serviceName: Jumio Risk Signals API\n    serviceCategory: API\n  - name: Jumio Retrieval API\n    baseURL: https://retrieval.amer-1.jumio.ai\n    tags:\n      - Retrieval\n      - Compliance\n      - Records\n    serviceName: Jumio Retrieval API\n    serviceCategory: API\n  - name: Jumio Callback / Webhook\n    baseURL: customer-configured\n    tags:\n      - Webhooks\n      - Callbacks\n      - Events\n    serviceName: Jumio Callback / Webhook\n    serviceCategory:\
  \ API\n  - name: Jumio Web SDK\n    baseURL: https://github.com/Jumio/web-sdk\n    tags:\n      - Web SDK\n      - JavaScript\n      - Client\n    serviceName: Jumio Web SDK\n    serviceCategory: API\n  - name: Jumio Mobile SDK (iOS)\n    baseURL: https://github.com/Jumio/mobile-sdk-ios\n    tags:\n      - SDK\n      - iOS\n      - Mobile\n    serviceName: Jumio Mobile SDK (iOS)\n    serviceCategory: API\n  - name: Jumio Mobile SDK (Android)\n    baseURL: https://github.com/Jumio/mobile-sdk-android\n    tags:\n      - SDK\n      - Android\n      - Mobile\n    serviceName: Jumio Mobile SDK (Android)\n    serviceCategory: API\n  - name: Jumio React Native Plugin\n    baseURL: https://github.com/Jumio/mobile-react\n    tags:\n      - SDK\n      - React Native\n      - Mobile\n    serviceName: Jumio React Native Plugin\n    serviceCategory: API\n  - name: Jumio Flutter Plugin\n    baseURL: https://github.com/Jumio/mobile-flutter\n    tags:\n      - SDK\n      - Flutter\n      - Mobile\n  \
  \  serviceName: Jumio Flutter Plugin\n    serviceCategory: API\n  - name: Jumio Cordova Plugin\n    baseURL: https://github.com/Jumio/mobile-cordova\n    tags:\n      - SDK\n      - Cordova\n      - Mobile\n    serviceName: Jumio Cordova Plugin\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/jumio/refs/heads/main/finops/jumio-finops.yml
sources: []
specification: FinOps Framework
tags:
- KYC
- Identity Verification
- Biometrics
- AML
- Fraud Prevention
- KYX
- FinOps
- Cost Management
- FOCUS
---
