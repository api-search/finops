---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: colab-drive-openapi.yml
  format: yaml
  label: Colab API via Google Drive API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/google-colab/refs/heads/main/openapi/colab-drive-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  - Tax
  - Adjustment
  pricingCategory: Subscription + Pay-As-You-Go
description: 'FOCUS-aligned FinOps for Google Colab: consumer Colab (Pro/Pro+/PAYG) bills monthly via the Google Account billing surface using compute-unit consumption; Colab Enterprise bills hourly through the standard Google Cloud Billing pipeline as Vertex AI usage. Colab compute units are the primary spend lever for non-enterprise users.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Google LLC
  ProviderName: Google
  PublisherName: Google LLC
  ServiceCategory: AI Compute / Notebooks
  ServiceName: Colab / Colab Enterprise
layout: finops
meters:
- aggregation: sum
  description: Compute units consumed by attached runtimes (consumer Colab)
  dimensions:
  - subscription
  - gpu_class
  - user
  name: compute_units
  unit: compute_unit
- aggregation: max
  description: Active Colab Pro / Pro+ subscription seats
  dimensions:
  - tier
  name: subscription_seat
  unit: seat-month
- aggregation: sum
  description: Vertex AI runtime hours for Colab Enterprise notebooks
  dimensions:
  - machine_type
  - accelerator
  - region
  - project
  name: enterprise_runtime_hours
  unit: instance-hour
- aggregation: sum
  description: Notebook storage consumed (Drive for consumer Colab; GCS for Enterprise)
  dimensions:
  - storage_backend
  name: storage_gb_month
  unit: GB-month
name: Google Colab Finops
provider_name: Google Colab
provider_slug: google-colab
publisher_name: Google LLC
service_category: Notebook / ML Compute
slug: google-colab-finops
source_filename: google-colab-finops.yml
source_heading: FinOps Profile
source_url: https://colab.research.google.com/signup
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Google Colab\nproviderId: google-colab\npublisherName: Google LLC\nserviceCategory: Notebook / ML Compute\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - Notebooks\n  - Machine Learning\n  - Google Cloud\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps for Google Colab: consumer Colab (Pro/Pro+/PAYG) bills monthly via\n  the Google Account billing surface using compute-unit consumption; Colab Enterprise bills hourly through\n  the standard Google Cloud Billing pipeline as Vertex AI usage. Colab compute units are the primary\n  spend lever for non-enterprise users.'\nsources:\n  - https://colab.research.google.com/signup\n\
  \  - https://cloud.google.com/colab/pricing\n  - https://research.google.com/colaboratory/faq.html\nbillingModel:\n  pricingCategory: Subscription + Pay-As-You-Go\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Adjustment\nfocusColumns:\n  ServiceName: Colab / Colab Enterprise\n  ServiceCategory: AI Compute / Notebooks\n  ProviderName: Google\n  PublisherName: Google LLC\n  InvoiceIssuerName: Google LLC\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: compute_units\n    description: Compute units consumed by attached runtimes (consumer Colab)\n    unit: compute_unit\n    aggregation: sum\n    dimensions:\n      - subscription\n      - gpu_class\n      - user\n  - name: subscription_seat\n    description: Active Colab Pro / Pro+ subscription seats\n    unit: seat-month\n    aggregation: max\n    dimensions:\n      - tier\n  - name: enterprise_runtime_hours\n    description: Vertex AI runtime hours\
  \ for Colab Enterprise notebooks\n    unit: instance-hour\n    aggregation: sum\n    dimensions:\n      - machine_type\n      - accelerator\n      - region\n      - project\n  - name: storage_gb_month\n    description: Notebook storage consumed (Drive for consumer Colab; GCS for Enterprise)\n    unit: GB-month\n    aggregation: sum\n    dimensions:\n      - storage_backend\napis:\n  - name: Colab Notebook\n    baseURL: https://colab.research.google.com\n    serviceName: Colab Notebook\n    serviceCategory: Notebook\n  - name: Colab Enterprise (Vertex AI)\n    baseURL: https://aiplatform.googleapis.com\n    serviceName: Vertex AI Notebooks\n    serviceCategory: AI Compute\nprinciples:\n  - name: Visibility\n    description: For consumer Colab, view compute-unit balance and burn rate in the runtime UI (\"Resource\n      Usage\" panel) and the Subscriptions page; for Colab Enterprise, use the standard Cloud Billing detailed\n      export to BigQuery filtered to Vertex AI Notebooks SKUs.\n\
  \  - name: Allocation\n    description: Allocate consumer Colab spend by user (each subscription is per-Google-account); for\n      Enterprise, tag Vertex AI notebook runtimes with team/project labels and pivot the FOCUS export\n      by labels.\n  - name: Optimization\n    description: Match GPU class to workload (e.g., T4 for prototyping, A100 only for serious training);\n      shut down idle runtimes promptly since compute units accrue continuously while connected; prefer\n      PAYG bundles when usage is bursty rather than steady.\n  - name: Accountability\n    description: Designate per-team Colab subscription owners; for Enterprise, set Cloud Billing budget\n      alerts on the Vertex AI Notebooks service per project; review monthly compute-unit burn and re-tier\n      where appropriate.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/google-colab/refs/heads/main/finops/google-colab-finops.yml
sources:
- https://colab.research.google.com/signup
- https://cloud.google.com/colab/pricing
- https://research.google.com/colaboratory/faq.html
specification: FinOps Framework
tags:
- Notebooks
- Machine Learning
- Google Cloud
- FinOps
- FOCUS
---
