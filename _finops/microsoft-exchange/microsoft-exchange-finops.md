---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: microsoft-exchange-graph-mail-openapi.yml
  format: yaml
  label: Microsoft Graph Mail API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-exchange/refs/heads/main/openapi/microsoft-exchange-graph-mail-openapi.yml
- filename: microsoft-exchange-graph-calendar-openapi.yml
  format: yaml
  label: Microsoft Graph Calendar API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-exchange/refs/heads/main/openapi/microsoft-exchange-graph-calendar-openapi.yml
- filename: microsoft-exchange-graph-contacts-openapi.yml
  format: yaml
  label: Microsoft Graph Contacts API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-exchange/refs/heads/main/openapi/microsoft-exchange-graph-contacts-openapi.yml
- filename: microsoft-exchange-graph-people-openapi.yml
  format: yaml
  label: Microsoft Graph People API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-exchange/refs/heads/main/openapi/microsoft-exchange-graph-people-openapi.yml
- filename: microsoft-exchange-admin-api-openapi.yml
  format: yaml
  label: Exchange Online Admin API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-exchange/refs/heads/main/openapi/microsoft-exchange-admin-api-openapi.yml
- filename: microsoft-exchange-graph-import-export-openapi.yml
  format: yaml
  label: Microsoft Graph Mailbox Import Export API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-exchange/refs/heads/main/openapi/microsoft-exchange-graph-import-export-openapi.yml
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
description: FinOps framework definition for the Microsoft Exchange API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Microsoft Exchange
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Microsoft Exchange
  PublisherName: Microsoft Exchange
  ServiceCategory: Developer Tools / API
  ServiceName: Microsoft Exchange
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
name: Microsoft Exchange Finops
provider_name: Microsoft Exchange
provider_slug: microsoft-exchange
publisher_name: Microsoft Exchange
service_category: API
slug: microsoft-exchange-finops
source_filename: microsoft-exchange-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Microsoft Exchange\nproviderId: microsoft-exchange\npublisherName: Microsoft Exchange\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Calendar\n  - Collaboration\n  - Contacts\n  - Email\n  - Enterprise\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Microsoft Exchange API surface. Provides a FOCUS-aligned\n  mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every\
  \ chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n   \
  \ capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Microsoft Exchange\n  ServiceCategory: Developer Tools / API\n  ProviderName: Microsoft Exchange\n  PublisherName: Microsoft Exchange\n  InvoiceIssuerName: Microsoft Exchange\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned\
  \ over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Microsoft Graph Mail API\n    baseURL: https://graph.microsoft.com/v1.0\n    tags:\n      - Email\n      - Mail\n      - Messaging\n      - Microsoft Graph\n      - REST\n    serviceName: Microsoft Graph Mail API\n    serviceCategory: API\n  - name: Microsoft Graph Calendar API\n    baseURL: https://graph.microsoft.com/v1.0\n    tags:\n      - Calendar\n      - Events\n      - Meetings\n      - Microsoft Graph\n      - Scheduling\n    serviceName: Microsoft Graph Calendar API\n    serviceCategory: API\n  - name: Microsoft Graph Contacts API\n    baseURL: https://graph.microsoft.com/v1.0\n    tags:\n      - Address Book\n      - Contacts\n\
  \      - Microsoft Graph\n      - Outlook\n      - People\n    serviceName: Microsoft Graph Contacts API\n    serviceCategory: API\n  - name: Microsoft Graph People API\n    baseURL: https://graph.microsoft.com/v1.0\n    tags:\n      - Collaboration\n      - Contacts\n      - Microsoft Graph\n      - People\n      - Social Intelligence\n    serviceName: Microsoft Graph People API\n    serviceCategory: API\n  - name: Exchange Web Services (EWS)\n    baseURL: https://outlook.office365.com/EWS/Exchange.asmx\n    tags:\n      - Exchange Server\n      - Legacy\n      - Mailbox\n      - SOAP\n      - Web Services\n    serviceName: Exchange Web Services (EWS)\n    serviceCategory: API\n  - name: Exchange Online PowerShell API\n    baseURL: https://outlook.office365.com/powershell-liveid/\n    tags:\n      - Administration\n      - Automation\n      - Exchange Online\n      - Management\n      - PowerShell\n    serviceName: Exchange Online PowerShell API\n    serviceCategory: API\n  - name: Exchange\
  \ Autodiscover API\n    baseURL: https://outlook.office365.com/autodiscover/autodiscover.svc\n    tags:\n      - Autodiscover\n      - Configuration\n      - Exchange Server\n      - Service Discovery\n      - SOAP\n    serviceName: Exchange Autodiscover API\n    serviceCategory: API\n  - name: Exchange Online Admin API\n    baseURL: https://outlook.office365.com/adminapi/v2.0\n    tags:\n      - Administration\n      - Exchange Online\n      - Management\n      - Permissions\n      - REST\n    serviceName: Exchange Online Admin API\n    serviceCategory: API\n  - name: Microsoft Graph Mailbox Import Export API\n    baseURL: https://graph.microsoft.com/beta\n    tags:\n      - Export\n      - Import\n      - Mailbox\n      - Microsoft Graph\n      - Migration\n    serviceName: Microsoft Graph Mailbox Import Export API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n\
  \    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n    url: https://apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/microsoft-exchange/refs/heads/main/finops/microsoft-exchange-finops.yml
sources: []
specification: FinOps Framework
tags:
- Calendar
- Collaboration
- Contacts
- Email
- Enterprise
- FinOps
- Cost Management
- FOCUS
---
