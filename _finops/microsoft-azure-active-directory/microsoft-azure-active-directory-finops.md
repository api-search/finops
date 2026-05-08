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
- filename: microsoft-graph-identity-api.yml
  format: yaml
  label: Microsoft Graph Identity and Access API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-azure-active-directory/refs/heads/main/openapi/microsoft-graph-identity-api.yml
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
description: FinOps framework definition for the Microsoft Azure Active Directory API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Microsoft Azure Active Directory
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Microsoft Azure Active Directory
  PublisherName: Microsoft Azure Active Directory
  ServiceCategory: Developer Tools / API
  ServiceName: Microsoft Azure Active Directory
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
name: Microsoft Azure Active Directory Finops
provider_name: Microsoft Azure Active Directory
provider_slug: microsoft-azure-active-directory
publisher_name: Microsoft Azure Active Directory
service_category: API
slug: microsoft-azure-active-directory-finops
source_filename: microsoft-azure-active-directory-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Microsoft Azure Active Directory\nproviderId: microsoft-azure-active-directory\npublisherName: Microsoft Azure Active Directory\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Authentication\n  - Authorization\n  - Identity\n  - Microsoft\n  - Microsoft Entra\n  - OAuth\n  - OpenID Connect\n  - SAML\n  - SCIM\n  - Single Sign-On\n  - Zero Trust\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Microsoft Azure Active Directory API surface. Provides\n  a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across\n  the provider's APIs.\nprinciples:\n  - name: Visibility\n    description:\
  \ Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n   \
  \   - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Microsoft Azure Active Directory\n  ServiceCategory: Developer Tools / API\n  ProviderName: Microsoft Azure Active Directory\n  PublisherName: Microsoft Azure Active Directory\n  InvoiceIssuerName: Microsoft Azure Active Directory\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable\
  \ API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Microsoft Graph API\n    baseURL: https://graph.microsoft.com\n    tags:\n      - Graph\n      - Groups\n      - Identity\n      - Users\n    serviceName: Microsoft Graph API\n    serviceCategory: API\n  - name: Microsoft Graph Identity and Access API\n    baseURL: https://graph.microsoft.com\n    tags:\n      - Access Management\n      - Authentication Methods\n      - Conditional Access\n      - Identity\n      - Identity Governance\n\
  \    serviceName: Microsoft Graph Identity and Access API\n    serviceCategory: API\n  - name: Azure AD Graph API (Deprecated)\n    baseURL: https://graph.windows.net\n    tags:\n      - Deprecated\n      - Identity\n      - Legacy\n    serviceName: Azure AD Graph API (Deprecated)\n    serviceCategory: API\n  - name: Azure AD Authentication Library (ADAL)\n    baseURL: ''\n    tags:\n      - Authentication\n      - Legacy\n      - Library\n    serviceName: Azure AD Authentication Library (ADAL)\n    serviceCategory: API\n  - name: Microsoft Authentication Library (MSAL)\n    baseURL: ''\n    tags:\n      - Authentication\n      - Library\n      - OAuth\n      - OpenID Connect\n    serviceName: Microsoft Authentication Library (MSAL)\n    serviceCategory: API\n  - name: Microsoft Identity Platform\n    baseURL: https://login.microsoftonline.com\n    tags:\n      - App Registration\n      - Authentication\n      - Authorization\n      - OAuth\n      - OpenID Connect\n    serviceName: Microsoft\
  \ Identity Platform\n    serviceCategory: API\n  - name: Microsoft Entra Verified ID API\n    baseURL: https://verifiedid.did.msidentity.com\n    tags:\n      - Decentralized Identity\n      - Identity Verification\n      - Verifiable Credentials\n      - W3C\n    serviceName: Microsoft Entra Verified ID API\n    serviceCategory: API\n  - name: Microsoft Entra ID Governance API\n    baseURL: https://graph.microsoft.com\n    tags:\n      - Access Reviews\n      - Entitlement Management\n      - Governance\n      - Lifecycle Workflows\n      - Privileged Identity Management\n    serviceName: Microsoft Entra ID Governance API\n    serviceCategory: API\n  - name: Microsoft Entra SCIM Provisioning API\n    baseURL: ''\n    tags:\n      - Automation\n      - Group Management\n      - Provisioning\n      - SCIM\n      - User Management\n    serviceName: Microsoft Entra SCIM Provisioning API\n    serviceCategory: API\n  - name: Microsoft Entra PowerShell\n    baseURL: ''\n    tags:\n      - Automation\n\
  \      - CLI\n      - PowerShell\n      - Scripting\n    serviceName: Microsoft Entra PowerShell\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - name: Microsoft\n    email: azuread@microsoft.com\n    url: https://azure.microsoft.com/en-us/services/active-directory/\n  - name: Kin Lane\n    email: kin@apievangelist.com\n    url: https://apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/microsoft-azure-active-directory/refs/heads/main/finops/microsoft-azure-active-directory-finops.yml
sources: []
specification: FinOps Framework
tags:
- Authentication
- Authorization
- Identity
- Microsoft
- Microsoft Entra
- OAuth
- OpenID Connect
- SAML
- SCIM
- Single Sign-On
- Zero Trust
- FinOps
- Cost Management
- FOCUS
---
