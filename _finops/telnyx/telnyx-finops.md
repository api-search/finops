---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: telnyx-openapi.yml
  format: yaml
  label: Telnyx Voice API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/telnyx/refs/heads/main/openapi/telnyx-openapi.yml
- filename: telnyx-openapi.yml
  format: yaml
  label: Telnyx Messaging API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/telnyx/refs/heads/main/openapi/telnyx-openapi.yml
- filename: telnyx-openapi.yml
  format: yaml
  label: Telnyx Numbers API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/telnyx/refs/heads/main/openapi/telnyx-openapi.yml
- filename: telnyx-openapi.yml
  format: yaml
  label: Telnyx Verify API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/telnyx/refs/heads/main/openapi/telnyx-openapi.yml
- filename: telnyx-openapi.yml
  format: yaml
  label: Telnyx Fax API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/telnyx/refs/heads/main/openapi/telnyx-openapi.yml
- filename: telnyx-openapi.yml
  format: yaml
  label: Telnyx Wireless API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/telnyx/refs/heads/main/openapi/telnyx-openapi.yml
- filename: telnyx-openapi.yml
  format: yaml
  label: Telnyx Networking API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/telnyx/refs/heads/main/openapi/telnyx-openapi.yml
- filename: telnyx-openapi.yml
  format: yaml
  label: Telnyx AI API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/telnyx/refs/heads/main/openapi/telnyx-openapi.yml
- filename: telnyx-openapi.yml
  format: yaml
  label: Telnyx Billing & Reporting API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/telnyx/refs/heads/main/openapi/telnyx-openapi.yml
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
description: FinOps framework definition for the Telnyx API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Telnyx
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Telnyx
  PublisherName: Telnyx
  ServiceCategory: Developer Tools / API
  ServiceName: Telnyx
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
name: Telnyx Finops
provider_name: Telnyx
provider_slug: telnyx
publisher_name: Telnyx
service_category: API
slug: telnyx-finops
source_filename: telnyx-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Telnyx\nproviderId: telnyx\npublisherName: Telnyx\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Communications\n  - CPaaS\n  - Voice\n  - SMS\n  - IoT\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Telnyx API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment,\
  \ application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      -\
  \ FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Telnyx\n  ServiceCategory: Developer Tools / API\n  ProviderName: Telnyx\n  PublisherName: Telnyx\n  InvoiceIssuerName: Telnyx\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n     \
  \ - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Telnyx Voice API\n    baseURL: https://api.telnyx.com/v2\n    tags:\n      - Voice\n      - Calling\n    serviceName: Telnyx Voice API\n    serviceCategory: API\n  - name: Telnyx Messaging API\n    baseURL: https://api.telnyx.com/v2\n    tags:\n      - SMS\n      - Messaging\n    serviceName: Telnyx Messaging API\n    serviceCategory: API\n  - name: Telnyx Numbers API\n    baseURL: https://api.telnyx.com/v2\n    tags:\n      - Numbers\n      - Provisioning\n    serviceName: Telnyx Numbers API\n    serviceCategory: API\n  - name: Telnyx Verify API\n    baseURL: https://api.telnyx.com/v2\n    tags:\n      - Verify\n      - 2FA\n    serviceName: Telnyx Verify API\n    serviceCategory: API\n  - name: Telnyx Fax API\n    baseURL: https://api.telnyx.com/v2\n\
  \    tags:\n      - Fax\n    serviceName: Telnyx Fax API\n    serviceCategory: API\n  - name: Telnyx Wireless API\n    baseURL: https://api.telnyx.com/v2\n    tags:\n      - Wireless\n      - IoT\n      - SIM\n    serviceName: Telnyx Wireless API\n    serviceCategory: API\n  - name: Telnyx Networking API\n    baseURL: https://api.telnyx.com/v2\n    tags:\n      - Networking\n    serviceName: Telnyx Networking API\n    serviceCategory: API\n  - name: Telnyx AI API\n    baseURL: https://api.telnyx.com/v2\n    tags:\n      - AI\n      - LLM\n      - Speech\n    serviceName: Telnyx AI API\n    serviceCategory: API\n  - name: Telnyx Billing & Reporting API\n    baseURL: https://api.telnyx.com/v2\n    tags:\n      - Billing\n      - Reporting\n    serviceName: Telnyx Billing & Reporting API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n\
  \    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/telnyx/refs/heads/main/finops/telnyx-finops.yml
sources: []
specification: FinOps Framework
tags:
- Communications
- CPaaS
- Voice
- SMS
- IoT
- FinOps
- Cost Management
- FOCUS
---
