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
  label: SailPoint Identity Security Cloud V3 API
  slug: identity-security-cloud-v3-api
  spec_type: OpenAPI
  url: https://developer.sailpoint.com/docs/api/v3/identity-security-cloud-v-3-api/
- filename: openapi.yaml
  format: yaml
  label: SailPoint Identity Security Cloud V2024 API
  slug: identity-security-cloud-v2024-api
  spec_type: OpenAPI
  url: https://developer.sailpoint.com/docs/api/v2024/identity-security-cloud-v-2024-api/
- filename: openapi.yaml
  format: yaml
  label: SailPoint Identity Security Cloud V2025 API
  slug: identity-security-cloud-v2025-api
  spec_type: OpenAPI
  url: https://developer.sailpoint.com/docs/api/v2025/identity-security-cloud-v-2025-api/
- filename: openapi.yaml
  format: yaml
  label: SailPoint Identity Security Cloud Beta API
  slug: identity-security-cloud-beta-api
  spec_type: OpenAPI
  url: https://developer.sailpoint.com/docs/api/beta/identity-security-cloud-beta-api/
- filename: openapi.yaml
  format: yaml
  label: SailPoint IdentityIQ SCIM API
  slug: identityiq-scim-api
  spec_type: OpenAPI
  url: https://developer.sailpoint.com/docs/api/iiq/identityiq-scim-rest-api/
- filename: openapi.yaml
  format: yaml
  label: SailPoint Identity Security Cloud V2026 API
  slug: identity-security-cloud-v2026-api
  spec_type: OpenAPI
  url: https://developer.sailpoint.com/docs/api/v2026/identity-security-cloud-v-2026-api/
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
description: FinOps framework definition for the SailPoint API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: SailPoint
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: SailPoint
  PublisherName: SailPoint
  ServiceCategory: Developer Tools / API
  ServiceName: SailPoint
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
name: Sailpoint Finops
provider_name: SailPoint
provider_slug: sailpoint
publisher_name: SailPoint
service_category: API
slug: sailpoint-finops
source_filename: sailpoint-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: SailPoint\nproviderId: sailpoint\npublisherName: SailPoint\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Access Governance\n  - Compliance\n  - IAM\n  - Identity Management\n  - Identity Security\n  - Security\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the SailPoint API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every\
  \ chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n   \
  \ capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: SailPoint\n  ServiceCategory: Developer Tools / API\n  ProviderName: SailPoint\n  PublisherName: SailPoint\n  InvoiceIssuerName: SailPoint\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n\
  \    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: SailPoint\n    baseURL: ''\n    tags: []\n    serviceName: SailPoint\n    serviceCategory: API\n  - name: SailPoint Identity Security Cloud V3 API\n    baseURL: ''\n    tags:\n      - Access Governance\n      - IAM\n      - Identity Security\n    serviceName: SailPoint Identity Security Cloud V3 API\n    serviceCategory: API\n  - name: SailPoint Identity Security Cloud V2024 API\n    baseURL: ''\n    tags:\n      - Access Governance\n      - IAM\n      - Identity Security\n    serviceName: SailPoint Identity Security Cloud V2024 API\n    serviceCategory: API\n  - name: SailPoint Identity Security Cloud V2025 API\n    baseURL: ''\n    tags:\n      - Access Governance\n\
  \      - IAM\n      - Identity Security\n    serviceName: SailPoint Identity Security Cloud V2025 API\n    serviceCategory: API\n  - name: SailPoint Identity Security Cloud Beta API\n    baseURL: ''\n    tags:\n      - Beta\n      - Identity Security\n    serviceName: SailPoint Identity Security Cloud Beta API\n    serviceCategory: API\n  - name: SailPoint IdentityIQ SCIM API\n    baseURL: ''\n    tags:\n      - Identity Governance\n      - On-Premise\n      - SCIM\n    serviceName: SailPoint IdentityIQ SCIM API\n    serviceCategory: API\n  - name: SailPoint Non-Employee Risk Management V1 API\n    baseURL: ''\n    tags:\n      - Identity Security\n      - Non-Employee\n      - Risk Management\n    serviceName: SailPoint Non-Employee Risk Management V1 API\n    serviceCategory: API\n  - name: SailPoint Non-Employee Risk Management V2025 API\n    baseURL: ''\n    tags:\n      - Identity Security\n      - Non-Employee\n      - Risk Management\n    serviceName: SailPoint Non-Employee Risk\
  \ Management V2025 API\n    serviceCategory: API\n  - name: SailPoint Identity Security Cloud V2026 API\n    baseURL: ''\n    tags:\n      - Access Governance\n      - Experimental\n      - IAM\n      - Identity Security\n    serviceName: SailPoint Identity Security Cloud V2026 API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n  - name: SailPoint Technologies\n    email: developer@sailpoint.com\n    url: https://developer.sailpoint.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/sailpoint/refs/heads/main/finops/sailpoint-finops.yml
sources: []
specification: FinOps Framework
tags:
- Access Governance
- Compliance
- IAM
- Identity Management
- Identity Security
- Security
- FinOps
- Cost Management
- FOCUS
---
