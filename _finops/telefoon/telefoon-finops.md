---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: telefoon-voice-openapi.yml
  format: yaml
  label: Telefoon Voice API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/telefoon/refs/heads/main/openapi/telefoon-voice-openapi.yml
- filename: telefoon-sms-openapi.yml
  format: yaml
  label: Telefoon SMS API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/telefoon/refs/heads/main/openapi/telefoon-sms-openapi.yml
- filename: telefoon-numbers-openapi.yml
  format: yaml
  label: Telefoon Number Management API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/telefoon/refs/heads/main/openapi/telefoon-numbers-openapi.yml
billing_model:
  billingCurrency: EUR
  billingFrequency: Per-Invoice
  chargeCategories:
  - Purchase
  pricingCategory: Unverified
description: FinOps shape for the telefoon.com slug could not be reconciled; no public pricing or billing surface is documented.
focus_columns:
  BillingCurrency: EUR
  InvoiceIssuerName: Telefoon
  ProviderName: Telefoon
  PublisherName: Telefoon
  ServiceCategory: Communications / CPaaS
  ServiceName: Telefoon
layout: finops
meters:
- aggregation: sum
  name: unverified_usage
  unit: varies
name: Telefoon Finops
provider_name: Telefoon
provider_slug: telefoon
publisher_name: Telefoon
service_category: Communications / CPaaS
slug: telefoon-finops
source_filename: telefoon-finops.yml
source_heading: FinOps Profile
source_url: https://www.telefoon.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Telefoon\nproviderId: telefoon\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Belgium\n  - CPaaS\n  - EU Data Residency\n  - Europe\n  - GDPR Compliant\n  - Messaging\n  - Netherlands\n  - Number Provisioning\n  - SMS\n  - Telephony\n  - Voice\n  - FinOps\n  - FOCUS\ndescription: FinOps shape for the telefoon.com slug could not be reconciled; no public pricing or\n  billing surface is documented.\nsources:\n  - https://www.telefoon.com/\nnotes: Provider identity is unverified. FOCUS columns capture the slug name only; meters are not\n  reconciled to real billing lines.\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Telefoon\nserviceCategory: Communications\
  \ / CPaaS\nbillingModel:\n  pricingCategory: Unverified\n  billingFrequency: Per-Invoice\n  billingCurrency: EUR\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: Telefoon\n  ServiceCategory: Communications / CPaaS\n  ProviderName: Telefoon\n  PublisherName: Telefoon\n  InvoiceIssuerName: Telefoon\n  BillingCurrency: EUR\nmeters:\n  - name: unverified_usage\n    unit: varies\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: No public usage-export surface is documented for this slug.\n  - name: Allocation\n    description: Allocation cannot be modeled until a real billing surface is identified.\n  - name: Optimization\n    description: No documented cost levers; this artifact is a placeholder.\n  - name: Accountability\n    description: Accountability cannot be assigned until the provider entry is verified.\nmaintainers:\n  - name: Telefoon API Team\n    email: api-team@telefoon.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/telefoon/refs/heads/main/finops/telefoon-finops.yml
sources:
- https://www.telefoon.com/
specification: FinOps Framework
tags:
- Belgium
- CPaaS
- EU Data Residency
- Europe
- GDPR Compliant
- Messaging
- Netherlands
- Number Provisioning
- SMS
- Telephony
- Voice
- FinOps
- FOCUS
---
