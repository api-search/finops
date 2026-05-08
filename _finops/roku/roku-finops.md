---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: roku-external-control-protocol.yaml
  format: yaml
  label: Roku External Control Protocol (ECP)
  slug: external-control-protocol
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/roku/refs/heads/main/openapi/roku-external-control-protocol.yaml
- filename: roku-pay-web-services.yaml
  format: yaml
  label: Roku Pay Web Services
  slug: pay
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/roku/refs/heads/main/openapi/roku-pay-web-services.yaml
- filename: roku-nabu-cloud.yaml
  format: yaml
  label: Roku Nabu Cloud
  slug: nabu-cloud
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/roku/refs/heads/main/openapi/roku-nabu-cloud.yaml
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
description: FinOps framework definition for the Roku API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Roku
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Roku
  PublisherName: Roku
  ServiceCategory: Developer Tools / API
  ServiceName: Roku
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
name: Roku Finops
provider_name: Roku
provider_slug: roku
publisher_name: Roku
service_category: API
slug: roku-finops
source_filename: roku-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Roku\nproviderId: roku\npublisherName: Roku\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Streaming\n  - Television\n  - Media\n  - Entertainment\n  - Connected TV\n  - Consumer Electronics\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Roku API surface. Provides a FOCUS-aligned mapping for\n  cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call\
  \ with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n    \
  \  - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Roku\n  ServiceCategory: Developer Tools / API\n  ProviderName: Roku\n  PublisherName: Roku\n  InvoiceIssuerName: Roku\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n\
  \      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Roku BrightScript SDK\n    baseURL: ''\n    tags:\n      - SDK\n      - BrightScript\n      - Channel Development\n    serviceName: Roku BrightScript SDK\n    serviceCategory: API\n  - name: Roku SceneGraph\n    baseURL: ''\n    tags:\n      - UI Framework\n      - SceneGraph\n      - Channel Development\n    serviceName: Roku SceneGraph\n    serviceCategory: API\n  - name: Roku External Control Protocol (ECP)\n    baseURL: ''\n    tags:\n      - REST\n      - HTTP\n      - Device Control\n      - LAN\n    serviceName: Roku External Control Protocol (ECP)\n    serviceCategory: API\n  - name: Roku Pay Web Services\n    baseURL: ''\n    tags:\n      - Billing\n      - Payments\n      - Subscriptions\n      - Monetization\n\
  \    serviceName: Roku Pay Web Services\n    serviceCategory: API\n  - name: Roku Nabu Cloud\n    baseURL: ''\n    tags:\n      - REST\n      - Developer Cloud\n      - Test Devices\n      - CI CD\n    serviceName: Roku Nabu Cloud\n    serviceCategory: API\n  - name: Roku Search Feed\n    baseURL: ''\n    tags:\n      - Feed\n      - Search\n      - Content Catalog\n    serviceName: Roku Search Feed\n    serviceCategory: API\n  - name: Roku Direct Publisher Feed\n    baseURL: ''\n    tags:\n      - Feed\n      - Direct Publisher\n      - Content Catalog\n    serviceName: Roku Direct Publisher Feed\n    serviceCategory: API\n  - name: Roku Analytics\n    baseURL: ''\n    tags:\n      - Analytics\n      - Reporting\n    serviceName: Roku Analytics\n    serviceCategory: API\n  - name: Roku Authentication Framework\n    baseURL: ''\n    tags:\n      - Authentication\n      - OAuth\n    serviceName: Roku Authentication Framework\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per\
  \ 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: API Evangelist\n    url: https://apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/roku/refs/heads/main/finops/roku-finops.yml
sources: []
specification: FinOps Framework
tags:
- Streaming
- Television
- Media
- Entertainment
- Connected TV
- Consumer Electronics
- FinOps
- Cost Management
- FOCUS
---
