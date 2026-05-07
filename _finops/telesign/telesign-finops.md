---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: telesign-sms-openapi.yml
  format: yaml
  label: Telesign SMS API
  slug: sms-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/telesign/refs/heads/main/openapi/telesign-sms-openapi.yml
- filename: telesign-phoneid-openapi.yml
  format: yaml
  label: Telesign PhoneID API
  slug: phoneid-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/telesign/refs/heads/main/openapi/telesign-phoneid-openapi.yml
- filename: telesign-verify-openapi.yml
  format: yaml
  label: Telesign Verify API
  slug: verify-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/telesign/refs/heads/main/openapi/telesign-verify-openapi.yml
- filename: telesign-score-openapi.yml
  format: yaml
  label: Telesign Score API
  slug: score-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/telesign/refs/heads/main/openapi/telesign-score-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Credit
  - Tax
  - Adjustment
  pricingCategory: Pay-As-You-Go
description: 'FOCUS-aligned FinOps for Telesign: pay-as-you-go per-message and per-request charges with destination-country pricing for SMS/Voice and per-lookup pricing for PhoneID, Score, and Verify, plus negotiated volume packaging.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Telesign Corporation
  ProviderName: Telesign
  PublisherName: Telesign Corporation
  ServiceCategory: Communications
  ServiceName: Telesign
layout: finops
meters:
- aggregation: sum
  dimensions:
  - destination_country
  - sender_id
  - message_class
  name: sms_messages
  unit: request
- aggregation: sum
  dimensions:
  - destination_country
  - call_type
  name: voice_calls
  unit: request
- aggregation: sum
  dimensions:
  - product_variant
  - country
  name: phoneid_lookups
  unit: request
- aggregation: sum
  dimensions:
  - product_variant
  - country
  name: score_requests
  unit: request
- aggregation: sum
  dimensions:
  - channel
  - country
  name: verify_requests
  unit: request
- aggregation: sum
  dimensions:
  - product
  name: trial_credits_consumed
  unit: request
name: Telesign Finops
provider_name: Telesign
provider_slug: telesign
publisher_name: Telesign Corporation
service_category: Communications
slug: telesign-finops
source_filename: telesign-finops.yml
source_heading: FinOps Profile
source_url: https://www.telesign.com/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Telesign\nproviderId: telesign\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Communications\n  - SMS\n  - Phone Intelligence\n  - Verification\ndescription: >-\n  FOCUS-aligned FinOps for Telesign: pay-as-you-go per-message and per-request charges with destination-country\n  pricing for SMS/Voice and per-lookup pricing for PhoneID, Score, and Verify, plus negotiated volume packaging.\nsources:\n  - https://www.telesign.com/pricing\n  - https://www.telesign.com/pricing/sms\n  - https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Telesign Corporation\nserviceCategory: Communications\n\
  billingModel:\n  pricingCategory: Pay-As-You-Go\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Credit\n    - Tax\n    - Adjustment\nfocusColumns:\n  ServiceName: Telesign\n  ServiceCategory: Communications\n  ProviderName: Telesign\n  PublisherName: Telesign Corporation\n  InvoiceIssuerName: Telesign Corporation\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: sms_messages\n    unit: request\n    aggregation: sum\n    dimensions:\n      - destination_country\n      - sender_id\n      - message_class\n  - name: voice_calls\n    unit: request\n    aggregation: sum\n    dimensions:\n      - destination_country\n      - call_type\n  - name: phoneid_lookups\n    unit: request\n    aggregation: sum\n    dimensions:\n      - product_variant\n      - country\n  - name: score_requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - product_variant\n      - country\n  - name: verify_requests\n    unit: request\n\
  \    aggregation: sum\n    dimensions:\n      - channel\n      - country\n  - name: trial_credits_consumed\n    unit: request\n    aggregation: sum\n    dimensions:\n      - product\nprinciples:\n  - name: Visibility\n    description: Use the Telesign customer portal usage and transactions exports to attribute consumption\n      by API and destination country at near-real-time granularity.\n  - name: Allocation\n    description: Tag traffic via separate API keys / sub-accounts per consuming team or product line so\n      Telesign invoice line items can be split for chargeback.\n  - name: Optimization\n    description: Lower SMS spend by routing OTP traffic through Verify (which can fall back to lower-cost\n      channels), caching PhoneID lookups for the documented validity window, and negotiating committed-use\n      packaging once monthly volume stabilizes.\n  - name: Accountability\n    description: Assign a budget owner per Telesign sub-account and review high-cost destination countries\n\
  \      and Verify fallback rates monthly with the account manager.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/telesign/refs/heads/main/finops/telesign-finops.yml
sources:
- https://www.telesign.com/pricing
- https://www.telesign.com/pricing/sms
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Communications
- SMS
- Phone Intelligence
- Verification
---
