---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: helpscout-openapi.yml
  format: yaml
  label: Help Scout Conversations API
  slug: helpscout-conversations-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/helpscout/refs/heads/main/openapi/helpscout-openapi.yml
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
description: FinOps framework definition for the Help Scout API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Help Scout
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Help Scout
  PublisherName: Help Scout
  ServiceCategory: Developer Tools / API
  ServiceName: Help Scout
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
name: Helpscout Finops
provider_name: Help Scout
provider_slug: helpscout
publisher_name: Help Scout
service_category: API
slug: helpscout-finops
source_filename: helpscout-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Help Scout\nproviderId: helpscout\npublisherName: Help Scout\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Customer Support\n  - Help Desk\n  - Email\n  - Live Chat\n  - Knowledge Base\n  - SaaS\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Help Scout API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable\
  \ API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n\
  \      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Help Scout\n  ServiceCategory: Developer Tools / API\n  ProviderName: Help Scout\n  PublisherName: Help Scout\n  InvoiceIssuerName: Help Scout\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n\
  \    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Help Scout Conversations API\n    baseURL: ''\n    tags:\n      - Conversations\n      - Threads\n      - Tickets\n    serviceName: Help Scout Conversations API\n    serviceCategory: API\n  - name: Help Scout Threads API\n    baseURL: ''\n    tags:\n      - Threads\n      - Replies\n    serviceName: Help Scout Threads API\n    serviceCategory: API\n  - name: Help Scout Customers API\n    baseURL: ''\n    tags:\n      - Customers\n      - Contacts\n    serviceName: Help Scout Customers API\n    serviceCategory: API\n  - name: Help Scout Mailboxes API\n    baseURL: ''\n    tags:\n      - Mailboxes\n      - Inboxes\n    serviceName: Help Scout Mailboxes API\n    serviceCategory: API\n\
  \  - name: Help Scout Users API\n    baseURL: ''\n    tags:\n      - Users\n      - Agents\n    serviceName: Help Scout Users API\n    serviceCategory: API\n  - name: Help Scout Teams API\n    baseURL: ''\n    tags:\n      - Teams\n    serviceName: Help Scout Teams API\n    serviceCategory: API\n  - name: Help Scout Tags API\n    baseURL: ''\n    tags:\n      - Tags\n      - Categorization\n    serviceName: Help Scout Tags API\n    serviceCategory: API\n  - name: Help Scout Workflows API\n    baseURL: ''\n    tags:\n      - Workflows\n      - Automation\n    serviceName: Help Scout Workflows API\n    serviceCategory: API\n  - name: Help Scout Custom Fields API\n    baseURL: ''\n    tags:\n      - Custom Fields\n      - Metadata\n    serviceName: Help Scout Custom Fields API\n    serviceCategory: API\n  - name: Help Scout Attachments API\n    baseURL: ''\n    tags:\n      - Attachments\n      - Files\n    serviceName: Help Scout Attachments API\n    serviceCategory: API\n  - name: Help\
  \ Scout Ratings API\n    baseURL: ''\n    tags:\n      - Ratings\n      - Happiness\n      - CSAT\n    serviceName: Help Scout Ratings API\n    serviceCategory: API\n  - name: Help Scout Reports API\n    baseURL: ''\n    tags:\n      - Reports\n      - Analytics\n    serviceName: Help Scout Reports API\n    serviceCategory: API\n  - name: Help Scout Webhooks API\n    baseURL: ''\n    tags:\n      - Webhooks\n      - Events\n    serviceName: Help Scout Webhooks API\n    serviceCategory: API\n  - name: Help Scout Docs API\n    baseURL: ''\n    tags:\n      - Docs\n      - Knowledge Base\n      - Articles\n    serviceName: Help Scout Docs API\n    serviceCategory: API\n  - name: Help Scout Beacon API\n    baseURL: ''\n    tags:\n      - Beacon\n      - Live Chat\n      - Embed\n    serviceName: Help Scout Beacon API\n    serviceCategory: API\n  - name: Help Scout Chat API\n    baseURL: ''\n    tags:\n      - Chat\n      - Live Chat\n    serviceName: Help Scout Chat API\n    serviceCategory:\
  \ API\n  - name: Help Scout Apps API\n    baseURL: ''\n    tags:\n      - Apps\n      - Sidebar\n      - Marketplace\n    serviceName: Help Scout Apps API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/helpscout/refs/heads/main/finops/helpscout-finops.yml
sources: []
specification: FinOps Framework
tags:
- Customer Support
- Help Desk
- Email
- Live Chat
- Knowledge Base
- SaaS
- FinOps
- Cost Management
- FOCUS
---
