---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
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
description: FinOps framework definition for the Casdoor API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Casdoor
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Casdoor
  PublisherName: Casdoor
  ServiceCategory: Developer Tools / API
  ServiceName: Casdoor
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
name: Casdoor Finops
provider_name: Casdoor
provider_slug: casdoor
publisher_name: Casdoor
service_category: API
slug: casdoor-finops
source_filename: casdoor-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Casdoor\nproviderId: casdoor\npublisherName: Casdoor\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Authentication\n  - Authorization\n  - IAM\n  - Identity\n  - LDAP\n  - MCP\n  - MFA\n  - OAuth\n  - OIDC\n  - Open Source\n  - Passkeys\n  - SAML\n  - SCIM\n  - Single Sign-On\n  - SSO\n  - WebAuthn\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Casdoor API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and\
  \ finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud\
  \ Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Casdoor\n  ServiceCategory: Developer Tools / API\n  ProviderName: Casdoor\n  PublisherName: Casdoor\n  InvoiceIssuerName: Casdoor\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n\
  \    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Casdoor REST API\n    baseURL: https://door.casdoor.com\n    tags:\n      - Applications\n      - IAM\n      - Organizations\n      - REST\n      - Roles\n      - Sessions\n      - Tokens\n      - Users\n    serviceName: Casdoor REST API\n    serviceCategory: API\n  - name: Casdoor OAuth 2.0 / OIDC Provider\n    baseURL: ''\n    tags:\n      - Authentication\n      - JWT\n      - OAuth\n      - OIDC\n      - SSO\n      - Tokens\n    serviceName: Casdoor OAuth 2.0 / OIDC Provider\n    serviceCategory: API\n  - name: Casdoor SAML 2.0 Identity Provider\n    baseURL: ''\n    tags:\n      - Enterprise SSO\n\
  \      - Federation\n      - SAML\n      - SSO\n    serviceName: Casdoor SAML 2.0 Identity Provider\n    serviceCategory: API\n  - name: Casdoor CAS Server\n    baseURL: ''\n    tags:\n      - Authentication\n      - CAS\n      - SSO\n    serviceName: Casdoor CAS Server\n    serviceCategory: API\n  - name: Casdoor LDAP Server\n    baseURL: ''\n    tags:\n      - Directory\n      - LDAP\n      - Sync\n    serviceName: Casdoor LDAP Server\n    serviceCategory: API\n  - name: Casdoor SCIM 2.0 API\n    baseURL: ''\n    tags:\n      - Identity\n      - Provisioning\n      - SCIM\n    serviceName: Casdoor SCIM 2.0 API\n    serviceCategory: API\n  - name: Casdoor MCP Gateway\n    baseURL: ''\n    tags:\n      - A2A\n      - Agents\n      - AI\n      - MCP\n    serviceName: Casdoor MCP Gateway\n    serviceCategory: API\n  - name: Casdoor Webhooks\n    baseURL: ''\n    tags:\n      - Events\n      - Integration\n      - Webhooks\n    serviceName: Casdoor Webhooks\n    serviceCategory: API\nunitEconomics:\n\
  \  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/casdoor/refs/heads/main/finops/casdoor-finops.yml
sources: []
specification: FinOps Framework
tags:
- Authentication
- Authorization
- IAM
- Identity
- LDAP
- MCP
- MFA
- OAuth
- OIDC
- Open Source
- Passkeys
- SAML
- SCIM
- Single Sign-On
- SSO
- WebAuthn
- FinOps
- Cost Management
- FOCUS
---
