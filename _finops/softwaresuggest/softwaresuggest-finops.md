---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
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
description: FinOps framework definition for the SoftwareSuggest API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: SoftwareSuggest
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: SoftwareSuggest
  PublisherName: SoftwareSuggest
  ServiceCategory: Developer Tools / API
  ServiceName: SoftwareSuggest
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
name: Softwaresuggest Finops
provider_name: SoftwareSuggest
provider_slug: softwaresuggest
publisher_name: SoftwareSuggest
service_category: API
slug: softwaresuggest-finops
source_filename: softwaresuggest-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: SoftwareSuggest\nproviderId: softwaresuggest\npublisherName: SoftwareSuggest\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Software Discovery\n  - Business Software\n  - SaaS\n  - Software Reviews\n  - B2B\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the SoftwareSuggest API surface. Provides a FOCUS-aligned\n  mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag\
  \ every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n\
  \    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: SoftwareSuggest\n  ServiceCategory: Developer Tools / API\n  ProviderName: SoftwareSuggest\n  PublisherName: SoftwareSuggest\n  InvoiceIssuerName: SoftwareSuggest\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the\
  \ network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: SoftwareSuggest Software Catalog\n    baseURL: https://www.softwaresuggest.com\n    tags:\n      - Software Catalog\n      - Discovery\n      - Comparison\n      - B2B Software\n    serviceName: SoftwareSuggest Software Catalog\n    serviceCategory: API\n  - name: SoftwareSuggest Vendor Portal\n    baseURL: https://www.softwaresuggest.com/vendorsportal\n    tags:\n      - Vendor Management\n      - Lead Generation\n      - Product Listing\n      - Analytics\n    serviceName: SoftwareSuggest Vendor Portal\n    serviceCategory: API\n  - name: SoftwareSuggest Affiliate Program\n    baseURL: https://www.softwaresuggest.com\n    tags:\n      -\
  \ Affiliate Marketing\n      - Partner Program\n      - Lead Generation\n      - CPL\n    serviceName: SoftwareSuggest Affiliate Program\n    serviceCategory: API\n  - name: SoftwareSuggest Data Products\n    baseURL: https://datarade.ai\n    tags:\n      - Business Data\n      - Market Intelligence\n      - Software Adoption Data\n      - Data Marketplace\n    serviceName: SoftwareSuggest Data Products\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/softwaresuggest/refs/heads/main/finops/softwaresuggest-finops.yml
sources: []
specification: FinOps Framework
tags:
- Software Discovery
- Business Software
- SaaS
- Software Reviews
- B2B
- FinOps
- Cost Management
- FOCUS
---
