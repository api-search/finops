---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: constellation-brands-openapi.yml
  format: yaml
  label: Product Items API
  slug: product
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/constellation-brands/refs/heads/main/openapi/constellation-brands-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Per-Invoice
  chargeCategories:
  - Purchase
  - Adjustment
  pricingCategory: Partner-Bundled
description: 'FOCUS-aligned FinOps for Constellation Brands: partner-distributed product / digital-asset API; access is governed by the partner agreement rather than per-call billing. FinOps applies to internal attribution of partner-API consumption and to commercial counterparty spend, not to a metered API bill.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Constellation Brands, Inc.
  ProviderName: Constellation Brands
  PublisherName: Constellation Brands, Inc.
  ServiceCategory: Beverages / Product Data API
  ServiceName: Constellation Brands API
layout: finops
meters:
- aggregation: sum
  description: Internal-only meter — count of API calls per consuming application for chargeback within the partner organization. Not billed externally by Constellation Brands.
  dimensions:
  - api
  - consumer_app
  - environment
  name: api_calls_internal
  unit: request
- aggregation: sum
  description: Bottle shot / digital-asset downloads served from the partner API
  dimensions:
  - asset_type
  - brand
  name: digital_asset_downloads
  unit: download
name: Constellation Brands Finops
provider_name: Constellation Brands
provider_slug: constellation-brands
publisher_name: Constellation Brands, Inc.
service_category: Beverages / Product Data API
slug: constellation-brands-finops
source_filename: constellation-brands-finops.yml
source_heading: FinOps Profile
source_url: https://dev.cbrands.com
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Constellation Brands\nproviderId: constellation-brands\npublisherName: Constellation Brands, Inc.\nserviceCategory: Beverages / Product Data API\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Beverages\n  - Digital Assets\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps for Constellation Brands: partner-distributed product / digital-asset\n  API; access is governed by the partner agreement rather than per-call billing. FinOps applies to internal\n  attribution of partner-API consumption and to commercial counterparty spend, not to a metered API\n  bill.'\nnotes: Constellation Brands does not publish per-call\
  \ API pricing. This artifact tracks internal-only\n  meters useful for chargeback within consuming organizations.\nsources:\n  - https://dev.cbrands.com\nbillingModel:\n  pricingCategory: Partner-Bundled\n  billingFrequency: Per-Invoice\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Adjustment\nfocusColumns:\n  ServiceName: Constellation Brands API\n  ServiceCategory: Beverages / Product Data API\n  ProviderName: Constellation Brands\n  PublisherName: Constellation Brands, Inc.\n  InvoiceIssuerName: Constellation Brands, Inc.\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: api_calls_internal\n    description: Internal-only meter — count of API calls per consuming application for chargeback within\n      the partner organization. Not billed externally by Constellation Brands.\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - consumer_app\n      - environment\n  - name: digital_asset_downloads\n    description: Bottle\
  \ shot / digital-asset downloads served from the partner API\n    unit: download\n    aggregation: sum\n    dimensions:\n      - asset_type\n      - brand\nprinciples:\n  - name: Visibility\n    description: Track API key usage internally; coordinate with api.support@cbrands.com for partner-side\n      usage reports under the partner agreement.\n  - name: Allocation\n    description: Allocate by consuming product / brand integration via API-key segmentation.\n  - name: Optimization\n    description: Cache product metadata and bottle-shot assets; pull deltas via the items product API\n      rather than full refresh; right-size partner agreement scope at renewal.\n  - name: Accountability\n    description: Trade-marketing / partner-integration teams own consumption against the partner agreement.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/constellation-brands/refs/heads/main/finops/constellation-brands-finops.yml
sources:
- https://dev.cbrands.com
specification: FinOps Framework
tags:
- Beverages
- Digital Assets
- FinOps
- FOCUS
---
