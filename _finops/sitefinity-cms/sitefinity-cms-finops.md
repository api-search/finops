---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: sitefinity-cms-content-api-openapi.yml
  format: yaml
  label: Sitefinity CMS Content API
  slug: content-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/sitefinity-cms/refs/heads/main/openapi/sitefinity-cms-content-api-openapi.yml
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
description: FinOps framework definition for the Sitefinity CMS API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Sitefinity CMS
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Sitefinity CMS
  PublisherName: Sitefinity CMS
  ServiceCategory: Developer Tools / API
  ServiceName: Sitefinity CMS
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
name: Sitefinity Cms Finops
provider_name: Sitefinity CMS
provider_slug: sitefinity-cms
publisher_name: Sitefinity CMS
service_category: API
slug: sitefinity-cms-finops
source_filename: sitefinity-cms-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Sitefinity CMS\nproviderId: sitefinity-cms\npublisherName: Sitefinity CMS\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Content Management\n  - Headless CMS\n  - .NET\n  - REST\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Sitefinity CMS API surface. Provides a FOCUS-aligned\n  mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with\
  \ the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps\
  \ Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Sitefinity CMS\n  ServiceCategory: Developer Tools / API\n  ProviderName: Sitefinity CMS\n  PublisherName: Sitefinity CMS\n  InvoiceIssuerName: Sitefinity CMS\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n\
  \    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Sitefinity CMS Content API\n    baseURL: https://your-site.sitefinity.com/api/default\n    tags:\n      - Content Management\n      - Content Types\n      - REST\n    serviceName: Sitefinity CMS Content API\n    serviceCategory: API\n  - name: Sitefinity CMS Pages API\n    baseURL: https://your-site.sitefinity.com/api/default\n    tags:\n      - Pages\n      - Content Management\n      - REST\n    serviceName: Sitefinity CMS Pages API\n    serviceCategory: API\n  - name: Sitefinity CMS Users and Roles API\n    baseURL: https://your-site.sitefinity.com/api/default\n    tags:\n      - Users\n      - Roles\n      - Identity\n      - REST\n    serviceName: Sitefinity CMS Users and Roles\
  \ API\n    serviceCategory: API\n  - name: Sitefinity CMS Media API\n    baseURL: https://your-site.sitefinity.com/api/default\n    tags:\n      - Media\n      - Digital Assets\n      - Libraries\n      - REST\n    serviceName: Sitefinity CMS Media API\n    serviceCategory: API\n  - name: Sitefinity CMS Taxonomies API\n    baseURL: https://your-site.sitefinity.com/api/default\n    tags:\n      - Taxonomies\n      - Classification\n      - Content Management\n      - REST\n    serviceName: Sitefinity CMS Taxonomies API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers: []\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/sitefinity-cms/refs/heads/main/finops/sitefinity-cms-finops.yml
sources: []
specification: FinOps Framework
tags:
- Content Management
- Headless CMS
- .NET
- REST
- FinOps
- Cost Management
- FOCUS
---
