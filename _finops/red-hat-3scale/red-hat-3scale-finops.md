---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: red-hat-3scale-service-management-openapi.yml
  format: yaml
  label: Red Hat 3scale Service Management API
  slug: service-management-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/red-hat-3scale/refs/heads/main/openapi/red-hat-3scale-service-management-openapi.yml
- filename: red-hat-3scale-account-management-openapi.yml
  format: yaml
  label: Red Hat 3scale Account Management API
  slug: account-management-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/red-hat-3scale/refs/heads/main/openapi/red-hat-3scale-account-management-openapi.yml
- filename: red-hat-3scale-analytics-openapi.yml
  format: yaml
  label: Red Hat 3scale Analytics API
  slug: analytics-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/red-hat-3scale/refs/heads/main/openapi/red-hat-3scale-analytics-openapi.yml
- filename: red-hat-3scale-billing-openapi.yml
  format: yaml
  label: Red Hat 3scale Billing API
  slug: billing-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/red-hat-3scale/refs/heads/main/openapi/red-hat-3scale-billing-openapi.yml
- filename: red-hat-3scale-apicast-management-openapi.yml
  format: yaml
  label: Red Hat 3scale APIcast Management API
  slug: apicast-management-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/red-hat-3scale/refs/heads/main/openapi/red-hat-3scale-apicast-management-openapi.yml
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
description: FinOps framework definition for the Red Hat 3scale API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Red Hat 3scale
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Red Hat 3scale
  PublisherName: Red Hat 3scale
  ServiceCategory: Developer Tools / API
  ServiceName: Red Hat 3scale
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
name: Red Hat 3Scale Finops
provider_name: Red Hat 3scale
provider_slug: red-hat-3scale
publisher_name: Red Hat 3scale
service_category: API
slug: red-hat-3scale-finops
source_filename: red-hat-3scale-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Red Hat 3scale\nproviderId: red-hat-3scale\npublisherName: Red Hat 3scale\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - API Gateway\n  - API Management\n  - Developer Portal\n  - Enterprise\n  - Red Hat\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Red Hat 3scale API surface. Provides a FOCUS-aligned\n  mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every\
  \ chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n   \
  \ capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Red Hat 3scale\n  ServiceCategory: Developer Tools / API\n  ProviderName: Red Hat 3scale\n  PublisherName: Red Hat 3scale\n  InvoiceIssuerName: Red Hat 3scale\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network\
  \ in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Red Hat 3scale Service Management API\n    baseURL: https://su1.3scale.net\n    tags:\n      - Access Control\n      - API Management\n      - Authorization\n      - Traffic Management\n    serviceName: Red Hat 3scale Service Management API\n    serviceCategory: API\n  - name: Red Hat 3scale Account Management API\n    baseURL: https://{your-domain}-admin.3scale.net\n    tags:\n      - Account Management\n      - API Management\n      - Applications\n      - Developer Portal\n    serviceName: Red Hat 3scale Account Management API\n    serviceCategory: API\n  - name: Red Hat 3scale Analytics API\n    baseURL: https://{your-domain}-admin.3scale.net\n\
  \    tags:\n      - Analytics\n      - API Management\n      - Metrics\n      - Reporting\n    serviceName: Red Hat 3scale Analytics API\n    serviceCategory: API\n  - name: Red Hat 3scale Billing API\n    baseURL: https://{your-domain}-admin.3scale.net\n    tags:\n      - API Management\n      - Billing\n      - Invoices\n      - Monetization\n    serviceName: Red Hat 3scale Billing API\n    serviceCategory: API\n  - name: Red Hat 3scale Webhooks\n    baseURL: ''\n    tags:\n      - API Management\n      - Events\n      - Notifications\n      - Webhooks\n    serviceName: Red Hat 3scale Webhooks\n    serviceCategory: API\n  - name: Red Hat 3scale APIcast Management API\n    baseURL: http://localhost:8090\n    tags:\n      - API Gateway\n      - Configuration\n      - Health Checks\n      - Management\n    serviceName: Red Hat 3scale APIcast Management API\n    serviceCategory: API\n  - name: Red Hat 3scale Toolbox CLI\n    baseURL: ''\n    tags:\n      - API Management\n      - Automation\n\
  \      - CLI\n      - DevOps\n    serviceName: Red Hat 3scale Toolbox CLI\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/red-hat-3scale/refs/heads/main/finops/red-hat-3scale-finops.yml
sources: []
specification: FinOps Framework
tags:
- API Gateway
- API Management
- Developer Portal
- Enterprise
- Red Hat
- FinOps
- Cost Management
- FOCUS
---
