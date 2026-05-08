---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: microsoft-entra-graph-identity-openapi.yml
  format: yaml
  label: Microsoft Entra ID (Azure AD) API
  slug: graph-identity
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-entra/refs/heads/main/openapi/microsoft-entra-graph-identity-openapi.yml
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
description: FinOps framework definition for the Microsoft Entra API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Microsoft Entra
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Microsoft Entra
  PublisherName: Microsoft Entra
  ServiceCategory: Developer Tools / API
  ServiceName: Microsoft Entra
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
name: Microsoft Entra Finops
provider_name: Microsoft Entra
provider_slug: microsoft-entra
publisher_name: Microsoft Entra
service_category: API
slug: microsoft-entra-finops
source_filename: microsoft-entra-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Microsoft Entra\nproviderId: microsoft-entra\npublisherName: Microsoft Entra\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Access Management\n  - Authentication\n  - Azure AD\n  - Entra\n  - Identity\n  - Identity Governance\n  - Microsoft\n  - Network Security\n  - Security\n  - Zero Trust\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Microsoft Entra API surface. Provides a FOCUS-aligned\n  mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and\
  \ finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud\
  \ Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Microsoft Entra\n  ServiceCategory: Developer Tools / API\n  ProviderName: Microsoft Entra\n  PublisherName: Microsoft Entra\n  InvoiceIssuerName: Microsoft Entra\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n\
  \      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Microsoft Entra ID (Azure AD) API\n    baseURL: https://graph.microsoft.com/v1.0\n    tags:\n      - Authentication\n      - Authorization\n      - Directory\n      - Groups\n      - Identity\n      - Users\n    serviceName: Microsoft Entra ID (Azure AD) API\n    serviceCategory: API\n  - name: Microsoft Entra ID Protection API\n    baseURL: https://graph.microsoft.com/v1.0\n    tags:\n      - Identity Protection\n      - Risk Detection\n      - Security\n      - Threat Protection\n    serviceName: Microsoft Entra ID Protection API\n    serviceCategory: API\n\
  \  - name: Microsoft Entra Conditional Access API\n    baseURL: https://graph.microsoft.com/v1.0\n    tags:\n      - Access Control\n      - Conditional Access\n      - Policies\n      - Security\n    serviceName: Microsoft Entra Conditional Access API\n    serviceCategory: API\n  - name: Microsoft Entra Privileged Identity Management API\n    baseURL: https://graph.microsoft.com/v1.0\n    tags:\n      - Just-In-Time\n      - PIM\n      - Privileged Access\n      - Role Management\n    serviceName: Microsoft Entra Privileged Identity Management API\n    serviceCategory: API\n  - name: Microsoft Entra Verified ID API\n    baseURL: https://verifiedid.did.msidentity.com/v1.0\n    tags:\n      - Decentralized Identity\n      - DID\n      - SSI\n      - Verifiable Credentials\n    serviceName: Microsoft Entra Verified ID API\n    serviceCategory: API\n  - name: Microsoft Entra External ID API\n    baseURL: https://graph.microsoft.com/v1.0\n    tags:\n      - B2B\n      - B2C\n      - Customer\
  \ Identity\n      - External Identities\n    serviceName: Microsoft Entra External ID API\n    serviceCategory: API\n  - name: Microsoft Entra ID Governance API\n    baseURL: https://graph.microsoft.com/v1.0\n    tags:\n      - Access Reviews\n      - Compliance\n      - Entitlement Management\n      - Identity Governance\n      - Lifecycle Workflows\n    serviceName: Microsoft Entra ID Governance API\n    serviceCategory: API\n  - name: Microsoft Entra Application Management API\n    baseURL: https://graph.microsoft.com/v1.0\n    tags:\n      - App Registration\n      - Applications\n      - Credentials\n      - OAuth\n      - Service Principals\n    serviceName: Microsoft Entra Application Management API\n    serviceCategory: API\n  - name: Microsoft Entra Authentication Methods API\n    baseURL: https://graph.microsoft.com/v1.0\n    tags:\n      - Authentication Methods\n      - FIDO2\n      - MFA\n      - Passkeys\n      - Passwordless\n    serviceName: Microsoft Entra Authentication\
  \ Methods API\n    serviceCategory: API\n  - name: Microsoft Entra Workload ID API\n    baseURL: https://graph.microsoft.com/v1.0\n    tags:\n      - Managed Identities\n      - Service Principals\n      - Workload Identities\n      - Workload Identity Federation\n    serviceName: Microsoft Entra Workload ID API\n    serviceCategory: API\n  - name: Microsoft Entra Provisioning API\n    baseURL: https://graph.microsoft.com/v1.0\n    tags:\n      - Inbound Provisioning\n      - Provisioning\n      - SCIM\n      - Synchronization\n      - User Lifecycle\n    serviceName: Microsoft Entra Provisioning API\n    serviceCategory: API\n  - name: Microsoft Entra Global Secure Access API\n    baseURL: https://graph.microsoft.com/beta\n    tags:\n      - Internet Access\n      - Network Security\n      - Private Access\n      - Secure Web Gateway\n      - Zero Trust\n      - ZTNA\n    serviceName: Microsoft Entra Global Secure Access API\n    serviceCategory: API\n  - name: Microsoft Identity Platform\
  \ API\n    baseURL: https://login.microsoftonline.com\n    tags:\n      - Identity Platform\n      - OAuth 2.0\n      - OpenID Connect\n      - SAML\n      - Token Service\n    serviceName: Microsoft Identity Platform API\n    serviceCategory: API\n  - name: Microsoft Entra Agent ID API\n    baseURL: https://graph.microsoft.com/beta\n    tags:\n      - Agent Identity\n      - Agent Registry\n      - AI Agents\n      - Machine Identity\n    serviceName: Microsoft Entra Agent ID API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n    url: https://apievangelist.com/\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/microsoft-entra/refs/heads/main/finops/microsoft-entra-finops.yml
sources: []
specification: FinOps Framework
tags:
- Access Management
- Authentication
- Azure AD
- Entra
- Identity
- Identity Governance
- Microsoft
- Network Security
- Security
- Zero Trust
- FinOps
- Cost Management
- FOCUS
---
