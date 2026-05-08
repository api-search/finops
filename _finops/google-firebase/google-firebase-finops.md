---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: firebase-realtime-database-openapi.yml
  format: yaml
  label: Firebase Realtime Database API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/google-firebase/refs/heads/main/openapi/firebase-realtime-database-openapi.yml
- filename: firebase-cloud-messaging-openapi.yml
  format: yaml
  label: Firebase Cloud Messaging API (FCM)
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/google-firebase/refs/heads/main/openapi/firebase-cloud-messaging-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  - Tax
  - Adjustment
  - Credit
  pricingCategory: Free + Pay-As-You-Go
description: 'FOCUS-aligned FinOps for Firebase: Spark is free with hard caps; Blaze is Pay-As-You-Go using underlying GCP service prices and flows through the standard Cloud Billing pipeline. The dominant meters are Firestore reads/writes/storage, Realtime Database storage and downloads, Cloud Functions invocations and GB-seconds, Cloud Storage, and Hosting transfer.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Google LLC
  ProviderName: Google Cloud
  PublisherName: Google LLC
  ServiceCategory: Mobile / Web Backend
  ServiceName: Firebase
layout: finops
meters:
- aggregation: sum
  description: Firestore document reads
  dimensions:
  - project
  - database
  - region
  name: firestore_reads
  unit: read
- aggregation: sum
  description: Firestore document writes (and deletes)
  dimensions:
  - project
  - database
  - region
  name: firestore_writes
  unit: write
- aggregation: max
  description: Firestore stored data
  dimensions:
  - project
  - database
  - region
  name: firestore_storage
  unit: GiB-month
- aggregation: max
  description: Realtime Database stored data
  dimensions:
  - project
  - database
  name: rtdb_storage
  unit: GB-month
- aggregation: sum
  description: Realtime Database egress downloads
  dimensions:
  - project
  - database
  name: rtdb_downloads
  unit: GB
- aggregation: max
  description: Firebase-managed Cloud Storage stored data
  dimensions:
  - project
  - bucket
  - storage_class
  name: cloud_storage_gb
  unit: GB-month
- aggregation: sum
  description: Cloud Storage downloads / egress
  dimensions:
  - project
  - bucket
  - destination
  name: cloud_storage_egress
  unit: GB
- aggregation: sum
  description: Cloud Functions invocations
  dimensions:
  - project
  - function
  - region
  name: functions_invocations
  unit: invocation
- aggregation: sum
  description: Cloud Functions GB-seconds
  dimensions:
  - project
  - function
  - region
  name: functions_gb_seconds
  unit: GB-second
- aggregation: sum
  description: Firebase Hosting data transfer
  dimensions:
  - site
  - region
  name: hosting_bandwidth
  unit: GB
- aggregation: max
  description: Authentication monthly active users (Identity Platform billing above 50K)
  dimensions:
  - project
  - sign_in_method
  name: auth_mau
  unit: MAU
name: Google Firebase Finops
provider_name: Google Firebase
provider_slug: google-firebase
publisher_name: Google LLC
service_category: Mobile / Web Backend
slug: google-firebase-finops
source_filename: google-firebase-finops.yml
source_heading: FinOps Profile
source_url: https://firebase.google.com/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Google Firebase\nproviderId: google-firebase\npublisherName: Google LLC\nserviceCategory: Mobile / Web Backend\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - Mobile Backend\n  - Serverless\n  - Realtime Database\n  - Google Cloud\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps for Firebase: Spark is free with hard caps; Blaze is Pay-As-You-Go\n  using underlying GCP service prices and flows through the standard Cloud Billing pipeline. The dominant\n  meters are Firestore reads/writes/storage, Realtime Database storage and downloads, Cloud Functions\n  invocations and GB-seconds, Cloud Storage, and Hosting\
  \ transfer.'\nsources:\n  - https://firebase.google.com/pricing\n  - https://cloud.google.com/billing/docs/how-to/export-data-bigquery\nbillingModel:\n  pricingCategory: Free + Pay-As-You-Go\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Adjustment\n    - Credit\nfocusColumns:\n  ServiceName: Firebase\n  ServiceCategory: Mobile / Web Backend\n  ProviderName: Google Cloud\n  PublisherName: Google LLC\n  InvoiceIssuerName: Google LLC\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: firestore_reads\n    description: Firestore document reads\n    unit: read\n    aggregation: sum\n    dimensions:\n      - project\n      - database\n      - region\n  - name: firestore_writes\n    description: Firestore document writes (and deletes)\n    unit: write\n    aggregation: sum\n    dimensions:\n      - project\n      - database\n      - region\n  - name: firestore_storage\n    description: Firestore stored\
  \ data\n    unit: GiB-month\n    aggregation: max\n    dimensions:\n      - project\n      - database\n      - region\n  - name: rtdb_storage\n    description: Realtime Database stored data\n    unit: GB-month\n    aggregation: max\n    dimensions:\n      - project\n      - database\n  - name: rtdb_downloads\n    description: Realtime Database egress downloads\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - project\n      - database\n  - name: cloud_storage_gb\n    description: Firebase-managed Cloud Storage stored data\n    unit: GB-month\n    aggregation: max\n    dimensions:\n      - project\n      - bucket\n      - storage_class\n  - name: cloud_storage_egress\n    description: Cloud Storage downloads / egress\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - project\n      - bucket\n      - destination\n  - name: functions_invocations\n    description: Cloud Functions invocations\n    unit: invocation\n    aggregation: sum\n    dimensions:\n      - project\n\
  \      - function\n      - region\n  - name: functions_gb_seconds\n    description: Cloud Functions GB-seconds\n    unit: GB-second\n    aggregation: sum\n    dimensions:\n      - project\n      - function\n      - region\n  - name: hosting_bandwidth\n    description: Firebase Hosting data transfer\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - site\n      - region\n  - name: auth_mau\n    description: Authentication monthly active users (Identity Platform billing above 50K)\n    unit: MAU\n    aggregation: max\n    dimensions:\n      - project\n      - sign_in_method\napis:\n  - name: Cloud Firestore API\n    baseURL: https://firestore.googleapis.com\n    serviceName: Cloud Firestore\n    serviceCategory: Database\n  - name: Realtime Database\n    baseURL: https://firebasedatabase.googleapis.com\n    serviceName: Realtime Database\n    serviceCategory: Database\n  - name: Cloud Storage for Firebase\n    baseURL: https://firebasestorage.googleapis.com\n    serviceName: Cloud\
  \ Storage for Firebase\n    serviceCategory: Storage\n  - name: Cloud Functions for Firebase\n    baseURL: https://cloudfunctions.googleapis.com\n    serviceName: Cloud Functions\n    serviceCategory: Compute\n  - name: Firebase Hosting API\n    baseURL: https://firebasehosting.googleapis.com\n    serviceName: Firebase Hosting\n    serviceCategory: Hosting\n  - name: Firebase Authentication / Identity Toolkit\n    baseURL: https://identitytoolkit.googleapis.com\n    serviceName: Firebase Authentication\n    serviceCategory: Identity\nprinciples:\n  - name: Visibility\n    description: Enable Cloud Billing detailed export to BigQuery; filter to Firebase services. Use the\n      Firebase console's Usage and Billing dashboards per-service to spot trend breaks.\n  - name: Allocation\n    description: Use one Firebase project per environment/team and tag underlying GCP resources with team\n      labels for chargeback. For multi-tenant apps, write a custom dimension into Firestore reads/writes\n\
  \      via labels in your BigQuery export.\n  - name: Optimization\n    description: Cache Firestore reads (memoize hot documents); reduce listener fan-out by querying narrower\n      paths; deny anonymous Hosting traffic at the CDN edge; right-size Cloud Functions memory; convert\n      legacy Cloud Storage default buckets to managed buckets to reduce egress.\n  - name: Accountability\n    description: Set Cloud Billing budgets per Firebase project at 50/80/100% with Pub/Sub triggers; configure\n      project-level spend caps; review monthly which services account for the top 80% of spend and target\n      optimization there.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/google-firebase/refs/heads/main/finops/google-firebase-finops.yml
sources:
- https://firebase.google.com/pricing
- https://cloud.google.com/billing/docs/how-to/export-data-bigquery
specification: FinOps Framework
tags:
- Mobile Backend
- Serverless
- Realtime Database
- Google Cloud
- FinOps
- FOCUS
---
