---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: shopify-api-openapi.yml
  format: yaml
  label: Shopify Admin REST API
  slug: shopify-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/shopify/refs/heads/main/openapi/shopify-api-openapi.yml
- filename: shopify-ajax-api-openapi.yml
  format: yaml
  label: Shopify Ajax API
  slug: ajax-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/shopify/refs/heads/main/openapi/shopify-ajax-api-openapi.yml
- filename: shopify-webhooks-api-openapi.yml
  format: yaml
  label: Shopify Webhooks API
  slug: webhooks-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/shopify/refs/heads/main/openapi/shopify-webhooks-api-openapi.yml
- filename: shopify-multipass-api-openapi.yml
  format: yaml
  label: Shopify Multipass API
  slug: multipass-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/shopify/refs/heads/main/openapi/shopify-multipass-api-openapi.yml
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
description: FinOps framework definition for the Shopify API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Shopify
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Shopify
  PublisherName: Shopify
  ServiceCategory: Developer Tools / API
  ServiceName: Shopify
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
name: Shopify Finops
provider_name: Shopify
provider_slug: shopify
publisher_name: Shopify
service_category: API
slug: shopify-finops
source_filename: shopify-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Shopify\nproviderId: shopify\npublisherName: Shopify\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Commerce\n  - Ecommerce\n  - Payments\n  - Retail\n  - Shopping Cart\n  - T1\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Shopify API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming\
  \ team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice\
  \ Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Shopify\n  ServiceCategory: Developer Tools / API\n  ProviderName: Shopify\n  PublisherName: Shopify\n  InvoiceIssuerName: Shopify\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n\
  \      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Shopify Admin REST API\n    baseURL: ''\n    tags:\n      - Admin\n      - Commerce\n      - Ecommerce\n      - REST\n      - Retail\n    serviceName: Shopify Admin REST API\n    serviceCategory: API\n  - name: Shopify GraphQL Admin API\n    baseURL: ''\n    tags:\n      - Admin\n      - Commerce\n      - GraphQL\n    serviceName: Shopify GraphQL Admin API\n    serviceCategory: API\n  - name: Shopify Storefront API\n    baseURL: ''\n    tags:\n      - Commerce\n      - GraphQL\n      - Headless\n      - Storefronts\n    serviceName: Shopify Storefront API\n    serviceCategory: API\n  - name: Shopify Customer Account API\n    baseURL: ''\n    tags:\n      - Accounts\n      - Commerce\n      - Customers\n      - GraphQL\n\
  \    serviceName: Shopify Customer Account API\n    serviceCategory: API\n  - name: Shopify Partner API\n    baseURL: ''\n    tags:\n      - Commerce\n      - GraphQL\n      - Partners\n    serviceName: Shopify Partner API\n    serviceCategory: API\n  - name: Shopify Payments Apps API\n    baseURL: ''\n    tags:\n      - Commerce\n      - GraphQL\n      - Payments\n    serviceName: Shopify Payments Apps API\n    serviceCategory: API\n  - name: Shopify Ajax API\n    baseURL: ''\n    tags:\n      - Commerce\n      - REST\n      - Themes\n    serviceName: Shopify Ajax API\n    serviceCategory: API\n  - name: Shopify Liquid API\n    baseURL: ''\n    tags:\n      - Commerce\n      - Templates\n      - Themes\n    serviceName: Shopify Liquid API\n    serviceCategory: API\n  - name: Shopify Functions API\n    baseURL: ''\n    tags:\n      - Commerce\n      - Serverless\n      - WebAssembly\n    serviceName: Shopify Functions API\n    serviceCategory: API\n  - name: Shopify Discount Function API\n\
  \    baseURL: ''\n    tags:\n      - Commerce\n      - Discounts\n      - Functions\n    serviceName: Shopify Discount Function API\n    serviceCategory: API\n  - name: Shopify Webhooks API\n    baseURL: ''\n    tags:\n      - Commerce\n      - Events\n      - Webhooks\n    serviceName: Shopify Webhooks API\n    serviceCategory: API\n  - name: Shopify App Bridge\n    baseURL: ''\n    tags:\n      - Commerce\n      - Embedded Apps\n      - UI\n    serviceName: Shopify App Bridge\n    serviceCategory: API\n  - name: Shopify App Home API\n    baseURL: ''\n    tags:\n      - Apps\n      - Commerce\n      - UI\n    serviceName: Shopify App Home API\n    serviceCategory: API\n  - name: Shopify Checkout UI Extensions API\n    baseURL: ''\n    tags:\n      - Checkout\n      - Commerce\n      - Extensions\n    serviceName: Shopify Checkout UI Extensions API\n    serviceCategory: API\n  - name: Shopify Multipass API\n    baseURL: ''\n    tags:\n      - Authentication\n      - Commerce\n      - SSO\n\
  \    serviceName: Shopify Multipass API\n    serviceCategory: API\n  - name: Shopify POS UI Extensions API\n    baseURL: ''\n    tags:\n      - Commerce\n      - Extensions\n      - Point of Sale\n    serviceName: Shopify POS UI Extensions API\n    serviceCategory: API\n  - name: Shopify Admin Extensions API\n    baseURL: ''\n    tags:\n      - Admin\n      - Commerce\n      - Extensions\n    serviceName: Shopify Admin Extensions API\n    serviceCategory: API\n  - name: Shopify Hydrogen\n    baseURL: ''\n    tags:\n      - Commerce\n      - Framework\n      - Headless\n      - React\n    serviceName: Shopify Hydrogen\n    serviceCategory: API\n  - name: Shopify Polaris\n    baseURL: ''\n    tags:\n      - Commerce\n      - Components\n      - Design System\n      - UI\n    serviceName: Shopify Polaris\n    serviceCategory: API\n  - name: Shopify CLI\n    baseURL: ''\n    tags:\n      - CLI\n      - Commerce\n      - Development Tools\n    serviceName: Shopify CLI\n    serviceCategory:\
  \ API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    url: http://apievangelist.com\n    email: kin@apievangelist.com\n  - name: Shopify\n    email: api@shopify.com\n    url: https://www.shopify.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/shopify/refs/heads/main/finops/shopify-finops.yml
sources: []
specification: FinOps Framework
tags:
- Commerce
- Ecommerce
- Payments
- Retail
- Shopping Cart
- T1
- FinOps
- Cost Management
- FOCUS
---
