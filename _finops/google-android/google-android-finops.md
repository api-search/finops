---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: rest
  format: yaml
  label: Android Management API
  slug: android-management-api
  spec_type: OpenAPI
  url: https://androidmanagement.googleapis.com/$discovery/rest?version=v1
- filename: rest
  format: yaml
  label: Google Play Developer API
  slug: google-play-developer-api
  spec_type: OpenAPI
  url: https://androidpublisher.googleapis.com/$discovery/rest?version=v3
- filename: rest
  format: yaml
  label: Firebase Cloud Messaging API
  slug: firebase-cloud-messaging-api
  spec_type: OpenAPI
  url: https://fcm.googleapis.com/$discovery/rest?version=v1
- filename: rest
  format: yaml
  label: Google Play Games Services API
  slug: google-play-games-services-api
  spec_type: OpenAPI
  url: https://www.googleapis.com/discovery/v1/apis/games/v1/rest
- filename: rest
  format: yaml
  label: Android Over the Air API
  slug: android-over-the-air-api
  spec_type: OpenAPI
  url: https://androidovertheair.googleapis.com/$discovery/rest?version=v1
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
description: FinOps framework definition for the Google Android API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Google Android
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Google Android
  PublisherName: Google Android
  ServiceCategory: Developer Tools / API
  ServiceName: Google Android
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
name: Google Android Finops
provider_name: Google Android
provider_slug: google-android
publisher_name: Google Android
service_category: API
slug: google-android-finops
source_filename: google-android-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Google Android\nproviderId: google-android\npublisherName: Google Android\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Android\n  - Google\n  - Mobile Development\n  - Mobile Operating System\n  - Open Source\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Google Android API surface. Provides a FOCUS-aligned\n  mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description:\
  \ Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n\
  \    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Google Android\n  ServiceCategory: Developer Tools / API\n  ProviderName: Google Android\n  PublisherName: Google Android\n  InvoiceIssuerName: Google Android\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network\
  \ in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Android Management API\n    baseURL: https://androidmanagement.googleapis.com\n    tags:\n      - Device Management\n      - Enterprise\n      - MDM\n      - Policies\n    serviceName: Android Management API\n    serviceCategory: API\n  - name: Google Play Developer API\n    baseURL: https://androidpublisher.googleapis.com\n    tags:\n      - In-App Purchases\n      - Play Store\n      - Publishing\n      - Subscriptions\n    serviceName: Google Play Developer API\n    serviceCategory: API\n  - name: Firebase Cloud Messaging API\n    baseURL: https://fcm.googleapis.com\n    tags:\n      - Cloud Messaging\n      - Firebase\n      - Messaging\n   \
  \   - Push Notifications\n    serviceName: Firebase Cloud Messaging API\n    serviceCategory: API\n  - name: Google Play Games Services API\n    baseURL: https://www.googleapis.com/games/v1\n    tags:\n      - Achievements\n      - Gaming\n      - Leaderboards\n      - Multiplayer\n    serviceName: Google Play Games Services API\n    serviceCategory: API\n  - name: Android Device Provisioning Partner API\n    baseURL: https://androiddeviceprovisioning.googleapis.com\n    tags:\n      - Device Provisioning\n      - Enterprise\n      - Reseller\n      - Zero-Touch Enrollment\n    serviceName: Android Device Provisioning Partner API\n    serviceCategory: API\n  - name: Android Over the Air API\n    baseURL: https://androidovertheair.googleapis.com\n    tags:\n      - Device Updates\n      - Firmware\n      - OTA Updates\n      - System Updates\n    serviceName: Android Over the Air API\n    serviceCategory: API\n  - name: Google Play EMM API\n    baseURL: https://androidenterprise.googleapis.com\n\
  \    tags:\n      - App Management\n      - EMM\n      - Enterprise\n      - Enterprise Mobility\n    serviceName: Google Play EMM API\n    serviceCategory: API\n  - name: Play Integrity API\n    baseURL: https://playintegrity.googleapis.com\n    tags:\n      - App Verification\n      - Fraud Prevention\n      - Integrity\n      - Security\n    serviceName: Play Integrity API\n    serviceCategory: API\n  - name: Cloud Testing API\n    baseURL: https://testing.googleapis.com\n    tags:\n      - Firebase\n      - Quality Assurance\n      - Test Lab\n      - Testing\n    serviceName: Cloud Testing API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/google-android/refs/heads/main/finops/google-android-finops.yml
sources: []
specification: FinOps Framework
tags:
- Android
- Google
- Mobile Development
- Mobile Operating System
- Open Source
- FinOps
- Cost Management
- FOCUS
---
