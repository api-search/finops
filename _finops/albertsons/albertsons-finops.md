---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: albertsons-retail-media-api-openapi.yml
  format: yaml
  label: Albertsons Media Collective API
  slug: retail-media-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/albertsons/refs/heads/main/openapi/albertsons-retail-media-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  - Adjustment
  pricingCategory: Subscription
description: 'FOCUS-aligned FinOps shell for Albertsons APIs: commercial surface is the Albertsons Media Collective plus CPG-partner agreements. No public meter rates; reconcile against the negotiated agreement.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Albertsons Companies, Inc.
  ProviderName: Albertsons
  PublisherName: Albertsons Companies, Inc.
  ServiceCategory: Retail Media
  ServiceName: Albertsons Partner APIs
layout: finops
meters:
- aggregation: sum
  description: Annual media-spend commitment for retail-media campaigns
  dimensions:
  - campaign
  - brand
  name: media_spend_commit
  unit: USD
- aggregation: sum
  description: API call volume for analytics / campaign / data-collaboration endpoints (where contractually metered)
  dimensions:
  - api
  - partner
  name: api_calls
  unit: request
name: Albertsons Finops
provider_name: albertsons
provider_slug: albertsons
publisher_name: Albertsons Companies, Inc.
service_category: Retail Media
slug: albertsons-finops
source_filename: albertsons-finops.yml
source_heading: FinOps Profile
source_url: https://www.albertsons.com
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: albertsons\nproviderId: albertsons\npublisherName: Albertsons Companies, Inc.\nserviceCategory: Retail Media\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Grocery\n  - Retail\n  - Retail Media\n  - Advertising\n  - Pharmacy\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps shell for Albertsons APIs: commercial surface is the Albertsons Media\n  Collective plus CPG-partner agreements. No public meter rates; reconcile against the negotiated agreement.'\nsources:\n  - https://www.albertsons.com\n  - https://www.albertsonsmediacollective.com\n  - https://focus.finops.org/focus-specification/v1-3/\nbillingModel:\n\
  \  pricingCategory: Subscription\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Adjustment\nfocusColumns:\n  ServiceName: Albertsons Partner APIs\n  ServiceCategory: Retail Media\n  ProviderName: Albertsons\n  PublisherName: Albertsons Companies, Inc.\n  InvoiceIssuerName: Albertsons Companies, Inc.\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: media_spend_commit\n    description: Annual media-spend commitment for retail-media campaigns\n    unit: USD\n    aggregation: sum\n    dimensions:\n      - campaign\n      - brand\n  - name: api_calls\n    description: API call volume for analytics / campaign / data-collaboration endpoints (where contractually\n      metered)\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - partner\nprinciples:\n  - name: Visibility\n    description: Track Media Collective spend and campaign performance via Albertsons partner reporting;\n      tie API consumption\
  \ to specific campaigns or data-collaboration projects.\n  - name: Allocation\n    description: Allocate media spend and API integration costs across brands and product lines.\n  - name: Optimization\n    description: Right-size media spend and integration footprint at annual renewal; consolidate underused\n      campaigns.\n  - name: Accountability\n    description: Owned by retail-media / shopper-marketing leads on the partner side; reviewed against\n      campaign ROAS and category sell-through.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/albertsons/refs/heads/main/finops/albertsons-finops.yml
sources:
- https://www.albertsons.com
- https://www.albertsonsmediacollective.com
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Grocery
- Retail
- Retail Media
- Advertising
- Pharmacy
- FinOps
- FOCUS
---
