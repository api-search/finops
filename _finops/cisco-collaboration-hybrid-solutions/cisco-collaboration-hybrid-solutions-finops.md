---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: openapi.json
  format: json
  label: Webex APIs
  slug: webex-api
  spec_type: OpenAPI
  url: https://developer.webex.com/docs/api/v1/openapi.json
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
description: FinOps framework definition for the Cisco Collaboration Hybrid Solutions API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Cisco Collaboration Hybrid Solutions
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Cisco Collaboration Hybrid Solutions
  PublisherName: Cisco Collaboration Hybrid Solutions
  ServiceCategory: Developer Tools / API
  ServiceName: Cisco Collaboration Hybrid Solutions
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
name: Cisco Collaboration Hybrid Solutions Finops
provider_name: Cisco Collaboration Hybrid Solutions
provider_slug: cisco-collaboration-hybrid-solutions
publisher_name: Cisco Collaboration Hybrid Solutions
service_category: API
slug: cisco-collaboration-hybrid-solutions-finops
source_filename: cisco-collaboration-hybrid-solutions-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Cisco Collaboration Hybrid Solutions\nproviderId: cisco-collaboration-hybrid-solutions\npublisherName: Cisco Collaboration Hybrid Solutions\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Calling\n  - Collaboration\n  - Hybrid Cloud\n  - Meetings\n  - Messaging\n  - Unified Communications\n  - Webex\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Cisco Collaboration Hybrid Solutions API surface. Provides\n  a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across\n  the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible\
  \ to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload\
  \ Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Cisco Collaboration Hybrid Solutions\n  ServiceCategory: Developer Tools / API\n  ProviderName: Cisco Collaboration Hybrid Solutions\n  PublisherName: Cisco Collaboration Hybrid Solutions\n  InvoiceIssuerName: Cisco Collaboration Hybrid Solutions\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit:\
  \ request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Webex APIs\n    baseURL: https://webexapis.com/v1\n    tags:\n      - Collaboration\n      - Meetings\n      - Messaging\n      - Spaces\n      - Teams\n    serviceName: Webex APIs\n    serviceCategory: API\n  - name: Webex Meetings API\n    baseURL: https://webexapis.com/v1/meetings\n    tags:\n      - Meetings\n      - Recordings\n      - Scheduling\n    serviceName: Webex Meetings API\n    serviceCategory: API\n  - name: Webex Hybrid Services API\n\
  \    baseURL: https://webexapis.com/v1\n    tags:\n      - Calendar\n      - Connectors\n      - Hybrid\n      - Media\n    serviceName: Webex Hybrid Services API\n    serviceCategory: API\n  - name: Webex Calling API\n    baseURL: https://webexapis.com/v1\n    tags:\n      - Call Control\n      - Calling\n      - Telephony\n      - Voicemail\n    serviceName: Webex Calling API\n    serviceCategory: API\n  - name: Control Hub API\n    baseURL: https://webexapis.com/v1\n    tags:\n      - Administration\n      - Management\n      - Organizations\n      - Users\n    serviceName: Control Hub API\n    serviceCategory: API\n  - name: Webex Devices API\n    baseURL: https://webexapis.com/v1\n    tags:\n      - Devices\n      - Endpoints\n      - Room Systems\n    serviceName: Webex Devices API\n    serviceCategory: API\n  - name: Webex Events API\n    baseURL: https://webexapis.com/v1\n    tags:\n      - Events\n      - Virtual Events\n      - Webinars\n    serviceName: Webex Events API\n  \
  \  serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/cisco-collaboration-hybrid-solutions/refs/heads/main/finops/cisco-collaboration-hybrid-solutions-finops.yml
sources: []
specification: FinOps Framework
tags:
- Calling
- Collaboration
- Hybrid Cloud
- Meetings
- Messaging
- Unified Communications
- Webex
- FinOps
- Cost Management
- FOCUS
---
