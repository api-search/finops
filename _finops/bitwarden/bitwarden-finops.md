---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: bitwarden-public-swagger.json
  format: json
  label: Bitwarden Public API - Members
  slug: public-members
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/bitwarden/refs/heads/main/openapi/bitwarden-public-swagger.json
- filename: bitwarden-public-swagger.json
  format: json
  label: Bitwarden Public API - Groups
  slug: public-groups
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/bitwarden/refs/heads/main/openapi/bitwarden-public-swagger.json
- filename: bitwarden-public-swagger.json
  format: json
  label: Bitwarden Public API - Collections
  slug: public-collections
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/bitwarden/refs/heads/main/openapi/bitwarden-public-swagger.json
- filename: bitwarden-public-swagger.json
  format: json
  label: Bitwarden Public API - Policies
  slug: public-policies
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/bitwarden/refs/heads/main/openapi/bitwarden-public-swagger.json
- filename: bitwarden-public-swagger.json
  format: json
  label: Bitwarden Public API - Event Logs
  slug: public-events
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/bitwarden/refs/heads/main/openapi/bitwarden-public-swagger.json
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
description: FinOps framework definition for the Bitwarden API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Bitwarden
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Bitwarden
  PublisherName: Bitwarden
  ServiceCategory: Developer Tools / API
  ServiceName: Bitwarden
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
name: Bitwarden Finops
provider_name: Bitwarden
provider_slug: bitwarden
publisher_name: Bitwarden
service_category: API
slug: bitwarden-finops
source_filename: bitwarden-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Bitwarden\nproviderId: bitwarden\npublisherName: Bitwarden\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Security\n  - Password Manager\n  - Open Source\n  - Vault\n  - Identity\n  - SCIM\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Bitwarden API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call\
  \ with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n    \
  \  - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Bitwarden\n  ServiceCategory: Developer Tools / API\n  ProviderName: Bitwarden\n  PublisherName: Bitwarden\n  InvoiceIssuerName: Bitwarden\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation:\
  \ sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Bitwarden Public API - Members\n    baseURL: https://api.bitwarden.com/public\n    tags:\n      - Members\n      - Users\n      - Public API\n    serviceName: Bitwarden Public API - Members\n    serviceCategory: API\n  - name: Bitwarden Public API - Groups\n    baseURL: https://api.bitwarden.com/public\n    tags:\n      - Groups\n      - Permissions\n      - Public API\n    serviceName: Bitwarden Public API - Groups\n    serviceCategory: API\n  - name: Bitwarden Public API - Collections\n    baseURL: https://api.bitwarden.com/public\n    tags:\n      - Collections\n      - Sharing\n      - Public API\n    serviceName: Bitwarden Public API - Collections\n    serviceCategory: API\n  - name: Bitwarden\
  \ Public API - Policies\n    baseURL: https://api.bitwarden.com/public\n    tags:\n      - Policies\n      - Enterprise\n      - Public API\n    serviceName: Bitwarden Public API - Policies\n    serviceCategory: API\n  - name: Bitwarden Public API - Event Logs\n    baseURL: https://api.bitwarden.com/public\n    tags:\n      - Events\n      - Audit Logs\n      - Compliance\n      - Public API\n    serviceName: Bitwarden Public API - Event Logs\n    serviceCategory: API\n  - name: Bitwarden Identity API\n    baseURL: https://identity.bitwarden.com/connect/token\n    tags:\n      - Identity\n      - OAuth\n      - Authentication\n    serviceName: Bitwarden Identity API\n    serviceCategory: API\n  - name: Bitwarden SCIM API\n    baseURL: https://scim.bitwarden.com/v2\n    tags:\n      - SCIM\n      - Provisioning\n      - Identity\n    serviceName: Bitwarden SCIM API\n    serviceCategory: API\n  - name: Bitwarden Vault Management API\n    baseURL: http://localhost:8087\n    tags:\n      -\
  \ Vault Items\n      - CLI\n      - Local\n    serviceName: Bitwarden Vault Management API\n    serviceCategory: API\n  - name: Bitwarden Secrets Manager API\n    baseURL: https://api.bitwarden.com\n    tags:\n      - Secrets Manager\n      - Secrets\n      - DevOps\n    serviceName: Bitwarden Secrets Manager API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/bitwarden/refs/heads/main/finops/bitwarden-finops.yml
sources: []
specification: FinOps Framework
tags:
- Security
- Password Manager
- Open Source
- Vault
- Identity
- SCIM
- FinOps
- Cost Management
- FOCUS
---
