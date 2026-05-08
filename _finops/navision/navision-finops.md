---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: nav-webservices.yaml
  format: yaml
  label: Dynamics NAV Web Services API
  slug: ''
  spec_type: OpenAPI
  url: https://example.com/openapi/nav-webservices.yaml
- filename: nav-odata.yaml
  format: yaml
  label: Dynamics NAV OData API
  slug: ''
  spec_type: OpenAPI
  url: https://example.com/openapi/nav-odata.yaml
- filename: business-central-api-v2.yml
  format: yaml
  label: Business Central API v2.0
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/navision/refs/heads/main/openapi/business-central-api-v2.yml
- filename: admin-center-api.yml
  format: yaml
  label: Business Central Administration Center API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/navision/refs/heads/main/openapi/admin-center-api.yml
- filename: automation-api.yml
  format: yaml
  label: Business Central Automation API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/navision/refs/heads/main/openapi/automation-api.yml
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
description: FinOps framework definition for the Microsoft Dynamics NAV API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Microsoft Dynamics NAV
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Microsoft Dynamics NAV
  PublisherName: Microsoft Dynamics NAV
  ServiceCategory: Developer Tools / API
  ServiceName: Microsoft Dynamics NAV
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
name: Navision Finops
provider_name: Microsoft Dynamics NAV
provider_slug: navision
publisher_name: Microsoft Dynamics NAV
service_category: API
slug: navision-finops
source_filename: navision-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Microsoft Dynamics NAV\nproviderId: navision\npublisherName: Microsoft Dynamics NAV\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Business Management\n  - Dynamics NAV\n  - ERP\n  - Finance\n  - Inventory\n  - Microsoft\n  - Navision\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Microsoft Dynamics NAV API surface. Provides a FOCUS-aligned\n  mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name:\
  \ Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  -\
  \ name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Microsoft Dynamics NAV\n  ServiceCategory: Developer Tools / API\n  ProviderName: Microsoft Dynamics NAV\n  PublisherName: Microsoft Dynamics NAV\n  InvoiceIssuerName: Microsoft Dynamics NAV\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n\
  \  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Dynamics NAV Web Services API\n    baseURL: https://{server}:{port}/{instance}/api/{version}\n    tags:\n      - Enterprise Resource Planning\n      - OData\n      - SOAP\n      - Web Services\n    serviceName: Dynamics NAV Web Services API\n    serviceCategory: API\n  - name: Dynamics NAV OData API\n    baseURL: https://{server}:{port}/{instance}/OData/Company('{company}')\n    tags:\n      - Business Data\n      - Data Integration\n      - OData\n      - Queries\n    serviceName: Dynamics NAV OData API\n    serviceCategory: API\n  - name: Dynamics NAV SOAP Web Services\n   \
  \ baseURL: https://{server}:{port}/{instance}/WS/{company}/\n    tags:\n      - Business Logic\n      - Codeunits\n      - Legacy Integration\n      - SOAP\n    serviceName: Dynamics NAV SOAP Web Services\n    serviceCategory: API\n  - name: Business Central API v2.0\n    baseURL: https://api.businesscentral.dynamics.com/v2.0/{environment}/api/v2.0\n    tags:\n      - Business Central\n      - Business Data\n      - Cloud ERP\n      - Connect Apps\n      - REST API\n    serviceName: Business Central API v2.0\n    serviceCategory: API\n  - name: Business Central Administration Center API\n    baseURL: https://api.businesscentral.dynamics.com/admin/v2.28\n    tags:\n      - Administration\n      - Cloud ERP\n      - Environment Management\n      - Tenant Management\n    serviceName: Business Central Administration Center API\n    serviceCategory: API\n  - name: Business Central Automation API\n    baseURL: https://api.businesscentral.dynamics.com/v2.0/{environment}/api/microsoft/automation/v2.0\n\
  \    tags:\n      - Automation\n      - Extension Management\n      - Tenant Management\n      - User Management\n    serviceName: Business Central Automation API\n    serviceCategory: API\n  - name: Business Central REST API Web Services\n    baseURL: https://api.businesscentral.dynamics.com/v2.0/{environment}/api\n    tags:\n      - Business Central\n      - Custom APIs\n      - Data Integration\n      - REST API\n      - Web Services\n    serviceName: Business Central REST API Web Services\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/navision/refs/heads/main/finops/navision-finops.yml
sources: []
specification: FinOps Framework
tags:
- Business Management
- Dynamics NAV
- ERP
- Finance
- Inventory
- Microsoft
- Navision
- FinOps
- Cost Management
- FOCUS
---
