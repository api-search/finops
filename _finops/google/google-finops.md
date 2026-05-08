---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: books-api-openapi.yml
  format: yaml
  label: Books API
  slug: books-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/google/refs/heads/main/openapi/books-api-openapi.yml
- filename: google-drive-api-openapi.yml
  format: yaml
  label: Google Drive API
  slug: google-drive-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/google/refs/heads/main/openapi/google-drive-api-openapi.yml
- filename: google-drive-activity-api-openapi.yml
  format: yaml
  label: Google Drive Activity API
  slug: google-drive-activity-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/google/refs/heads/main/openapi/google-drive-activity-api-openapi.yml
- filename: google-drive-labels-api-openapi.yml
  format: yaml
  label: Google Drive Labels API
  slug: google-drive-labels-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/google/refs/heads/main/openapi/google-drive-labels-api-openapi.yml
- filename: google-calendar-api-openapi.yml
  format: yaml
  label: Google Calendar API
  slug: google-calendar-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/google/refs/heads/main/openapi/google-calendar-api-openapi.yml
- filename: google-gmail-api-openapi.yml
  format: yaml
  label: Google Gmail API
  slug: google-gmail-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/google/refs/heads/main/openapi/google-gmail-api-openapi.yml
- filename: google-sheets-api-openapi.yml
  format: yaml
  label: Google Sheets API
  slug: google-sheets-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/google/refs/heads/main/openapi/google-sheets-api-openapi.yml
- filename: google-docs-api-openapi.yml
  format: yaml
  label: Google Docs API
  slug: google-docs-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/google/refs/heads/main/openapi/google-docs-api-openapi.yml
- filename: google-gemini-api-openapi.yml
  format: yaml
  label: Google Gemini API
  slug: google-gemini-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/google/refs/heads/main/openapi/google-gemini-api-openapi.yml
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
description: FinOps framework definition for the Google API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Google
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Google
  PublisherName: Google
  ServiceCategory: Developer Tools / API
  ServiceName: Google
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
name: Google Finops
provider_name: Google
provider_slug: google
publisher_name: Google
service_category: API
slug: google-finops
source_filename: google-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Google\nproviderId: google\npublisherName: Google\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Advertising\n  - Cloud\n  - Developer\n  - Google\n  - Platform\n  - Search\n  - T1\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Google API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the\
  \ consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps\
  \ Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Google\n  ServiceCategory: Developer Tools / API\n  ProviderName: Google\n  PublisherName: Google\n  InvoiceIssuerName: Google\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n\
  \      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Google Cloud API Gateway\n    baseURL: https://api.example.com\n    tags:\n      - API Gateway\n    serviceName: Google Cloud API Gateway\n    serviceCategory: API\n  - name: Books API\n    baseURL: https://api.example.com\n    tags:\n      - Books\n    serviceName: Books API\n    serviceCategory: API\n  - name: Google Drive API\n    baseURL: ''\n    tags:\n      - Documents\n      - Storage\n    serviceName: Google Drive API\n    serviceCategory: API\n  - name: Google Drive Activity API\n    baseURL: ''\n    tags:\n      - Activity\n      - Documents\n    serviceName: Google Drive Activity API\n    serviceCategory: API\n  - name: Google Drive Labels API\n    baseURL: ''\n    tags:\n      - Documents\n      - Labels\n\
  \    serviceName: Google Drive Labels API\n    serviceCategory: API\n  - name: Google Calendar API\n    baseURL: ''\n    tags:\n      - Calendar\n    serviceName: Google Calendar API\n    serviceCategory: API\n  - name: Google Gmail API\n    baseURL: ''\n    tags:\n      - Email\n    serviceName: Google Gmail API\n    serviceCategory: API\n  - name: Google Sheets API\n    baseURL: ''\n    tags:\n      - Spreadsheets\n    serviceName: Google Sheets API\n    serviceCategory: API\n  - name: Google Docs API\n    baseURL: ''\n    tags:\n      - Documents\n    serviceName: Google Docs API\n    serviceCategory: API\n  - name: Google Maps API\n    baseURL: ''\n    tags:\n      - Geolocation\n      - Maps\n    serviceName: Google Maps API\n    serviceCategory: API\n  - name: Google Places API\n    baseURL: ''\n    tags:\n      - Places\n    serviceName: Google Places API\n    serviceCategory: API\n  - name: Google Aggregate Places API\n    baseURL: ''\n    tags:\n      - Maps\n      - Places\n\
  \    serviceName: Google Aggregate Places API\n    serviceCategory: API\n  - name: Google Places Insights API\n    baseURL: ''\n    tags:\n      - Analytics\n      - Maps\n      - Places\n    serviceName: Google Places Insights API\n    serviceCategory: API\n  - name: Google Street View Imagery API\n    baseURL: ''\n    tags:\n      - Images\n      - Maps\n      - Street View\n    serviceName: Google Street View Imagery API\n    serviceCategory: API\n  - name: Google Elevation API\n    baseURL: ''\n    tags:\n      - Elevation\n      - Maps\n    serviceName: Google Elevation API\n    serviceCategory: API\n  - name: Google Routes API\n    baseURL: ''\n    tags:\n      - Directions\n      - Maps\n      - Routes\n    serviceName: Google Routes API\n    serviceCategory: API\n  - name: Google Geocoding API\n    baseURL: ''\n    tags:\n      - Geocoding\n      - Maps\n    serviceName: Google Geocoding API\n    serviceCategory: API\n  - name: Google Geolocation API\n    baseURL: ''\n    tags:\n\
  \      - Geolocation\n      - Maps\n    serviceName: Google Geolocation API\n    serviceCategory: API\n  - name: Google Address Validation API\n    baseURL: ''\n    tags:\n      - Address\n      - Maps\n      - Validation\n    serviceName: Google Address Validation API\n    serviceCategory: API\n  - name: Google Time Zone API\n    baseURL: ''\n    tags:\n      - Maps\n      - Time Zone\n    serviceName: Google Time Zone API\n    serviceCategory: API\n  - name: Google Air Quality API\n    baseURL: ''\n    tags:\n      - Air Quality\n      - Environment\n      - Maps\n    serviceName: Google Air Quality API\n    serviceCategory: API\n  - name: Google Pollen API\n    baseURL: ''\n    tags:\n      - Environment\n      - Maps\n      - Pollen\n    serviceName: Google Pollen API\n    serviceCategory: API\n  - name: Google Solar API\n    baseURL: ''\n    tags:\n      - Energy\n      - Maps\n      - Solar\n    serviceName: Google Solar API\n    serviceCategory: API\n  - name: Google Weather API\n\
  \    baseURL: ''\n    tags:\n      - Environment\n      - Maps\n      - Weather\n    serviceName: Google Weather API\n    serviceCategory: API\n  - name: Google Gemini API\n    baseURL: ''\n    tags:\n      - AI\n      - Documents\n      - Machine Learning\n    serviceName: Google Gemini API\n    serviceCategory: API\n  - name: YouTube Data API\n    baseURL: ''\n    tags:\n      - Media\n      - Video\n    serviceName: YouTube Data API\n    serviceCategory: API\n  - name: Google Analytics Data API\n    baseURL: ''\n    tags:\n      - Analytics\n      - Reporting\n    serviceName: Google Analytics Data API\n    serviceCategory: API\n  - name: Google Ads API\n    baseURL: ''\n    tags:\n      - Advertising\n    serviceName: Google Ads API\n    serviceCategory: API\n  - name: Google Custom Search JSON API\n    baseURL: ''\n    tags:\n      - Search\n    serviceName: Google Custom Search JSON API\n    serviceCategory: API\n  - name: Google Cloud Translation API\n    baseURL: ''\n    tags:\n\
  \      - AI\n      - Machine Learning\n      - Translation\n    serviceName: Google Cloud Translation API\n    serviceCategory: API\n  - name: Google Cloud Vision API\n    baseURL: ''\n    tags:\n      - AI\n      - Machine Learning\n      - Vision\n    serviceName: Google Cloud Vision API\n    serviceCategory: API\n  - name: Google Cloud Natural Language API\n    baseURL: ''\n    tags:\n      - AI\n      - Machine Learning\n      - Natural Language Processing\n    serviceName: Google Cloud Natural Language API\n    serviceCategory: API\n  - name: Google Cloud Speech-to-Text API\n    baseURL: ''\n    tags:\n      - AI\n      - Machine Learning\n      - Speech\n    serviceName: Google Cloud Speech-to-Text API\n    serviceCategory: API\n  - name: Google Cloud Text-to-Speech API\n    baseURL: ''\n    tags:\n      - AI\n      - Machine Learning\n      - Speech\n    serviceName: Google Cloud Text-to-Speech API\n    serviceCategory: API\n  - name: Google Cloud BigQuery API\n    baseURL: ''\n\
  \    tags:\n      - Analytics\n      - Big Data\n      - Database\n    serviceName: Google Cloud BigQuery API\n    serviceCategory: API\n  - name: Google Fonts API\n    baseURL: ''\n    tags:\n      - Design\n      - Fonts\n    serviceName: Google Fonts API\n    serviceCategory: API\n  - name: Google People API\n    baseURL: ''\n    tags:\n      - Contacts\n      - People\n    serviceName: Google People API\n    serviceCategory: API\n  - name: Google Blogger API\n    baseURL: ''\n    tags:\n      - Blogging\n    serviceName: Google Blogger API\n    serviceCategory: API\n  - name: Google Slides API\n    baseURL: ''\n    tags:\n      - Presentations\n    serviceName: Google Slides API\n    serviceCategory: API\n  - name: Google Tasks API\n    baseURL: ''\n    tags:\n      - Productivity\n      - Tasks\n    serviceName: Google Tasks API\n    serviceCategory: API\n  - name: Google Chat API\n    baseURL: ''\n    tags:\n      - Chat\n      - Messaging\n    serviceName: Google Chat API\n    serviceCategory:\
  \ API\n  - name: Google Classroom API\n    baseURL: ''\n    tags:\n      - Classroom\n      - Education\n    serviceName: Google Classroom API\n    serviceCategory: API\n  - name: Google Forms API\n    baseURL: ''\n    tags:\n      - Forms\n      - Surveys\n    serviceName: Google Forms API\n    serviceCategory: API\n  - name: Google Meet REST API\n    baseURL: ''\n    tags:\n      - Meetings\n      - Video Conferencing\n    serviceName: Google Meet REST API\n    serviceCategory: API\n  - name: Google Knowledge Graph Search API\n    baseURL: ''\n    tags:\n      - Knowledge Graph\n      - Search\n    serviceName: Google Knowledge Graph Search API\n    serviceCategory: API\n  - name: Google PageSpeed Insights API\n    baseURL: ''\n    tags:\n      - Performance\n      - Web\n    serviceName: Google PageSpeed Insights API\n    serviceCategory: API\n  - name: Google Civic Information API\n    baseURL: ''\n    tags:\n      - Civic\n      - Government\n    serviceName: Google Civic Information\
  \ API\n    serviceCategory: API\n  - name: Google Roads API\n    baseURL: ''\n    tags:\n      - Maps\n      - Roads\n    serviceName: Google Roads API\n    serviceCategory: API\n  - name: Google Map Tiles API\n    baseURL: ''\n    tags:\n      - Maps\n      - Tiles\n    serviceName: Google Map Tiles API\n    serviceCategory: API\n  - name: Google Route Optimization API\n    baseURL: ''\n    tags:\n      - Maps\n      - Optimization\n      - Routes\n    serviceName: Google Route Optimization API\n    serviceCategory: API\n  - name: Google Play Developer API\n    baseURL: ''\n    tags:\n      - Android\n      - App Store\n    serviceName: Google Play Developer API\n    serviceCategory: API\n  - name: Firebase API\n    baseURL: ''\n    tags:\n      - Backend\n      - Cloud\n      - Mobile\n    serviceName: Firebase API\n    serviceCategory: API\n  - name: Google Picker API\n    baseURL: ''\n    tags:\n      - Documents\n      - File Picker\n    serviceName: Google Picker API\n    serviceCategory:\
  \ API\n  - name: Google Keep API\n    baseURL: ''\n    tags:\n      - Notes\n      - Productivity\n    serviceName: Google Keep API\n    serviceCategory: API\n  - name: Google Vault API\n    baseURL: ''\n    tags:\n      - Compliance\n      - Legal\n    serviceName: Google Vault API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    url: https://apievangelist.com\n    email: kin@apievangelist.com\n  - FN: Google\n    url: https://developers.google.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/google/refs/heads/main/finops/google-finops.yml
sources: []
specification: FinOps Framework
tags:
- Advertising
- Cloud
- Developer
- Google
- Platform
- Search
- T1
- FinOps
- Cost Management
- FOCUS
---
