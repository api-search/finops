---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: refinitiv-data-platform-openapi.yml
  format: yaml
  label: Refinitiv Data Platform (RDP) API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/refinitiv/refs/heads/main/openapi/refinitiv-data-platform-openapi.yml
- filename: refinitiv-real-time-websocket-asyncapi.yml
  format: yaml
  label: Refinitiv Real-Time WebSocket API
  slug: ''
  spec_type: AsyncAPI
  url: https://raw.githubusercontent.com/api-evangelist/refinitiv/refs/heads/main/asyncapi/refinitiv-real-time-websocket-asyncapi.yml
- filename: refinitiv-datascope-select-openapi.yml
  format: yaml
  label: LSEG DataScope Select - REST API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/refinitiv/refs/heads/main/openapi/refinitiv-datascope-select-openapi.yml
- filename: refinitiv-world-check-one-openapi.yml
  format: yaml
  label: World-Check One API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/refinitiv/refs/heads/main/openapi/refinitiv-world-check-one-openapi.yml
- filename: refinitiv-qual-id-openapi.yml
  format: yaml
  label: Qual-ID API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/refinitiv/refs/heads/main/openapi/refinitiv-qual-id-openapi.yml
- filename: refinitiv-permid-entity-search-openapi.yml
  format: yaml
  label: PermID Entity Search API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/refinitiv/refs/heads/main/openapi/refinitiv-permid-entity-search-openapi.yml
billing_model:
  billingCurrency: USD (settlement varies)
  billingFrequency: Per-Invoice
  chargeCategories:
  - Purchase
  pricingCategory: Contact Sales
description: FinOps shape for Refinitiv (LSEG) data licensing. Pricing is contract-driven rather than metered self-serve, so meters and FOCUS columns reflect what an LSEG invoice itemizes rather than fabricated request-level meters.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: London Stock Exchange Group plc
  ProviderName: LSEG
  PublisherName: London Stock Exchange Group plc
  ServiceCategory: Market Data
  ServiceName: Refinitiv
layout: finops
meters:
- aggregation: sum
  name: licensed_users
  unit: seat
- aggregation: sum
  name: data_subscription
  unit: month
name: Refinitiv Finops
provider_name: Refinitiv
provider_slug: refinitiv
publisher_name: London Stock Exchange Group plc
service_category: Market Data
slug: refinitiv-finops
source_filename: refinitiv-finops.yml
source_heading: FinOps Profile
source_url: https://developers.lseg.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Refinitiv\nproviderId: refinitiv\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Financial Data\n  - Market Data\n  - LSEG\ndescription: FinOps shape for Refinitiv (LSEG) data licensing. Pricing is contract-driven rather than\n  metered self-serve, so meters and FOCUS columns reflect what an LSEG invoice itemizes rather than fabricated\n  request-level meters.\nsources:\n  - https://developers.lseg.com/\n  - https://www.lseg.com/en/data-analytics/products/eikon-trading-software\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: London Stock Exchange Group plc\nserviceCategory: Market Data\nbillingModel:\n  pricingCategory: Contact\
  \ Sales\n  billingFrequency: Per-Invoice\n  billingCurrency: USD (settlement varies)\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: Refinitiv\n  ServiceCategory: Market Data\n  ProviderName: LSEG\n  PublisherName: London Stock Exchange Group plc\n  InvoiceIssuerName: London Stock Exchange Group plc\n  BillingCurrency: USD\nmeters:\n  - name: licensed_users\n    unit: seat\n    aggregation: sum\n  - name: data_subscription\n    unit: month\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Visibility relies on the LSEG invoice and per-product entitlement reports; there is no\n      cross-product self-serve usage API.\n  - name: Allocation\n    description: Allocate by entitled seat, data set, and redistribution scope per the contract; tag each\n      licensed user to a cost center.\n  - name: Optimization\n    description: Optimization happens at renewal — right-size seats, drop unused data sets, and consolidate\n      contracts under a single\
  \ LSEG enterprise agreement.\n  - name: Accountability\n    description: Owner is the market-data licensing function that holds the LSEG contract; entitlement\n      changes route through that owner.\nnotes: Contract-driven licensing; no public meter list. Generic per-request FOCUS columns and meters\n  removed.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/refinitiv/refs/heads/main/finops/refinitiv-finops.yml
sources:
- https://developers.lseg.com/
- https://www.lseg.com/en/data-analytics/products/eikon-trading-software
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Financial Data
- Market Data
- LSEG
---
