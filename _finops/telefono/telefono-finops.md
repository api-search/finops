---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: telefono-validation-openapi.yml
  format: yaml
  label: Telefono Phone Validation API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/telefono/refs/heads/main/openapi/telefono-validation-openapi.yml
- filename: telefono-carrier-openapi.yml
  format: yaml
  label: Telefono Carrier Lookup API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/telefono/refs/heads/main/openapi/telefono-carrier-openapi.yml
- filename: telefono-format-openapi.yml
  format: yaml
  label: Telefono Number Formatting API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/telefono/refs/heads/main/openapi/telefono-format-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Per-Invoice
  chargeCategories:
  - Purchase
  pricingCategory: Unverified
description: FinOps shape for the telefono.com slug could not be reconciled; no public pricing or billing surface is documented.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Telefono
  ProviderName: Telefono
  PublisherName: Telefono
  ServiceCategory: Number Intelligence
  ServiceName: Telefono
layout: finops
meters:
- aggregation: sum
  name: unverified_usage
  unit: varies
name: Telefono Finops
provider_name: Telefono
provider_slug: telefono
publisher_name: Telefono
service_category: Number Intelligence
slug: telefono-finops
source_filename: telefono-finops.yml
source_heading: FinOps Profile
source_url: https://www.telefono.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Telefono\nproviderId: telefono\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Carrier Lookup\n  - Data Enrichment\n  - Fraud Prevention\n  - Number Intelligence\n  - Number Verification\n  - Phone Lookup\n  - Phone Validation\n  - Telecommunications\n  - FinOps\n  - FOCUS\ndescription: FinOps shape for the telefono.com slug could not be reconciled; no public pricing or\n  billing surface is documented.\nsources:\n  - https://www.telefono.com/\nnotes: Provider identity is unverified. FOCUS columns capture the slug name only; meters are not\n  reconciled to real billing lines.\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Telefono\nserviceCategory:\
  \ Number Intelligence\nbillingModel:\n  pricingCategory: Unverified\n  billingFrequency: Per-Invoice\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: Telefono\n  ServiceCategory: Number Intelligence\n  ProviderName: Telefono\n  PublisherName: Telefono\n  InvoiceIssuerName: Telefono\n  BillingCurrency: USD\nmeters:\n  - name: unverified_usage\n    unit: varies\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: No public usage-export surface is documented for this slug.\n  - name: Allocation\n    description: Allocation cannot be modeled until a real billing surface is identified.\n  - name: Optimization\n    description: No documented cost levers; this artifact is a placeholder.\n  - name: Accountability\n    description: Accountability cannot be assigned until the provider entry is verified.\nmaintainers:\n  - name: Telefono Team\n    email: api@telefono.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/telefono/refs/heads/main/finops/telefono-finops.yml
sources:
- https://www.telefono.com/
specification: FinOps Framework
tags:
- Carrier Lookup
- Data Enrichment
- Fraud Prevention
- Number Intelligence
- Number Verification
- Phone Lookup
- Phone Validation
- Telecommunications
- FinOps
- FOCUS
---
