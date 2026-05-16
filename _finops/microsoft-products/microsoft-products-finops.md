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
  slug: microsoft-graph-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/microsoftgraph/msgraph-metadata/master/openapi/v1.0/openapi.yaml
- filename: azure-rest-api-specs
  format: yaml
  label: Azure REST API
  slug: azure-rest-api
  spec_type: OpenAPI
  url: https://github.com/Azure/azure-rest-api-specs
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
description: FinOps framework definition for the Microsoft Products API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Microsoft Products
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Microsoft Products
  PublisherName: Microsoft Products
  ServiceCategory: Developer Tools / API
  ServiceName: Microsoft Products
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
name: Microsoft Products Finops
provider_name: Microsoft Products
provider_slug: microsoft-products
publisher_name: Microsoft Products
service_category: API
slug: microsoft-products-finops
source_filename: microsoft-products-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Microsoft Products\nproviderId: microsoft-products\npublisherName: Microsoft Products\nserviceCategory: API\ncreated: '2026-05-04'\nmodified: '2026-05-04'\ntags:\n  - Cloud\n  - Enterprise\n  - Microsoft\n  - Productivity\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Microsoft Products API surface. Provides a FOCUS-aligned\n  mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable\
  \ API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n\
  \      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Microsoft Products\n  ServiceCategory: Developer Tools / API\n  ProviderName: Microsoft Products\n  PublisherName: Microsoft Products\n  InvoiceIssuerName: Microsoft Products\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network\
  \ in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Microsoft Graph API\n    baseURL: ''\n    tags:\n      - Azure-Ad\n      - Graph\n      - Microsoft-365\n      - Unified-Api\n    serviceName: Microsoft Graph API\n    serviceCategory: API\n  - name: Azure REST API\n    baseURL: ''\n    tags:\n      - Azure\n      - Cloud\n      - Iaas\n      - Infrastructure\n      - Paas\n    serviceName: Azure REST API\n    serviceCategory: API\n  - name: Microsoft 365 API\n    baseURL: ''\n    tags:\n      - Collaboration\n      - Exchange\n      - Office-365\n      - Productivity\n      - Sharepoint\n    serviceName: Microsoft 365 API\n    serviceCategory: API\n  - name: Microsoft Teams API\n    baseURL: ''\n\
  \    tags:\n      - Chat\n      - Collaboration\n      - Meetings\n      - Teams\n    serviceName: Microsoft Teams API\n    serviceCategory: API\n  - name: Azure Cognitive Services API\n    baseURL: ''\n    tags:\n      - Ai\n      - Cognitive-Services\n      - Computer-Vision\n      - Machine-Learning\n      - Nlp\n    serviceName: Azure Cognitive Services API\n    serviceCategory: API\n  - name: Power Platform API\n    baseURL: ''\n    tags:\n      - Automation\n      - Business-Intelligence\n      - Low-Code\n      - Power-Platform\n    serviceName: Power Platform API\n    serviceCategory: API\n  - name: Dynamics 365 API\n    baseURL: ''\n    tags:\n      - Business-Applications\n      - Crm\n      - Dynamics\n      - Erp\n    serviceName: Dynamics 365 API\n    serviceCategory: API\n  - name: Xbox Live API\n    baseURL: ''\n    tags:\n      - Achievements\n      - Gaming\n      - Multiplayer\n      - Xbox\n    serviceName: Xbox Live API\n    serviceCategory: API\nunitEconomics:\n  -\
  \ name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/microsoft-products/refs/heads/main/finops/microsoft-products-finops.yml
sources: []
specification: FinOps Framework
tags:
- Cloud
- Enterprise
- Microsoft
- Productivity
- FinOps
- Cost Management
- FOCUS
---
