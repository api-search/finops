---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: samsung-smartthings-openapi.yml
  format: yaml
  label: SmartThings API
  slug: smartthings
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/samsung/refs/heads/main/openapi/samsung-smartthings-openapi.yml
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
description: FinOps framework definition for the Samsung API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Samsung
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Samsung
  PublisherName: Samsung
  ServiceCategory: Developer Tools / API
  ServiceName: Samsung
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
name: Samsung Finops
provider_name: Samsung
provider_slug: samsung
publisher_name: Samsung
service_category: API
slug: samsung-finops
source_filename: samsung-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Samsung\nproviderId: samsung\npublisherName: Samsung\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Consumer Electronics\n  - Developer Platform\n  - IoT\n  - Mobile\n  - Smart Home\n  - Smart TV\n  - Wearables\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Samsung API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every\
  \ chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n   \
  \ capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Samsung\n  ServiceCategory: Developer Tools / API\n  ProviderName: Samsung\n  PublisherName: Samsung\n  InvoiceIssuerName: Samsung\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit:\
  \ GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: SmartThings API\n    baseURL: https://api.smartthings.com/v1\n    tags:\n      - Automations\n      - Connected Devices\n      - IoT\n      - Locations\n      - Rules\n      - Scenes\n      - Smart Home\n      - SmartThings\n    serviceName: SmartThings API\n    serviceCategory: API\n  - name: Knox Cloud APIs\n    baseURL: ''\n    tags:\n      - Device Management\n      - Enterprise\n      - Knox\n      - MDM\n      - Mobile Device Management\n      - Security\n    serviceName: Knox Cloud APIs\n    serviceCategory: API\n  - name: Samsung Health SDK\n    baseURL: ''\n    tags:\n      - Fitness\n      - Galaxy Watch\n      - Health\n      - Wearables\n    serviceName: Samsung\
  \ Health SDK\n    serviceCategory: API\n  - name: Galaxy Mobile SDKs\n    baseURL: ''\n    tags:\n      - Android\n      - Foldable\n      - Galaxy\n      - Mobile\n      - S Pen\n      - Samsung DeX\n    serviceName: Galaxy Mobile SDKs\n    serviceCategory: API\n  - name: Samsung Smart TV SDK\n    baseURL: ''\n    tags:\n      - Media\n      - Smart TV\n      - Streaming\n      - Tizen\n      - TV\n    serviceName: Samsung Smart TV SDK\n    serviceCategory: API\n  - name: Bixby Developer API\n    baseURL: ''\n    tags:\n      - AI\n      - Bixby\n      - Natural Language Processing\n      - Voice Assistant\n    serviceName: Bixby Developer API\n    serviceCategory: API\n  - name: Samsung Wallet API\n    baseURL: ''\n    tags:\n      - Digital Wallet\n      - Loyalty\n      - Passes\n      - Payments\n      - Wallet\n    serviceName: Samsung Wallet API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target:\
  \ TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/samsung/refs/heads/main/finops/samsung-finops.yml
sources: []
specification: FinOps Framework
tags:
- Consumer Electronics
- Developer Platform
- IoT
- Mobile
- Smart Home
- Smart TV
- Wearables
- FinOps
- Cost Management
- FOCUS
---
