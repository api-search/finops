---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: telefonica-number-verification-openapi.yml
  format: yaml
  label: Telefónica Number Verification API
  slug: number-verification-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/telefonica/refs/heads/main/openapi/telefonica-number-verification-openapi.yml
- filename: telefonica-sim-swap-openapi.yml
  format: yaml
  label: Telefónica SIM Swap API
  slug: sim-swap-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/telefonica/refs/heads/main/openapi/telefonica-sim-swap-openapi.yml
- filename: telefonica-kyc-match-openapi.yml
  format: yaml
  label: Telefónica Know Your Customer Match API
  slug: kyc-match-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/telefonica/refs/heads/main/openapi/telefonica-kyc-match-openapi.yml
- filename: telefonica-location-verification-openapi.yml
  format: yaml
  label: Telefónica Location Verification API
  slug: location-verification-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/telefonica/refs/heads/main/openapi/telefonica-location-verification-openapi.yml
- filename: telefonica-quality-on-demand-openapi.yml
  format: yaml
  label: Telefónica Quality on Demand API
  slug: quality-on-demand-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/telefonica/refs/heads/main/openapi/telefonica-quality-on-demand-openapi.yml
- filename: telefonica-device-roaming-openapi.yml
  format: yaml
  label: Telefónica Device Roaming Status API
  slug: device-roaming-status-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/telefonica/refs/heads/main/openapi/telefonica-device-roaming-openapi.yml
billing_model:
  billingCurrency: EUR
  billingFrequency: Per-Invoice
  chargeCategories:
  - Purchase
  pricingCategory: Partner-Negotiated
description: FOCUS-aligned FinOps shape for Telefónica Open Gateway. Open Gateway production consumption is billed under partner agreements rather than as a self-service consumption product; this artifact captures the publisher identity and a generic per-API-call meter pending visibility into the partner billing surface.
focus_columns:
  BillingCurrency: EUR
  InvoiceIssuerName: Telefónica, S.A.
  ProviderName: Telefónica
  PublisherName: Telefónica, S.A.
  ServiceCategory: Telecommunications / Network APIs
  ServiceName: Telefónica Open Gateway
layout: finops
meters:
- aggregation: sum
  dimensions:
  - api
  - operator
  - country
  name: api_calls
  unit: request
name: Telefonica Finops
provider_name: Telefónica
provider_slug: telefonica
publisher_name: Telefónica, S.A.
service_category: Telecommunications / Network APIs
slug: telefonica-finops
source_filename: telefonica-finops.yml
source_heading: FinOps Profile
source_url: https://opengateway.telefonica.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Telefónica\nproviderId: telefonica\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Telecommunications\n  - Mobile Network\n  - CAMARA\n  - Open Gateway\n  - Authentication\n  - Fraud Prevention\n  - Location Services\n  - FinOps\n  - FOCUS\ndescription: FOCUS-aligned FinOps shape for Telefónica Open Gateway. Open Gateway production\n  consumption is billed under partner agreements rather than as a self-service consumption product;\n  this artifact captures the publisher identity and a generic per-API-call meter pending visibility\n  into the partner billing surface.\nsources:\n  - https://opengateway.telefonica.com/\nnotes: Telefónica does not publish a public consumption price list or usage-export surface for\n  Open Gateway. FOCUS columns capture the publisher identity; the per-call meter is generic until\n  partner-side billing\
  \ detail is reconciled.\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Telefónica, S.A.\nserviceCategory: Telecommunications / Network APIs\nbillingModel:\n  pricingCategory: Partner-Negotiated\n  billingFrequency: Per-Invoice\n  billingCurrency: EUR\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: Telefónica Open Gateway\n  ServiceCategory: Telecommunications / Network APIs\n  ProviderName: Telefónica\n  PublisherName: Telefónica, S.A.\n  InvoiceIssuerName: Telefónica, S.A.\n  BillingCurrency: EUR\nmeters:\n  - name: api_calls\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - operator\n      - country\nprinciples:\n  - name: Visibility\n    description: Sandbox and partner production usage are reported through the Open Gateway\n      developer hub and\
  \ partner reporting; no public Telefónica spend dashboard is exposed for Open\n      Gateway.\n  - name: Allocation\n    description: Allocation is by partner / aggregator, by CAMARA API (Number Verification, SIM\n      Swap, etc.), and by operating-country footprint.\n  - name: Optimization\n    description: Optimization is contractual (partner agreement, country mix, batching); there are\n      no published self-service committed-use discounts.\n  - name: Accountability\n    description: The integrating partner / aggregator is the accountable owner of Open Gateway\n      production spend.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/telefonica/refs/heads/main/finops/telefonica-finops.yml
sources:
- https://opengateway.telefonica.com/
specification: FinOps Framework
tags:
- Telecommunications
- Mobile Network
- CAMARA
- Open Gateway
- Authentication
- Fraud Prevention
- Location Services
- FinOps
- FOCUS
---
