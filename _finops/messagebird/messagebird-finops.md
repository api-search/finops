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
  pricingCategory: Pay As You Go (Per Channel)
description: FOCUS-aligned FinOps for Bird (MessageBird).
focus_columns:
  BillingCurrency: USD
  ProviderName: Bird (MessageBird)
  PublisherName: Bird (MessageBird)
  ServiceCategory: Omnichannel CPaaS
  ServiceName: Bird (MessageBird)
layout: finops
meters:
- aggregation: sum
  name: email_messages
  unit: email
- aggregation: sum
  dimensions:
  - direction
  - country
  name: sms_messages
  unit: message
- aggregation: sum
  dimensions:
  - template_category
  name: whatsapp_messages
  unit: message
- aggregation: sum
  name: push_notifications
  unit: notification
- aggregation: sum
  name: rcs_messages
  unit: message
- aggregation: sum
  name: voice_minutes
  unit: minute
name: Messagebird Finops
provider_name: messagebird
provider_slug: messagebird
publisher_name: Bird (MessageBird)
service_category: Omnichannel CPaaS
slug: messagebird-finops
source_filename: messagebird-finops.yml
source_heading: FinOps Profile
source_url: https://bird.com/en/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Bird (MessageBird)\nproviderId: messagebird\ncreated: '2026-05-04'\nmodified: '2026-05-04'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Omnichannel CPaaS\ndescription: FOCUS-aligned FinOps for Bird (MessageBird).\nsources:\n  - https://bird.com/en/pricing\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Bird (MessageBird)\nserviceCategory: Omnichannel CPaaS\nbillingModel:\n  pricingCategory: Pay As You Go (Per Channel)\n  billingFrequency: Monthly\n  billingCurrency: USD\nfocusColumns:\n  ServiceName: Bird (MessageBird)\n  ServiceCategory: Omnichannel CPaaS\n  ProviderName: Bird (MessageBird)\n  PublisherName: Bird (MessageBird)\n  BillingCurrency: USD\nmeters:\n  - name:\
  \ email_messages\n    unit: email\n    aggregation: sum\n  - name: sms_messages\n    unit: message\n    aggregation: sum\n    dimensions:\n      - direction\n      - country\n  - name: whatsapp_messages\n    unit: message\n    aggregation: sum\n    dimensions:\n      - template_category\n  - name: push_notifications\n    unit: notification\n    aggregation: sum\n  - name: rcs_messages\n    unit: message\n    aggregation: sum\n  - name: voice_minutes\n    unit: minute\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Track Bird (MessageBird) consumption monthly.\n  - name: Allocation\n    description: Tag usage to teams/cost centers.\n  - name: Optimization\n    description: Right-size; reclaim unused entitlements.\n  - name: Accountability\n    description: Set spend alerts; quarterly review.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/messagebird/refs/heads/main/finops/messagebird-finops.yml
sources:
- https://bird.com/en/pricing
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Omnichannel CPaaS
---
