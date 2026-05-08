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
description: FinOps framework definition for the Maya API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Maya
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Maya
  PublisherName: Maya
  ServiceCategory: Developer Tools / API
  ServiceName: Maya
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
name: Maya Finops
provider_name: Maya
provider_slug: maya
publisher_name: Maya
service_category: API
slug: maya-finops
source_filename: maya-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Maya\nproviderId: maya\npublisherName: Maya\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - 3D\n  - Animation\n  - Autodesk\n  - CGI\n  - Modeling\n  - Rendering\n  - Scripting\n  - VFX\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Maya API surface. Provides a FOCUS-aligned mapping for\n  cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the\
  \ consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps\
  \ Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Maya\n  ServiceCategory: Developer Tools / API\n  ProviderName: Maya\n  PublisherName: Maya\n  InvoiceIssuerName: Maya\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n\
  \      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Maya Python API 2.0\n    baseURL: ''\n    tags:\n      - Automation\n      - OpenMaya\n      - Plugins\n      - Python\n      - Scripting\n    serviceName: Maya Python API 2.0\n    serviceCategory: API\n  - name: Maya Python API 1.0\n    baseURL: ''\n    tags:\n      - OpenMaya\n      - Plugins\n      - Python\n      - Scripting\n    serviceName: Maya Python API 1.0\n    serviceCategory: API\n  - name: Maya C++ API\n    baseURL: ''\n    tags:\n      - C++\n      - OpenMaya\n      - Performance\n      - Plugins\n      - SDK\n    serviceName: Maya C++ API\n    serviceCategory: API\n  - name: Maya Commands (MEL)\n    baseURL: ''\n    tags:\n      - Automation\n      - Commands\n      - MEL\n      - Scripting\n    serviceName:\
  \ Maya Commands (MEL)\n    serviceCategory: API\n  - name: Maya Commands (Python)\n    baseURL: ''\n    tags:\n      - Automation\n      - Commands\n      - Python\n      - Scripting\n    serviceName: Maya Commands (Python)\n    serviceCategory: API\n  - name: Maya USD API\n    baseURL: ''\n    tags:\n      - Interchange\n      - OpenUSD\n      - Pipeline\n      - Pixar\n      - USD\n    serviceName: Maya USD API\n    serviceCategory: API\n  - name: Maya Batch Rendering API\n    baseURL: ''\n    tags:\n      - Batch\n      - Pipeline\n      - Rendering\n    serviceName: Maya Batch Rendering API\n    serviceCategory: API\n  - name: Maya Hydra API\n    baseURL: ''\n    tags:\n      - Hydra\n      - OpenSource\n      - Rendering\n      - Viewport\n    serviceName: Maya Hydra API\n    serviceCategory: API\n  - name: Autodesk Platform Services - Maya API\n    baseURL: ''\n    tags:\n      - APS\n      - Cloud\n      - OAuth\n      - Platform\n      - REST\n    serviceName: Autodesk Platform\
  \ Services - Maya API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n    X-twitter: apievangelist\n    X-github: kinlane\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/maya/refs/heads/main/finops/maya-finops.yml
sources: []
specification: FinOps Framework
tags:
- 3D
- Animation
- Autodesk
- CGI
- Modeling
- Rendering
- Scripting
- VFX
- FinOps
- Cost Management
- FOCUS
---
