---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: overview
  format: yaml
  label: Microsoft Graph API
  slug: ''
  spec_type: OpenAPI
  url: https://learn.microsoft.com/en-us/graph/api/overview
- filename: microsoft-azure-rest-openapi.yml
  format: yaml
  label: Azure REST API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft/refs/heads/main/openapi/microsoft-azure-rest-openapi.yml
- filename: microsoft-azure-openai-openapi.yml
  format: yaml
  label: Azure OpenAI Service API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft/refs/heads/main/openapi/microsoft-azure-openai-openapi.yml
- filename: microsoft-azure-cognitive-services-openapi.yml
  format: yaml
  label: Azure Cognitive Services API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft/refs/heads/main/openapi/microsoft-azure-cognitive-services-openapi.yml
- filename: microsoft-teams-openapi.yml
  format: yaml
  label: Microsoft Teams API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft/refs/heads/main/openapi/microsoft-teams-openapi.yml
- filename: microsoft-onedrive-openapi.yml
  format: yaml
  label: OneDrive API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft/refs/heads/main/openapi/microsoft-onedrive-openapi.yml
- filename: microsoft-power-platform-openapi.yml
  format: yaml
  label: Power Platform API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft/refs/heads/main/openapi/microsoft-power-platform-openapi.yml
- filename: microsoft-bing-search-openapi.yml
  format: yaml
  label: Bing Search APIs
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft/refs/heads/main/openapi/microsoft-bing-search-openapi.yml
- filename: microsoft-sharepoint-openapi.yml
  format: yaml
  label: SharePoint REST API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft/refs/heads/main/openapi/microsoft-sharepoint-openapi.yml
- filename: microsoft-power-bi-openapi.yml
  format: yaml
  label: Power BI REST API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft/refs/heads/main/openapi/microsoft-power-bi-openapi.yml
- filename: microsoft-azure-devops-openapi.yml
  format: yaml
  label: Azure DevOps REST API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft/refs/heads/main/openapi/microsoft-azure-devops-openapi.yml
- filename: microsoft-dynamics-365-openapi.yml
  format: yaml
  label: Dynamics 365 REST API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft/refs/heads/main/openapi/microsoft-dynamics-365-openapi.yml
- filename: microsoft-linkedin-openapi.yml
  format: yaml
  label: LinkedIn API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft/refs/heads/main/openapi/microsoft-linkedin-openapi.yml
- filename: microsoft-azure-communication-services-openapi.yml
  format: yaml
  label: Azure Communication Services API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft/refs/heads/main/openapi/microsoft-azure-communication-services-openapi.yml
- filename: microsoft-entra-id-openapi.yml
  format: yaml
  label: Microsoft Entra ID API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft/refs/heads/main/openapi/microsoft-entra-id-openapi.yml
- filename: microsoft-outlook-openapi.yml
  format: yaml
  label: Microsoft Outlook API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft/refs/heads/main/openapi/microsoft-outlook-openapi.yml
- filename: microsoft-intune-openapi.yml
  format: yaml
  label: Microsoft Intune API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft/refs/heads/main/openapi/microsoft-intune-openapi.yml
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
description: FinOps framework definition for the Microsoft API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Microsoft
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Microsoft
  PublisherName: Microsoft
  ServiceCategory: Developer Tools / API
  ServiceName: Microsoft
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
name: Microsoft Finops
provider_name: Microsoft
provider_slug: microsoft
publisher_name: Microsoft
service_category: API
slug: microsoft-finops
source_filename: microsoft-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Microsoft\nproviderId: microsoft\npublisherName: Microsoft\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Microsoft API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be\
  \ allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing\
  \ and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Microsoft\n  ServiceCategory: Developer Tools / API\n  ProviderName: Microsoft\n  PublisherName: Microsoft\n  InvoiceIssuerName: Microsoft\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n\
  \    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Microsoft Graph API\n    baseURL: https://graph.microsoft.com\n    tags:\n      - Azure AD\n      - Office 365\n      - OneDrive\n      - Outlook\n      - Teams\n    serviceName: Microsoft Graph API\n    serviceCategory: API\n  - name: Azure REST API\n    baseURL: https://management.azure.com\n    tags:\n      - Azure\n      - Cloud\n      - Infrastructure\n      - Resources\n    serviceName: Azure REST API\n    serviceCategory: API\n  - name: Azure OpenAI Service API\n    baseURL: https://{resource-name}.openai.azure.com\n    tags:\n      - AI\n      - GPT\n      - Machine Learning\n      - OpenAI\n    serviceName: Azure OpenAI Service API\n    serviceCategory: API\n  - name: Azure Cognitive Services API\n    baseURL: https://{region}.api.cognitive.microsoft.com\n    tags:\n      - AI\n \
  \     - Computer Vision\n      - Language\n      - Machine Learning\n      - Speech\n    serviceName: Azure Cognitive Services API\n    serviceCategory: API\n  - name: Microsoft Teams API\n    baseURL: https://graph.microsoft.com/v1.0/teams\n    tags:\n      - Chat\n      - Collaboration\n      - Messaging\n      - Teams\n    serviceName: Microsoft Teams API\n    serviceCategory: API\n  - name: OneDrive API\n    baseURL: https://graph.microsoft.com/v1.0/me/drive\n    tags:\n      - Files\n      - OneDrive\n      - SharePoint\n      - Storage\n    serviceName: OneDrive API\n    serviceCategory: API\n  - name: Power Platform API\n    baseURL: https://api.powerplatform.com\n    tags:\n      - Automation\n      - Business Intelligence\n      - Low Code\n      - Power Apps\n    serviceName: Power Platform API\n    serviceCategory: API\n  - name: Bing Search APIs\n    baseURL: https://api.bing.microsoft.com/v7.0\n    tags:\n      - Bing\n      - Image Search\n      - Search\n      - Web Search\n\
  \    serviceName: Bing Search APIs\n    serviceCategory: API\n  - name: SharePoint REST API\n    baseURL: https://{tenant}.sharepoint.com/_api\n    tags:\n      - Collaboration\n      - Content Management\n      - Documents\n      - SharePoint\n    serviceName: SharePoint REST API\n    serviceCategory: API\n  - name: Power BI REST API\n    baseURL: https://api.powerbi.com/v1.0/myorg\n    tags:\n      - Analytics\n      - Business Intelligence\n      - Dashboards\n      - Reports\n    serviceName: Power BI REST API\n    serviceCategory: API\n  - name: Azure DevOps REST API\n    baseURL: https://dev.azure.com/{organization}/_apis\n    tags:\n      - CI/CD\n      - DevOps\n      - Git\n      - Pipelines\n      - Work Items\n    serviceName: Azure DevOps REST API\n    serviceCategory: API\n  - name: Dynamics 365 REST API\n    baseURL: https://{org}.api.crm.dynamics.com/api/data/v9.2\n    tags:\n      - Business Applications\n      - CRM\n      - Dynamics\n      - ERP\n    serviceName: Dynamics\
  \ 365 REST API\n    serviceCategory: API\n  - name: LinkedIn API\n    baseURL: https://api.linkedin.com/v2\n    tags:\n      - Marketing\n      - Professional Network\n      - Recruiting\n      - Social\n    serviceName: LinkedIn API\n    serviceCategory: API\n  - name: Azure Communication Services API\n    baseURL: https://{resource}.communication.azure.com\n    tags:\n      - Chat\n      - Communication\n      - Email\n      - SMS\n      - Video\n      - Voice\n    serviceName: Azure Communication Services API\n    serviceCategory: API\n  - name: Microsoft Entra ID API\n    baseURL: https://graph.microsoft.com/v1.0\n    tags:\n      - Authentication\n      - Authorization\n      - Directory\n      - Identity\n      - Security\n    serviceName: Microsoft Entra ID API\n    serviceCategory: API\n  - name: Microsoft Outlook API\n    baseURL: https://graph.microsoft.com/v1.0/me\n    tags:\n      - Calendar\n      - Contacts\n      - Email\n      - Outlook\n    serviceName: Microsoft Outlook\
  \ API\n    serviceCategory: API\n  - name: Microsoft Intune API\n    baseURL: https://graph.microsoft.com/v1.0\n    tags:\n      - Compliance\n      - Device Management\n      - Endpoint Management\n      - Mobile\n    serviceName: Microsoft Intune API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - name: Kin Lane\n    email: kin@apievangelist.com\n    url: https://apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/microsoft/refs/heads/main/finops/microsoft-finops.yml
sources: []
specification: FinOps Framework
tags:
- FinOps
- Cost Management
- FOCUS
---
