---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: telefon-voice-openapi.yml
  format: yaml
  label: Telefon Voice API
  slug: telefon-voice-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/telefon/refs/heads/main/openapi/telefon-voice-openapi.yml
- filename: telefon-sms-openapi.yml
  format: yaml
  label: Telefon SMS API
  slug: telefon-sms-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/telefon/refs/heads/main/openapi/telefon-sms-openapi.yml
- filename: telefon-numbers-openapi.yml
  format: yaml
  label: Telefon Number Management API
  slug: telefon-number-management-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/telefon/refs/heads/main/openapi/telefon-numbers-openapi.yml
- filename: telefon-recording-openapi.yml
  format: yaml
  label: Telefon Call Recording API
  slug: telefon-call-recording-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/telefon/refs/heads/main/openapi/telefon-recording-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Per-Invoice
  chargeCategories:
  - Purchase
  pricingCategory: Unverified
description: FinOps shape for the telefon.com slug could not be reconciled. No pricing, billing, or usage-export surface is publicly reachable.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Telefon
  ProviderName: Telefon
  PublisherName: Telefon
  ServiceCategory: Communications / CPaaS
  ServiceName: Telefon
layout: finops
meters:
- aggregation: sum
  name: unverified_usage
  unit: varies
name: Telefon Finops
provider_name: Telefon
provider_slug: telefon
publisher_name: Telefon
service_category: Communications / CPaaS
slug: telefon-finops
source_filename: telefon-finops.yml
source_heading: FinOps Profile
source_url: https://www.telefon.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Telefon\nproviderId: telefon\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Call Recording\n  - Communications\n  - CPaaS\n  - Global Coverage\n  - Messaging\n  - Number Provisioning\n  - SMS\n  - Telephony\n  - Voice\n  - VoIP\n  - FinOps\n  - FOCUS\ndescription: FinOps shape for the telefon.com slug could not be reconciled. No pricing, billing, or\n  usage-export surface is publicly reachable.\nsources:\n  - https://www.telefon.com/\nnotes: Provider identity is unverified. FOCUS columns capture the slug name only; meters are not\n  reconciled to real billing lines.\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Telefon\nserviceCategory: Communications\
  \ / CPaaS\nbillingModel:\n  pricingCategory: Unverified\n  billingFrequency: Per-Invoice\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: Telefon\n  ServiceCategory: Communications / CPaaS\n  ProviderName: Telefon\n  PublisherName: Telefon\n  InvoiceIssuerName: Telefon\n  BillingCurrency: USD\nmeters:\n  - name: unverified_usage\n    unit: varies\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: No public usage-export surface is documented for this slug.\n  - name: Allocation\n    description: Allocation cannot be modeled until a real billing surface is identified.\n  - name: Optimization\n    description: No documented cost levers; this artifact is a placeholder.\n  - name: Accountability\n    description: Accountability cannot be assigned until the provider entry is verified.\nmaintainers:\n  - name: Telefon API Team\n    email: api@telefon.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/telefon/refs/heads/main/finops/telefon-finops.yml
sources:
- https://www.telefon.com/
specification: FinOps Framework
tags:
- Call Recording
- Communications
- CPaaS
- Global Coverage
- Messaging
- Number Provisioning
- SMS
- Telephony
- Voice
- VoIP
- FinOps
- FOCUS
---
