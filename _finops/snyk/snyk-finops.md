---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: snyk-rest-openapi.json
  format: json
  label: Snyk REST API - Groups
  slug: rest-groups
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/snyk/refs/heads/main/openapi/snyk-rest-openapi.json
- filename: snyk-rest-openapi.json
  format: json
  label: Snyk REST API - Organizations
  slug: rest-organizations
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/snyk/refs/heads/main/openapi/snyk-rest-openapi.json
- filename: snyk-rest-openapi.json
  format: json
  label: Snyk REST API - Projects
  slug: rest-projects
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/snyk/refs/heads/main/openapi/snyk-rest-openapi.json
- filename: snyk-rest-openapi.json
  format: json
  label: Snyk REST API - Issues
  slug: rest-issues
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/snyk/refs/heads/main/openapi/snyk-rest-openapi.json
- filename: snyk-rest-openapi.json
  format: json
  label: Snyk REST API - Targets
  slug: rest-targets
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/snyk/refs/heads/main/openapi/snyk-rest-openapi.json
- filename: snyk-rest-openapi.json
  format: json
  label: Snyk REST API - Integrations
  slug: rest-integrations
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/snyk/refs/heads/main/openapi/snyk-rest-openapi.json
- filename: snyk-rest-openapi.json
  format: json
  label: Snyk REST API - Audit Logs
  slug: rest-audit-logs
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/snyk/refs/heads/main/openapi/snyk-rest-openapi.json
- filename: snyk-rest-openapi.json
  format: json
  label: Snyk REST API - SBOMs
  slug: rest-sboms
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/snyk/refs/heads/main/openapi/snyk-rest-openapi.json
- filename: snyk-rest-openapi.json
  format: json
  label: Snyk REST API - Container Images
  slug: rest-container-images
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/snyk/refs/heads/main/openapi/snyk-rest-openapi.json
- filename: snyk-rest-openapi.json
  format: json
  label: Snyk REST API - Custom Base Images
  slug: rest-custom-base-images
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/snyk/refs/heads/main/openapi/snyk-rest-openapi.json
- filename: snyk-rest-openapi.json
  format: json
  label: Snyk REST API - Webhooks
  slug: rest-webhooks
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/snyk/refs/heads/main/openapi/snyk-rest-openapi.json
- filename: snyk-rest-openapi.json
  format: json
  label: Snyk REST API - Export
  slug: rest-export
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/snyk/refs/heads/main/openapi/snyk-rest-openapi.json
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
description: FinOps framework definition for the Snyk API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Snyk
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Snyk
  PublisherName: Snyk
  ServiceCategory: Developer Tools / API
  ServiceName: Snyk
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
name: Snyk Finops
provider_name: Snyk
provider_slug: snyk
publisher_name: Snyk
service_category: API
slug: snyk-finops
source_filename: snyk-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Snyk\nproviderId: snyk\npublisherName: Snyk\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Security\n  - DevSecOps\n  - Vulnerability Management\n  - Application Security\n  - SCA\n  - SAST\n  - Container Security\n  - IaC\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Snyk API surface. Provides a FOCUS-aligned mapping for\n  cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description:\
  \ Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n\
  \    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Snyk\n  ServiceCategory: Developer Tools / API\n  ProviderName: Snyk\n  PublisherName: Snyk\n  InvoiceIssuerName: Snyk\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n   \
  \ aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Snyk REST API - Groups\n    baseURL: https://api.snyk.io/rest\n    tags:\n      - Groups\n      - Tenancy\n      - REST API\n    serviceName: Snyk REST API - Groups\n    serviceCategory: API\n  - name: Snyk REST API - Organizations\n    baseURL: https://api.snyk.io/rest\n    tags:\n      - Organizations\n      - Memberships\n      - REST API\n    serviceName: Snyk REST API - Organizations\n    serviceCategory: API\n  - name: Snyk REST API - Projects\n    baseURL: https://api.snyk.io/rest\n    tags:\n      - Projects\n      - REST API\n    serviceName: Snyk REST API - Projects\n    serviceCategory: API\n  - name: Snyk REST API - Issues\n    baseURL: https://api.snyk.io/rest\n    tags:\n\
  \      - Issues\n      - Vulnerabilities\n      - REST API\n    serviceName: Snyk REST API - Issues\n    serviceCategory: API\n  - name: Snyk REST API - Targets\n    baseURL: https://api.snyk.io/rest\n    tags:\n      - Targets\n      - Import Sources\n      - REST API\n    serviceName: Snyk REST API - Targets\n    serviceCategory: API\n  - name: Snyk REST API - Integrations\n    baseURL: https://api.snyk.io/rest\n    tags:\n      - Integrations\n      - SCM\n      - Registries\n      - REST API\n    serviceName: Snyk REST API - Integrations\n    serviceCategory: API\n  - name: Snyk REST API - Audit Logs\n    baseURL: https://api.snyk.io/rest\n    tags:\n      - Audit Logs\n      - Compliance\n      - REST API\n    serviceName: Snyk REST API - Audit Logs\n    serviceCategory: API\n  - name: Snyk REST API - SBOMs\n    baseURL: https://api.snyk.io/rest\n    tags:\n      - SBOM\n      - CycloneDX\n      - SPDX\n      - REST API\n    serviceName: Snyk REST API - SBOMs\n    serviceCategory:\
  \ API\n  - name: Snyk REST API - Container Images\n    baseURL: https://api.snyk.io/rest\n    tags:\n      - Container Images\n      - Container Security\n      - REST API\n    serviceName: Snyk REST API - Container Images\n    serviceCategory: API\n  - name: Snyk REST API - Custom Base Images\n    baseURL: https://api.snyk.io/rest\n    tags:\n      - Custom Base Images\n      - Container Security\n      - REST API\n    serviceName: Snyk REST API - Custom Base Images\n    serviceCategory: API\n  - name: Snyk REST API - Webhooks\n    baseURL: https://api.snyk.io/rest\n    tags:\n      - Webhooks\n      - Events\n      - REST API\n    serviceName: Snyk REST API - Webhooks\n    serviceCategory: API\n  - name: Snyk REST API - Export\n    baseURL: https://api.snyk.io/rest\n    tags:\n      - Export\n      - Reporting\n      - Bulk\n      - REST API\n    serviceName: Snyk REST API - Export\n    serviceCategory: API\n  - name: Snyk REST API - Apps (OAuth)\n    baseURL: https://api.snyk.io/rest\n\
  \    tags:\n      - Apps\n      - OAuth\n      - Extensibility\n      - REST API\n    serviceName: Snyk REST API - Apps (OAuth)\n    serviceCategory: API\n  - name: Snyk V1 API (Legacy)\n    baseURL: https://api.snyk.io/v1\n    tags:\n      - V1\n      - Legacy\n      - Test\n      - Monitor\n    serviceName: Snyk V1 API (Legacy)\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/snyk/refs/heads/main/finops/snyk-finops.yml
sources: []
specification: FinOps Framework
tags:
- Security
- DevSecOps
- Vulnerability Management
- Application Security
- SCA
- SAST
- Container Security
- IaC
- FinOps
- Cost Management
- FOCUS
---
