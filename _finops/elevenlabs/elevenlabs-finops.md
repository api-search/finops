---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: elevenlabs-text-to-speech-openapi.yml
  format: yaml
  label: ElevenLabs Text to Speech API
  slug: text-to-speech
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/elevenlabs/refs/heads/main/openapi/elevenlabs-text-to-speech-openapi.yml
- filename: elevenlabs-speech-to-text-openapi.yml
  format: yaml
  label: ElevenLabs Speech to Text API
  slug: speech-to-text
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/elevenlabs/refs/heads/main/openapi/elevenlabs-speech-to-text-openapi.yml
- filename: elevenlabs-voice-cloning-openapi.yml
  format: yaml
  label: ElevenLabs Voice Cloning API
  slug: voice-cloning
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/elevenlabs/refs/heads/main/openapi/elevenlabs-voice-cloning-openapi.yml
- filename: elevenlabs-voices-openapi.yml
  format: yaml
  label: ElevenLabs Voices API
  slug: voices
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/elevenlabs/refs/heads/main/openapi/elevenlabs-voices-openapi.yml
- filename: elevenlabs-sound-effects-openapi.yml
  format: yaml
  label: ElevenLabs Sound Effects API
  slug: sound-effects
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/elevenlabs/refs/heads/main/openapi/elevenlabs-sound-effects-openapi.yml
- filename: elevenlabs-audio-isolation-openapi.yml
  format: yaml
  label: ElevenLabs Audio Isolation API
  slug: audio-isolation
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/elevenlabs/refs/heads/main/openapi/elevenlabs-audio-isolation-openapi.yml
- filename: elevenlabs-dubbing-openapi.yml
  format: yaml
  label: ElevenLabs Dubbing API
  slug: dubbing
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/elevenlabs/refs/heads/main/openapi/elevenlabs-dubbing-openapi.yml
- filename: elevenlabs-voice-changer-openapi.yml
  format: yaml
  label: ElevenLabs Voice Changer API
  slug: voice-changer
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/elevenlabs/refs/heads/main/openapi/elevenlabs-voice-changer-openapi.yml
- filename: elevenlabs-music-openapi.yml
  format: yaml
  label: ElevenLabs Music Generation API
  slug: music
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/elevenlabs/refs/heads/main/openapi/elevenlabs-music-openapi.yml
- filename: elevenlabs-conversational-ai-openapi.yml
  format: yaml
  label: ElevenLabs Conversational AI API
  slug: conversational-ai
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/elevenlabs/refs/heads/main/openapi/elevenlabs-conversational-ai-openapi.yml
- filename: elevenlabs-studio-openapi.yml
  format: yaml
  label: ElevenLabs Studio API
  slug: studio
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/elevenlabs/refs/heads/main/openapi/elevenlabs-studio-openapi.yml
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
description: FinOps framework definition for the elevenlabs API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: elevenlabs
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: elevenlabs
  PublisherName: elevenlabs
  ServiceCategory: Developer Tools / API
  ServiceName: elevenlabs
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
name: Elevenlabs Finops
provider_name: elevenlabs
provider_slug: elevenlabs
publisher_name: elevenlabs
service_category: API
slug: elevenlabs-finops
source_filename: elevenlabs-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: elevenlabs\nproviderId: elevenlabs\npublisherName: elevenlabs\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the elevenlabs API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can\
  \ be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing\
  \ and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: elevenlabs\n  ServiceCategory: Developer Tools / API\n  ProviderName: elevenlabs\n  PublisherName: elevenlabs\n  InvoiceIssuerName: elevenlabs\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name:\
  \ compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: ElevenLabs Text to Speech API\n    baseURL: https://api.elevenlabs.io\n    tags:\n      - AI\n      - Audio\n      - Speech Synthesis\n      - Text to Speech\n      - Voice\n    serviceName: ElevenLabs Text to Speech API\n    serviceCategory: API\n  - name: ElevenLabs Speech to Text API\n    baseURL: https://api.elevenlabs.io\n    tags:\n      - AI\n      - Audio\n      - Speech to Text\n      - Transcription\n    serviceName: ElevenLabs Speech to Text API\n    serviceCategory: API\n  - name: ElevenLabs Voice Cloning API\n    baseURL: https://api.elevenlabs.io\n    tags:\n      - AI\n      - Audio\n      - Voice\n      - Voice Cloning\n    serviceName: ElevenLabs Voice Cloning API\n    serviceCategory: API\n  - name: ElevenLabs Voices API\n    baseURL: https://api.elevenlabs.io\n\
  \    tags:\n      - AI\n      - Voice Library\n      - Voice Management\n      - Voices\n    serviceName: ElevenLabs Voices API\n    serviceCategory: API\n  - name: ElevenLabs Sound Effects API\n    baseURL: https://api.elevenlabs.io\n    tags:\n      - AI\n      - Audio Generation\n      - Sound Effects\n    serviceName: ElevenLabs Sound Effects API\n    serviceCategory: API\n  - name: ElevenLabs Audio Isolation API\n    baseURL: https://api.elevenlabs.io\n    tags:\n      - Audio Isolation\n      - Audio Processing\n      - Noise Removal\n    serviceName: ElevenLabs Audio Isolation API\n    serviceCategory: API\n  - name: ElevenLabs Dubbing API\n    baseURL: https://api.elevenlabs.io\n    tags:\n      - Audio\n      - Dubbing\n      - Localization\n      - Translation\n      - Video\n    serviceName: ElevenLabs Dubbing API\n    serviceCategory: API\n  - name: ElevenLabs Voice Changer API\n    baseURL: https://api.elevenlabs.io\n    tags:\n      - Audio Processing\n      - Voice Changer\n\
  \      - Voice Conversion\n    serviceName: ElevenLabs Voice Changer API\n    serviceCategory: API\n  - name: ElevenLabs Music Generation API\n    baseURL: https://api.elevenlabs.io\n    tags:\n      - AI\n      - Audio Generation\n      - Music\n    serviceName: ElevenLabs Music Generation API\n    serviceCategory: API\n  - name: ElevenLabs Conversational AI API\n    baseURL: https://api.elevenlabs.io\n    tags:\n      - AI\n      - Conversational AI\n      - Real-Time\n      - Voice Agents\n    serviceName: ElevenLabs Conversational AI API\n    serviceCategory: API\n  - name: ElevenLabs Studio API\n    baseURL: https://api.elevenlabs.io\n    tags:\n      - Content Management\n      - Projects\n      - Studio\n    serviceName: ElevenLabs Studio API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\
  \ []\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/elevenlabs/refs/heads/main/finops/elevenlabs-finops.yml
sources: []
specification: FinOps Framework
tags:
- FinOps
- Cost Management
- FOCUS
---
