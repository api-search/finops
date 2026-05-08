---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: mulesoft-anypoint-platform-openapi.yml
  format: yaml
  label: MuleSoft Anypoint Platform Management API
  slug: mulesoft-anypoint-platform-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/mulesoft/refs/heads/main/openapi/mulesoft-anypoint-platform-openapi.yml
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
description: FinOps framework definition for the MuleSoft API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: MuleSoft
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: MuleSoft
  PublisherName: MuleSoft
  ServiceCategory: Developer Tools / API
  ServiceName: MuleSoft
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
name: Mulesoft Finops
provider_name: MuleSoft
provider_slug: mulesoft
publisher_name: MuleSoft
service_category: API
slug: mulesoft-finops
source_filename: mulesoft-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: MuleSoft\nproviderId: mulesoft\npublisherName: MuleSoft\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - API Gateway\n  - API Management\n  - Enterprise\n  - Integration\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the MuleSoft API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming\
  \ team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice\
  \ Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: MuleSoft\n  ServiceCategory: Developer Tools / API\n  ProviderName: MuleSoft\n  PublisherName: MuleSoft\n  InvoiceIssuerName: MuleSoft\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n\
  \      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: MuleSoft Anypoint Platform\n    baseURL: ''\n    tags:\n      - API Gateway\n      - API Management\n      - Enterprise\n    serviceName: MuleSoft Anypoint Platform\n    serviceCategory: API\n  - name: MuleSoft Anypoint Platform Management API\n    baseURL: https://anypoint.mulesoft.com\n    tags:\n      - Administration\n      - API Management\n      - Enterprise\n      - REST\n    serviceName: MuleSoft Anypoint Platform Management API\n    serviceCategory: API\n  - name: MuleSoft Anypoint Exchange API\n    baseURL: https://anypoint.mulesoft.com/exchange/api/v2\n    tags:\n      - API Catalog\n      - Asset Management\n      - Enterprise\n      - Marketplace\n    serviceName: MuleSoft Anypoint Exchange API\n    serviceCategory:\
  \ API\n  - name: MuleSoft Anypoint Runtime Manager API\n    baseURL: https://anypoint.mulesoft.com/cloudhub/api\n    tags:\n      - CI/CD\n      - CloudHub\n      - Deployment\n      - Runtime Manager\n    serviceName: MuleSoft Anypoint Runtime Manager API\n    serviceCategory: API\n  - name: MuleSoft Anypoint MQ API\n    baseURL: https://anypoint.mulesoft.com/mq/stats/api/v1\n    tags:\n      - Async\n      - Cloud\n      - Messaging\n      - Queue\n    serviceName: MuleSoft Anypoint MQ API\n    serviceCategory: API\n  - name: MuleSoft Anypoint Design Center API\n    baseURL: https://anypoint.mulesoft.com/designcenter/api-designer\n    tags:\n      - API Design\n      - Design Center\n      - OpenAPI\n      - RAML\n    serviceName: MuleSoft Anypoint Design Center API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n\
  \    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/mulesoft/refs/heads/main/finops/mulesoft-finops.yml
sources: []
specification: FinOps Framework
tags:
- API Gateway
- API Management
- Enterprise
- Integration
- FinOps
- Cost Management
- FOCUS
---
