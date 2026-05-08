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
description: FinOps framework definition for the Plivo API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Plivo
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Plivo
  PublisherName: Plivo
  ServiceCategory: Developer Tools / API
  ServiceName: Plivo
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
name: Plivo Finops
provider_name: Plivo
provider_slug: plivo
publisher_name: Plivo
service_category: API
slug: plivo-finops
source_filename: plivo-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Plivo\nproviderId: plivo\npublisherName: Plivo\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Communications\n  - CPaaS\n  - Voice\n  - SMS\n  - Messaging\n  - WhatsApp\n  - SIP Trunking\n  - Verify\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Plivo API surface. Provides a FOCUS-aligned mapping for\n  cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable\
  \ API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n\
  \      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Plivo\n  ServiceCategory: Developer Tools / API\n  ProviderName: Plivo\n  PublisherName: Plivo\n  InvoiceIssuerName: Plivo\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n\
  \    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Plivo Account API\n    baseURL: ''\n    tags:\n      - Account\n      - Authentication\n    serviceName: Plivo Account API\n    serviceCategory: API\n  - name: Plivo Subaccount API\n    baseURL: ''\n    tags:\n      - Subaccounts\n      - Multi-Tenant\n    serviceName: Plivo Subaccount API\n    serviceCategory: API\n  - name: Plivo Application API\n    baseURL: ''\n    tags:\n      - Applications\n      - Voice\n      - Webhooks\n    serviceName: Plivo Application API\n    serviceCategory: API\n  - name: Plivo SIP Authentication API\n    baseURL: ''\n    tags:\n      - SIP\n      - Authentication\n      - Endpoints\n    serviceName: Plivo SIP Authentication API\n    serviceCategory: API\n  - name: Plivo\
  \ Voice Call API\n    baseURL: ''\n    tags:\n      - Voice\n      - Calls\n      - Outbound\n      - Inbound\n    serviceName: Plivo Voice Call API\n    serviceCategory: API\n  - name: Plivo Conference API\n    baseURL: ''\n    tags:\n      - Voice\n      - Conferences\n    serviceName: Plivo Conference API\n    serviceCategory: API\n  - name: Plivo Multiparty Call API\n    baseURL: ''\n    tags:\n      - Voice\n      - Multiparty\n    serviceName: Plivo Multiparty Call API\n    serviceCategory: API\n  - name: Plivo Recording API\n    baseURL: ''\n    tags:\n      - Voice\n      - Recordings\n      - Media\n    serviceName: Plivo Recording API\n    serviceCategory: API\n  - name: Plivo Endpoint API\n    baseURL: ''\n    tags:\n      - SIP\n      - Endpoints\n      - WebRTC\n    serviceName: Plivo Endpoint API\n    serviceCategory: API\n  - name: Plivo Audio Stream API\n    baseURL: ''\n    tags:\n      - Voice\n      - Streaming\n      - WebSocket\n      - AI\n    serviceName: Plivo Audio\
  \ Stream API\n    serviceCategory: API\n  - name: Plivo Verified Caller ID API\n    baseURL: ''\n    tags:\n      - Voice\n      - Caller ID\n      - Verification\n    serviceName: Plivo Verified Caller ID API\n    serviceCategory: API\n  - name: Plivo Message API\n    baseURL: ''\n    tags:\n      - SMS\n      - MMS\n      - WhatsApp\n      - Messaging\n    serviceName: Plivo Message API\n    serviceCategory: API\n  - name: Plivo Media API\n    baseURL: ''\n    tags:\n      - MMS\n      - Media\n      - Uploads\n    serviceName: Plivo Media API\n    serviceCategory: API\n  - name: Plivo Powerpack API\n    baseURL: ''\n    tags:\n      - Messaging\n      - Number Pool\n      - Throughput\n    serviceName: Plivo Powerpack API\n    serviceCategory: API\n  - name: Plivo 10DLC Brand and Campaign API\n    baseURL: ''\n    tags:\n      - 10DLC\n      - A2P\n      - Compliance\n      - Brand\n      - Campaign\n    serviceName: Plivo 10DLC Brand and Campaign API\n    serviceCategory: API\n  -\
  \ name: Plivo Toll-Free Verification API\n    baseURL: ''\n    tags:\n      - Toll-Free\n      - Compliance\n      - Verification\n    serviceName: Plivo Toll-Free Verification API\n    serviceCategory: API\n  - name: Plivo Numbers API\n    baseURL: ''\n    tags:\n      - Phone Numbers\n      - Provisioning\n      - DIDs\n    serviceName: Plivo Numbers API\n    serviceCategory: API\n  - name: Plivo Pricing API\n    baseURL: ''\n    tags:\n      - Pricing\n      - Rates\n    serviceName: Plivo Pricing API\n    serviceCategory: API\n  - name: Plivo Verify API\n    baseURL: ''\n    tags:\n      - Verify\n      - OTP\n      - 2FA\n      - Authentication\n    serviceName: Plivo Verify API\n    serviceCategory: API\n  - name: Plivo Lookup API\n    baseURL: ''\n    tags:\n      - Lookup\n      - Number Validation\n      - HLR\n      - Carrier\n    serviceName: Plivo Lookup API\n    serviceCategory: API\n  - name: Plivo Zentrunk SIP Trunking API\n    baseURL: ''\n    tags:\n      - SIP\n     \
  \ - Trunking\n      - Voice\n    serviceName: Plivo Zentrunk SIP Trunking API\n    serviceCategory: API\n  - name: Plivo CNAM Lookup and Branded Calling API\n    baseURL: ''\n    tags:\n      - CNAM\n      - Caller ID\n      - Branded Calling\n    serviceName: Plivo CNAM Lookup and Branded Calling API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/plivo/refs/heads/main/finops/plivo-finops.yml
sources: []
specification: FinOps Framework
tags:
- Communications
- CPaaS
- Voice
- SMS
- Messaging
- WhatsApp
- SIP Trunking
- Verify
- FinOps
- Cost Management
- FOCUS
---
