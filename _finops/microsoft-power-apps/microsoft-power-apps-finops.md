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
  label: Power Apps API
  slug: ''
  spec_type: OpenAPI
  url: https://docs.microsoft.com/en-us/connectors/powerappsforappmakers/
- filename: openapi
  format: yaml
  label: Dataverse API (Common Data Service)
  slug: ''
  spec_type: OpenAPI
  url: https://docs.microsoft.com/en-us/power-apps/developer/data-platform/webapi/openapi
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
description: FinOps framework definition for the Microsoft Power Apps API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Microsoft Power Apps
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Microsoft Power Apps
  PublisherName: Microsoft Power Apps
  ServiceCategory: Developer Tools / API
  ServiceName: Microsoft Power Apps
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
name: Microsoft Power Apps Finops
provider_name: Microsoft Power Apps
provider_slug: microsoft-power-apps
publisher_name: Microsoft Power Apps
service_category: API
slug: microsoft-power-apps-finops
source_filename: microsoft-power-apps-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Microsoft Power Apps\nproviderId: microsoft-power-apps\npublisherName: Microsoft Power Apps\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Business Applications\n  - Cloud\n  - Enterprise\n  - Low-Code\n  - Microsoft\n  - No-Code\n  - Power Platform\n  - SaaS\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Microsoft Power Apps API surface. Provides a FOCUS-aligned\n  mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n \
  \     real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n    \
  \  - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Microsoft Power Apps\n  ServiceCategory: Developer Tools / API\n  ProviderName: Microsoft Power Apps\n  PublisherName: Microsoft Power Apps\n  InvoiceIssuerName: Microsoft Power Apps\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n\
  \      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Power Apps API\n    baseURL: https://api.powerapps.com\n    tags:\n      - Applications\n      - Development\n      - Low-Code\n      - Power Platform\n    serviceName: Power Apps API\n    serviceCategory: API\n  - name: Dataverse API (Common Data Service)\n    baseURL: https://[organization].api.crm.dynamics.com/api/data/v9.2\n    tags:\n      - CRM\n      - Data Platform\n      - Database\n      - REST API\n    serviceName: Dataverse API (Common Data Service)\n    serviceCategory: API\n  - name: Power Apps Management API\n    baseURL: https://api.bap.microsoft.com\n\
  \    tags:\n      - Administration\n      - Environments\n      - Governance\n      - Management\n    serviceName: Power Apps Management API\n    serviceCategory: API\n  - name: Power Apps Connectors API\n    baseURL: https://api.powerapps.com/providers/Microsoft.PowerApps\n    tags:\n      - Connectors\n      - Custom Connectors\n      - Integration\n    serviceName: Power Apps Connectors API\n    serviceCategory: API\n  - name: Power Apps Canvas Apps API\n    baseURL: https://api.powerapps.com\n    tags:\n      - Canvas Apps\n      - Low-Code\n      - Mobile\n      - UI\n    serviceName: Power Apps Canvas Apps API\n    serviceCategory: API\n  - name: Power Apps Model-driven Apps API\n    baseURL: https://[organization].crm.dynamics.com\n    tags:\n      - Business Logic\n      - Forms\n      - Model-Driven Apps\n      - Views\n    serviceName: Power Apps Model-driven Apps API\n    serviceCategory: API\n  - name: Power Apps Component Framework (PCF) API\n    baseURL: https://api.powerapps.com\n\
  \    tags:\n      - Code Components\n      - Component Framework\n      - Custom Controls\n      - PCF\n      - TypeScript\n    serviceName: Power Apps Component Framework (PCF) API\n    serviceCategory: API\n  - name: Power Platform REST API\n    baseURL: https://api.powerplatform.com\n    tags:\n      - Administration\n      - Environments\n      - Governance\n      - Licensing\n      - REST API\n    serviceName: Power Platform REST API\n    serviceCategory: API\n  - name: Power Pages Web API\n    baseURL: https://[site-url]/_api\n    tags:\n      - CRUD\n      - External Users\n      - Portals\n      - Power Pages\n      - Web API\n    serviceName: Power Pages Web API\n    serviceCategory: API\n  - name: Dataverse Organization Service SDK\n    baseURL: https://[organization].api.crm.dynamics.com\n    tags:\n      - .NET\n      - Organization Service\n      - Plugins\n      - SDK\n      - Server-Side\n    serviceName: Dataverse Organization Service SDK\n    serviceCategory: API\n  -\
  \ name: Power Apps Code Apps API\n    baseURL: https://api.powerapps.com\n    tags:\n      - Code Apps\n      - Code-First\n      - Pro Developer\n      - React\n      - Vue\n    serviceName: Power Apps Code Apps API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/microsoft-power-apps/refs/heads/main/finops/microsoft-power-apps-finops.yml
sources: []
specification: FinOps Framework
tags:
- Business Applications
- Cloud
- Enterprise
- Low-Code
- Microsoft
- No-Code
- Power Platform
- SaaS
- FinOps
- Cost Management
- FOCUS
---
