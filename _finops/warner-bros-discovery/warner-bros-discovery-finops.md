---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: warner-bros-discovery-content-partner-openapi.yml
  format: yaml
  label: Warner Bros. Discovery Content Partner API
  slug: wbd-content-partner-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/warner-bros-discovery/refs/heads/main/openapi/warner-bros-discovery-content-partner-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Per-Invoice
  chargeCategories:
  - Purchase
  - Adjustment
  pricingCategory: Custom Contract
description: FinOps view of Warner Bros. Discovery at the corporate level. WBD does not bill API consumption; integration costs and revenues flow through content-licensing, distribution, and partnership settlements rather than a metered API invoice surface.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Warner Bros. Discovery, Inc.
  ProviderName: Warner Bros. Discovery
  PublisherName: Warner Bros. Discovery, Inc.
  ServiceCategory: Entertainment / Media
  ServiceName: Warner Bros. Discovery Partnerships
layout: finops
meters:
- aggregation: sum
  description: Negotiated settlement under the bilateral partnership / licensing agreement.
  dimensions:
  - brand
  - partner
  name: partnership_settlement
  unit: varies
name: Warner Bros Discovery Finops
provider_name: Warner Bros. Discovery
provider_slug: warner-bros-discovery
publisher_name: Warner Bros. Discovery, Inc.
service_category: Entertainment / Media
slug: warner-bros-discovery-finops
source_filename: warner-bros-discovery-finops.yml
source_heading: FinOps Profile
source_url: https://www.wbd.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Warner Bros. Discovery\nproviderId: warner-bros-discovery\npublisherName: Warner Bros. Discovery, Inc.\nserviceCategory: Entertainment / Media\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Entertainment\n  - Media\n  - Streaming\n  - FinOps\n  - FOCUS\ndescription: FinOps view of Warner Bros. Discovery at the corporate level.\n  WBD does not bill API consumption; integration costs and revenues flow\n  through content-licensing, distribution, and partnership settlements\n  rather than a metered API invoice surface.\nsources:\n  - https://www.wbd.com/\nnotes: No corporate-level API invoice; FOCUS attribution flows through the\n  partnership-settlement entity.\n\
  billingModel:\n  pricingCategory: Custom Contract\n  billingFrequency: Per-Invoice\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Adjustment\nfocusColumns:\n  ServiceName: Warner Bros. Discovery Partnerships\n  ServiceCategory: Entertainment / Media\n  ProviderName: Warner Bros. Discovery\n  PublisherName: Warner Bros. Discovery, Inc.\n  InvoiceIssuerName: Warner Bros. Discovery, Inc.\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: partnership_settlement\n    description: Negotiated settlement under the bilateral partnership /\n      licensing agreement.\n    unit: varies\n    aggregation: sum\n    dimensions:\n      - brand\n      - partner\nprinciples:\n  - name: Visibility\n    description: Track partnership-level settlements at the corporate\n      treasury layer; per-API consumption telemetry is partner-side.\n  - name: Allocation\n    description: Allocate partnership cost / revenue to the relevant WBD\n      brand or business unit (Max,\
  \ CNN, Studios, DC).\n  - name: Optimization\n    description: Optimization happens at partnership renegotiation; there\n      is no in-flight metered usage to tune.\n  - name: Accountability\n    description: Corporate development and brand leadership own\n      partnership terms; legal and finance own settlement.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n    url: https://apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/warner-bros-discovery/refs/heads/main/finops/warner-bros-discovery-finops.yml
sources:
- https://www.wbd.com/
specification: FinOps Framework
tags:
- Entertainment
- Media
- Streaming
- FinOps
- FOCUS
---
