---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: microsoft-bing-openapi.yml
  format: yaml
  label: Bing Web Search API
  slug: web-search
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-bing/refs/heads/main/openapi/microsoft-bing-openapi.yml
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
description: FinOps framework definition for the Microsoft Bing API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Microsoft Bing
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Microsoft Bing
  PublisherName: Microsoft Bing
  ServiceCategory: Developer Tools / API
  ServiceName: Microsoft Bing
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
name: Microsoft Bing Finops
provider_name: Microsoft Bing
provider_slug: microsoft-bing
publisher_name: Microsoft Bing
service_category: API
slug: microsoft-bing-finops
source_filename: microsoft-bing-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Microsoft Bing\nproviderId: microsoft-bing\npublisherName: Microsoft Bing\nserviceCategory: API\ncreated: '2026-05-04'\nmodified: '2026-05-04'\ntags:\n  - Search\n  - Web Search\n  - Images\n  - Videos\n  - News\n  - Azure AI\n  - Autosuggest\n  - Visual Search\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Microsoft Bing API surface. Provides a FOCUS-aligned\n  mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n\
  \    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage\
  \ the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Microsoft Bing\n  ServiceCategory: Developer Tools / API\n  ProviderName: Microsoft Bing\n  PublisherName: Microsoft Bing\n  InvoiceIssuerName: Microsoft Bing\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes\
  \ returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Bing Web Search API\n    baseURL: https://api.bing.microsoft.com/\n    tags:\n      - Search\n      - Web Search\n      - Azure AI\n    serviceName: Bing Web Search API\n    serviceCategory: API\n  - name: Bing Image Search API\n    baseURL: https://api.bing.microsoft.com/\n    tags:\n      - Search\n      - Images\n      - Azure AI\n    serviceName: Bing Image Search API\n    serviceCategory: API\n  - name: Bing Video Search API\n    baseURL: https://api.bing.microsoft.com/\n    tags:\n      - Search\n      - Videos\n      - Azure AI\n    serviceName: Bing Video Search API\n    serviceCategory: API\n  - name: Bing News\
  \ Search API\n    baseURL: https://api.bing.microsoft.com/\n    tags:\n      - Search\n      - News\n      - Azure AI\n    serviceName: Bing News Search API\n    serviceCategory: API\n  - name: Bing Entity Search API\n    baseURL: https://api.bing.microsoft.com/\n    tags:\n      - Search\n      - Entities\n      - Knowledge Graph\n      - Azure AI\n    serviceName: Bing Entity Search API\n    serviceCategory: API\n  - name: Bing Autosuggest API\n    baseURL: https://api.bing.microsoft.com/\n    tags:\n      - Search\n      - Autosuggest\n      - Autocomplete\n      - Azure AI\n    serviceName: Bing Autosuggest API\n    serviceCategory: API\n  - name: Bing Spell Check API\n    baseURL: https://api.bing.microsoft.com/\n    tags:\n      - Search\n      - Spell Check\n      - NLP\n      - Azure AI\n    serviceName: Bing Spell Check API\n    serviceCategory: API\n  - name: Bing Visual Search API\n    baseURL: https://api.bing.microsoft.com/\n    tags:\n      - Search\n      - Visual Search\n\
  \      - Image Recognition\n      - Azure AI\n    serviceName: Bing Visual Search API\n    serviceCategory: API\n  - name: Bing Custom Search API\n    baseURL: https://api.bing.microsoft.com/\n    tags:\n      - Search\n      - Custom Search\n      - Azure AI\n    serviceName: Bing Custom Search API\n    serviceCategory: API\n  - name: Bing Local Business Search API\n    baseURL: https://api.bing.microsoft.com/\n    tags:\n      - Search\n      - Local Business\n      - Places\n      - Azure AI\n    serviceName: Bing Local Business Search API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/microsoft-bing/refs/heads/main/finops/microsoft-bing-finops.yml
sources: []
specification: FinOps Framework
tags:
- Search
- Web Search
- Images
- Videos
- News
- Azure AI
- Autosuggest
- Visual Search
- FinOps
- Cost Management
- FOCUS
---
