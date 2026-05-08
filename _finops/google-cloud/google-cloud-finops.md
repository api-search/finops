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
  label: Google Compute Engine API
  slug: ''
  spec_type: OpenAPI
  url: https://compute.googleapis.com/$discovery/rest?version=v1
- filename: rest
  format: yaml
  label: Google Cloud Storage API
  slug: ''
  spec_type: OpenAPI
  url: https://storage.googleapis.com/$discovery/rest?version=v1
- filename: rest
  format: yaml
  label: Google Kubernetes Engine API
  slug: ''
  spec_type: OpenAPI
  url: https://container.googleapis.com/$discovery/rest?version=v1
- filename: rest
  format: yaml
  label: Google Cloud Functions API
  slug: ''
  spec_type: OpenAPI
  url: https://cloudfunctions.googleapis.com/$discovery/rest?version=v1
- filename: rest
  format: yaml
  label: Google BigQuery API
  slug: ''
  spec_type: OpenAPI
  url: https://bigquery.googleapis.com/$discovery/rest?version=v2
- filename: rest
  format: yaml
  label: Google Cloud Pub/Sub API
  slug: ''
  spec_type: OpenAPI
  url: https://pubsub.googleapis.com/$discovery/rest?version=v1
- filename: rest
  format: yaml
  label: Google Cloud Vision API
  slug: ''
  spec_type: OpenAPI
  url: https://vision.googleapis.com/$discovery/rest?version=v1
- filename: rest
  format: yaml
  label: Google Cloud SQL Admin API
  slug: ''
  spec_type: OpenAPI
  url: https://sqladmin.googleapis.com/$discovery/rest?version=v1
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
description: FinOps framework definition for the Google Cloud Platform API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Google Cloud Platform
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Google Cloud Platform
  PublisherName: Google Cloud Platform
  ServiceCategory: Developer Tools / API
  ServiceName: Google Cloud Platform
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
name: Google Cloud Finops
provider_name: Google Cloud Platform
provider_slug: google-cloud
publisher_name: Google Cloud Platform
service_category: API
slug: google-cloud-finops
source_filename: google-cloud-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Google Cloud Platform\nproviderId: google-cloud\npublisherName: Google Cloud Platform\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Cloud Computing\n  - Data Analytics\n  - Infrastructure\n  - Machine Learning\n  - Platform as a Service\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Google Cloud Platform API surface. Provides a FOCUS-aligned\n  mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name:\
  \ Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  -\
  \ name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Google Cloud Platform\n  ServiceCategory: Developer Tools / API\n  ProviderName: Google Cloud Platform\n  PublisherName: Google Cloud Platform\n  InvoiceIssuerName: Google Cloud Platform\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name:\
  \ data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Google Compute Engine API\n    baseURL: https://compute.googleapis.com\n    tags:\n      - Compute\n      - IaaS\n      - Infrastructure\n      - Virtual Machines\n    serviceName: Google Compute Engine API\n    serviceCategory: API\n  - name: Google Cloud Storage API\n    baseURL: https://storage.googleapis.com\n    tags:\n      - Buckets\n      - Files\n      - Object Storage\n      - Storage\n    serviceName: Google Cloud Storage API\n    serviceCategory: API\n  - name: Google Kubernetes Engine API\n    baseURL: https://container.googleapis.com\n    tags:\n      - Containers\n     \
  \ - Docker\n      - Kubernetes\n      - Orchestration\n    serviceName: Google Kubernetes Engine API\n    serviceCategory: API\n  - name: Google Cloud Functions API\n    baseURL: https://cloudfunctions.googleapis.com\n    tags:\n      - Event-Driven\n      - FaaS\n      - Functions\n      - Serverless\n    serviceName: Google Cloud Functions API\n    serviceCategory: API\n  - name: Google BigQuery API\n    baseURL: https://bigquery.googleapis.com\n    tags:\n      - Analytics\n      - Big Data\n      - Data Warehouse\n      - SQL\n    serviceName: Google BigQuery API\n    serviceCategory: API\n  - name: Google Cloud Pub/Sub API\n    baseURL: https://pubsub.googleapis.com\n    tags:\n      - Event Streaming\n      - Messaging\n      - Pub/Sub\n      - Queue\n    serviceName: Google Cloud Pub/Sub API\n    serviceCategory: API\n  - name: Google Cloud Vision API\n    baseURL: https://vision.googleapis.com\n    tags:\n      - AI\n      - Computer Vision\n      - Image Analysis\n      - Machine\
  \ Learning\n    serviceName: Google Cloud Vision API\n    serviceCategory: API\n  - name: Google Cloud SQL Admin API\n    baseURL: https://sqladmin.googleapis.com\n    tags:\n      - Database\n      - MySQL\n      - PostgreSQL\n      - SQL\n    serviceName: Google Cloud SQL Admin API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n    url: https://apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/google-cloud/refs/heads/main/finops/google-cloud-finops.yml
sources: []
specification: FinOps Framework
tags:
- Cloud Computing
- Data Analytics
- Infrastructure
- Machine Learning
- Platform as a Service
- FinOps
- Cost Management
- FOCUS
---
