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
  slug: google-play-developer-apis
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/android/refs/heads/main/openapi/google-play-developer-api.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  - Tax
  - Adjustment
  - Refund
  - Credit
  pricingCategory: Take Rate + Pay-As-You-Go + Subscription
description: FOCUS-aligned FinOps for the Android ecosystem. The platform mixes free on-device SDKs with three monetized surfaces — Google Play (take rate on paid apps / IAP / subscriptions plus a one-time $25 developer registration), Google Maps Platform (per-1000-call usage charges with a 10K monthly free allowance), and Firebase / Google Cloud (pay-as-you-go on Cloud Storage, Firestore, RTDB, etc.). AdMob runs in the opposite direction as a publisher revenue share. All Android-related Google charges flow through Google Cloud / Google Play billing accounts and are visible in Cloud Billing exports (BigQuery), Play Console financial reports, and Firebase usage tabs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Google LLC (region-specific Google entity)
  ProviderName: Google
  PublisherName: Google LLC
  ServiceCategory: Mobile Development Platform
  ServiceName: Android Platform (Google Play, Maps, Firebase, AdMob)
layout: finops
meters:
- aggregation: count
  description: One-time $25 developer account fee
  dimensions:
  - account
  name: play_developer_registration
  unit: account
- aggregation: sum
  description: Gross revenue from paid app downloads and in-app purchases sold via Google Play Billing
  dimensions:
  - app
  - country
  - revenue_tier
  name: play_paid_app_revenue
  unit: USD
- aggregation: sum
  description: Service fee retained by Google (15% on first $1M, 30% above; 15% on subscriptions)
  dimensions:
  - app
  - country
  - fee_tier
  name: play_service_fee
  unit: USD
- aggregation: sum
  description: Auto-renewing subscription revenue
  dimensions:
  - app
  - product_id
  - country
  name: play_subscription_revenue
  unit: USD
- aggregation: sum
  description: Billable Google Maps Platform calls beyond the 10K monthly free events
  dimensions:
  - product
  - api_key
  - country
  name: maps_api_calls
  unit: request
- aggregation: max
  description: GB stored across Firebase Cloud Storage / RTDB / Firestore
  dimensions:
  - service
  - region
  - project
  name: firebase_storage_gb
  unit: GB-month
- aggregation: sum
  description: GB downloaded / egressed from Firebase services
  dimensions:
  - service
  - region
  - project
  name: firebase_egress_gb
  unit: GB
- aggregation: sum
  description: Firestore document operations beyond the Spark allowance
  dimensions:
  - operation_type
  - region
  - project
  name: firestore_reads_writes
  unit: operation
- aggregation: max
  description: Authentication monthly active users beyond the Spark 50K cap
  dimensions:
  - project
  - region
  name: auth_mau
  unit: user
- aggregation: sum
  description: Ad revenue paid out to the publisher (negative cost / inflow)
  dimensions:
  - app
  - ad_unit
  - country
  - format
  name: admob_ad_revenue
  unit: USD
- aggregation: sum
  description: Calls against the Google Play Developer API (informational; not directly billed)
  dimensions:
  - bucket
  - project
  name: play_developer_api_quota
  unit: request
name: Android Finops
provider_name: Android
provider_slug: android
publisher_name: Google LLC
service_category: Mobile Development Platform
slug: android-finops
source_filename: android-finops.yml
source_heading: FinOps Profile
source_url: https://support.google.com/googleplay/android-developer/answer/112622
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Android\nproviderId: android\npublisherName: Google LLC\nserviceCategory: Mobile Development Platform\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Android\n  - Google Play\n  - Maps\n  - Firebase\n  - AdMob\ndescription: >-\n  FOCUS-aligned FinOps for the Android ecosystem. The platform mixes free\n  on-device SDKs with three monetized surfaces — Google Play (take rate on\n  paid apps / IAP / subscriptions plus a one-time $25 developer registration),\n  Google Maps Platform (per-1000-call usage charges with a 10K monthly free\n  allowance), and Firebase / Google Cloud (pay-as-you-go on Cloud\
  \ Storage,\n  Firestore, RTDB, etc.). AdMob runs in the opposite direction as a publisher\n  revenue share. All Android-related Google charges flow through Google Cloud\n  / Google Play billing accounts and are visible in Cloud Billing exports\n  (BigQuery), Play Console financial reports, and Firebase usage tabs.\nsources:\n  - https://support.google.com/googleplay/android-developer/answer/112622\n  - https://developers.google.com/maps/billing-and-pricing/pricing\n  - https://firebase.google.com/pricing\n  - https://cloud.google.com/billing/docs/how-to/export-data-bigquery\nbillingModel:\n  pricingCategory: Take Rate + Pay-As-You-Go + Subscription\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Adjustment\n    - Refund\n    - Credit\nfocusColumns:\n  ServiceName: Android Platform (Google Play, Maps, Firebase, AdMob)\n  ServiceCategory: Mobile Development Platform\n  ProviderName: Google\n  PublisherName: Google LLC\n\
  \  InvoiceIssuerName: Google LLC (region-specific Google entity)\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: play_developer_registration\n    description: One-time $25 developer account fee\n    unit: account\n    aggregation: count\n    dimensions:\n      - account\n  - name: play_paid_app_revenue\n    description: Gross revenue from paid app downloads and in-app purchases sold via Google Play Billing\n    unit: USD\n    aggregation: sum\n    dimensions:\n      - app\n      - country\n      - revenue_tier\n  - name: play_service_fee\n    description: Service fee retained by Google (15% on first $1M, 30% above; 15% on subscriptions)\n    unit: USD\n    aggregation: sum\n    dimensions:\n      - app\n      - country\n      - fee_tier\n  - name: play_subscription_revenue\n    description: Auto-renewing subscription revenue\n    unit: USD\n    aggregation: sum\n    dimensions:\n      - app\n      - product_id\n      - country\n  - name: maps_api_calls\n    description:\
  \ Billable Google Maps Platform calls beyond the 10K monthly free events\n    unit: request\n    aggregation: sum\n    dimensions:\n      - product\n      - api_key\n      - country\n  - name: firebase_storage_gb\n    description: GB stored across Firebase Cloud Storage / RTDB / Firestore\n    unit: GB-month\n    aggregation: max\n    dimensions:\n      - service\n      - region\n      - project\n  - name: firebase_egress_gb\n    description: GB downloaded / egressed from Firebase services\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - service\n      - region\n      - project\n  - name: firestore_reads_writes\n    description: Firestore document operations beyond the Spark allowance\n    unit: operation\n    aggregation: sum\n    dimensions:\n      - operation_type\n      - region\n      - project\n  - name: auth_mau\n    description: Authentication monthly active users beyond the Spark 50K cap\n    unit: user\n    aggregation: max\n    dimensions:\n      - project\n   \
  \   - region\n  - name: admob_ad_revenue\n    description: Ad revenue paid out to the publisher (negative cost / inflow)\n    unit: USD\n    aggregation: sum\n    dimensions:\n      - app\n      - ad_unit\n      - country\n      - format\n  - name: play_developer_api_quota\n    description: Calls against the Google Play Developer API (informational; not directly billed)\n    unit: request\n    aggregation: sum\n    dimensions:\n      - bucket\n      - project\nprinciples:\n  - name: Visibility\n    description: >-\n      Combine Cloud Billing BigQuery exports for Firebase / Maps spend, the\n      Google Play Console financial reports for app and IAP earnings, and the\n      AdMob payouts report for ad revenue. Use Google Cloud Console > Billing\n      > Reports for cross-product cost views.\n  - name: Allocation\n    description: >-\n      Tag Google Cloud projects per app or environment (dev / staging / prod);\n      use distinct API keys per app for Maps so per-app spend can be sliced.\n\
  \      Allocate Google Play earnings by package name and country in the Play\n      financial CSV.\n  - name: Optimization\n    description: >-\n      Stay under Maps' 10K monthly free events through caching and request\n      consolidation; right-size Firestore indexes and avoid hot documents to\n      respect the 1 write/sec/document soft limit; keep app revenue in the 15%\n      tier as long as possible by structuring multiple developer accounts only\n      where Google's policy allows; use AdMob mediation to maximize fill at\n      the floor price you set.\n  - name: Accountability\n    description: >-\n      Mobile / app team owns Maps and Firebase budgets per project; finance\n      reconciles Play payouts and AdMob payouts against the Google merchant\n      accounts. Set Cloud Billing budget alerts per project and Play Console\n      payout monitoring per app.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/android/refs/heads/main/finops/android-finops.yml
sources:
- https://support.google.com/googleplay/android-developer/answer/112622
- https://developers.google.com/maps/billing-and-pricing/pricing
- https://firebase.google.com/pricing
- https://cloud.google.com/billing/docs/how-to/export-data-bigquery
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Android
- Google Play
- Maps
- Firebase
- AdMob
---
