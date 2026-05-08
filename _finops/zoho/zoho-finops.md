---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: crm-oas
  format: yaml
  label: Zoho CRM
  slug: zoho-crm
  spec_type: OpenAPI
  url: https://github.com/zoho/crm-oas
- filename: zohodesk-oas
  format: yaml
  label: Zoho Desk
  slug: zoho-desk
  spec_type: OpenAPI
  url: https://github.com/zoho/zohodesk-oas
- filename: analytics-oas
  format: yaml
  label: Zoho Analytics
  slug: zoho-analytics
  spec_type: OpenAPI
  url: https://github.com/zoho/analytics-oas
- filename: bigin-oas
  format: yaml
  label: Zoho Bigin
  slug: zoho-bigin
  spec_type: OpenAPI
  url: https://github.com/zoho/bigin-oas
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
description: FinOps framework definition for the Zoho API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Zoho
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Zoho
  PublisherName: Zoho
  ServiceCategory: Developer Tools / API
  ServiceName: Zoho
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
name: Zoho Finops
provider_name: Zoho
provider_slug: zoho
publisher_name: Zoho
service_category: API
slug: zoho-finops
source_filename: zoho-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Zoho\nproviderId: zoho\npublisherName: Zoho\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Analytics\n  - Collaboration\n  - CRM\n  - Customer Service\n  - Email\n  - Finance\n  - Human Resources\n  - Project Management\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Zoho API surface. Provides a FOCUS-aligned mapping for\n  cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag\
  \ every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n\
  \    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Zoho\n  ServiceCategory: Developer Tools / API\n  ProviderName: Zoho\n  PublisherName: Zoho\n  InvoiceIssuerName: Zoho\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n   \
  \ aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Zoho Inventory\n    baseURL: ''\n    tags:\n      - Inventory\n      - Stock\n      - Warehouse\n    serviceName: Zoho Inventory\n    serviceCategory: API\n  - name: Zoho CRM\n    baseURL: ''\n    tags:\n      - Contacts\n      - CRM\n      - Leads\n      - Sales\n    serviceName: Zoho CRM\n    serviceCategory: API\n  - name: Zoho Books\n    baseURL: ''\n    tags:\n      - Accounting\n      - Books\n      - Finance\n      - Invoices\n    serviceName: Zoho Books\n    serviceCategory: API\n  - name: Zoho Invoice\n    baseURL: ''\n    tags:\n      - Billing\n      - Finance\n      - Invoicing\n    serviceName: Zoho Invoice\n    serviceCategory: API\n  - name: Zoho Billing\n    baseURL:\
  \ ''\n    tags:\n      - Billing\n      - Payments\n      - Subscriptions\n    serviceName: Zoho Billing\n    serviceCategory: API\n  - name: Zoho Expense\n    baseURL: ''\n    tags:\n      - Expense Management\n      - Receipts\n      - Trips\n    serviceName: Zoho Expense\n    serviceCategory: API\n  - name: Zoho Desk\n    baseURL: ''\n    tags:\n      - Customer Support\n      - Help Desk\n      - Tickets\n    serviceName: Zoho Desk\n    serviceCategory: API\n  - name: Zoho People\n    baseURL: ''\n    tags:\n      - Employees\n      - HR\n      - Human Resources\n    serviceName: Zoho People\n    serviceCategory: API\n  - name: Zoho Recruit\n    baseURL: ''\n    tags:\n      - Candidates\n      - Hiring\n      - HR\n      - Recruitment\n    serviceName: Zoho Recruit\n    serviceCategory: API\n  - name: Zoho Projects\n    baseURL: ''\n    tags:\n      - Project Management\n      - Tasks\n      - Time Tracking\n    serviceName: Zoho Projects\n    serviceCategory: API\n  - name: Zoho\
  \ Mail\n    baseURL: ''\n    tags:\n      - Email\n      - Mail\n      - Messaging\n    serviceName: Zoho Mail\n    serviceCategory: API\n  - name: Zoho Sign\n    baseURL: ''\n    tags:\n      - Documents\n      - E-Signatures\n      - Signing\n    serviceName: Zoho Sign\n    serviceCategory: API\n  - name: Zoho Analytics\n    baseURL: ''\n    tags:\n      - Analytics\n      - Business Intelligence\n      - Reporting\n    serviceName: Zoho Analytics\n    serviceCategory: API\n  - name: Zoho Campaigns\n    baseURL: ''\n    tags:\n      - Campaigns\n      - Email Marketing\n      - Marketing Automation\n    serviceName: Zoho Campaigns\n    serviceCategory: API\n  - name: Zoho SalesIQ\n    baseURL: ''\n    tags:\n      - Live Chat\n      - Sales\n      - Visitor Tracking\n    serviceName: Zoho SalesIQ\n    serviceCategory: API\n  - name: Zoho Creator\n    baseURL: ''\n    tags:\n      - Application Development\n      - Custom Apps\n      - Low-Code\n    serviceName: Zoho Creator\n    serviceCategory:\
  \ API\n  - name: Zoho Cliq\n    baseURL: ''\n    tags:\n      - Collaboration\n      - Messaging\n      - Team Chat\n    serviceName: Zoho Cliq\n    serviceCategory: API\n  - name: Zoho Meeting\n    baseURL: ''\n    tags:\n      - Meetings\n      - Video Conferencing\n      - Webinars\n    serviceName: Zoho Meeting\n    serviceCategory: API\n  - name: Zoho Connect\n    baseURL: ''\n    tags:\n      - Collaboration\n      - Social Intranet\n      - Team Communication\n    serviceName: Zoho Connect\n    serviceCategory: API\n  - name: Zoho WorkDrive\n    baseURL: ''\n    tags:\n      - Cloud Storage\n      - Document Management\n      - File Management\n    serviceName: Zoho WorkDrive\n    serviceCategory: API\n  - name: Zoho Sprints\n    baseURL: ''\n    tags:\n      - Agile\n      - Scrum\n      - Sprints\n    serviceName: Zoho Sprints\n    serviceCategory: API\n  - name: Zoho Bookings\n    baseURL: ''\n    tags:\n      - Appointments\n      - Bookings\n      - Scheduling\n    serviceName:\
  \ Zoho Bookings\n    serviceCategory: API\n  - name: Zoho Commerce\n    baseURL: ''\n    tags:\n      - E-Commerce\n      - Online Store\n      - Shopping\n    serviceName: Zoho Commerce\n    serviceCategory: API\n  - name: Zoho Assist\n    baseURL: ''\n    tags:\n      - Remote Access\n      - Remote Support\n      - Screen Sharing\n    serviceName: Zoho Assist\n    serviceCategory: API\n  - name: Zoho BugTracker\n    baseURL: ''\n    tags:\n      - Bug Tracking\n      - Issue Tracking\n      - QA\n    serviceName: Zoho BugTracker\n    serviceCategory: API\n  - name: Zoho Writer\n    baseURL: ''\n    tags:\n      - Documents\n      - Word Processing\n      - Writing\n    serviceName: Zoho Writer\n    serviceCategory: API\n  - name: Zoho Sheet\n    baseURL: ''\n    tags:\n      - Collaboration\n      - Data\n      - Spreadsheets\n    serviceName: Zoho Sheet\n    serviceCategory: API\n  - name: Zoho Calendar\n    baseURL: ''\n    tags:\n      - Calendar\n      - Events\n      - Scheduling\n\
  \    serviceName: Zoho Calendar\n    serviceCategory: API\n  - name: Zoho Vault\n    baseURL: ''\n    tags:\n      - Password Management\n      - Secrets\n      - Security\n    serviceName: Zoho Vault\n    serviceCategory: API\n  - name: Zoho Catalyst\n    baseURL: ''\n    tags:\n      - Application Development\n      - Cloud Platform\n      - Serverless\n    serviceName: Zoho Catalyst\n    serviceCategory: API\n  - name: Zoho Bigin\n    baseURL: ''\n    tags:\n      - CRM\n      - Pipelines\n      - Small Business\n    serviceName: Zoho Bigin\n    serviceCategory: API\n  - name: Zoho ZeptoMail\n    baseURL: ''\n    tags:\n      - Email Delivery\n      - SMTP\n      - Transactional Email\n    serviceName: Zoho ZeptoMail\n    serviceCategory: API\n  - name: Zoho Office Integrator\n    baseURL: ''\n    tags:\n      - Document Editing\n      - Embed\n      - Office Suite\n    serviceName: Zoho Office Integrator\n    serviceCategory: API\n  - name: Zoho PDF Editor\n    baseURL: ''\n    tags:\n\
  \      - Document Editing\n      - PDF\n      - PDF Management\n    serviceName: Zoho PDF Editor\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/zoho/refs/heads/main/finops/zoho-finops.yml
sources: []
specification: FinOps Framework
tags:
- Analytics
- Collaboration
- CRM
- Customer Service
- Email
- Finance
- Human Resources
- Project Management
- FinOps
- Cost Management
- FOCUS
---
