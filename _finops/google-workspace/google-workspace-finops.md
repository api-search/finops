---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: admin-sdk-directory-api.yml
  format: yaml
  label: Admin SDK Directory API
  slug: admin-directory
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/google-workspace/refs/heads/main/openapi/admin-sdk-directory-api.yml
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
description: FinOps framework definition for the Google Workspace API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Google Workspace
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Google Workspace
  PublisherName: Google Workspace
  ServiceCategory: Developer Tools / API
  ServiceName: Google Workspace
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
name: Google Workspace Finops
provider_name: Google Workspace
provider_slug: google-workspace
publisher_name: Google Workspace
service_category: API
slug: google-workspace-finops
source_filename: google-workspace-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Google Workspace\nproviderId: google-workspace\npublisherName: Google Workspace\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Calendar\n  - Collaboration\n  - Email\n  - Productivity\n  - Storage\n  - Video Conferencing\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Google Workspace API surface. Provides a FOCUS-aligned\n  mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description:\
  \ Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n\
  \    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Google Workspace\n  ServiceCategory: Developer Tools / API\n  ProviderName: Google Workspace\n  PublisherName: Google Workspace\n  InvoiceIssuerName: Google Workspace\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over\
  \ the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Gmail API\n    baseURL: https://gmail.googleapis.com\n    tags:\n      - Email\n      - Messaging\n    serviceName: Gmail API\n    serviceCategory: API\n  - name: Google Drive API\n    baseURL: https://www.googleapis.com/drive/v3\n    tags:\n      - Cloud\n      - Files\n      - Storage\n    serviceName: Google Drive API\n    serviceCategory: API\n  - name: Google Calendar API\n    baseURL: https://www.googleapis.com/calendar/v3\n    tags:\n      - Calendar\n      - Events\n      - Scheduling\n    serviceName: Google Calendar API\n    serviceCategory: API\n  - name: Google Meet REST API\n    baseURL: https://meet.googleapis.com\n    tags:\n\
  \      - Conferencing\n      - Meetings\n      - Video\n    serviceName: Google Meet REST API\n    serviceCategory: API\n  - name: Google Docs API\n    baseURL: https://docs.googleapis.com\n    tags:\n      - Collaboration\n      - Documents\n      - Word Processing\n    serviceName: Google Docs API\n    serviceCategory: API\n  - name: Google Sheets API\n    baseURL: https://sheets.googleapis.com\n    tags:\n      - Analytics\n      - Data\n      - Spreadsheets\n    serviceName: Google Sheets API\n    serviceCategory: API\n  - name: Google Slides API\n    baseURL: https://slides.googleapis.com\n    tags:\n      - Presentations\n      - Slides\n    serviceName: Google Slides API\n    serviceCategory: API\n  - name: Admin SDK Directory API\n    baseURL: https://admin.googleapis.com\n    tags:\n      - Admin\n      - Groups\n      - Management\n      - Users\n    serviceName: Admin SDK Directory API\n    serviceCategory: API\n  - name: Google Chat API\n    baseURL: https://chat.googleapis.com\n\
  \    tags:\n      - Chat\n      - Collaboration\n      - Messaging\n    serviceName: Google Chat API\n    serviceCategory: API\n  - name: Admin SDK Reports API\n    baseURL: https://admin.googleapis.com\n    tags:\n      - Admin\n      - Audit\n      - Reports\n      - Usage\n    serviceName: Admin SDK Reports API\n    serviceCategory: API\n  - name: Google Forms API\n    baseURL: https://forms.googleapis.com\n    tags:\n      - Forms\n      - Quizzes\n      - Surveys\n    serviceName: Google Forms API\n    serviceCategory: API\n  - name: Google Tasks API\n    baseURL: https://tasks.googleapis.com\n    tags:\n      - Productivity\n      - Tasks\n      - To-Do\n    serviceName: Google Tasks API\n    serviceCategory: API\n  - name: Google Keep API\n    baseURL: https://keep.googleapis.com\n    tags:\n      - Notes\n      - Productivity\n    serviceName: Google Keep API\n    serviceCategory: API\n  - name: Google Vault API\n    baseURL: https://vault.googleapis.com\n    tags:\n      - Compliance\n\
  \      - Ediscovery\n      - Legal\n    serviceName: Google Vault API\n    serviceCategory: API\n  - name: Google Classroom API\n    baseURL: https://classroom.googleapis.com\n    tags:\n      - Classroom\n      - Education\n      - Learning\n    serviceName: Google Classroom API\n    serviceCategory: API\n  - name: People API\n    baseURL: https://people.googleapis.com\n    tags:\n      - Contacts\n      - Directory\n      - People\n    serviceName: People API\n    serviceCategory: API\n  - name: Google Cloud Search API\n    baseURL: https://cloudsearch.googleapis.com\n    tags:\n      - Enterprise Search\n      - Indexing\n      - Search\n    serviceName: Google Cloud Search API\n    serviceCategory: API\n  - name: Drive Activity API\n    baseURL: https://driveactivity.googleapis.com\n    tags:\n      - Activity\n      - Audit\n      - Drive\n    serviceName: Drive Activity API\n    serviceCategory: API\n  - name: Drive Labels API\n    baseURL: https://drivelabels.googleapis.com\n  \
  \  tags:\n      - Drive\n      - Labels\n      - Metadata\n    serviceName: Drive Labels API\n    serviceCategory: API\n  - name: Alert Center API\n    baseURL: https://alertcenter.googleapis.com\n    tags:\n      - Admin\n      - Alerts\n      - Security\n    serviceName: Alert Center API\n    serviceCategory: API\n  - name: Groups Settings API\n    baseURL: https://www.googleapis.com/groups/v1\n    tags:\n      - Admin\n      - Groups\n      - Settings\n    serviceName: Groups Settings API\n    serviceCategory: API\n  - name: Groups Migration API\n    baseURL: https://groupsmigration.googleapis.com\n    tags:\n      - Admin\n      - Groups\n      - Migration\n    serviceName: Groups Migration API\n    serviceCategory: API\n  - name: Admin SDK Data Transfer API\n    baseURL: https://admin.googleapis.com\n    tags:\n      - Admin\n      - Data Transfer\n      - Migration\n    serviceName: Admin SDK Data Transfer API\n    serviceCategory: API\n  - name: Enterprise License Manager API\n\
  \    baseURL: https://licensing.googleapis.com\n    tags:\n      - Admin\n      - Licensing\n      - Management\n    serviceName: Enterprise License Manager API\n    serviceCategory: API\n  - name: Google Workspace Reseller API\n    baseURL: https://reseller.googleapis.com\n    tags:\n      - Admin\n      - Reseller\n      - Subscriptions\n    serviceName: Google Workspace Reseller API\n    serviceCategory: API\n  - name: Gmail Postmaster Tools API\n    baseURL: https://gmailpostmastertools.googleapis.com\n    tags:\n      - Deliverability\n      - Email\n      - Postmaster\n    serviceName: Gmail Postmaster Tools API\n    serviceCategory: API\n  - name: Google Workspace Marketplace API\n    baseURL: https://appsmarket.googleapis.com\n    tags:\n      - Apps\n      - Licensing\n      - Marketplace\n    serviceName: Google Workspace Marketplace API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n\
  \  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/google-workspace/refs/heads/main/finops/google-workspace-finops.yml
sources: []
specification: FinOps Framework
tags:
- Calendar
- Collaboration
- Email
- Productivity
- Storage
- Video Conferencing
- FinOps
- Cost Management
- FOCUS
---
