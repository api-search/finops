---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: magento-rest-api-openapi.yml
  format: yaml
  label: Magento REST API
  slug: rest-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/magento/refs/heads/main/openapi/magento-rest-api-openapi.yml
- filename: magento-webhooks-asyncapi.yml
  format: yaml
  label: Adobe Commerce Webhooks
  slug: webhooks
  spec_type: AsyncAPI
  url: https://raw.githubusercontent.com/api-evangelist/magento/refs/heads/main/asyncapi/magento-webhooks-asyncapi.yml
- filename: magento-events-asyncapi.yml
  format: yaml
  label: Adobe Commerce Eventing
  slug: events
  spec_type: AsyncAPI
  url: https://raw.githubusercontent.com/api-evangelist/magento/refs/heads/main/asyncapi/magento-events-asyncapi.yml
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
description: FinOps framework definition for the magento API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: magento
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: magento
  PublisherName: magento
  ServiceCategory: Developer Tools / API
  ServiceName: magento
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
name: Magento Finops
provider_name: magento
provider_slug: magento
publisher_name: magento
service_category: API
slug: magento-finops
source_filename: magento-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: magento\nproviderId: magento\npublisherName: magento\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the magento API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n\
  \  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n\
  \      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: magento\n  ServiceCategory: Developer Tools / API\n  ProviderName: magento\n  PublisherName: magento\n  InvoiceIssuerName: magento\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description:\
  \ Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Magento REST API\n    baseURL: https://your-store.example.com/rest\n    tags:\n      - Catalog\n      - Customers\n      - E-Commerce\n      - Orders\n      - Products\n      - REST\n    serviceName: Magento REST API\n    serviceCategory: API\n  - name: Magento GraphQL API\n    baseURL: https://your-store.example.com/graphql\n    tags:\n      - Cart\n      - Catalog\n      - E-Commerce\n      - GraphQL\n      - Headless Commerce\n      - Storefront\n    serviceName: Magento GraphQL API\n    serviceCategory: API\n  - name: Magento SOAP API\n    baseURL: https://your-store.example.com/soap\n    tags:\n      - E-Commerce\n      - Integration\n      - SOAP\n      - Web Services\n    serviceName: Magento SOAP API\n    serviceCategory: API\n  - name: Adobe Commerce Webhooks\n    baseURL: https://api.example.com\n\
  \    tags:\n      - E-Commerce\n      - Events\n      - Extensibility\n      - Real-Time\n      - Webhooks\n    serviceName: Adobe Commerce Webhooks\n    serviceCategory: API\n  - name: Adobe Commerce Admin UI SDK\n    baseURL: https://api.example.com\n    tags:\n      - Admin Panel\n      - App Builder\n      - E-Commerce\n      - Extensibility\n      - UI Extensions\n    serviceName: Adobe Commerce Admin UI SDK\n    serviceCategory: API\n  - name: Adobe Commerce Eventing\n    baseURL: https://api.example.com\n    tags:\n      - Adobe I/O\n      - App Builder\n      - E-Commerce\n      - Events\n      - Extensibility\n    serviceName: Adobe Commerce Eventing\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers: []\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/magento/refs/heads/main/finops/magento-finops.yml
sources: []
specification: FinOps Framework
tags:
- FinOps
- Cost Management
- FOCUS
---
