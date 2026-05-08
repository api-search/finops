---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: miro-openapi.json
  format: json
  label: Miro Boards API
  slug: miro-boards-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/miro/refs/heads/main/openapi/miro-openapi.json
- filename: miro-openapi.json
  format: json
  label: Miro Board Items API
  slug: miro-board-items-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/miro/refs/heads/main/openapi/miro-openapi.json
- filename: miro-openapi.json
  format: json
  label: Miro Connectors API
  slug: miro-connectors-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/miro/refs/heads/main/openapi/miro-openapi.json
- filename: miro-openapi.json
  format: json
  label: Miro Tags API
  slug: miro-tags-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/miro/refs/heads/main/openapi/miro-openapi.json
- filename: miro-openapi.json
  format: json
  label: Miro Mind Map API
  slug: miro-mind-map-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/miro/refs/heads/main/openapi/miro-openapi.json
- filename: miro-openapi.json
  format: json
  label: Miro Board Members API
  slug: miro-board-members-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/miro/refs/heads/main/openapi/miro-openapi.json
- filename: miro-openapi.json
  format: json
  label: Miro Webhooks API
  slug: miro-webhooks-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/miro/refs/heads/main/openapi/miro-openapi.json
- filename: miro-openapi.json
  format: json
  label: Miro Organization API
  slug: miro-organization-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/miro/refs/heads/main/openapi/miro-openapi.json
- filename: miro-openapi.json
  format: json
  label: Miro Teams API
  slug: miro-teams-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/miro/refs/heads/main/openapi/miro-openapi.json
- filename: miro-openapi.json
  format: json
  label: Miro Audit Logs API
  slug: miro-audit-logs-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/miro/refs/heads/main/openapi/miro-openapi.json
- filename: miro-openapi.json
  format: json
  label: Miro SCIM API
  slug: miro-scim-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/miro/refs/heads/main/openapi/miro-openapi.json
- filename: miro-openapi.json
  format: json
  label: Miro Web SDK
  slug: miro-web-sdk
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/miro/refs/heads/main/openapi/miro-openapi.json
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
description: FinOps framework definition for the Miro API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Miro
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Miro
  PublisherName: Miro
  ServiceCategory: Developer Tools / API
  ServiceName: Miro
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
name: Miro Finops
provider_name: Miro
provider_slug: miro
publisher_name: Miro
service_category: API
slug: miro-finops
source_filename: miro-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Miro\nproviderId: miro\npublisherName: Miro\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Productivity\n  - Whiteboard\n  - Visual Collaboration\n  - Diagramming\n  - SaaS\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Miro API surface. Provides a FOCUS-aligned mapping for\n  cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming\
  \ team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice\
  \ Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Miro\n  ServiceCategory: Developer Tools / API\n  ProviderName: Miro\n  PublisherName: Miro\n  InvoiceIssuerName: Miro\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      -\
  \ api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Miro Boards API\n    baseURL: https://api.miro.com/v2\n    tags:\n      - Boards\n      - CRUD\n    serviceName: Miro Boards API\n    serviceCategory: API\n  - name: Miro Board Items API\n    baseURL: https://api.miro.com/v2\n    tags:\n      - Items\n      - Sticky Notes\n      - Shapes\n    serviceName: Miro Board Items API\n    serviceCategory: API\n  - name: Miro Connectors API\n    baseURL: https://api.miro.com/v2\n    tags:\n      - Connectors\n      - Diagramming\n    serviceName: Miro Connectors API\n    serviceCategory: API\n  - name: Miro Tags API\n    baseURL: https://api.miro.com/v2\n    tags:\n      - Tags\n      - Metadata\n    serviceName: Miro Tags API\n    serviceCategory: API\n  - name: Miro Mind Map API\n\
  \    baseURL: https://api.miro.com/v2\n    tags:\n      - Mind Map\n      - Diagramming\n    serviceName: Miro Mind Map API\n    serviceCategory: API\n  - name: Miro Board Members API\n    baseURL: https://api.miro.com/v2\n    tags:\n      - Members\n      - Sharing\n      - Permissions\n    serviceName: Miro Board Members API\n    serviceCategory: API\n  - name: Miro Webhooks API\n    baseURL: https://api.miro.com/v2\n    tags:\n      - Webhooks\n      - Events\n    serviceName: Miro Webhooks API\n    serviceCategory: API\n  - name: Miro Organization API\n    baseURL: https://api.miro.com/v2\n    tags:\n      - Organization\n      - Enterprise\n    serviceName: Miro Organization API\n    serviceCategory: API\n  - name: Miro Teams API\n    baseURL: https://api.miro.com/v2\n    tags:\n      - Teams\n      - Membership\n    serviceName: Miro Teams API\n    serviceCategory: API\n  - name: Miro Audit Logs API\n    baseURL: https://api.miro.com/v2\n    tags:\n      - Audit\n      - Compliance\n\
  \      - Enterprise\n    serviceName: Miro Audit Logs API\n    serviceCategory: API\n  - name: Miro SCIM API\n    baseURL: https://miro.com/api/v1/scim\n    tags:\n      - SCIM\n      - Identity\n      - Provisioning\n    serviceName: Miro SCIM API\n    serviceCategory: API\n  - name: Miro Web SDK\n    baseURL: https://miro.com\n    tags:\n      - SDK\n      - Browser\n      - Apps\n    serviceName: Miro Web SDK\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/miro/refs/heads/main/finops/miro-finops.yml
sources: []
specification: FinOps Framework
tags:
- Productivity
- Whiteboard
- Visual Collaboration
- Diagramming
- SaaS
- FinOps
- Cost Management
- FOCUS
---
