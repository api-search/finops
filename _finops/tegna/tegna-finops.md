---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: tegna-audience-one-openapi.yml
  format: yaml
  label: TEGNA AudienceOne API
  slug: audience-one-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/tegna/refs/heads/main/openapi/tegna-audience-one-openapi.yml
- filename: tegna-premion-openapi.yml
  format: yaml
  label: TEGNA Premion OTT Advertising API
  slug: premion-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/tegna/refs/heads/main/openapi/tegna-premion-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Per-Invoice
  chargeCategories:
  - Purchase
  pricingCategory: Contract / Insertion Order
description: FOCUS-aligned FinOps shape for TEGNA's advertising surface. TEGNA bills advertisers via insertion orders and programmatic deal settlements rather than as developer API consumption, so meters describe ad-impression delivery rather than API call cost.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: TEGNA Inc.
  ProviderName: TEGNA
  PublisherName: TEGNA Inc.
  ServiceCategory: Media / Advertising
  ServiceName: TEGNA Advertising
layout: finops
meters:
- aggregation: sum
  dimensions:
  - station
  - daypart
  - audience
  - campaign
  name: ad_impressions
  unit: impression
- aggregation: sum
  dimensions:
  - campaign
  - product_line
  name: media_spend
  unit: USD
name: Tegna Finops
provider_name: TEGNA
provider_slug: tegna
publisher_name: TEGNA Inc.
service_category: Media / Advertising
slug: tegna-finops
source_filename: tegna-finops.yml
source_heading: FinOps Profile
source_url: https://www.tegna.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: TEGNA\nproviderId: tegna\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Broadcasting\n  - Media\n  - Television\n  - Digital Advertising\n  - OTT\n  - CTV\n  - Fortune 500\n  - FinOps\n  - FOCUS\ndescription: FOCUS-aligned FinOps shape for TEGNA's advertising surface. TEGNA bills advertisers\n  via insertion orders and programmatic deal settlements rather than as developer API consumption,\n  so meters describe ad-impression delivery rather than API call cost.\nsources:\n  - https://www.tegna.com/\n  - https://www.premion.com/\nnotes: TEGNA does not operate a developer-billed API product. There is no published consumption\n  price list or usage-export surface to reconcile to FOCUS columns. The meters below describe the\n  underlying media-buy lines (impressions, GRPs) rather than API requests.\nalignedWith:\n  framework: FinOps Foundation\
  \ Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: TEGNA Inc.\nserviceCategory: Media / Advertising\nbillingModel:\n  pricingCategory: Contract / Insertion Order\n  billingFrequency: Per-Invoice\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: TEGNA Advertising\n  ServiceCategory: Media / Advertising\n  ProviderName: TEGNA\n  PublisherName: TEGNA Inc.\n  InvoiceIssuerName: TEGNA Inc.\n  BillingCurrency: USD\nmeters:\n  - name: ad_impressions\n    unit: impression\n    aggregation: sum\n    dimensions:\n      - station\n      - daypart\n      - audience\n      - campaign\n  - name: media_spend\n    unit: USD\n    aggregation: sum\n    dimensions:\n      - campaign\n      - product_line\nprinciples:\n  - name: Visibility\n    description: Campaign delivery and pacing are reported through TEGNA's ad-ops and Premion\n\
  \      reporting; there is no public developer usage dashboard.\n  - name: Allocation\n    description: Spend is allocated by advertiser, agency, campaign, and product line (broadcast,\n      Premion OTT/CTV, AudienceOne).\n  - name: Optimization\n    description: Optimization is editorial / media-mix (daypart, audience targeting, deal type)\n      rather than API-cost driven.\n  - name: Accountability\n    description: The advertiser / agency is the accountable owner of the insertion order or\n      programmatic deal.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/tegna/refs/heads/main/finops/tegna-finops.yml
sources:
- https://www.tegna.com/
- https://www.premion.com/
specification: FinOps Framework
tags:
- Broadcasting
- Media
- Television
- Digital Advertising
- OTT
- CTV
- Fortune 500
- FinOps
- FOCUS
---
