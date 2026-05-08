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
description: FinOps framework definition for the Microsoft Applications APIs API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Microsoft Applications APIs
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Microsoft Applications APIs
  PublisherName: Microsoft Applications APIs
  ServiceCategory: Developer Tools / API
  ServiceName: Microsoft Applications APIs
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
name: Ms Applications Finops
provider_name: Microsoft Applications APIs
provider_slug: ms-applications
publisher_name: Microsoft Applications APIs
service_category: API
slug: ms-applications-finops
source_filename: ms-applications-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Microsoft Applications APIs\nproviderId: ms-applications\npublisherName: Microsoft Applications APIs\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Cloud\n  - Enterprise\n  - Microsoft\n  - Microsoft-365\n  - Office\n  - Productivity\n  - Saas\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Microsoft Applications APIs API surface. Provides a FOCUS-aligned\n  mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n\
  \  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and\
  \ SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Microsoft Applications APIs\n  ServiceCategory: Developer Tools / API\n  ProviderName: Microsoft Applications APIs\n  PublisherName: Microsoft Applications APIs\n  InvoiceIssuerName: Microsoft Applications APIs\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n    \
  \  - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Microsoft Graph API\n    baseURL: https://graph.microsoft.com\n    tags:\n      - Cloud\n      - Collaboration\n      - Identity\n      - Productivity\n    serviceName: Microsoft Graph API\n    serviceCategory: API\n  - name: Microsoft Teams API\n    baseURL: https://graph.microsoft.com/v1.0/teams\n    tags:\n      - Chat\n      - Collaboration\n      - Meetings\n      - Productivity\n    serviceName: Microsoft Teams API\n    serviceCategory: API\n  - name: Outlook Mail API\n    baseURL: https://graph.microsoft.com/v1.0/me/messages\n    tags:\n  \
  \    - Email\n      - Messaging\n      - Productivity\n    serviceName: Outlook Mail API\n    serviceCategory: API\n  - name: OneDrive API\n    baseURL: https://graph.microsoft.com/v1.0/me/drive\n    tags:\n      - Cloud\n      - Collaboration\n      - Files\n      - Storage\n    serviceName: OneDrive API\n    serviceCategory: API\n  - name: SharePoint API\n    baseURL: https://graph.microsoft.com/v1.0/sites\n    tags:\n      - Collaboration\n      - Content Management\n      - Enterprise\n      - Intranet\n    serviceName: SharePoint API\n    serviceCategory: API\n  - name: Azure Active Directory API\n    baseURL: https://graph.microsoft.com/v1.0/users\n    tags:\n      - Authentication\n      - Authorization\n      - Identity\n      - Security\n    serviceName: Azure Active Directory API\n    serviceCategory: API\n  - name: Microsoft To Do API\n    baseURL: https://graph.microsoft.com/v1.0/me/todo\n    tags:\n      - Planning\n      - Productivity\n      - Tasks\n    serviceName: Microsoft\
  \ To Do API\n    serviceCategory: API\n  - name: Microsoft Planner API\n    baseURL: https://graph.microsoft.com/v1.0/planner\n    tags:\n      - Collaboration\n      - Productivity\n      - Project Management\n      - Tasks\n    serviceName: Microsoft Planner API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/ms-applications/refs/heads/main/finops/ms-applications-finops.yml
sources: []
specification: FinOps Framework
tags:
- Cloud
- Enterprise
- Microsoft
- Microsoft-365
- Office
- Productivity
- Saas
- FinOps
- Cost Management
- FOCUS
---
