---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: braintree-payments-openapi.yml
  format: yaml
  label: Braintree Payments API
  slug: payments-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/braintree/refs/heads/main/openapi/braintree-payments-openapi.yml
- filename: braintree-webhooks-asyncapi.yml
  format: yaml
  label: Braintree Webhooks
  slug: webhooks
  spec_type: AsyncAPI
  url: https://raw.githubusercontent.com/api-evangelist/braintree/refs/heads/main/asyncapi/braintree-webhooks-asyncapi.yml
- filename: braintree-payments-openapi.yml
  format: yaml
  label: Braintree Vault API
  slug: vault-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/braintree/refs/heads/main/openapi/braintree-payments-openapi.yml
- filename: braintree-subscriptions-openapi.yml
  format: yaml
  label: Braintree Subscriptions API
  slug: subscriptions-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/braintree/refs/heads/main/openapi/braintree-subscriptions-openapi.yml
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
description: FinOps framework definition for the braintree API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: braintree
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: braintree
  PublisherName: braintree
  ServiceCategory: Developer Tools / API
  ServiceName: braintree
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
name: Braintree Finops
provider_name: braintree
provider_slug: braintree
publisher_name: braintree
service_category: API
slug: braintree-finops
source_filename: braintree-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: braintree\nproviderId: braintree\npublisherName: braintree\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the braintree API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be\
  \ allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing\
  \ and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: braintree\n  ServiceCategory: Developer Tools / API\n  ProviderName: braintree\n  PublisherName: braintree\n  InvoiceIssuerName: braintree\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n\
  \    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Braintree Payments API\n    baseURL: https://api.braintreegateway.com\n    tags:\n      - Credit Cards\n      - Payments\n      - PayPal\n      - Transactions\n    serviceName: Braintree Payments API\n    serviceCategory: API\n  - name: Braintree GraphQL API\n    baseURL: https://payments.braintree-api.com/graphql\n    tags:\n      - GraphQL\n      - Payment Methods\n      - Payments\n      - Transactions\n    serviceName: Braintree GraphQL API\n    serviceCategory: API\n  - name: Braintree JavaScript Client SDK\n    baseURL: https://api.example.com\n    tags:\n      - Browser\n      - Client SDK\n      - Drop-In UI\n      - JavaScript\n      - Payments\n    serviceName: Braintree JavaScript Client SDK\n    serviceCategory: API\n  - name: Braintree iOS SDK\n    baseURL: https://api.example.com\n\
  \    tags:\n      - iOS\n      - Mobile\n      - Objective-C\n      - Payments\n      - Swift\n    serviceName: Braintree iOS SDK\n    serviceCategory: API\n  - name: Braintree Android SDK\n    baseURL: https://api.example.com\n    tags:\n      - Android\n      - Java\n      - Kotlin\n      - Mobile\n      - Payments\n    serviceName: Braintree Android SDK\n    serviceCategory: API\n  - name: Braintree Webhooks\n    baseURL: https://api.example.com\n    tags:\n      - Disputes\n      - Events\n      - Notifications\n      - Subscriptions\n      - Webhooks\n    serviceName: Braintree Webhooks\n    serviceCategory: API\n  - name: Braintree Vault API\n    baseURL: https://api.braintreegateway.com\n    tags:\n      - Customers\n      - Payment Methods\n      - PCI Compliance\n      - Storage\n      - Vault\n    serviceName: Braintree Vault API\n    serviceCategory: API\n  - name: Braintree Subscriptions API\n    baseURL: https://api.braintreegateway.com\n    tags:\n      - Payments\n     \
  \ - Plans\n      - Recurring Billing\n      - Subscriptions\n    serviceName: Braintree Subscriptions API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers: []\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/braintree/refs/heads/main/finops/braintree-finops.yml
sources: []
specification: FinOps Framework
tags:
- FinOps
- Cost Management
- FOCUS
---
