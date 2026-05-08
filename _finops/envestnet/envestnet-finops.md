---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: envestnet-account-aggregation-openapi-original.yml
  format: yaml
  label: Envestnet Account Aggregation API
  slug: envestnet-account-aggregation-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/envestnet/refs/heads/main/openapi/envestnet-account-aggregation-openapi-original.yml
- filename: envestnet-account-token-openapi-original.yml
  format: yaml
  label: Envestnet Account Token APIs
  slug: envestnet-account-token-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/envestnet/refs/heads/main/openapi/envestnet-account-token-openapi-original.yml
- filename: envestnet-verification-openapi-original.yml
  format: yaml
  label: Envestnet Account Verification APIs
  slug: envestnet-account-verification-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/envestnet/refs/heads/main/openapi/envestnet-verification-openapi-original.yml
- filename: envestnet-credit-accelerator-openapi-original.yml
  format: yaml
  label: Envestnet Credit Accelerator API
  slug: envestnet-credit-accelerator-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/envestnet/refs/heads/main/openapi/envestnet-credit-accelerator-openapi-original.yml
- filename: envestnet-insights-openapi-original.yml
  format: yaml
  label: Envestnet Insights API
  slug: envestnet-insights-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/envestnet/refs/heads/main/openapi/envestnet-insights-openapi-original.yml
- filename: envestnet-personalized-views-openapi-original.yml
  format: yaml
  label: Envestnet Personalized View API
  slug: envestnet-personalized-view-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/envestnet/refs/heads/main/openapi/envestnet-personalized-views-openapi-original.yml
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
description: FinOps framework definition for the Envestnet API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Envestnet
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Envestnet
  PublisherName: Envestnet
  ServiceCategory: Developer Tools / API
  ServiceName: Envestnet
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
name: Envestnet Finops
provider_name: Envestnet
provider_slug: envestnet
publisher_name: Envestnet
service_category: API
slug: envestnet-finops
source_filename: envestnet-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Envestnet\nproviderId: envestnet\npublisherName: Envestnet\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Financial\n  - Wealth Management\n  - Open Banking\n  - Account Aggregation\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Envestnet API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with\
  \ the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps\
  \ Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Envestnet\n  ServiceCategory: Developer Tools / API\n  ProviderName: Envestnet\n  PublisherName: Envestnet\n  InvoiceIssuerName: Envestnet\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation:\
  \ sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Envestnet Account Aggregation API\n    baseURL: ''\n    tags:\n      - Account Aggregation\n      - Open Banking\n    serviceName: Envestnet Account Aggregation API\n    serviceCategory: API\n  - name: Envestnet Account Token APIs\n    baseURL: ''\n    tags:\n      - Account Token\n      - Payments\n    serviceName: Envestnet Account Token APIs\n    serviceCategory: API\n  - name: Envestnet Account Verification APIs\n    baseURL: ''\n    tags:\n      - Verification\n      - Payments\n    serviceName: Envestnet Account Verification APIs\n    serviceCategory: API\n  - name: Envestnet Credit Accelerator API\n    baseURL: ''\n    tags:\n      - Credit\n      - Underwriting\n    serviceName: Envestnet\
  \ Credit Accelerator API\n    serviceCategory: API\n  - name: Envestnet Insights API\n    baseURL: ''\n    tags:\n      - Insights\n      - Personalization\n    serviceName: Envestnet Insights API\n    serviceCategory: API\n  - name: Envestnet Personalized View API\n    baseURL: ''\n    tags:\n      - Personalized Views\n      - Transactions\n    serviceName: Envestnet Personalized View API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/envestnet/refs/heads/main/finops/envestnet-finops.yml
sources: []
specification: FinOps Framework
tags:
- Financial
- Wealth Management
- Open Banking
- Account Aggregation
- FinOps
- Cost Management
- FOCUS
---
