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
  label: Webex Admin API
  slug: webex-admin-api
  spec_type: OpenAPI
  url: https://developer.webex.com/docs/api/v1/openapi.json
- filename: openapi.json
  format: json
  label: Webex Calling API
  slug: webex-calling-api
  spec_type: OpenAPI
  url: https://developer.webex.com/docs/api/v1/openapi.json
- filename: openapi.json
  format: json
  label: Webex Devices API
  slug: webex-devices-api
  spec_type: OpenAPI
  url: https://developer.webex.com/docs/api/v1/openapi.json
- filename: openapi.json
  format: json
  label: Webex Workspaces API
  slug: webex-workspaces-api
  spec_type: OpenAPI
  url: https://developer.webex.com/docs/api/v1/openapi.json
- filename: openapi.json
  format: json
  label: Webex People API
  slug: webex-people-api
  spec_type: OpenAPI
  url: https://developer.webex.com/docs/api/v1/openapi.json
- filename: openapi.json
  format: json
  label: Webex Organizations API
  slug: webex-organizations-api
  spec_type: OpenAPI
  url: https://developer.webex.com/docs/api/v1/openapi.json
- filename: openapi.json
  format: json
  label: Webex Licenses API
  slug: webex-licenses-api
  spec_type: OpenAPI
  url: https://developer.webex.com/docs/api/v1/openapi.json
- filename: openapi.json
  format: json
  label: Webex Locations API
  slug: webex-locations-api
  spec_type: OpenAPI
  url: https://developer.webex.com/docs/api/v1/openapi.json
- filename: openapi.json
  format: json
  label: Webex Reports API
  slug: webex-reports-api
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
description: FinOps framework definition for the Cisco Control Hub API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Cisco Control Hub
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Cisco Control Hub
  PublisherName: Cisco Control Hub
  ServiceCategory: Developer Tools / API
  ServiceName: Cisco Control Hub
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
name: Cisco Control Hub Finops
provider_name: Cisco Control Hub
provider_slug: cisco-control-hub
publisher_name: Cisco Control Hub
service_category: API
slug: cisco-control-hub-finops
source_filename: cisco-control-hub-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Cisco Control Hub\nproviderId: cisco-control-hub\npublisherName: Cisco Control Hub\nserviceCategory: API\ncreated: '2026-05-04'\nmodified: '2026-05-04'\ntags:\n  - Administration\n  - Calling\n  - Collaboration\n  - Communications\n  - Device Management\n  - Identity Management\n  - Licenses\n  - Reporting\n  - Webex\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Cisco Control Hub API surface. Provides a FOCUS-aligned\n  mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance\
  \ teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n\
  \      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Cisco Control Hub\n  ServiceCategory: Developer Tools / API\n  ProviderName: Cisco Control Hub\n  PublisherName: Cisco Control Hub\n  InvoiceIssuerName: Cisco Control Hub\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      -\
  \ consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Webex Admin API\n    baseURL: https://webexapis.com/v1\n    tags:\n      - Administration\n      - Audit\n      - Organizations\n      - Users\n    serviceName: Webex Admin API\n    serviceCategory: API\n  - name: Webex Calling API\n    baseURL: https://webexapis.com/v1\n    tags:\n      - Calling\n      - Phone Numbers\n      - Telephony\n      - Voice\n    serviceName: Webex Calling API\n    serviceCategory: API\n  - name: Webex Devices API\n    baseURL: https://webexapis.com/v1\n    tags:\n      - Configuration\n      - Devices\n      - Endpoints\n      - Room Systems\n\
  \    serviceName: Webex Devices API\n    serviceCategory: API\n  - name: Webex Workspaces API\n    baseURL: https://webexapis.com/v1\n    tags:\n      - Locations\n      - Meeting Rooms\n      - Workspaces\n    serviceName: Webex Workspaces API\n    serviceCategory: API\n  - name: Webex People API\n    baseURL: https://webexapis.com/v1\n    tags:\n      - Directory\n      - People\n      - Profiles\n      - Users\n    serviceName: Webex People API\n    serviceCategory: API\n  - name: Webex Organizations API\n    baseURL: https://webexapis.com/v1\n    tags:\n      - Configuration\n      - Organizations\n      - Settings\n    serviceName: Webex Organizations API\n    serviceCategory: API\n  - name: Webex Licenses API\n    baseURL: https://webexapis.com/v1\n    tags:\n      - Entitlements\n      - Licenses\n      - Subscriptions\n    serviceName: Webex Licenses API\n    serviceCategory: API\n  - name: Webex Locations API\n    baseURL: https://webexapis.com/v1\n    tags:\n      - Calling\n\
  \      - Geography\n      - Locations\n    serviceName: Webex Locations API\n    serviceCategory: API\n  - name: Webex Reports API\n    baseURL: https://webexapis.com/v1\n    tags:\n      - Analytics\n      - Metrics\n      - Reports\n      - Usage\n    serviceName: Webex Reports API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/cisco-control-hub/refs/heads/main/finops/cisco-control-hub-finops.yml
sources: []
specification: FinOps Framework
tags:
- Administration
- Calling
- Collaboration
- Communications
- Device Management
- Identity Management
- Licenses
- Reporting
- Webex
- FinOps
- Cost Management
- FOCUS
---
