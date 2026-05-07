---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: radius-applications-core-openapi.json
  format: json
  label: Radius Applications.Core API
  slug: applications-core
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/radius/refs/heads/main/openapi/radius-applications-core-openapi.json
- filename: radius-applications-dapr-openapi.json
  format: json
  label: Radius Applications.Dapr API
  slug: applications-dapr
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/radius/refs/heads/main/openapi/radius-applications-dapr-openapi.json
- filename: radius-applications-datastores-openapi.json
  format: json
  label: Radius Applications.Datastores API
  slug: applications-datastores
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/radius/refs/heads/main/openapi/radius-applications-datastores-openapi.json
- filename: radius-applications-messaging-openapi.json
  format: json
  label: Radius Applications.Messaging API
  slug: applications-messaging
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/radius/refs/heads/main/openapi/radius-applications-messaging-openapi.json
- filename: radius-ucp-openapi.json
  format: json
  label: Radius Universal Control Plane (UCP) API
  slug: ucp
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/radius/refs/heads/main/openapi/radius-ucp-openapi.json
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
description: FinOps framework definition for the Radius API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Radius
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Radius
  PublisherName: Radius
  ServiceCategory: Developer Tools / API
  ServiceName: Radius
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
name: Radius Finops
provider_name: Radius
provider_slug: radius
publisher_name: Radius
service_category: API
slug: radius-finops
source_filename: radius-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Radius\nproviderId: radius\npublisherName: Radius\nserviceCategory: API\ncreated: '2026-05-04'\nmodified: '2026-05-04'\ntags:\n  - Application Platform\n  - Cloud Native\n  - Infrastructure\n  - Multi Cloud\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Radius API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming\
  \ team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice\
  \ Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Radius\n  ServiceCategory: Developer Tools / API\n  ProviderName: Radius\n  PublisherName: Radius\n  InvoiceIssuerName: Radius\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n\
  \      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Radius Applications.Core API\n    baseURL: https://management.azure.com\n    tags:\n      - Applications\n      - Containers\n      - Environments\n      - Gateways\n      - Secret Stores\n      - Volumes\n    serviceName: Radius Applications.Core API\n    serviceCategory: API\n  - name: Radius Applications.Dapr API\n    baseURL: https://management.azure.com\n    tags:\n      - Dapr\n      - Building Blocks\n    serviceName: Radius Applications.Dapr API\n    serviceCategory: API\n  - name: Radius Applications.Datastores API\n    baseURL: https://management.azure.com\n    tags:\n      - Datastores\n      - Databases\n      - Redis\n      - MongoDB\n      - SQL\n    serviceName: Radius Applications.Datastores API\n   \
  \ serviceCategory: API\n  - name: Radius Applications.Messaging API\n    baseURL: https://management.azure.com\n    tags:\n      - Messaging\n      - Queues\n    serviceName: Radius Applications.Messaging API\n    serviceCategory: API\n  - name: Radius Universal Control Plane (UCP) API\n    baseURL: https://management.azure.com\n    tags:\n      - Control Plane\n      - UCP\n      - Multi Cloud\n    serviceName: Radius Universal Control Plane (UCP) API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/radius/refs/heads/main/finops/radius-finops.yml
sources: []
specification: FinOps Framework
tags:
- Application Platform
- Cloud Native
- Infrastructure
- Multi Cloud
- FinOps
- Cost Management
- FOCUS
---
