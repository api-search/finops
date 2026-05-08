---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: starwood-hotel-search-openapi.yml
  format: yaml
  label: Hotel Search API
  slug: hotel-search-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/starwood-hotels-and-resorts/refs/heads/main/openapi/starwood-hotel-search-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Per-Contract
  chargeCategories:
  - Purchase
  pricingCategory: Contract
description: Starwood Hotels and Resorts has no standalone metered API surface — the brand is now part of Marriott. There is no public FOCUS-billable line for Starwood-branded API usage; any cost lives in a Marriott partner contract.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Marriott International, Inc.
  ProviderName: Starwood Hotels and Resorts
  PublisherName: Marriott International, Inc.
  ServiceCategory: Hospitality / Hotels
  ServiceName: Starwood Hotels and Resorts
layout: finops
meters:
- aggregation: sum
  description: Placeholder for line items defined in a Marriott / Starwood partner contract.
  name: contracted_engagement
  unit: varies
name: Starwood Hotels And Resorts Finops
provider_name: Starwood Hotels and Resorts
provider_slug: starwood-hotels-and-resorts
publisher_name: Marriott International, Inc.
service_category: Hospitality / Hotels
slug: starwood-hotels-and-resorts-finops
source_filename: starwood-hotels-and-resorts-finops.yml
source_heading: FinOps Profile
source_url: https://www.starwoodhotels.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Starwood Hotels and Resorts\nproviderId: starwood-hotels-and-resorts\npublisherName: Marriott International, Inc.\nserviceCategory: Hospitality / Hotels\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Hospitality\ndescription: Starwood Hotels and Resorts has no standalone metered API surface — the brand is now part\n  of Marriott. There is no public FOCUS-billable line for Starwood-branded API usage; any cost lives\n  in a Marriott partner contract.\nsources:\n  - https://www.starwoodhotels.com/\nnotes: No public Starwood API billing surface exists. Meters and FOCUS values are placeholders pending\n\
  \  a Marriott partner engagement.\nbillingModel:\n  pricingCategory: Contract\n  billingFrequency: Per-Contract\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: Starwood Hotels and Resorts\n  ServiceCategory: Hospitality / Hotels\n  ProviderName: Starwood Hotels and Resorts\n  PublisherName: Marriott International, Inc.\n  InvoiceIssuerName: Marriott International, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: contracted_engagement\n    description: Placeholder for line items defined in a Marriott / Starwood partner contract.\n    unit: varies\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Visibility is whatever Marriott's partner reporting (channel manager / GDS feed) provides;\n      there is no public Starwood usage API.\n  - name: Allocation\n    description: Allocate the partnership cost line in your own ERP — Marriott does not break it down\n      under a Starwood label.\n  - name: Optimization\n    description:\
  \ Optimization happens via contract / channel-mix renegotiation, not pay-as-you-go tuning.\n  - name: Accountability\n    description: A single business owner of the Marriott partnership should own this cost line and renewal.\nmaintainers: []\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/starwood-hotels-and-resorts/refs/heads/main/finops/starwood-hotels-and-resorts-finops.yml
sources:
- https://www.starwoodhotels.com/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Hospitality
---
