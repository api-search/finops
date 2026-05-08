---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: v1
  format: yaml
  label: Power Apps API
  slug: ''
  spec_type: OpenAPI
  url: https://api.powerapps.com/openapi/v1
- filename: v1
  format: yaml
  label: Power Automate API
  slug: ''
  spec_type: OpenAPI
  url: https://api.flow.microsoft.com/openapi/v1
- filename: swagger.json
  format: json
  label: Power BI REST API
  slug: ''
  spec_type: OpenAPI
  url: https://api.powerbi.com/v1.0/myorg/swagger.json
- filename: power-platform-api-openapi.json
  format: json
  label: Power Platform Unified API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/power-platform/refs/heads/main/openapi/power-platform-api-openapi.json
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
description: FinOps framework definition for the Microsoft Power Platform APIs API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Microsoft Power Platform APIs
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Microsoft Power Platform APIs
  PublisherName: Microsoft Power Platform APIs
  ServiceCategory: Developer Tools / API
  ServiceName: Microsoft Power Platform APIs
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
name: Power Platform Finops
provider_name: Microsoft Power Platform APIs
provider_slug: power-platform
publisher_name: Microsoft Power Platform APIs
service_category: API
slug: power-platform-finops
source_filename: power-platform-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Microsoft Power Platform APIs\nproviderId: power-platform\npublisherName: Microsoft Power Platform APIs\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Business Applications\n  - Copilot Studio\n  - Dataverse\n  - Low-Code\n  - Microsoft\n  - No-Code\n  - Power Pages\n  - Power Platform\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Microsoft Power Platform APIs API surface. Provides a\n  FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the\n  provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering,\
  \ product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n\
  \      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Microsoft Power Platform APIs\n  ServiceCategory: Developer Tools / API\n  ProviderName: Microsoft Power Platform APIs\n  PublisherName: Microsoft Power Platform APIs\n  InvoiceIssuerName: Microsoft Power Platform APIs\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n\
  \      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Power Apps API\n    baseURL: https://api.powerapps.com\n    tags:\n      - Applications\n      - Canvas Apps\n      - Model-Driven Apps\n      - Power Apps\n    serviceName: Power Apps API\n    serviceCategory: API\n  - name: Dataverse API (Common Data Service)\n    baseURL: https://[org].api.crm.dynamics.com/api/data/v9.2\n    tags:\n      - CDS\n      - Data Platform\n      - Database\n      - Dataverse\n      - OData\n    serviceName: Dataverse API (Common Data Service)\n    serviceCategory: API\n\
  \  - name: Power Automate API\n    baseURL: https://api.flow.microsoft.com\n    tags:\n      - Automation\n      - Desktop Flows\n      - Flow\n      - Power Automate\n      - RPA\n      - Workflow\n    serviceName: Power Automate API\n    serviceCategory: API\n  - name: Power BI REST API\n    baseURL: https://api.powerbi.com\n    tags:\n      - Analytics\n      - Business Intelligence\n      - Dashboards\n      - Embedded Analytics\n      - Power BI\n      - Reporting\n    serviceName: Power BI REST API\n    serviceCategory: API\n  - name: Microsoft Copilot Studio API (formerly Power Virtual Agents)\n    baseURL: https://api.powerva.microsoft.com\n    tags:\n      - AI Agents\n      - Chatbots\n      - Conversational AI\n      - Copilot Studio\n      - Power Virtual Agents\n      - Virtual Agents\n    serviceName: Microsoft Copilot Studio API (formerly Power Virtual Agents)\n    serviceCategory: API\n  - name: Power Platform Admin API\n    baseURL: https://api.bap.microsoft.com\n    tags:\n\
  \      - Administration\n      - Environments\n      - Governance\n      - Licensing\n      - Management\n    serviceName: Power Platform Admin API\n    serviceCategory: API\n  - name: Power Platform Connectors API\n    baseURL: https://api.connectors.microsoft.com\n    tags:\n      - Connectors\n      - Custom Connectors\n      - Integration\n      - OpenAPI\n    serviceName: Power Platform Connectors API\n    serviceCategory: API\n  - name: Power Platform Unified API\n    baseURL: https://api.powerplatform.com\n    tags:\n      - Administration\n      - App Management\n      - Governance\n      - Licensing\n      - Power Platform API\n      - Unified API\n    serviceName: Power Platform Unified API\n    serviceCategory: API\n  - name: Power Pages Web API\n    baseURL: https://[site].powerappsportals.com/_api\n    tags:\n      - Dataverse\n      - Portals\n      - Power Pages\n      - Web API\n      - Websites\n    serviceName: Power Pages Web API\n    serviceCategory: API\nunitEconomics:\n\
  \  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - name: Kin Lane\n    email: kin@apievangelist.com\n    url: https://apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/power-platform/refs/heads/main/finops/power-platform-finops.yml
sources: []
specification: FinOps Framework
tags:
- Business Applications
- Copilot Studio
- Dataverse
- Low-Code
- Microsoft
- No-Code
- Power Pages
- Power Platform
- FinOps
- Cost Management
- FOCUS
---
