---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: verizon-thingspace-connectivity-openapi.yml
  format: yaml
  label: Verizon ThingSpace
  slug: thingspace
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/verizon/refs/heads/main/openapi/verizon-thingspace-connectivity-openapi.yml
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
description: FinOps framework definition for the Verizon API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Verizon
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Verizon
  PublisherName: Verizon
  ServiceCategory: Developer Tools / API
  ServiceName: Verizon
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
name: Verizon Finops
provider_name: Verizon
provider_slug: verizon
publisher_name: Verizon
service_category: API
slug: verizon-finops
source_filename: verizon-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Verizon\nproviderId: verizon\npublisherName: Verizon\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Wireless\n  - Telecommunications\n  - IoT\n  - 5G\n  - Enterprise\n  - Network APIs\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Verizon API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with\
  \ the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps\
  \ Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Verizon\n  ServiceCategory: Developer Tools / API\n  ProviderName: Verizon\n  PublisherName: Verizon\n  InvoiceIssuerName: Verizon\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n  \
  \  dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Verizon 5G Edge\n    baseURL: ''\n    tags:\n      - Wireless\n    serviceName: Verizon 5G Edge\n    serviceCategory: API\n  - name: Verizon ThingSpace\n    baseURL: ''\n    tags:\n      - IoT\n      - Device Management\n      - Connectivity\n      - Wireless\n    serviceName: Verizon ThingSpace\n    serviceCategory: API\n  - name: Verizon Communications Platform as a Service (CPaaS)\n    baseURL: ''\n    tags: []\n    serviceName: Verizon Communications Platform as a Service (CPaaS)\n    serviceCategory: API\n  - name: Verizon Inventory Management\n    baseURL: ''\n    tags: []\n    serviceName: Verizon Inventory Management\n    serviceCategory: API\n  - name: Verizon Incident Management\n    baseURL:\
  \ ''\n    tags: []\n    serviceName: Verizon Incident Management\n    serviceCategory: API\n  - name: Verizon Change Management\n    baseURL: ''\n    tags: []\n    serviceName: Verizon Change Management\n    serviceCategory: API\n  - name: Verizon Event Management\n    baseURL: ''\n    tags: []\n    serviceName: Verizon Event Management\n    serviceCategory: API\n  - name: Verizon Problem Management\n    baseURL: ''\n    tags: []\n    serviceName: Verizon Problem Management\n    serviceCategory: API\n  - name: Verizon Order Management\n    baseURL: ''\n    tags: []\n    serviceName: Verizon Order Management\n    serviceCategory: API\n  - name: Verizon Billing Management\n    baseURL: ''\n    tags: []\n    serviceName: Verizon Billing Management\n    serviceCategory: API\n  - name: Verizon Dynamic Bandwidth APIs\n    baseURL: ''\n    tags: []\n    serviceName: Verizon Dynamic Bandwidth APIs\n    serviceCategory: API\n  - name: Dynamic Network Manager (DNM) Standardized APIs\n    baseURL:\
  \ ''\n    tags: []\n    serviceName: Dynamic Network Manager (DNM) Standardized APIs\n    serviceCategory: API\n  - name: Secure Cloud Interconnect APIs Utilization\n    baseURL: ''\n    tags: []\n    serviceName: Secure Cloud Interconnect APIs Utilization\n    serviceCategory: API\n  - name: Secure Cloud Interconnect APIs Billing Usage\n    baseURL: ''\n    tags: []\n    serviceName: Secure Cloud Interconnect APIs Billing Usage\n    serviceCategory: API\n  - name: Dynamic Network Manager (DNM) Standardized APIs\n    baseURL: ''\n    tags: []\n    serviceName: Dynamic Network Manager (DNM) Standardized APIs\n    serviceCategory: API\n  - name: Dynamic Network Manager (DNM) Standardized APIs\n    baseURL: ''\n    tags: []\n    serviceName: Dynamic Network Manager (DNM) Standardized APIs\n    serviceCategory: API\n  - name: Dynamic Network Manager (DNM) Standardized APIs\n    baseURL: ''\n    tags: []\n    serviceName: Dynamic Network Manager (DNM) Standardized APIs\n    serviceCategory:\
  \ API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/verizon/refs/heads/main/finops/verizon-finops.yml
sources: []
specification: FinOps Framework
tags:
- Wireless
- Telecommunications
- IoT
- 5G
- Enterprise
- Network APIs
- FinOps
- Cost Management
- FOCUS
---
