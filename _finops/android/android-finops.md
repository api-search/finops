---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: google-play-developer-api.yml
  format: yaml
  label: Google Play Developer APIs
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/android/refs/heads/main/openapi/google-play-developer-api.yml
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
description: FinOps framework definition for the Android API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Android
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Android
  PublisherName: Android
  ServiceCategory: Developer Tools / API
  ServiceName: Android
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
name: Android Finops
provider_name: Android
provider_slug: android
publisher_name: Android
service_category: API
slug: android-finops
source_filename: android-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Android\nproviderId: android\npublisherName: Android\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - AI\n  - Android\n  - Automotive\n  - Google\n  - Machine Learning\n  - Mobile Development\n  - SDK\n  - TV\n  - Wearables\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Android API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description:\
  \ Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n\
  \    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Android\n  ServiceCategory: Developer Tools / API\n  ProviderName: Android\n  PublisherName: Android\n  InvoiceIssuerName: Android\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit:\
  \ GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Android Platform APIs\n    baseURL: https://developer.android.com\n    tags:\n      - Android\n      - Framework\n      - Mobile\n      - SDK\n    serviceName: Android Platform APIs\n    serviceCategory: API\n  - name: Google Play Services APIs\n    baseURL: https://developers.google.com/android\n    tags:\n      - Authentication\n      - Google Play\n      - Location\n      - Maps\n    serviceName: Google Play Services APIs\n    serviceCategory: API\n  - name: Firebase Android APIs\n    baseURL: https://firebase.google.com\n    tags:\n      - Analytics\n      - Authentication\n      - Backend\n      - Cloud Messaging\n      - Database\n      - Firebase\n    serviceName: Firebase\
  \ Android APIs\n    serviceCategory: API\n  - name: Google Maps Android API\n    baseURL: https://maps.googleapis.com\n    tags:\n      - Geolocation\n      - Location\n      - Maps\n      - Navigation\n    serviceName: Google Maps Android API\n    serviceCategory: API\n  - name: Android Jetpack APIs\n    baseURL: https://developer.android.com/jetpack\n    tags:\n      - Architecture\n      - Compose\n      - Jetpack\n      - Libraries\n      - UI\n    serviceName: Android Jetpack APIs\n    serviceCategory: API\n  - name: Google Play Console API\n    baseURL: https://androidpublisher.googleapis.com\n    tags:\n      - Analytics\n      - Distribution\n      - Publishing\n      - REST API\n    serviceName: Google Play Console API\n    serviceCategory: API\n  - name: Google Play Billing API\n    baseURL: https://developer.android.com/google/play/billing\n    tags:\n      - Billing\n      - In-App Purchases\n      - Monetization\n      - Subscriptions\n    serviceName: Google Play Billing\
  \ API\n    serviceCategory: API\n  - name: Android NDK APIs\n    baseURL: https://developer.android.com/ndk\n    tags:\n      - C++\n      - Native\n      - NDK\n      - OpenGL\n      - Performance\n      - Vulkan\n    serviceName: Android NDK APIs\n    serviceCategory: API\n  - name: Google ML Kit Android APIs\n    baseURL: https://developers.google.com/ml-kit\n    tags:\n      - Barcode Scanning\n      - Face Detection\n      - Machine Learning\n      - ML Kit\n      - On-Device\n      - Text Recognition\n      - Vision\n    serviceName: Google ML Kit Android APIs\n    serviceCategory: API\n  - name: Android Health Connect API\n    baseURL: https://developer.android.com/health-and-fitness\n    tags:\n      - Data Sharing\n      - Fitness\n      - Health\n      - Privacy\n      - Wearables\n    serviceName: Android Health Connect API\n    serviceCategory: API\n  - name: Android CameraX API\n    baseURL: https://developer.android.com/media/camera\n    tags:\n      - Camera\n      - Image\
  \ Capture\n      - Jetpack\n      - Media\n      - Video\n    serviceName: Android CameraX API\n    serviceCategory: API\n  - name: Wear OS APIs\n    baseURL: https://developer.android.com/wear\n    tags:\n      - Smartwatch\n      - Tiles\n      - Watch Face\n      - Wear OS\n      - Wearables\n    serviceName: Wear OS APIs\n    serviceCategory: API\n  - name: Android for Cars APIs\n    baseURL: https://developer.android.com/cars\n    tags:\n      - Android Auto\n      - Automotive\n      - Cars\n      - Media\n      - Navigation\n    serviceName: Android for Cars APIs\n    serviceCategory: API\n  - name: Google AdMob Android API\n    baseURL: https://developers.google.com/admob\n    tags:\n      - AdMob\n      - Ads\n      - Advertising\n      - Banner\n      - Interstitial\n      - Monetization\n    serviceName: Google AdMob Android API\n    serviceCategory: API\n  - name: Android Accessibility APIs\n    baseURL: https://developer.android.com\n    tags:\n      - A11y\n      - Accessibility\n\
  \      - Assistive Technology\n      - Screen Reader\n    serviceName: Android Accessibility APIs\n    serviceCategory: API\n  - name: Android TV APIs\n    baseURL: https://developer.android.com/tv\n    tags:\n      - Android TV\n      - Leanback\n      - Living Room\n      - Media\n      - Television\n    serviceName: Android TV APIs\n    serviceCategory: API\n  - name: Google Play Integrity API\n    baseURL: https://developer.android.com/google/play/integrity\n    tags:\n      - Anti-Fraud\n      - Device Attestation\n      - Integrity\n      - Security\n      - Verification\n    serviceName: Google Play Integrity API\n    serviceCategory: API\n  - name: Android Credential Manager API\n    baseURL: https://developer.android.com/identity\n    tags:\n      - Authentication\n      - Credentials\n      - Identity\n      - Passkeys\n      - Security\n      - Sign-In\n    serviceName: Android Credential Manager API\n    serviceCategory: API\n  - name: Gemini Nano On-Device AI API\n    baseURL:\
  \ https://developer.android.com/ai\n    tags:\n      - AI\n      - Gemini Nano\n      - Generative AI\n      - LLM\n      - Machine Learning\n      - On-Device\n    serviceName: Gemini Nano On-Device AI API\n    serviceCategory: API\n  - name: Google Play Developer APIs\n    baseURL: https://androidpublisher.googleapis.com\n    tags:\n      - App Management\n      - Google Play\n      - Publishing\n      - Purchases\n      - Reporting\n      - REST API\n      - Reviews\n      - Subscriptions\n    serviceName: Google Play Developer APIs\n    serviceCategory: API\n  - name: Gemini Developer API for Android\n    baseURL: https://developer.android.com/ai\n    tags:\n      - AI\n      - Cloud\n      - Gemini\n      - Generative AI\n      - LLM\n    serviceName: Gemini Developer API for Android\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost\
  \ / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n    url: https://apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/android/refs/heads/main/finops/android-finops.yml
sources: []
specification: FinOps Framework
tags:
- AI
- Android
- Automotive
- Google
- Machine Learning
- Mobile Development
- SDK
- TV
- Wearables
- FinOps
- Cost Management
- FOCUS
---
