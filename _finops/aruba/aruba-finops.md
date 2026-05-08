---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: aruba-central-api.yml
  format: yaml
  label: Aruba Central API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/aruba/refs/heads/main/openapi/aruba-central-api.yml
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
description: FinOps framework definition for the Aruba API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Aruba
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Aruba
  PublisherName: Aruba
  ServiceCategory: Developer Tools / API
  ServiceName: Aruba
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
name: Aruba Finops
provider_name: Aruba
provider_slug: aruba
publisher_name: Aruba
service_category: API
slug: aruba-finops
source_filename: aruba-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Aruba\nproviderId: aruba\npublisherName: Aruba\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Cloud\n  - Infrastructure\n  - Network Management\n  - Networking\n  - SD-WAN\n  - Security\n  - Switches\n  - Wireless\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Aruba API surface. Provides a FOCUS-aligned mapping for\n  cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every\
  \ chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n   \
  \ capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Aruba\n  ServiceCategory: Developer Tools / API\n  ProviderName: Aruba\n  PublisherName: Aruba\n  InvoiceIssuerName: Aruba\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n  \
  \  aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Aruba Central API\n    baseURL: https://apigw-prod2.central.arubanetworks.com\n    tags:\n      - Analytics\n      - Cloud Management\n      - Monitoring\n      - Network Automation\n    serviceName: Aruba Central API\n    serviceCategory: API\n  - name: Aruba ClearPass API\n    baseURL: https://clearpass.example.com/api\n    tags:\n      - Authentication\n      - Authorization\n      - Network Access Control\n      - Policy Management\n    serviceName: Aruba ClearPass API\n    serviceCategory: API\n  - name: Aruba AOS-CX REST API\n    baseURL: ''\n    tags:\n      - Infrastructure\n      - Network Automation\n      - Programmability\n      - Switches\n    serviceName: Aruba AOS-CX\
  \ REST API\n    serviceCategory: API\n  - name: Aruba EdgeConnect SD-WAN API\n    baseURL: ''\n    tags:\n      - Edge Networking\n      - Orchestrator\n      - SD-WAN\n      - WAN Optimization\n    serviceName: Aruba EdgeConnect SD-WAN API\n    serviceCategory: API\n  - name: Aruba Fabric Composer API\n    baseURL: ''\n    tags:\n      - Data Center\n      - Fabric\n      - Leaf-Spine\n      - Orchestration\n    serviceName: Aruba Fabric Composer API\n    serviceCategory: API\n  - name: Aruba User Experience Insight API\n    baseURL: ''\n    tags:\n      - Monitoring\n      - Network Testing\n      - Sensors\n      - User Experience\n    serviceName: Aruba User Experience Insight API\n    serviceCategory: API\n  - name: Aruba AirWave API\n    baseURL: https://airwave.example.com/api\n    tags:\n      - Monitoring\n      - Network Management\n      - Reporting\n    serviceName: Aruba AirWave API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost\
  \ / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n    url: https://apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/aruba/refs/heads/main/finops/aruba-finops.yml
sources: []
specification: FinOps Framework
tags:
- Cloud
- Infrastructure
- Network Management
- Networking
- SD-WAN
- Security
- Switches
- Wireless
- FinOps
- Cost Management
- FOCUS
---
