---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: messagebird-sms-messaging-openapi.yml
  format: yaml
  label: MessageBird SMS Messaging API
  slug: sms-messaging-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/messagebird/refs/heads/main/openapi/messagebird-sms-messaging-openapi.yml
- filename: messagebird-voice-calling-openapi.yml
  format: yaml
  label: MessageBird Voice Calling API
  slug: voice-calling-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/messagebird/refs/heads/main/openapi/messagebird-voice-calling-openapi.yml
- filename: messagebird-voice-messaging-openapi.yml
  format: yaml
  label: MessageBird Voice Messaging API
  slug: voice-messaging-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/messagebird/refs/heads/main/openapi/messagebird-voice-messaging-openapi.yml
- filename: messagebird-conversations-openapi.yml
  format: yaml
  label: MessageBird Conversations API
  slug: conversations-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/messagebird/refs/heads/main/openapi/messagebird-conversations-openapi.yml
- filename: messagebird-whatsapp-openapi.yml
  format: yaml
  label: MessageBird WhatsApp API
  slug: whatsapp-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/messagebird/refs/heads/main/openapi/messagebird-whatsapp-openapi.yml
- filename: messagebird-verify-openapi.yml
  format: yaml
  label: MessageBird Verify API
  slug: verify-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/messagebird/refs/heads/main/openapi/messagebird-verify-openapi.yml
- filename: messagebird-lookup-openapi.yml
  format: yaml
  label: MessageBird Lookup API
  slug: lookup-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/messagebird/refs/heads/main/openapi/messagebird-lookup-openapi.yml
- filename: messagebird-hlr-openapi.yml
  format: yaml
  label: MessageBird HLR API
  slug: hlr-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/messagebird/refs/heads/main/openapi/messagebird-hlr-openapi.yml
- filename: messagebird-contacts-openapi.yml
  format: yaml
  label: MessageBird Contacts API
  slug: contacts-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/messagebird/refs/heads/main/openapi/messagebird-contacts-openapi.yml
- filename: messagebird-numbers-openapi.yml
  format: yaml
  label: MessageBird Numbers API
  slug: numbers-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/messagebird/refs/heads/main/openapi/messagebird-numbers-openapi.yml
- filename: messagebird-balance-openapi.yml
  format: yaml
  label: MessageBird Balance API
  slug: balance-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/messagebird/refs/heads/main/openapi/messagebird-balance-openapi.yml
- filename: messagebird-integrations-openapi.yml
  format: yaml
  label: MessageBird Integrations API
  slug: integrations-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/messagebird/refs/heads/main/openapi/messagebird-integrations-openapi.yml
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
description: FinOps framework definition for the messagebird API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: messagebird
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: messagebird
  PublisherName: messagebird
  ServiceCategory: Developer Tools / API
  ServiceName: messagebird
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
name: Messagebird Finops
provider_name: messagebird
provider_slug: messagebird
publisher_name: messagebird
service_category: API
slug: messagebird-finops
source_filename: messagebird-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: messagebird\nproviderId: messagebird\npublisherName: messagebird\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the messagebird API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost\
  \ can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n     \
  \ - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: messagebird\n  ServiceCategory: Developer Tools / API\n  ProviderName: messagebird\n  PublisherName: messagebird\n  InvoiceIssuerName: messagebird\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n\
  \  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: MessageBird SMS Messaging API\n    baseURL: https://rest.messagebird.com\n    tags:\n      - Communications\n      - Messaging\n      - SMS\n      - Text Messages\n    serviceName: MessageBird SMS Messaging API\n    serviceCategory: API\n  - name: MessageBird Voice Calling API\n    baseURL: https://voice.messagebird.com\n    tags:\n      - Calling\n      - Communications\n      - Telephony\n      - Voice\n    serviceName: MessageBird Voice Calling API\n    serviceCategory: API\n  - name: MessageBird Voice Messaging API\n    baseURL: https://rest.messagebird.com\n    tags:\n      - Communications\n      - Messaging\n      - Text-To-Speech\n      - Voice\n    serviceName: MessageBird Voice Messaging API\n    serviceCategory: API\n  - name: MessageBird Conversations\
  \ API\n    baseURL: https://conversations.messagebird.com\n    tags:\n      - Chat\n      - Communications\n      - Messaging\n      - Omnichannel\n      - WhatsApp\n    serviceName: MessageBird Conversations API\n    serviceCategory: API\n  - name: MessageBird WhatsApp API\n    baseURL: https://conversations.messagebird.com\n    tags:\n      - Communications\n      - Messaging\n      - Notifications\n      - WhatsApp\n    serviceName: MessageBird WhatsApp API\n    serviceCategory: API\n  - name: MessageBird Verify API\n    baseURL: https://rest.messagebird.com\n    tags:\n      - OTP\n      - Security\n      - Two-Factor Authentication\n      - Verification\n    serviceName: MessageBird Verify API\n    serviceCategory: API\n  - name: MessageBird Lookup API\n    baseURL: https://rest.messagebird.com\n    tags:\n      - HLR\n      - Number Intelligence\n      - Phone Numbers\n      - Validation\n    serviceName: MessageBird Lookup API\n    serviceCategory: API\n  - name: MessageBird HLR\
  \ API\n    baseURL: https://rest.messagebird.com\n    tags:\n      - HLR\n      - Mobile Network\n      - Network Query\n      - Phone Numbers\n    serviceName: MessageBird HLR API\n    serviceCategory: API\n  - name: MessageBird Contacts API\n    baseURL: https://rest.messagebird.com\n    tags:\n      - Address Book\n      - Contacts\n      - Customer Data\n      - Groups\n    serviceName: MessageBird Contacts API\n    serviceCategory: API\n  - name: MessageBird Numbers API\n    baseURL: https://numbers.messagebird.com\n    tags:\n      - Number Management\n      - Phone Numbers\n      - Provisioning\n      - Telecommunications\n    serviceName: MessageBird Numbers API\n    serviceCategory: API\n  - name: MessageBird Balance API\n    baseURL: https://rest.messagebird.com\n    tags:\n      - Account\n      - Balance\n      - Billing\n      - Credits\n    serviceName: MessageBird Balance API\n    serviceCategory: API\n  - name: MessageBird Integrations API\n    baseURL: https://integrations.messagebird.com\n\
  \    tags:\n      - Integrations\n      - Message Templates\n      - Templates\n      - WhatsApp\n    serviceName: MessageBird Integrations API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers: []\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/messagebird/refs/heads/main/finops/messagebird-finops.yml
sources: []
specification: FinOps Framework
tags:
- FinOps
- Cost Management
- FOCUS
---
