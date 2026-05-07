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
description: FinOps framework definition for the Brocade API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Brocade
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Brocade
  PublisherName: Brocade
  ServiceCategory: Developer Tools / API
  ServiceName: Brocade
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
name: Brocade Finops
provider_name: Brocade
provider_slug: brocade
publisher_name: Brocade
service_category: API
slug: brocade-finops
source_filename: brocade-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Brocade\nproviderId: brocade\npublisherName: Brocade\nserviceCategory: API\ncreated: '2026-05-04'\nmodified: '2026-05-04'\ntags:\n  - Data Center\n  - Directors\n  - Fibre Channel\n  - Network Automation\n  - Networking\n  - SAN\n  - Storage Area Networks\n  - Switches\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Brocade API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n\
  \    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage\
  \ the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Brocade\n  ServiceCategory: Developer Tools / API\n  ProviderName: Brocade\n  PublisherName: Brocade\n  InvoiceIssuerName: Brocade\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in\
  \ API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Brocade Fabric OS REST API\n    baseURL: https://{switch-ip}/rest\n    tags:\n      - Fabric OS\n      - Fibre Channel\n      - Network Management\n      - SAN\n      - Switches\n    serviceName: Brocade Fabric OS REST API\n    serviceCategory: API\n  - name: Brocade SANnav Management Portal REST API\n    baseURL: https://{sannav-host}/external-api/v1\n    tags:\n      - Discovery\n      - Fibre Channel\n      - Monitoring\n      - SAN Management\n      - Zoning\n    serviceName: Brocade SANnav Management Portal REST API\n    serviceCategory: API\n  - name: Brocade SANnav Northbound Streaming API\n    baseURL: https://{sannav-host}/external-api/v1/stream\n\
  \    tags:\n      - Events\n      - Monitoring\n      - SAN Management\n      - Streaming\n      - Telemetry\n    serviceName: Brocade SANnav Northbound Streaming API\n    serviceCategory: API\n  - name: Brocade Network Advisor REST API\n    baseURL: https://{bna-host}/rest\n    tags:\n      - Analytics\n      - Deprecated\n      - Monitoring\n      - SAN Management\n    serviceName: Brocade Network Advisor REST API\n    serviceCategory: API\n  - name: Brocade Workflow Composer API\n    baseURL: https://{bwc-host}/api/v1\n    tags:\n      - Automation\n      - Deprecated\n      - Orchestration\n      - Workflow\n    serviceName: Brocade Workflow Composer API\n    serviceCategory: API\n  - name: Brocade VCS Fabric API\n    baseURL: https://{switch-ip}/rest\n    tags:\n      - Deprecated\n      - Fabric\n      - Switching\n      - VCS\n    serviceName: Brocade VCS Fabric API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests\
  \ / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n    url: https://apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/brocade/refs/heads/main/finops/brocade-finops.yml
sources: []
specification: FinOps Framework
tags:
- Data Center
- Directors
- Fibre Channel
- Network Automation
- Networking
- SAN
- Storage Area Networks
- Switches
- FinOps
- Cost Management
- FOCUS
---
