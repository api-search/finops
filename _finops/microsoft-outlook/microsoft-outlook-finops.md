---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: microsoft-graph-mail-api-openapi.yml
  format: yaml
  label: Microsoft Graph Mail API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-outlook/refs/heads/main/openapi/microsoft-graph-mail-api-openapi.yml
- filename: openapi.yaml
  format: yaml
  label: Microsoft Graph Calendar API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/microsoftgraph/msgraph-metadata/master/openapi/v1.0/openapi.yaml
- filename: openapi.yaml
  format: yaml
  label: Microsoft Graph Contacts API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/microsoftgraph/msgraph-metadata/master/openapi/v1.0/openapi.yaml
- filename: openapi.yaml
  format: yaml
  label: Microsoft Graph Tasks API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/microsoftgraph/msgraph-metadata/master/openapi/v1.0/openapi.yaml
- filename: openapi.yaml
  format: yaml
  label: Microsoft Graph People API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/microsoftgraph/msgraph-metadata/master/openapi/v1.0/openapi.yaml
- filename: openapi.yaml
  format: yaml
  label: Microsoft Graph Change Notifications API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/microsoftgraph/msgraph-metadata/master/openapi/v1.0/openapi.yaml
- filename: openapi.yaml
  format: yaml
  label: Microsoft Graph Focused Inbox API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/microsoftgraph/msgraph-metadata/master/openapi/v1.0/openapi.yaml
- filename: openapi.yaml
  format: yaml
  label: Microsoft Graph Mail Rules API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/microsoftgraph/msgraph-metadata/master/openapi/v1.0/openapi.yaml
- filename: openapi.yaml
  format: yaml
  label: Microsoft Graph Categories API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/microsoftgraph/msgraph-metadata/master/openapi/v1.0/openapi.yaml
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
description: FinOps framework definition for the Microsoft Outlook API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Microsoft Outlook
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Microsoft Outlook
  PublisherName: Microsoft Outlook
  ServiceCategory: Developer Tools / API
  ServiceName: Microsoft Outlook
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
name: Microsoft Outlook Finops
provider_name: Microsoft Outlook
provider_slug: microsoft-outlook
publisher_name: Microsoft Outlook
service_category: API
slug: microsoft-outlook-finops
source_filename: microsoft-outlook-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Microsoft Outlook\nproviderId: microsoft-outlook\npublisherName: Microsoft Outlook\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Calendar\n  - Contacts\n  - Email\n  - Enterprise\n  - Microsoft\n  - Office 365\n  - Productivity\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Microsoft Outlook API surface. Provides a FOCUS-aligned\n  mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n\
  \    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage\
  \ the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Microsoft Outlook\n  ServiceCategory: Developer Tools / API\n  ProviderName: Microsoft Outlook\n  PublisherName: Microsoft Outlook\n  InvoiceIssuerName: Microsoft Outlook\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description:\
  \ Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Microsoft Graph Mail API\n    baseURL: https://graph.microsoft.com/v1.0\n    tags:\n      - Email\n      - Folders\n      - Mail\n      - Messages\n    serviceName: Microsoft Graph Mail API\n    serviceCategory: API\n  - name: Microsoft Graph Calendar API\n    baseURL: https://graph.microsoft.com/v1.0\n    tags:\n      - Calendar\n      - Events\n      - Meetings\n      - Scheduling\n    serviceName: Microsoft Graph Calendar API\n    serviceCategory: API\n  - name: Microsoft Graph Contacts API\n    baseURL: https://graph.microsoft.com/v1.0\n    tags:\n      - Address Book\n      - Contacts\n      - People\n    serviceName:\
  \ Microsoft Graph Contacts API\n    serviceCategory: API\n  - name: Microsoft Graph Tasks API\n    baseURL: https://graph.microsoft.com/v1.0\n    tags:\n      - Task Management\n      - Tasks\n      - To-Do\n    serviceName: Microsoft Graph Tasks API\n    serviceCategory: API\n  - name: Outlook Add-ins API\n    baseURL: https://appsforoffice.microsoft.com/lib/1/hosted/office.js\n    tags:\n      - Add-Ins\n      - Extensions\n      - Office.js\n      - Plugins\n    serviceName: Outlook Add-ins API\n    serviceCategory: API\n  - name: Microsoft Graph People API\n    baseURL: https://graph.microsoft.com/v1.0\n    tags:\n      - Contacts\n      - Directory\n      - People\n      - Social\n    serviceName: Microsoft Graph People API\n    serviceCategory: API\n  - name: Microsoft Graph Change Notifications API\n    baseURL: https://graph.microsoft.com/v1.0\n    tags:\n      - Events\n      - Notifications\n      - Subscriptions\n      - Webhooks\n    serviceName: Microsoft Graph Change Notifications\
  \ API\n    serviceCategory: API\n  - name: Microsoft Graph Focused Inbox API\n    baseURL: https://graph.microsoft.com/v1.0\n    tags:\n      - Classification\n      - Email Organization\n      - Focused Inbox\n    serviceName: Microsoft Graph Focused Inbox API\n    serviceCategory: API\n  - name: Microsoft Graph Mail Rules API\n    baseURL: https://graph.microsoft.com/v1.0\n    tags:\n      - Email Automation\n      - Filters\n      - Inbox Rules\n      - Rules\n    serviceName: Microsoft Graph Mail Rules API\n    serviceCategory: API\n  - name: Microsoft Graph Categories API\n    baseURL: https://graph.microsoft.com/v1.0\n    tags:\n      - Categories\n      - Labels\n      - Organization\n    serviceName: Microsoft Graph Categories API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n\
  \  - FN: Kin Lane\n    email: kin@apievangelist.com\n    url: https://apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/microsoft-outlook/refs/heads/main/finops/microsoft-outlook-finops.yml
sources: []
specification: FinOps Framework
tags:
- Calendar
- Contacts
- Email
- Enterprise
- Microsoft
- Office 365
- Productivity
- FinOps
- Cost Management
- FOCUS
---
