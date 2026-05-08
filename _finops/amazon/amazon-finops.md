---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: amazon-selling-partner-api-openapi.yml
  format: yaml
  label: Amazon Selling Partner API
  slug: selling-partner-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/amazon/refs/heads/main/openapi/amazon-selling-partner-api-openapi.yml
- filename: amazon-advertising-api-openapi.yml
  format: yaml
  label: Amazon Advertising API
  slug: advertising-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/amazon/refs/heads/main/openapi/amazon-advertising-api-openapi.yml
- filename: amazon-pay-api-openapi.yml
  format: yaml
  label: Amazon Pay API
  slug: pay-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/amazon/refs/heads/main/openapi/amazon-pay-api-openapi.yml
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
description: FinOps framework definition for the Amazon API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Amazon
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Amazon
  PublisherName: Amazon
  ServiceCategory: Developer Tools / API
  ServiceName: Amazon
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
name: Amazon Finops
provider_name: Amazon
provider_slug: amazon
publisher_name: Amazon
service_category: API
slug: amazon-finops
source_filename: amazon-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Amazon\nproviderId: amazon\npublisherName: Amazon\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Amazon\n  - Advertising\n  - Alexa\n  - E-Commerce\n  - Marketplace\n  - Payments\n  - Voice\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Amazon API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call\
  \ with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n    \
  \  - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Amazon\n  ServiceCategory: Developer Tools / API\n  ProviderName: Amazon\n  PublisherName: Amazon\n  InvoiceIssuerName: Amazon\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n\
  \    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Amazon Selling Partner API\n    baseURL: https://sellingpartnerapi-na.amazon.com\n    tags:\n      - E-Commerce\n      - Fulfillment\n      - Marketplace\n      - Orders\n      - Sellers\n    serviceName: Amazon Selling Partner API\n    serviceCategory: API\n  - name: Amazon Advertising API\n    baseURL: https://advertising-api.amazon.com\n    tags:\n      - Advertising\n      - Campaigns\n      - Marketing\n      - Sponsored Products\n    serviceName: Amazon Advertising API\n    serviceCategory: API\n  - name: Amazon Creators API\n    baseURL: https://affiliate-program.amazon.com/creatorsapi\n    tags:\n      - Affiliates\n      - Content Creators\n      - E-Commerce\n      - Products\n    serviceName:\
  \ Amazon Creators API\n    serviceCategory: API\n  - name: Amazon Pay API\n    baseURL: https://pay-api.amazon.com\n    tags:\n      - Checkout\n      - E-Commerce\n      - Payments\n      - Subscriptions\n    serviceName: Amazon Pay API\n    serviceCategory: API\n  - name: Amazon Alexa Skills Kit API\n    baseURL: https://api.amazonalexa.com\n    tags:\n      - Alexa\n      - Skills\n      - Smart Home\n      - Voice\n    serviceName: Amazon Alexa Skills Kit API\n    serviceCategory: API\n  - name: Amazon Appstore API\n    baseURL: https://developer.amazon.com/api/appstore\n    tags:\n      - App Store\n      - Apps\n      - In-App Purchases\n      - Mobile\n    serviceName: Amazon Appstore API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/amazon/refs/heads/main/finops/amazon-finops.yml
sources: []
specification: FinOps Framework
tags:
- Amazon
- Advertising
- Alexa
- E-Commerce
- Marketplace
- Payments
- Voice
- FinOps
- Cost Management
- FOCUS
---
