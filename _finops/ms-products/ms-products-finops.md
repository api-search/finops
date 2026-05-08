---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: ms-products-openapi.yml
  format: yaml
  label: Microsoft Graph API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/ms-products/refs/heads/main/openapi/ms-products-openapi.yml
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
description: FinOps framework definition for the Microsoft Products APIs API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Microsoft Products APIs
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Microsoft Products APIs
  PublisherName: Microsoft Products APIs
  ServiceCategory: Developer Tools / API
  ServiceName: Microsoft Products APIs
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
name: Ms Products Finops
provider_name: Microsoft Products APIs
provider_slug: ms-products
publisher_name: Microsoft Products APIs
service_category: API
slug: ms-products-finops
source_filename: ms-products-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Microsoft Products APIs\nproviderId: ms-products\npublisherName: Microsoft Products APIs\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Azure\n  - Cloud\n  - Enterprise\n  - Microsoft\n  - Office 365\n  - Productivity\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Microsoft Products APIs API surface. Provides a FOCUS-aligned\n  mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n\
  \    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage\
  \ the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Microsoft Products APIs\n  ServiceCategory: Developer Tools / API\n  ProviderName: Microsoft Products APIs\n  PublisherName: Microsoft Products APIs\n  InvoiceIssuerName: Microsoft Products APIs\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name:\
  \ data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Microsoft Graph API\n    baseURL: https://graph.microsoft.com/v1.0\n    tags:\n      - Azure AD\n      - Microsoft 365\n      - Office\n      - OneDrive\n      - Outlook\n      - Teams\n    serviceName: Microsoft Graph API\n    serviceCategory: API\n  - name: Azure REST API\n    baseURL: ''\n    tags:\n      - Azure\n      - Cloud\n      - Infrastructure\n      - Resource Management\n    serviceName: Azure REST API\n    serviceCategory: API\n  - name: Office 365 APIs\n    baseURL: ''\n    tags:\n      - Calendar\n      - Email\n      - Office 365\n      - Outlook\n    serviceName: Office\
  \ 365 APIs\n    serviceCategory: API\n  - name: Microsoft Teams API\n    baseURL: ''\n    tags:\n      - Chat\n      - Collaboration\n      - Meetings\n      - Teams\n    serviceName: Microsoft Teams API\n    serviceCategory: API\n  - name: OneDrive API\n    baseURL: ''\n    tags:\n      - Files\n      - OneDrive\n      - SharePoint\n      - Storage\n    serviceName: OneDrive API\n    serviceCategory: API\n  - name: Power Platform APIs\n    baseURL: ''\n    tags:\n      - Low Code\n      - Power Apps\n      - Power Automate\n      - Power BI\n      - Power Platform\n    serviceName: Power Platform APIs\n    serviceCategory: API\n  - name: Azure Cognitive Services API\n    baseURL: ''\n    tags:\n      - AI\n      - Computer Vision\n      - Machine Learning\n      - NLP\n      - Speech\n    serviceName: Azure Cognitive Services API\n    serviceCategory: API\n  - name: Dynamics 365 API\n    baseURL: ''\n    tags:\n      - Business Applications\n      - CRM\n      - Dynamics 365\n      -\
  \ ERP\n    serviceName: Dynamics 365 API\n    serviceCategory: API\n  - name: Microsoft 365 Defender API\n    baseURL: ''\n    tags:\n      - Defender\n      - Incidents\n      - Security\n      - Threat Protection\n    serviceName: Microsoft 365 Defender API\n    serviceCategory: API\n  - name: Xbox Live API\n    baseURL: ''\n    tags:\n      - Achievements\n      - Gaming\n      - Social\n      - Xbox\n    serviceName: Xbox Live API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/ms-products/refs/heads/main/finops/ms-products-finops.yml
sources: []
specification: FinOps Framework
tags:
- Azure
- Cloud
- Enterprise
- Microsoft
- Office 365
- Productivity
- FinOps
- Cost Management
- FOCUS
---
