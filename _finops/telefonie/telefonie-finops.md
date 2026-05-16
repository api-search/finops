---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: telefonie-voice-openapi.yml
  format: yaml
  label: Telefonie Voice API
  slug: telefonie-voice-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/telefonie/refs/heads/main/openapi/telefonie-voice-openapi.yml
- filename: telefonie-sms-openapi.yml
  format: yaml
  label: Telefonie SMS API
  slug: telefonie-sms-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/telefonie/refs/heads/main/openapi/telefonie-sms-openapi.yml
- filename: telefonie-numbers-openapi.yml
  format: yaml
  label: Telefonie Number Management API
  slug: telefonie-number-management-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/telefonie/refs/heads/main/openapi/telefonie-numbers-openapi.yml
- filename: telefonie-recording-openapi.yml
  format: yaml
  label: Telefonie Call Recording API
  slug: telefonie-call-recording-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/telefonie/refs/heads/main/openapi/telefonie-recording-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Per-Invoice
  chargeCategories:
  - Purchase
  pricingCategory: Unverified
description: FinOps shape for the telefonie.com slug could not be reconciled; no public pricing or billing surface is documented.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Telefonie
  ProviderName: Telefonie
  PublisherName: Telefonie
  ServiceCategory: Communications / CPaaS
  ServiceName: Telefonie
layout: finops
meters:
- aggregation: sum
  name: unverified_usage
  unit: varies
name: Telefonie Finops
provider_name: Telefonie
provider_slug: telefonie
publisher_name: Telefonie
service_category: Communications / CPaaS
slug: telefonie-finops
source_filename: telefonie-finops.yml
source_heading: FinOps Profile
source_url: https://www.telefonie.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Telefonie\nproviderId: telefonie\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Call Recording\n  - CPaaS\n  - Messaging\n  - Number Provisioning\n  - SMS\n  - Telecommunications\n  - Telephony\n  - Voice\n  - VoIP\n  - FinOps\n  - FOCUS\ndescription: FinOps shape for the telefonie.com slug could not be reconciled; no public pricing or\n  billing surface is documented.\nsources:\n  - https://www.telefonie.com/\nnotes: Provider identity is unverified. FOCUS columns capture the slug name only; meters are not\n  reconciled to real billing lines.\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Telefonie\nserviceCategory: Communications / CPaaS\nbillingModel:\n\
  \  pricingCategory: Unverified\n  billingFrequency: Per-Invoice\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: Telefonie\n  ServiceCategory: Communications / CPaaS\n  ProviderName: Telefonie\n  PublisherName: Telefonie\n  InvoiceIssuerName: Telefonie\n  BillingCurrency: USD\nmeters:\n  - name: unverified_usage\n    unit: varies\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: No public usage-export surface is documented for this slug.\n  - name: Allocation\n    description: Allocation cannot be modeled until a real billing surface is identified.\n  - name: Optimization\n    description: No documented cost levers; this artifact is a placeholder.\n  - name: Accountability\n    description: Accountability cannot be assigned until the provider entry is verified.\nmaintainers:\n  - name: Telefonie API Team\n    email: api@telefonie.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/telefonie/refs/heads/main/finops/telefonie-finops.yml
sources:
- https://www.telefonie.com/
specification: FinOps Framework
tags:
- Call Recording
- CPaaS
- Messaging
- Number Provisioning
- SMS
- Telecommunications
- Telephony
- Voice
- VoIP
- FinOps
- FOCUS
---
