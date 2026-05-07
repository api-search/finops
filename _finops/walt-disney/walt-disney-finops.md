---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: walt-disney-disney-api-openapi.yml
  format: yaml
  label: Disney Characters API
  slug: disney-characters-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/walt-disney/refs/heads/main/openapi/walt-disney-disney-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Per-Invoice
  chargeCategories:
  - Purchase
  - Adjustment
  pricingCategory: Custom Contract
description: FinOps view of The Walt Disney Company at the corporate level. Disney does not bill API consumption directly; integration costs and revenues flow through bilateral content-licensing, distribution, and partnership settlements rather than a metered API invoice surface.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: The Walt Disney Company
  ProviderName: The Walt Disney Company
  PublisherName: The Walt Disney Company
  ServiceCategory: Entertainment / Media
  ServiceName: Walt Disney Partnerships
layout: finops
meters:
- aggregation: sum
  description: Negotiated settlement under the bilateral partnership / licensing agreement.
  dimensions:
  - business_segment
  - partner
  name: partnership_settlement
  unit: varies
name: Walt Disney Finops
provider_name: Walt Disney
provider_slug: walt-disney
publisher_name: The Walt Disney Company
service_category: Entertainment / Media
slug: walt-disney-finops
source_filename: walt-disney-finops.yml
source_heading: FinOps Profile
source_url: https://thewaltdisneycompany.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Walt Disney\nproviderId: walt-disney\npublisherName: The Walt Disney Company\nserviceCategory: Entertainment / Media\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Entertainment\n  - Media\n  - Streaming\n  - FinOps\n  - FOCUS\ndescription: FinOps view of The Walt Disney Company at the corporate level.\n  Disney does not bill API consumption directly; integration costs and\n  revenues flow through bilateral content-licensing, distribution, and\n  partnership settlements rather than a metered API invoice surface.\nsources:\n  - https://thewaltdisneycompany.com/\nnotes: No corporate-level API invoice; FOCUS attribution flows through the\n  partnership-settlement\
  \ entity.\nbillingModel:\n  pricingCategory: Custom Contract\n  billingFrequency: Per-Invoice\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Adjustment\nfocusColumns:\n  ServiceName: Walt Disney Partnerships\n  ServiceCategory: Entertainment / Media\n  ProviderName: The Walt Disney Company\n  PublisherName: The Walt Disney Company\n  InvoiceIssuerName: The Walt Disney Company\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: partnership_settlement\n    description: Negotiated settlement under the bilateral partnership /\n      licensing agreement.\n    unit: varies\n    aggregation: sum\n    dimensions:\n      - business_segment\n      - partner\nprinciples:\n  - name: Visibility\n    description: Track partnership-level settlements at the corporate\n      treasury layer; per-API consumption telemetry is partner-side.\n  - name: Allocation\n    description: Allocate partnership cost / revenue to the relevant\n      Disney business segment (Studios,\
  \ Streaming, Parks, ESPN).\n  - name: Optimization\n    description: Optimization happens at the partnership-renegotiation\n      layer; there is no in-flight metered usage to tune.\n  - name: Accountability\n    description: Corporate development / business-segment leadership\n      owns the partnership terms; legal and finance own settlement.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n    url: https://apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/walt-disney/refs/heads/main/finops/walt-disney-finops.yml
sources:
- https://thewaltdisneycompany.com/
specification: FinOps Framework
tags:
- Entertainment
- Media
- Streaming
- FinOps
- FOCUS
---
