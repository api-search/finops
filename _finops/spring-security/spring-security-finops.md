---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: spring-security-oauth2-openapi.yml
  format: yaml
  label: Spring Security OAuth2 API
  slug: spring-security-oauth2
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/spring-security/refs/heads/main/openapi/spring-security-oauth2-openapi.yml
- filename: spring-authorization-server-openapi.yml
  format: yaml
  label: Spring Authorization Server API
  slug: spring-authorization-server
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/spring-security/refs/heads/main/openapi/spring-authorization-server-openapi.yml
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
description: FinOps framework definition for the Spring Security API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Spring Security
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Spring Security
  PublisherName: Spring Security
  ServiceCategory: Developer Tools / API
  ServiceName: Spring Security
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
name: Spring Security Finops
provider_name: Spring Security
provider_slug: spring-security
publisher_name: Spring Security
service_category: API
slug: spring-security-finops
source_filename: spring-security-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Spring Security\nproviderId: spring-security\npublisherName: Spring Security\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Authentication\n  - Authorization\n  - Java\n  - JWT\n  - OAuth2\n  - OpenID Connect\n  - SAML\n  - Security\n  - Spring Framework\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Spring Security API surface. Provides a FOCUS-aligned\n  mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n\
  \  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and\
  \ SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Spring Security\n  ServiceCategory: Developer Tools / API\n  ProviderName: Spring Security\n  PublisherName: Spring Security\n  InvoiceIssuerName: Spring Security\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n\
  \    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Spring Security OAuth2 API\n    baseURL: http://localhost:8080\n    tags:\n      - Authorization Server\n      - JWT\n      - OAuth2\n      - OpenID Connect\n      - Token\n    serviceName: Spring Security OAuth2 API\n    serviceCategory: API\n  - name: Spring Authorization Server API\n    baseURL: http://localhost:9000\n    tags:\n      - Authorization Server\n      - OAuth2\n      - OpenID Connect\n      - Token Issuance\n    serviceName: Spring Authorization Server API\n    serviceCategory: API\n  - name: Spring Security Core\n    baseURL: https://docs.spring.io/spring-security/site/docs/current/api/\n\
  \    tags:\n      - Authentication\n      - Authorization\n      - Core\n      - Method Security\n    serviceName: Spring Security Core\n    serviceCategory: API\n  - name: Spring Security SAML2\n    baseURL: ''\n    tags:\n      - Enterprise SSO\n      - Federation\n      - SAML\n      - Single Logout\n    serviceName: Spring Security SAML2\n    serviceCategory: API\n  - name: Spring Security LDAP\n    baseURL: ''\n    tags:\n      - Authentication\n      - Directory Services\n      - Enterprise\n      - LDAP\n    serviceName: Spring Security LDAP\n    serviceCategory: API\n  - name: Spring Security WebFlux\n    baseURL: ''\n    tags:\n      - Non-Blocking\n      - Reactive\n      - Security\n      - WebFlux\n    serviceName: Spring Security WebFlux\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\n\
  maintainers:\n  - FN: Spring Security Team\n    email: spring-security@vmware.com\n    url: https://spring.io/team\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/spring-security/refs/heads/main/finops/spring-security-finops.yml
sources: []
specification: FinOps Framework
tags:
- Authentication
- Authorization
- Java
- JWT
- OAuth2
- OpenID Connect
- SAML
- Security
- Spring Framework
- FinOps
- Cost Management
- FOCUS
---
