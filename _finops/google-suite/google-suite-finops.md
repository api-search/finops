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
  label: Gmail API
  slug: ''
  spec_type: OpenAPI
  url: https://gmail.googleapis.com/$discovery/rest?version=v1
- filename: rest
  format: yaml
  label: Google Calendar API
  slug: ''
  spec_type: OpenAPI
  url: https://www.googleapis.com/discovery/v1/apis/calendar/v3/rest
- filename: rest
  format: yaml
  label: Google Drive API
  slug: ''
  spec_type: OpenAPI
  url: https://www.googleapis.com/discovery/v1/apis/drive/v3/rest
- filename: rest
  format: yaml
  label: Google Docs API
  slug: ''
  spec_type: OpenAPI
  url: https://docs.googleapis.com/$discovery/rest?version=v1
- filename: rest
  format: yaml
  label: Google Sheets API
  slug: ''
  spec_type: OpenAPI
  url: https://sheets.googleapis.com/$discovery/rest?version=v4
- filename: rest
  format: yaml
  label: Google Slides API
  slug: ''
  spec_type: OpenAPI
  url: https://slides.googleapis.com/$discovery/rest?version=v1
- filename: rest
  format: yaml
  label: Google Chat API
  slug: ''
  spec_type: OpenAPI
  url: https://chat.googleapis.com/$discovery/rest?version=v1
- filename: rest
  format: yaml
  label: Google Admin SDK
  slug: ''
  spec_type: OpenAPI
  url: https://admin.googleapis.com/$discovery/rest?version=directory_v1
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
description: FinOps framework definition for the Google Workspace (G Suite) API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Google Workspace (G Suite)
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Google Workspace (G Suite)
  PublisherName: Google Workspace (G Suite)
  ServiceCategory: Developer Tools / API
  ServiceName: Google Workspace (G Suite)
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
name: Google Suite Finops
provider_name: Google Workspace (G Suite)
provider_slug: google-suite
publisher_name: Google Workspace (G Suite)
service_category: API
slug: google-suite-finops
source_filename: google-suite-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Google Workspace (G Suite)\nproviderId: google-suite\npublisherName: Google Workspace (G Suite)\nserviceCategory: API\ncreated: '2026-05-04'\nmodified: '2026-05-04'\ntags:\n  - Cloud\n  - Collaboration\n  - Enterprise\n  - Google\n  - Productivity\n  - Workspace\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Google Workspace (G Suite) API surface. Provides a FOCUS-aligned\n  mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name:\
  \ Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  -\
  \ name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Google Workspace (G Suite)\n  ServiceCategory: Developer Tools / API\n  ProviderName: Google Workspace (G Suite)\n  PublisherName: Google Workspace (G Suite)\n  InvoiceIssuerName: Google Workspace (G Suite)\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n  \
  \    - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Gmail API\n    baseURL: https://gmail.googleapis.com\n    tags:\n      - Email\n      - Messaging\n      - Productivity\n    serviceName: Gmail API\n    serviceCategory: API\n  - name: Google Calendar API\n    baseURL: https://www.googleapis.com/calendar/v3\n    tags:\n      - Calendar\n      - Events\n      - Productivity\n      - Scheduling\n    serviceName: Google Calendar API\n    serviceCategory: API\n  - name: Google Drive API\n    baseURL: https://www.googleapis.com/drive/v3\n    tags:\n      - Cloud\n      - Collaboration\n      - Files\n      - Storage\n\
  \    serviceName: Google Drive API\n    serviceCategory: API\n  - name: Google Docs API\n    baseURL: https://docs.googleapis.com/v1\n    tags:\n      - Collaboration\n      - Documents\n      - Productivity\n      - Word-Processing\n    serviceName: Google Docs API\n    serviceCategory: API\n  - name: Google Sheets API\n    baseURL: https://sheets.googleapis.com/v4\n    tags:\n      - Collaboration\n      - Data\n      - Productivity\n      - Spreadsheets\n    serviceName: Google Sheets API\n    serviceCategory: API\n  - name: Google Slides API\n    baseURL: https://slides.googleapis.com/v1\n    tags:\n      - Collaboration\n      - Presentations\n      - Productivity\n    serviceName: Google Slides API\n    serviceCategory: API\n  - name: Google Meet API\n    baseURL: https://meet.googleapis.com/v2\n    tags:\n      - Collaboration\n      - Communication\n      - Meetings\n      - Video-Conferencing\n    serviceName: Google Meet API\n    serviceCategory: API\n  - name: Google Chat API\n\
  \    baseURL: https://chat.googleapis.com/v1\n    tags:\n      - Bots\n      - Collaboration\n      - Communication\n      - Messaging\n    serviceName: Google Chat API\n    serviceCategory: API\n  - name: Google Admin SDK\n    baseURL: https://admin.googleapis.com\n    tags:\n      - Administration\n      - Groups\n      - Management\n      - Users\n    serviceName: Google Admin SDK\n    serviceCategory: API\n  - name: Google Forms API\n    baseURL: https://forms.googleapis.com/v1\n    tags:\n      - Data-Collection\n      - Forms\n      - Productivity\n      - Surveys\n    serviceName: Google Forms API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/google-suite/refs/heads/main/finops/google-suite-finops.yml
sources: []
specification: FinOps Framework
tags:
- Cloud
- Collaboration
- Enterprise
- Google
- Productivity
- Workspace
- FinOps
- Cost Management
- FOCUS
---
