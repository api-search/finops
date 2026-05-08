---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: openapi.yaml
  format: yaml
  label: Microsoft Graph API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/microsoftgraph/microsoft-graph-openapi/master/openapi/v1.0/openapi.yaml
- filename: mail.yaml
  format: yaml
  label: Outlook Mail API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/microsoftgraph/microsoft-graph-openapi/master/openapi/v1.0/mail.yaml
- filename: calendar.yaml
  format: yaml
  label: Outlook Calendar API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/microsoftgraph/microsoft-graph-openapi/master/openapi/v1.0/calendar.yaml
- filename: files.yaml
  format: yaml
  label: OneDrive API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/microsoftgraph/microsoft-graph-openapi/master/openapi/v1.0/files.yaml
- filename: sites.yaml
  format: yaml
  label: SharePoint API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/microsoftgraph/microsoft-graph-openapi/master/openapi/v1.0/sites.yaml
- filename: teams.yaml
  format: yaml
  label: Microsoft Teams API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/microsoftgraph/microsoft-graph-openapi/master/openapi/v1.0/teams.yaml
- filename: users.yaml
  format: yaml
  label: Office 365 Users API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/microsoftgraph/microsoft-graph-openapi/master/openapi/v1.0/users.yaml
- filename: planner.yaml
  format: yaml
  label: Planner API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/microsoftgraph/microsoft-graph-openapi/master/openapi/v1.0/planner.yaml
- filename: microsoft-graph-api-openapi.yml
  format: yaml
  label: Office 365 Groups API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-office-365/refs/heads/main/openapi/microsoft-graph-api-openapi.yml
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
description: FinOps framework definition for the Microsoft Office 365 API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Microsoft Office 365
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Microsoft Office 365
  PublisherName: Microsoft Office 365
  ServiceCategory: Developer Tools / API
  ServiceName: Microsoft Office 365
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
name: Microsoft Office 365 Finops
provider_name: Microsoft Office 365
provider_slug: microsoft-office-365
publisher_name: Microsoft Office 365
service_category: API
slug: microsoft-office-365-finops
source_filename: microsoft-office-365-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Microsoft Office 365\nproviderId: microsoft-office-365\npublisherName: Microsoft Office 365\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Cloud\n  - Collaboration\n  - Enterprise\n  - Microsoft\n  - Productivity\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Microsoft Office 365 API surface. Provides a FOCUS-aligned\n  mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description:\
  \ Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n\
  \    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Microsoft Office 365\n  ServiceCategory: Developer Tools / API\n  ProviderName: Microsoft Office 365\n  PublisherName: Microsoft Office 365\n  InvoiceIssuerName: Microsoft Office 365\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes\
  \ returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Microsoft Graph API\n    baseURL: https://graph.microsoft.com\n    tags:\n      - Calendar\n      - Graph\n      - Groups\n      - Mail\n      - Unified\n      - Users\n    serviceName: Microsoft Graph API\n    serviceCategory: API\n  - name: Outlook Mail API\n    baseURL: https://graph.microsoft.com/v1.0/me/messages\n    tags:\n      - Email\n      - Mail\n      - Messages\n      - Outlook\n    serviceName: Outlook Mail API\n    serviceCategory: API\n  - name: Outlook Calendar API\n    baseURL: https://graph.microsoft.com/v1.0/me/calendar\n    tags:\n      - Calendar\n      - Events\n      - Meetings\n      - Scheduling\n\
  \    serviceName: Outlook Calendar API\n    serviceCategory: API\n  - name: Outlook Contacts API\n    baseURL: https://graph.microsoft.com/v1.0/me/contacts\n    tags:\n      - Address-Book\n      - Contacts\n      - Outlook\n      - People\n    serviceName: Outlook Contacts API\n    serviceCategory: API\n  - name: OneDrive API\n    baseURL: https://graph.microsoft.com/v1.0/me/drive\n    tags:\n      - Files\n      - Onedrive\n      - Sharing\n      - Storage\n    serviceName: OneDrive API\n    serviceCategory: API\n  - name: SharePoint API\n    baseURL: https://graph.microsoft.com/v1.0/sites\n    tags:\n      - Collaboration\n      - Lists\n      - Sharepoint\n      - Sites\n    serviceName: SharePoint API\n    serviceCategory: API\n  - name: Microsoft Teams API\n    baseURL: https://graph.microsoft.com/v1.0/teams\n    tags:\n      - Channels\n      - Chat\n      - Collaboration\n      - Teams\n    serviceName: Microsoft Teams API\n    serviceCategory: API\n  - name: Office 365 Users API\n\
  \    baseURL: https://graph.microsoft.com/v1.0/users\n    tags:\n      - Directory\n      - Identity\n      - Profiles\n      - Users\n    serviceName: Office 365 Users API\n    serviceCategory: API\n  - name: Planner API\n    baseURL: https://graph.microsoft.com/v1.0/planner\n    tags:\n      - Planner\n      - Planning\n      - Projects\n      - Tasks\n    serviceName: Planner API\n    serviceCategory: API\n  - name: OneNote API\n    baseURL: https://graph.microsoft.com/v1.0/me/onenote\n    tags:\n      - Notebooks\n      - Notes\n      - Onenote\n      - Pages\n      - Sections\n    serviceName: OneNote API\n    serviceCategory: API\n  - name: Excel Workbooks and Charts API\n    baseURL: https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook\n    tags:\n      - Charts\n      - Excel\n      - Spreadsheets\n      - Tables\n      - Workbooks\n    serviceName: Excel Workbooks and Charts API\n    serviceCategory: API\n  - name: Microsoft To Do API\n    baseURL: https://graph.microsoft.com/v1.0/me/todo\n\
  \    tags:\n      - Productivity\n      - Task-Lists\n      - Tasks\n      - Todo\n    serviceName: Microsoft To Do API\n    serviceCategory: API\n  - name: Microsoft Bookings API\n    baseURL: https://graph.microsoft.com/v1.0/solutions/bookingBusinesses\n    tags:\n      - Appointments\n      - Bookings\n      - Business\n      - Scheduling\n    serviceName: Microsoft Bookings API\n    serviceCategory: API\n  - name: Office 365 Groups API\n    baseURL: https://graph.microsoft.com/v1.0/groups\n    tags:\n      - Collaboration\n      - Groups\n      - Membership\n      - Teams\n    serviceName: Office 365 Groups API\n    serviceCategory: API\n  - name: Microsoft Graph Security API\n    baseURL: https://graph.microsoft.com/v1.0/security\n    tags:\n      - Alerts\n      - Compliance\n      - Security\n      - Threats\n    serviceName: Microsoft Graph Security API\n    serviceCategory: API\n  - name: Microsoft Graph Communications API\n    baseURL: https://graph.microsoft.com/v1.0/communications\n\
  \    tags:\n      - Calls\n      - Communications\n      - Meetings\n      - Online-Meetings\n    serviceName: Microsoft Graph Communications API\n    serviceCategory: API\n  - name: Office Add-ins Platform\n    baseURL: ''\n    tags:\n      - Add-Ins\n      - Excel\n      - Extensions\n      - Office-Js\n      - Outlook\n      - Powerpoint\n      - Word\n    serviceName: Office Add-ins Platform\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n    url: https://apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/microsoft-office-365/refs/heads/main/finops/microsoft-office-365-finops.yml
sources: []
specification: FinOps Framework
tags:
- Cloud
- Collaboration
- Enterprise
- Microsoft
- Productivity
- FinOps
- Cost Management
- FOCUS
---
