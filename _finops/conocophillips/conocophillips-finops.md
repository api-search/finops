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
description: FinOps framework definition for the ConocoPhillips API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: ConocoPhillips
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: ConocoPhillips
  PublisherName: ConocoPhillips
  ServiceCategory: Developer Tools / API
  ServiceName: ConocoPhillips
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
name: Conocophillips Finops
provider_name: ConocoPhillips
provider_slug: conocophillips
publisher_name: ConocoPhillips
service_category: API
slug: conocophillips-finops
source_filename: conocophillips-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: ConocoPhillips\nproviderId: conocophillips\npublisherName: ConocoPhillips\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Crude Oil\n  - Energy\n  - Exploration and Production\n  - LNG\n  - Natural Gas\n  - Oil and Gas\n  - Sustainability\n  - Upstream\n  - Vendor Portal\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the ConocoPhillips API surface. Provides a FOCUS-aligned\n  mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n\
  \      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n   \
  \   - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: ConocoPhillips\n  ServiceCategory: Developer Tools / API\n  ProviderName: ConocoPhillips\n  PublisherName: ConocoPhillips\n  InvoiceIssuerName: ConocoPhillips\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name:\
  \ data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: ConocoPhillips Vendor Relations Portal\n    baseURL: ''\n    tags:\n      - Procurement\n      - Supplier Portal\n      - Vendor\n    serviceName: ConocoPhillips Vendor Relations Portal\n    serviceCategory: API\n  - name: ConocoPhillips LNG Technology and Licensing\n    baseURL: ''\n    tags:\n      - Licensing\n      - LNG\n      - Technology\n    serviceName: ConocoPhillips LNG Technology and Licensing\n    serviceCategory: API\n  - name: ConocoPhillips Custom Sustainability Report Builder\n    baseURL: ''\n    tags:\n      - ESG\n      - Reporting\n      - Sustainability\n    serviceName:\
  \ ConocoPhillips Custom Sustainability Report Builder\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/conocophillips/refs/heads/main/finops/conocophillips-finops.yml
sources: []
specification: FinOps Framework
tags:
- Crude Oil
- Energy
- Exploration and Production
- LNG
- Natural Gas
- Oil and Gas
- Sustainability
- Upstream
- Vendor Portal
- FinOps
- Cost Management
- FOCUS
---
