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
description: FinOps framework definition for the Citation File Format API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Citation File Format
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Citation File Format
  PublisherName: Citation File Format
  ServiceCategory: Developer Tools / API
  ServiceName: Citation File Format
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
name: Citation Cff Finops
provider_name: Citation File Format
provider_slug: citation-cff
publisher_name: Citation File Format
service_category: API
slug: citation-cff-finops
source_filename: citation-cff-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Citation File Format\nproviderId: citation-cff\npublisherName: Citation File Format\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Academic\n  - Citation\n  - Metadata\n  - Open Standard\n  - Repository\n  - Research\n  - Software\n  - YAML\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Citation File Format API surface. Provides a FOCUS-aligned\n  mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  -\
  \ name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n\
  \  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Citation File Format\n  ServiceCategory: Developer Tools / API\n  ProviderName: Citation File Format\n  PublisherName: Citation File Format\n  InvoiceIssuerName: Citation File Format\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name:\
  \ data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Citation File Format Schema\n    baseURL: ''\n    tags:\n      - JSON Schema\n      - Schema\n      - Validation\n      - YAML\n    serviceName: Citation File Format Schema\n    serviceCategory: API\n  - name: cffinit Authoring Tool\n    baseURL: ''\n    tags:\n      - Authoring\n      - cffinit\n      - Web App\n    serviceName: cffinit Authoring Tool\n    serviceCategory: API\n  - name: cffconvert\n    baseURL: ''\n    tags:\n      - BibTeX\n      - cffconvert\n      - CodeMeta\n      - Conversion\n      - RIS\n    serviceName: cffconvert\n    serviceCategory: API\n  - name: cff-validator\
  \ GitHub Action\n    baseURL: ''\n    tags:\n      - CI\n      - GitHub Action\n      - Validation\n    serviceName: cff-validator GitHub Action\n    serviceCategory: API\n  - name: GitHub Native Citation Support\n    baseURL: ''\n    tags:\n      - Discovery\n      - GitHub\n      - Integration\n    serviceName: GitHub Native Citation Support\n    serviceCategory: API\n  - name: Zenodo Software Publishing\n    baseURL: ''\n    tags:\n      - DOI\n      - Publishing\n      - Repository\n      - Zenodo\n    serviceName: Zenodo Software Publishing\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/citation-cff/refs/heads/main/finops/citation-cff-finops.yml
sources: []
specification: FinOps Framework
tags:
- Academic
- Citation
- Metadata
- Open Standard
- Repository
- Research
- Software
- YAML
- FinOps
- Cost Management
- FOCUS
---
