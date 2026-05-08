---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: vonage-openapi.yml
  format: yaml
  label: Vonage SMS API
  slug: vonage-sms-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/vonage/refs/heads/main/openapi/vonage-openapi.yml
- filename: vonage-openapi.yml
  format: yaml
  label: Vonage Voice API
  slug: vonage-voice-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/vonage/refs/heads/main/openapi/vonage-openapi.yml
- filename: vonage-openapi.yml
  format: yaml
  label: Vonage Messages API
  slug: vonage-messages-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/vonage/refs/heads/main/openapi/vonage-openapi.yml
- filename: vonage-openapi.yml
  format: yaml
  label: Vonage Verify API
  slug: vonage-verify-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/vonage/refs/heads/main/openapi/vonage-openapi.yml
- filename: vonage-openapi.yml
  format: yaml
  label: Vonage Numbers API
  slug: vonage-numbers-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/vonage/refs/heads/main/openapi/vonage-openapi.yml
- filename: vonage-openapi.yml
  format: yaml
  label: Vonage Application API
  slug: vonage-application-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/vonage/refs/heads/main/openapi/vonage-openapi.yml
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
description: FinOps framework definition for the Vonage API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Vonage
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Vonage
  PublisherName: Vonage
  ServiceCategory: Developer Tools / API
  ServiceName: Vonage
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
name: Vonage Finops
provider_name: Vonage
provider_slug: vonage
publisher_name: Vonage
service_category: API
slug: vonage-finops
source_filename: vonage-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Vonage\nproviderId: vonage\npublisherName: Vonage\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Communication\n  - Messaging\n  - Telecommunications\n  - Video Conferencing\n  - Voice\n  - SMS\n  - Verification\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Vonage API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every\
  \ chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n   \
  \ capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Vonage\n  ServiceCategory: Developer Tools / API\n  ProviderName: Vonage\n  PublisherName: Vonage\n  InvoiceIssuerName: Vonage\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n\
  \    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Vonage SMS API\n    baseURL: https://rest.nexmo.com\n    tags:\n      - Communication\n      - Messaging\n      - SMS\n      - Telecommunications\n    serviceName: Vonage SMS API\n    serviceCategory: API\n  - name: Vonage Voice API\n    baseURL: https://api.nexmo.com/v1\n    tags:\n      - Communication\n      - Telecommunications\n      - Voice\n      - VoIP\n    serviceName: Vonage Voice API\n    serviceCategory: API\n  - name: Vonage Messages API\n    baseURL: https://api.nexmo.com/v1/messages\n    tags:\n      - Communication\n      - Messaging\n      - Omnichannel\n      - WhatsApp\n      - RCS\n    serviceName: Vonage Messages API\n    serviceCategory: API\n  - name: Vonage\
  \ Verify API\n    baseURL: https://api.nexmo.com\n    tags:\n      - Authentication\n      - Communication\n      - Security\n      - Two-Factor Authentication\n      - Verification\n    serviceName: Vonage Verify API\n    serviceCategory: API\n  - name: Vonage Numbers API\n    baseURL: https://rest.nexmo.com\n    tags:\n      - Communication\n      - Number Management\n      - Telecommunications\n      - Virtual Numbers\n    serviceName: Vonage Numbers API\n    serviceCategory: API\n  - name: Vonage Application API\n    baseURL: https://api.nexmo.com/v2/applications\n    tags:\n      - API Management\n      - Communication\n      - Configuration\n      - Developer Tools\n    serviceName: Vonage Application API\n    serviceCategory: API\n  - name: Vonage Conversations API\n    baseURL: https://api.nexmo.com/v1\n    tags:\n      - Communication\n      - Conversations\n      - Messaging\n      - Real-Time\n    serviceName: Vonage Conversations API\n    serviceCategory: API\n  - name: Vonage\
  \ Reports API\n    baseURL: https://api.nexmo.com/v2/reports\n    tags:\n      - Analytics\n      - Communication\n      - Reporting\n    serviceName: Vonage Reports API\n    serviceCategory: API\n  - name: Vonage Video API\n    baseURL: https://api.opentok.com\n    tags:\n      - Communication\n      - Telecommunications\n      - Video\n      - WebRTC\n    serviceName: Vonage Video API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/vonage/refs/heads/main/finops/vonage-finops.yml
sources: []
specification: FinOps Framework
tags:
- Communication
- Messaging
- Telecommunications
- Video Conferencing
- Voice
- SMS
- Verification
- FinOps
- Cost Management
- FOCUS
---
