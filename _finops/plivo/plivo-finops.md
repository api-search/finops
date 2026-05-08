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
  billingTerm: Post-Paid (with optional prepaid balance)
  chargeCategories:
  - Usage
  - Purchase
  - Adjustment
  - Tax
  commitmentDiscount: Volume discounts and committed-spend Enterprise contracts (~$1,000/month minimum).
  pricingCategory: Usage-Based / Pay-As-You-Go
description: Plivo bills under a usage-based, post-paid model with optional prepaid balance top-ups. Charges accrue per outbound/inbound SMS segment, per voice minute (60-second billing increment), per phone-number rental (recurring), and per add-on (Verify, Lookup, MMS, WhatsApp, AI Voice Agent, CNAM). Enterprise customers move to committed-spend agreements starting at approximately $1,000/month.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Plivo
  PricingCategory: Standard Pricing
  ProviderName: Plivo
  PublisherName: Plivo
  ServiceCategory: Communications
  ServiceName: Plivo
layout: finops
meters:
- aggregation: sum
  description: Outbound SMS segments (pricing varies by destination country and number type).
  dimensions:
  - account
  - subaccount
  - country
  - number_type
  name: sms_segments_outbound
  unit: segment
- aggregation: sum
  description: Inbound SMS segments delivered to Plivo-hosted numbers.
  dimensions:
  - account
  - subaccount
  - country
  - number_type
  name: sms_segments_inbound
  unit: segment
- aggregation: sum
  description: MMS message events including media transfer fees.
  dimensions:
  - account
  - subaccount
  - country
  name: mms_messages
  unit: message
- aggregation: sum
  description: Outbound voice minutes (per-country rate, 60-second billing increment).
  dimensions:
  - account
  - subaccount
  - country
  - call_type
  name: voice_minutes_outbound
  unit: minute
- aggregation: sum
  description: Inbound voice minutes to Plivo-hosted numbers.
  dimensions:
  - account
  - subaccount
  - country
  - call_type
  name: voice_minutes_inbound
  unit: minute
- aggregation: max
  description: Monthly recurring rental for owned phone numbers (long codes, toll-free, short codes, mobile).
  dimensions:
  - account
  - subaccount
  - country
  - number_type
  name: phone_number_rental
  unit: number-month
- aggregation: sum
  description: Verification attempts initiated through the Plivo Verify API.
  dimensions:
  - account
  - channel
  - country
  name: verify_attempts
  unit: attempt
- aggregation: sum
  description: Lookup API requests (HLR, carrier, line-type).
  dimensions:
  - account
  - country
  name: lookup_requests
  unit: request
- aggregation: sum
  description: AI Voice Agent minutes (separate metering for STT/TTS/LLM round-trips).
  dimensions:
  - account
  - agent
  name: ai_voice_agent_minutes
  unit: minute
- aggregation: sum
  description: Carrier 10DLC registration / vetting / monthly fees passed through.
  dimensions:
  - account
  - brand
  - campaign
  name: 10dlc_brand_campaign
  unit: fee
name: Plivo Finops
provider_name: Plivo
provider_slug: plivo
publisher_name: Plivo
service_category: Communications
slug: plivo-finops
source_filename: plivo-finops.yml
source_heading: FinOps Profile
source_url: https://www.plivo.com/pricing/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Plivo\nproviderId: plivo\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: true\ntags:\n  - Communications\n  - CPaaS\n  - Voice\n  - SMS\n  - Messaging\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: >-\n  Plivo bills under a usage-based, post-paid model with optional prepaid balance top-ups. Charges accrue per outbound/inbound SMS segment, per voice minute (60-second billing increment), per phone-number rental (recurring), and per add-on (Verify, Lookup, MMS, WhatsApp, AI Voice Agent, CNAM). Enterprise customers move to committed-spend agreements starting at approximately $1,000/month.\nnotes: >-\n  Reconciled against Plivo published pricing on 2026-05-08. Plivo provides invoice CSV/PDF and a Console usage report; there is no public FOCUS-formatted feed. The Pricing API can be used to construct a current rate card for downstream cost-allocation.\n\
  sources:\n  - https://www.plivo.com/pricing/\n  - https://www.plivo.com/docs/account/api/pricing/\n  - https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Plivo\nserviceCategory: Communications\nbillingModel:\n  pricingCategory: Usage-Based / Pay-As-You-Go\n  billingFrequency: Monthly\n  billingTerm: Post-Paid (with optional prepaid balance)\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Adjustment\n    - Tax\n  commitmentDiscount: Volume discounts and committed-spend Enterprise contracts (~$1,000/month minimum).\nfocusColumns:\n  ServiceName: Plivo\n  ServiceCategory: Communications\n  ProviderName: Plivo\n  PublisherName: Plivo\n  InvoiceIssuerName: Plivo\n  BillingCurrency: USD\n  ChargeCategory: Usage\n  PricingCategory:\
  \ Standard Pricing\nmeters:\n  - name: sms_segments_outbound\n    description: Outbound SMS segments (pricing varies by destination country and number type).\n    unit: segment\n    aggregation: sum\n    dimensions:\n      - account\n      - subaccount\n      - country\n      - number_type\n  - name: sms_segments_inbound\n    description: Inbound SMS segments delivered to Plivo-hosted numbers.\n    unit: segment\n    aggregation: sum\n    dimensions:\n      - account\n      - subaccount\n      - country\n      - number_type\n  - name: mms_messages\n    description: MMS message events including media transfer fees.\n    unit: message\n    aggregation: sum\n    dimensions:\n      - account\n      - subaccount\n      - country\n  - name: voice_minutes_outbound\n    description: Outbound voice minutes (per-country rate, 60-second billing increment).\n    unit: minute\n    aggregation: sum\n    dimensions:\n      - account\n      - subaccount\n      - country\n      - call_type\n  - name: voice_minutes_inbound\n\
  \    description: Inbound voice minutes to Plivo-hosted numbers.\n    unit: minute\n    aggregation: sum\n    dimensions:\n      - account\n      - subaccount\n      - country\n      - call_type\n  - name: phone_number_rental\n    description: Monthly recurring rental for owned phone numbers (long codes, toll-free, short codes, mobile).\n    unit: number-month\n    aggregation: max\n    dimensions:\n      - account\n      - subaccount\n      - country\n      - number_type\n  - name: verify_attempts\n    description: Verification attempts initiated through the Plivo Verify API.\n    unit: attempt\n    aggregation: sum\n    dimensions:\n      - account\n      - channel\n      - country\n  - name: lookup_requests\n    description: Lookup API requests (HLR, carrier, line-type).\n    unit: request\n    aggregation: sum\n    dimensions:\n      - account\n      - country\n  - name: ai_voice_agent_minutes\n    description: AI Voice Agent minutes (separate metering for STT/TTS/LLM round-trips).\n\
  \    unit: minute\n    aggregation: sum\n    dimensions:\n      - account\n      - agent\n  - name: 10dlc_brand_campaign\n    description: Carrier 10DLC registration / vetting / monthly fees passed through.\n    unit: fee\n    aggregation: sum\n    dimensions:\n      - account\n      - brand\n      - campaign\nprinciples:\n  - name: Visibility\n    description: >-\n      Pull invoice CSV and the Console usage report regularly; for high-volume accounts, request scheduled usage exports. Use subaccount segregation to isolate cost centers from day one.\n  - name: Allocation\n    description: >-\n      Tag traffic by subaccount per business unit; use the Pricing API to convert raw usage into expected cost per dimension before invoice arrival.\n  - name: Optimization\n    description: >-\n      Move to a Powerpack to spread outbound MPS for better deliverability/cost; right-size phone-number inventory and release unused DIDs; promote chatty integrations to higher-vetted 10DLC brand scores; consider\
  \ an Enterprise commit once monthly spend approaches $1,000.\n  - name: Accountability\n    description: >-\n      Assign per-subaccount owners; alert on month-to-date consumption versus forecast; gate test traffic to a separate subaccount.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/plivo/refs/heads/main/finops/plivo-finops.yml
sources:
- https://www.plivo.com/pricing/
- https://www.plivo.com/docs/account/api/pricing/
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Communications
- CPaaS
- Voice
- SMS
- Messaging
- FinOps
- Cost Management
- FOCUS
---
