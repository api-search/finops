---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: realtor-connections-plus-asyncapi.yml
  format: yaml
  label: Realtor.com Connections Plus API
  slug: connections-plus-api
  spec_type: AsyncAPI
  url: https://raw.githubusercontent.com/api-evangelist/realtor/refs/heads/main/asyncapi/realtor-connections-plus-asyncapi.yml
- filename: realtor-lead-delivery-asyncapi.yml
  format: yaml
  label: Realtor.com Lead Delivery API
  slug: lead-delivery-api
  spec_type: AsyncAPI
  url: https://raw.githubusercontent.com/api-evangelist/realtor/refs/heads/main/asyncapi/realtor-lead-delivery-asyncapi.yml
- filename: realtor-property-data-openapi.yml
  format: yaml
  label: Realtor.com Property Data API
  slug: property-data-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/realtor/refs/heads/main/openapi/realtor-property-data-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  pricingCategory: Contract
description: FOCUS-aligned FinOps framing for realtor.com data partnerships. No public usage meter or billing API is documented; commercial terms are negotiated.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Move, Inc.
  ProviderName: Realtor.com
  PublisherName: Move, Inc.
  ServiceCategory: Real Estate Data
  ServiceName: Realtor.com Data API
layout: finops
meters:
- aggregation: sum
  description: Annual data-partnership fee with Move, Inc.
  name: partnership_contract
  unit: contract
name: Realtor Finops
provider_name: realtor
provider_slug: realtor
publisher_name: Move, Inc.
service_category: Real Estate Data
slug: realtor-finops
source_filename: realtor-finops.yml
source_heading: FinOps Profile
source_url: https://www.realtor.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: realtor\nproviderId: realtor\npublisherName: Move, Inc.\nserviceCategory: Real Estate Data\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Real Estate\n  - Listings\n  - FinOps\n  - FOCUS\ndescription: FOCUS-aligned FinOps framing for realtor.com data partnerships. No public usage\n  meter or billing API is documented; commercial terms are negotiated.\nsources:\n  - https://www.realtor.com/\nnotes: realtor.com developer/billing pages are gated; meters and FOCUS columns reflect a contract-level\n  shape rather than a fetched billing surface.\nbillingModel:\n  pricingCategory: Contract\n  billingFrequency: Annual\n  billingCurrency:\
  \ USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: Realtor.com Data API\n  ServiceCategory: Real Estate Data\n  ProviderName: Realtor.com\n  PublisherName: Move, Inc.\n  InvoiceIssuerName: Move, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: partnership_contract\n    description: Annual data-partnership fee with Move, Inc.\n    unit: contract\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Spend is invoiced at contract level; any usage telemetry is exchanged bilaterally\n      under the partnership agreement.\n  - name: Allocation\n    description: Allocate against the consuming line-of-business cost center; per-call attribution\n      is not exposed.\n  - name: Optimization\n    description: Renegotiate scope, geographic coverage, and refresh frequency at contract renewal.\n  - name: Accountability\n    description: The product team consuming listing data co-owns the contract with procurement.\nmaintainers:\n  - FN: Kin Lane\n    email:\
  \ kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/realtor/refs/heads/main/finops/realtor-finops.yml
sources:
- https://www.realtor.com/
specification: FinOps Framework
tags:
- Real Estate
- Listings
- FinOps
- FOCUS
---
