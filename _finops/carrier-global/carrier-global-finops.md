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
description: FinOps framework definition for the Carrier Global API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Carrier Global
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Carrier Global
  PublisherName: Carrier Global
  ServiceCategory: Developer Tools / API
  ServiceName: Carrier Global
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
name: Carrier Global Finops
provider_name: Carrier Global
provider_slug: carrier-global
publisher_name: Carrier Global
service_category: API
slug: carrier-global-finops
source_filename: carrier-global-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Carrier Global\nproviderId: carrier-global\npublisherName: Carrier Global\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - HVAC\n  - Cold Chain\n  - Telematics\n  - Building Automation\n  - IoT\n  - Refrigeration\n  - Fortune 500\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Carrier Global API surface. Provides a FOCUS-aligned\n  mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n\
  \    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage\
  \ the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Carrier Global\n  ServiceCategory: Developer Tools / API\n  ProviderName: Carrier Global\n  PublisherName: Carrier Global\n  InvoiceIssuerName: Carrier Global\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes\
  \ returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Carrier Lynx Fleet API\n    baseURL: https://doc-api.fleet.lynx.carrier.io/\n    tags:\n      - Cold Chain\n      - Telematics\n      - Fleet\n      - Refrigeration\n      - IoT\n    serviceName: Carrier Lynx Fleet API\n    serviceCategory: API\n  - name: Carrier i-Vu Building Automation\n    baseURL: ''\n    tags:\n      - Building Automation\n      - BACnet\n      - HVAC\n    serviceName: Carrier i-Vu Building Automation\n    serviceCategory: API\n  - name: Carrier Comfort Network\n    baseURL: ''\n    tags:\n      - Building Automation\n      - HVAC\n      - Chillers\n    serviceName: Carrier Comfort Network\n    serviceCategory:\
  \ API\n  - name: Carrier Abound\n    baseURL: ''\n    tags:\n      - Building Intelligence\n      - IAQ\n      - Analytics\n    serviceName: Carrier Abound\n    serviceCategory: API\n  - name: Carrier SmartHome App\n    baseURL: ''\n    tags:\n      - Smart Home\n      - Thermostats\n      - Residential\n    serviceName: Carrier SmartHome App\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: info@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/carrier-global/refs/heads/main/finops/carrier-global-finops.yml
sources: []
specification: FinOps Framework
tags:
- HVAC
- Cold Chain
- Telematics
- Building Automation
- IoT
- Refrigeration
- Fortune 500
- FinOps
- Cost Management
- FOCUS
---
