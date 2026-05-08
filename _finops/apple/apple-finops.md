---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: app-store-connect-openapi-specification.zip
  format: yaml
  label: App Store Connect API
  slug: ''
  spec_type: OpenAPI
  url: https://developer.apple.com/sample-code/app-store-connect/app-store-connect-openapi-specification.zip
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
description: FinOps framework definition for the Apple API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Apple
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Apple
  PublisherName: Apple
  ServiceCategory: Developer Tools / API
  ServiceName: Apple
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
name: Apple Finops
provider_name: Apple
provider_slug: apple
publisher_name: Apple
service_category: API
slug: apple-finops
source_filename: apple-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Apple\nproviderId: apple\npublisherName: Apple\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Developer\n  - iOS\n  - macOS\n  - Mobile\n  - Technology\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Apple API surface. Provides a FOCUS-aligned mapping for\n  cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment,\
  \ application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      -\
  \ FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Apple\n  ServiceCategory: Developer Tools / API\n  ProviderName: Apple\n  PublisherName: Apple\n  InvoiceIssuerName: Apple\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n\
  \      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Apple Music API\n    baseURL: https://api.music.apple.com/v1\n    tags:\n      - Media\n      - Music\n      - Streaming\n    serviceName: Apple Music API\n    serviceCategory: API\n  - name: WeatherKit REST API\n    baseURL: https://weatherkit.apple.com/api/v1\n    tags:\n      - Data\n      - Forecast\n      - Weather\n    serviceName: WeatherKit REST API\n    serviceCategory: API\n  - name: App Store Connect API\n    baseURL: https://api.appstoreconnect.apple.com/v1\n    tags:\n      - Analytics\n      - App Store\n      - Publishing\n    serviceName: App Store Connect API\n    serviceCategory: API\n  - name: MapKit JS\n    baseURL: https://cdn.apple-mapkit.com/mk/5.x.x/mapkit.js\n    tags:\n      - Javascript\n      - Location\n      - Maps\n\
  \    serviceName: MapKit JS\n    serviceCategory: API\n  - name: Sign in with Apple REST API\n    baseURL: https://appleid.apple.com/auth\n    tags:\n      - Authentication\n      - Identity\n      - OAuth\n    serviceName: Sign in with Apple REST API\n    serviceCategory: API\n  - name: Apple Push Notification Service (APNs)\n    baseURL: https://api.push.apple.com\n    tags:\n      - Messaging\n      - Notifications\n      - Push\n    serviceName: Apple Push Notification Service (APNs)\n    serviceCategory: API\n  - name: App Store Server API\n    baseURL: https://api.storekit.itunes.apple.com\n    tags:\n      - In-App Purchases\n      - Subscriptions\n      - Transactions\n    serviceName: App Store Server API\n    serviceCategory: API\n  - name: App Store Server Notifications V2\n    baseURL: ''\n    tags:\n      - In-App Purchases\n      - Subscriptions\n      - Webhooks\n    serviceName: App Store Server Notifications V2\n    serviceCategory: API\n  - name: Apple Maps Server API\n\
  \    baseURL: https://maps-api.apple.com\n    tags:\n      - Geocoding\n      - Location\n      - Maps\n      - Search\n    serviceName: Apple Maps Server API\n    serviceCategory: API\n  - name: Apple News API\n    baseURL: ''\n    tags:\n      - Content\n      - News\n      - Publishing\n    serviceName: Apple News API\n    serviceCategory: API\n  - name: DeviceCheck API\n    baseURL: https://api.devicecheck.apple.com\n    tags:\n      - Device\n      - Fraud Prevention\n      - Security\n    serviceName: DeviceCheck API\n    serviceCategory: API\n  - name: Apple Ads Campaign Management API\n    baseURL: https://api.searchads.apple.com\n    tags:\n      - Advertising\n      - Campaigns\n      - Search Ads\n    serviceName: Apple Ads Campaign Management API\n    serviceCategory: API\n  - name: Wallet Passes Web Service\n    baseURL: ''\n    tags:\n      - Passes\n      - Payments\n      - Wallet\n    serviceName: Wallet Passes Web Service\n    serviceCategory: API\n  - name: Enterprise\
  \ Program API\n    baseURL: ''\n    tags:\n      - Certificates\n      - Enterprise\n      - Provisioning\n    serviceName: Enterprise Program API\n    serviceCategory: API\n  - name: Apple School and Business Manager API\n    baseURL: ''\n    tags:\n      - Device Management\n      - Education\n      - Enrollment\n      - Enterprise\n    serviceName: Apple School and Business Manager API\n    serviceCategory: API\n  - name: Apple Pay on the Web\n    baseURL: ''\n    tags:\n      - Apple Pay\n      - Payments\n      - Web\n    serviceName: Apple Pay on the Web\n    serviceCategory: API\n  - name: Wallet Orders\n    baseURL: ''\n    tags:\n      - Orders\n      - Tracking\n      - Wallet\n    serviceName: Wallet Orders\n    serviceCategory: API\n  - name: ClassKit Catalog API\n    baseURL: https://classkit-catalog.apple.com\n    tags:\n      - ClassKit\n      - Education\n      - Schoolwork\n    serviceName: ClassKit Catalog API\n    serviceCategory: API\n  - name: Apple Music Feed API\n\
  \    baseURL: ''\n    tags:\n      - Catalog\n      - Feed\n      - Music\n    serviceName: Apple Music Feed API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - name: Apple Developer Relations\n    email: developer@apple.com\n    url: https://developer.apple.com/contact/\n  - name: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/apple/refs/heads/main/finops/apple-finops.yml
sources: []
specification: FinOps Framework
tags:
- Developer
- iOS
- macOS
- Mobile
- Technology
- FinOps
- Cost Management
- FOCUS
---
