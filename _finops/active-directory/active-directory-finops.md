---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: active-directory-users-openapi.yaml
  format: yaml
  label: Microsoft Graph Users API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/active-directory/refs/heads/main/openapi/active-directory-users-openapi.yaml
- filename: active-directory-groups-openapi.yaml
  format: yaml
  label: Microsoft Graph Groups API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/active-directory/refs/heads/main/openapi/active-directory-groups-openapi.yaml
- filename: active-directory-applications-openapi.yaml
  format: yaml
  label: Microsoft Graph Applications and Service Principals API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/active-directory/refs/heads/main/openapi/active-directory-applications-openapi.yaml
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
description: FinOps framework definition for the Microsoft Active Directory API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Microsoft Active Directory
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Microsoft Active Directory
  PublisherName: Microsoft Active Directory
  ServiceCategory: Developer Tools / API
  ServiceName: Microsoft Active Directory
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
name: Active Directory Finops
provider_name: Microsoft Active Directory
provider_slug: active-directory
publisher_name: Microsoft Active Directory
service_category: API
slug: active-directory-finops
source_filename: active-directory-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Microsoft Active Directory\nproviderId: active-directory\npublisherName: Microsoft Active Directory\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Active Directory\n  - Authentication\n  - Authorization\n  - Directory Services\n  - Identity Management\n  - Microsoft Entra\n  - Zero Trust\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Microsoft Active Directory API surface. Provides a FOCUS-aligned\n  mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product,\
  \ and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n     \
  \ - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Microsoft Active Directory\n  ServiceCategory: Developer Tools / API\n  ProviderName: Microsoft Active Directory\n  PublisherName: Microsoft Active Directory\n  InvoiceIssuerName: Microsoft Active Directory\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      -\
  \ api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Microsoft Graph Users API\n    baseURL: https://graph.microsoft.com/v1.0\n    tags:\n      - Directory Services\n      - Identity Management\n      - Users\n    serviceName: Microsoft Graph Users API\n    serviceCategory: API\n  - name: Microsoft Graph Groups API\n    baseURL: https://graph.microsoft.com/v1.0\n    tags:\n      - Directory Services\n      - Groups\n      - Identity Management\n    serviceName: Microsoft Graph Groups API\n    serviceCategory: API\n  - name: Microsoft Graph Applications and Service\
  \ Principals API\n    baseURL: https://graph.microsoft.com/v1.0\n    tags:\n      - Applications\n      - Identity Management\n      - OAuth2\n      - Service Principals\n    serviceName: Microsoft Graph Applications and Service Principals API\n    serviceCategory: API\n  - name: Microsoft Graph Devices API\n    baseURL: https://graph.microsoft.com/v1.0\n    tags:\n      - Devices\n      - Endpoint Management\n      - Identity Management\n    serviceName: Microsoft Graph Devices API\n    serviceCategory: API\n  - name: Microsoft Graph Directory Roles and Administrative Units API\n    baseURL: https://graph.microsoft.com/v1.0\n    tags:\n      - Authorization\n      - Directory Services\n      - Role Management\n    serviceName: Microsoft Graph Directory Roles and Administrative Units API\n    serviceCategory: API\n  - name: Microsoft Graph Conditional Access API\n    baseURL: https://graph.microsoft.com/v1.0\n    tags:\n      - Authorization\n      - Conditional Access\n      - Security\n\
  \      - Zero Trust\n    serviceName: Microsoft Graph Conditional Access API\n    serviceCategory: API\n  - name: Microsoft Graph Identity Governance API\n    baseURL: https://graph.microsoft.com/v1.0\n    tags:\n      - Governance\n      - Identity Management\n      - Lifecycle Management\n      - Privileged Identity Management\n    serviceName: Microsoft Graph Identity Governance API\n    serviceCategory: API\n  - name: Microsoft Graph Identity Protection API\n    baseURL: https://graph.microsoft.com/v1.0\n    tags:\n      - Identity Protection\n      - Risk Management\n      - Security\n    serviceName: Microsoft Graph Identity Protection API\n    serviceCategory: API\n  - name: Microsoft Graph Authentication Methods API\n    baseURL: https://graph.microsoft.com/v1.0\n    tags:\n      - Authentication\n      - MFA\n      - Passwordless\n      - Security\n    serviceName: Microsoft Graph Authentication Methods API\n    serviceCategory: API\n  - name: Microsoft Graph Identity and Access\
  \ Reports API\n    baseURL: https://graph.microsoft.com/v1.0\n    tags:\n      - Audit Logs\n      - Compliance\n      - Monitoring\n      - Reports\n    serviceName: Microsoft Graph Identity and Access Reports API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - name: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/active-directory/refs/heads/main/finops/active-directory-finops.yml
sources: []
specification: FinOps Framework
tags:
- Active Directory
- Authentication
- Authorization
- Directory Services
- Identity Management
- Microsoft Entra
- Zero Trust
- FinOps
- Cost Management
- FOCUS
---
