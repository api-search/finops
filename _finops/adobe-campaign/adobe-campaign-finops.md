---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: adobe-campaign-standard-openapi-original.yml
  format: yaml
  label: Adobe Campaign Standard API
  slug: standard-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/adobe-campaign/refs/heads/main/openapi/adobe-campaign-standard-openapi-original.yml
- filename: adobe-campaign-classic-openapi-original.yml
  format: yaml
  label: Adobe Campaign Classic API
  slug: classic-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/adobe-campaign/refs/heads/main/openapi/adobe-campaign-classic-openapi-original.yml
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
description: FinOps framework definition for the Adobe Campaign API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Adobe Campaign
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Adobe Campaign
  PublisherName: Adobe Campaign
  ServiceCategory: Developer Tools / API
  ServiceName: Adobe Campaign
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
name: Adobe Campaign Finops
provider_name: Adobe Campaign
provider_slug: adobe-campaign
publisher_name: Adobe Campaign
service_category: API
slug: adobe-campaign-finops
source_filename: adobe-campaign-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Adobe Campaign\nproviderId: adobe-campaign\npublisherName: Adobe Campaign\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Campaign Management\n  - Customer Experience\n  - Email Marketing\n  - Marketing Automation\n  - Multi-Channel Marketing\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Adobe Campaign API surface. Provides a FOCUS-aligned\n  mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name:\
  \ Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  -\
  \ name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Adobe Campaign\n  ServiceCategory: Developer Tools / API\n  ProviderName: Adobe Campaign\n  PublisherName: Adobe Campaign\n  InvoiceIssuerName: Adobe Campaign\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description:\
  \ Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Adobe Campaign Standard API\n    baseURL: https://mc.adobe.io/{ORGANIZATION}/campaign\n    tags:\n      - Email\n      - Marketing\n      - Profiles\n      - REST API\n      - Workflows\n    serviceName: Adobe Campaign Standard API\n    serviceCategory: API\n  - name: Adobe Campaign Classic API\n    baseURL: https://{instance}.campaign.adobe.com\n    tags:\n      - Campaign Classic\n      - Delivery\n      - JavaScript\n      - SOAP API\n    serviceName: Adobe Campaign Classic API\n    serviceCategory: API\n  - name: Adobe Campaign Classic JavaScript SDK\n    baseURL: https://{instance}.campaign.adobe.com\n    tags:\n\
  \      - Campaign Classic\n      - JavaScript SDK\n      - Node.js\n      - Open Source\n      - SOAP Wrapper\n    serviceName: Adobe Campaign Classic JavaScript SDK\n    serviceCategory: API\n  - name: Adobe I/O Campaign Standard SDK\n    baseURL: https://mc.adobe.io/{ORGANIZATION}/campaign\n    tags:\n      - Adobe I/O\n      - App Builder\n      - Campaign Standard\n      - JavaScript SDK\n      - Node.js\n    serviceName: Adobe I/O Campaign Standard SDK\n    serviceCategory: API\n  - name: Adobe Experience Platform Mobile SDK - Campaign Extensions\n    baseURL: https://api.example.com\n    tags:\n      - Android\n      - In-App Messaging\n      - iOS\n      - Mobile SDK\n      - Push Notifications\n    serviceName: Adobe Experience Platform Mobile SDK - Campaign Extensions\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n\
  \    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/adobe-campaign/refs/heads/main/finops/adobe-campaign-finops.yml
sources: []
specification: FinOps Framework
tags:
- Campaign Management
- Customer Experience
- Email Marketing
- Marketing Automation
- Multi-Channel Marketing
- FinOps
- Cost Management
- FOCUS
---
