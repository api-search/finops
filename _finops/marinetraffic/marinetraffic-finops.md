---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: marinetraffic-ais-openapi.yml
  format: yaml
  label: MarineTraffic AIS Vessel Tracking API
  slug: marinetraffic-ais-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/marinetraffic/refs/heads/main/openapi/marinetraffic-ais-openapi.yml
billing_model:
  billingCurrency: USD (settlement varies)
  billingFrequency: Annual / Per-Invoice
  chargeCategories:
  - Purchase
  - Usage
  - Tax
  - Adjustment
  pricingCategory: Prepaid Credit Pack + Contract
description: 'FOCUS-aligned FinOps shape for MarineTraffic (Kpler): credit-pack and contract-priced maritime data API where consumption is allocated through API-key attribution and credit drawdown rather than metered transaction billing.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Kpler Holding SA
  PricingCategory: Committed
  ProviderName: MarineTraffic
  PublisherName: Kpler Holding SA
  ServiceCategory: Maritime Data API
  ServiceName: MarineTraffic API
layout: finops
meters:
- aggregation: sum
  description: Prepaid credits drawn down per call; per-endpoint credit cost varies (PS01, VI01, EV01, etc.).
  dimensions:
  - endpoint
  - api_key
  - vessel_or_area
  name: api_credits
  unit: credit
- aggregation: max
  description: Per-vessel or per-fleet subscription used for tracked vessels and historical access.
  dimensions:
  - imo
  - mmsi
  - account
  name: vessel_subscriptions
  unit: vessel-month
- aggregation: max
  description: Negotiated bulk / streaming data feed (AIS satellite + terrestrial), priced per contract.
  dimensions:
  - feed_type
  - region
  name: data_feed
  unit: month
name: Marinetraffic Finops
provider_name: MarineTraffic
provider_slug: marinetraffic
publisher_name: Kpler Holding SA (MarineTraffic)
service_category: Maritime Data API
slug: marinetraffic-finops
source_filename: marinetraffic-finops.yml
source_heading: FinOps Profile
source_url: https://www.kpler.com/product/maritime/data-services
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: MarineTraffic\nproviderId: marinetraffic\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - AIS\n  - Maritime\n  - Shipping\n  - Vessel Tracking\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps shape for MarineTraffic (Kpler): credit-pack and contract-priced\n  maritime data API where consumption is allocated through API-key attribution and credit drawdown rather\n  than metered transaction billing.'\nnotes: |\n  Public pricing is not available; meters and FOCUS columns reflect the credit-based model historically\n  used by MarineTraffic and continued under Kpler. Replace 'varies' meter pricing once a quote is obtained.\nsources:\n  - https://www.kpler.com/product/maritime/data-services\n  - https://servicedocs.marinetraffic.com/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n\
  \  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Kpler Holding SA (MarineTraffic)\nserviceCategory: Maritime Data API\nbillingModel:\n  pricingCategory: Prepaid Credit Pack + Contract\n  billingFrequency: Annual / Per-Invoice\n  billingCurrency: USD (settlement varies)\n  chargeCategories:\n    - Purchase\n    - Usage\n    - Tax\n    - Adjustment\nfocusColumns:\n  ServiceName: MarineTraffic API\n  ServiceCategory: Maritime Data API\n  ProviderName: MarineTraffic\n  PublisherName: Kpler Holding SA\n  InvoiceIssuerName: Kpler Holding SA\n  BillingCurrency: USD\n  ChargeCategory: Purchase\n  PricingCategory: Committed\nmeters:\n  - name: api_credits\n    description: Prepaid credits drawn down per call; per-endpoint credit cost varies (PS01, VI01, EV01,\n      etc.).\n    unit: credit\n    aggregation: sum\n    dimensions:\n      - endpoint\n      - api_key\n      - vessel_or_area\n  - name: vessel_subscriptions\n\
  \    description: Per-vessel or per-fleet subscription used for tracked vessels and historical access.\n    unit: vessel-month\n    aggregation: max\n    dimensions:\n      - imo\n      - mmsi\n      - account\n  - name: data_feed\n    description: Negotiated bulk / streaming data feed (AIS satellite + terrestrial), priced per contract.\n    unit: month\n    aggregation: max\n    dimensions:\n      - feed_type\n      - region\nprinciples:\n  - name: Visibility\n    description: Consumption is visible through the customer's MarineTraffic / Kpler account dashboard\n      (credit balance, per-endpoint usage). There is no public usage API at this time; export usage CSVs\n      from the account portal.\n  - name: Allocation\n    description: Allocate by API key per consuming team or product; tag downstream queries with vessel,\n      voyage, or area-of-interest identifiers to support per-asset cost attribution.\n  - name: Optimization\n    description: Match endpoint polling cadence to the\
  \ underlying refresh frequency, prefer event endpoints\n      (port calls, bunkering) over polling positions, and cache vessel-static data (Ship Database) to\n      avoid redundant credit consumption.\n  - name: Accountability\n    description: Designate a credit-pack owner who monitors burn rate against the prepaid balance and\n      negotiates renewal volume / discounts before contract anniversary.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/marinetraffic/refs/heads/main/finops/marinetraffic-finops.yml
sources:
- https://www.kpler.com/product/maritime/data-services
- https://servicedocs.marinetraffic.com/
specification: FinOps Framework
tags:
- AIS
- Maritime
- Shipping
- Vessel Tracking
- FinOps
- FOCUS
---
