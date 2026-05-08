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
description: FinOps framework definition for the Rockwell Automation API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Rockwell Automation
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Rockwell Automation
  PublisherName: Rockwell Automation
  ServiceCategory: Developer Tools / API
  ServiceName: Rockwell Automation
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
name: Rockwell Automation Finops
provider_name: Rockwell Automation
provider_slug: rockwell-automation
publisher_name: Rockwell Automation
service_category: API
slug: rockwell-automation-finops
source_filename: rockwell-automation-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Rockwell Automation\nproviderId: rockwell-automation\npublisherName: Rockwell Automation\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Industrial Automation\n  - Manufacturing\n  - PLC\n  - SCADA\n  - IIoT\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Rockwell Automation API surface. Provides a FOCUS-aligned\n  mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description:\
  \ Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n\
  \    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Rockwell Automation\n  ServiceCategory: Developer Tools / API\n  ProviderName: Rockwell Automation\n  PublisherName: Rockwell Automation\n  InvoiceIssuerName: Rockwell Automation\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned\
  \ over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Rockwell Automation Plex ERP API\n    baseURL: https://api.plex.com\n    tags:\n      - ERP\n      - Manufacturing\n      - Smart Manufacturing\n      - REST\n      - Industrial Automation\n    serviceName: Rockwell Automation Plex ERP API\n    serviceCategory: API\n  - name: Rockwell Automation FactoryTalk DataMosaix API\n    baseURL: https://datamosaix-portal.cloud.rockwellautomation.com\n    tags:\n      - Industrial Data\n      - DataOps\n      - Manufacturing\n      - REST\n      - Industrial Automation\n    serviceName: Rockwell Automation FactoryTalk DataMosaix API\n    serviceCategory: API\n  - name: Rockwell Automation FactoryTalk\
  \ Remote Access Web API\n    baseURL: https://api.rockwellautomation.com\n    tags:\n      - Remote Access\n      - Industrial Automation\n      - REST\n      - Manufacturing\n    serviceName: Rockwell Automation FactoryTalk Remote Access Web API\n    serviceCategory: API\n  - name: Rockwell Automation Logix Designer SDK\n    baseURL: https://github.com/RockwellAutomation\n    tags:\n      - PLC\n      - Programming\n      - SDK\n      - Industrial Automation\n      - Manufacturing\n    serviceName: Rockwell Automation Logix Designer SDK\n    serviceCategory: API\n  - name: Rockwell Automation Emulate3D API\n    baseURL: https://github.com/RockwellAutomation\n    tags:\n      - Digital Twin\n      - Simulation\n      - Industrial Automation\n      - Manufacturing\n    serviceName: Rockwell Automation Emulate3D API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n\
  \    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/rockwell-automation/refs/heads/main/finops/rockwell-automation-finops.yml
sources: []
specification: FinOps Framework
tags:
- Industrial Automation
- Manufacturing
- PLC
- SCADA
- IIoT
- FinOps
- Cost Management
- FOCUS
---
