---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: whatsapp-cloud-api-openapi.yml
  format: yaml
  label: WhatsApp Business Platform API
  slug: business-platform-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/whatsapp/refs/heads/main/openapi/whatsapp-cloud-api-openapi.yml
- filename: whatsapp-business-management-api-openapi.yml
  format: yaml
  label: WhatsApp Business Account Management API
  slug: business-account-management-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/whatsapp/refs/heads/main/openapi/whatsapp-business-management-api-openapi.yml
- filename: whatsapp-flows-api-openapi.yml
  format: yaml
  label: WhatsApp Flows API
  slug: flows-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/whatsapp/refs/heads/main/openapi/whatsapp-flows-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Credit
  - Tax
  - Adjustment
  - Refund
  pricingCategory: Conversation-Based Pay-As-You-Go
description: 'FOCUS-aligned FinOps for WhatsApp Business Platform: pay-per-conversation across four categories (Marketing, Utility, Authentication, Service) with per-recipient-country pricing, plus free entry-point and a service-conversation free allotment. The billable unit is the 24-hour conversation, not the API call.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Meta Platforms, Inc.
  ProviderName: Meta
  PublisherName: Meta Platforms, Inc.
  ServiceCategory: Business Messaging
  ServiceName: WhatsApp Business Platform
layout: finops
meters:
- aggregation: sum
  dimensions:
  - recipient_country
  - waba_id
  - phone_number
  - template_id
  name: marketing_conversations
  unit: conversation
- aggregation: sum
  dimensions:
  - recipient_country
  - waba_id
  - phone_number
  - template_id
  name: utility_conversations
  unit: conversation
- aggregation: sum
  dimensions:
  - recipient_country
  - waba_id
  - phone_number
  - international_authentication_flag
  name: authentication_conversations
  unit: conversation
- aggregation: sum
  dimensions:
  - recipient_country
  - waba_id
  - phone_number
  - free_tier_allotment_used
  name: service_conversations
  unit: conversation
- aggregation: sum
  dimensions:
  - entry_point
  - waba_id
  name: free_entry_point_conversations
  unit: conversation
- aggregation: sum
  dimensions:
  - waba_id
  - phone_number
  - direction
  name: messages_sent
  unit: message
name: Whatsapp Finops
provider_name: WhatsApp
provider_slug: whatsapp
publisher_name: Meta Platforms, Inc.
service_category: Business Messaging
slug: whatsapp-finops
source_filename: whatsapp-finops.yml
source_heading: FinOps Profile
source_url: https://developers.facebook.com/docs/whatsapp/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: WhatsApp\nproviderId: whatsapp\npublisherName: Meta Platforms, Inc.\nserviceCategory: Business Messaging\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - Messaging\n  - Business\n  - FinOps\n  - FOCUS\n  - Conversation-Based Pricing\ndescription: 'FOCUS-aligned FinOps for WhatsApp Business Platform: pay-per-conversation across four categories (Marketing, Utility, Authentication, Service) with per-recipient-country pricing, plus free entry-point and a service-conversation free allotment. The billable unit is the 24-hour conversation, not the API call.'\nsources:\n  - https://developers.facebook.com/docs/whatsapp/pricing\n\
  \  - https://developers.facebook.com/docs/whatsapp/pricing/conversation-based-pricing\n  - https://business.whatsapp.com/products/platform-pricing\nbillingModel:\n  pricingCategory: Conversation-Based Pay-As-You-Go\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Credit\n    - Tax\n    - Adjustment\n    - Refund\nfocusColumns:\n  ServiceName: WhatsApp Business Platform\n  ServiceCategory: Business Messaging\n  ProviderName: Meta\n  PublisherName: Meta Platforms, Inc.\n  InvoiceIssuerName: Meta Platforms, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: marketing_conversations\n    unit: conversation\n    aggregation: sum\n    dimensions:\n      - recipient_country\n      - waba_id\n      - phone_number\n      - template_id\n  - name: utility_conversations\n    unit: conversation\n    aggregation: sum\n    dimensions:\n      - recipient_country\n      - waba_id\n      - phone_number\n      - template_id\n  - name: authentication_conversations\n\
  \    unit: conversation\n    aggregation: sum\n    dimensions:\n      - recipient_country\n      - waba_id\n      - phone_number\n      - international_authentication_flag\n  - name: service_conversations\n    unit: conversation\n    aggregation: sum\n    dimensions:\n      - recipient_country\n      - waba_id\n      - phone_number\n      - free_tier_allotment_used\n  - name: free_entry_point_conversations\n    unit: conversation\n    aggregation: sum\n    dimensions:\n      - entry_point\n      - waba_id\n  - name: messages_sent\n    unit: message\n    aggregation: sum\n    dimensions:\n      - waba_id\n      - phone_number\n      - direction\nprinciples:\n  - name: Visibility\n    description: 'Pull conversation analytics from the WhatsApp Business Management API (conversation_analytics, pricing_analytics) and the WABA-level usage views in Meta Business Manager; reconcile against the monthly Meta invoice.'\n  - name: Allocation\n    description: Allocate by WABA, phone number, conversation\
  \ category, recipient country, and template ID. Templates and entry points drive category classification, which directly drives unit price.\n  - name: Optimization\n    description: 'Levers are: send Utility instead of Marketing where the use case allows (lower per-conversation rate in most countries), exhaust the monthly service-conversation free allotment before opening paid Marketing, route ads-that-click-to-WhatsApp through the free entry-point window, and consolidate multiple notifications into one 24h conversation.'\n  - name: Accountability\n    description: Marketing owns Marketing-conversation spend (campaign tied to template ID); product / lifecycle owns Utility and Authentication; CX owns Service. Phone-number quality rating (Green / Yellow / Red) is a shared signal because demotion lowers tier caps and constrains all categories.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/whatsapp/refs/heads/main/finops/whatsapp-finops.yml
sources:
- https://developers.facebook.com/docs/whatsapp/pricing
- https://developers.facebook.com/docs/whatsapp/pricing/conversation-based-pricing
- https://business.whatsapp.com/products/platform-pricing
specification: FinOps Framework
tags:
- Messaging
- Business
- FinOps
- FOCUS
- Conversation-Based Pricing
---
