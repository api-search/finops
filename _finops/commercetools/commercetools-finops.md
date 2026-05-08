---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: commercetools-http-api-openapi.yml
  format: yaml
  label: Commercetools HTTP API
  slug: http-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/commercetools/refs/heads/main/openapi/commercetools-http-api-openapi.yml
- filename: commercetools-import-api-openapi.yml
  format: yaml
  label: Commercetools Import API
  slug: import-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/commercetools/refs/heads/main/openapi/commercetools-import-api-openapi.yml
- filename: commercetools-change-history-api-openapi.yml
  format: yaml
  label: Commercetools Change History API
  slug: change-history-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/commercetools/refs/heads/main/openapi/commercetools-change-history-api-openapi.yml
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
description: FinOps framework definition for the commercetools API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: commercetools
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: commercetools
  PublisherName: commercetools
  ServiceCategory: Developer Tools / API
  ServiceName: commercetools
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
name: Commercetools Finops
provider_name: commercetools
provider_slug: commercetools
publisher_name: commercetools
service_category: API
slug: commercetools-finops
source_filename: commercetools-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: commercetools\nproviderId: commercetools\npublisherName: commercetools\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Commerce\n  - Composable Commerce\n  - E-Commerce\n  - GraphQL\n  - REST\n  - SDK\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the commercetools API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable\
  \ API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n\
  \      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: commercetools\n  ServiceCategory: Developer Tools / API\n  ProviderName: commercetools\n  PublisherName: commercetools\n  InvoiceIssuerName: commercetools\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n\
  \    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Commercetools HTTP API\n    baseURL: https://api.{region}.commercetools.com\n    tags:\n      - Commerce\n      - Composable Commerce\n      - E-Commerce\n      - REST\n    serviceName: Commercetools HTTP API\n    serviceCategory: API\n  - name: Commercetools GraphQL API\n    baseURL: https://api.{region}.commercetools.com\n    tags:\n      - Commerce\n      - Composable Commerce\n      - E-Commerce\n      - GraphQL\n    serviceName: Commercetools GraphQL API\n    serviceCategory: API\n  - name: Commercetools Import API\n    baseURL: https://import.{region}.commercetools.com\n    tags:\n      - Bulk Operations\n      - Commerce\n      - Data Migration\n      - Import\n\
  \    serviceName: Commercetools Import API\n    serviceCategory: API\n  - name: Commercetools Change History API\n    baseURL: https://history.{region}.commercetools.com\n    tags:\n      - Audit Log\n      - Change History\n      - Commerce\n      - Compliance\n    serviceName: Commercetools Change History API\n    serviceCategory: API\n  - name: Commercetools TypeScript SDK\n    baseURL: https://api.example.com\n    tags:\n      - Commerce\n      - JavaScript\n      - SDK\n      - TypeScript\n    serviceName: Commercetools TypeScript SDK\n    serviceCategory: API\n  - name: Commercetools Java SDK\n    baseURL: https://api.example.com\n    tags:\n      - Commerce\n      - Java\n      - JVM\n      - SDK\n    serviceName: Commercetools Java SDK\n    serviceCategory: API\n  - name: Commercetools Checkout API\n    baseURL: https://api.example.com\n    tags:\n      - Checkout\n      - Commerce\n      - Embedded Components\n      - Payments\n    serviceName: Commercetools Checkout API\n   \
  \ serviceCategory: API\n  - name: Commercetools Merchant Center Customizations API\n    baseURL: https://api.example.com\n    tags:\n      - Commerce\n      - Customizations\n      - Extensions\n      - Merchant Center\n    serviceName: Commercetools Merchant Center Customizations API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/commercetools/refs/heads/main/finops/commercetools-finops.yml
sources: []
specification: FinOps Framework
tags:
- Commerce
- Composable Commerce
- E-Commerce
- GraphQL
- REST
- SDK
- FinOps
- Cost Management
- FOCUS
---
