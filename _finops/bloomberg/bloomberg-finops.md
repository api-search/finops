---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: blpapi-core.yml
  format: yaml
  label: Bloomberg BLPAPI Core
  slug: bloomberg-blpapi-core
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/bloomberg/refs/heads/main/openapi/blpapi-core.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  - Usage
  - Tax
  - Adjustment
  pricingCategory: Subscription (Seat) + Enterprise Data License
description: 'FOCUS-aligned FinOps for Bloomberg: per-user Terminal seat subscriptions plus contract-negotiated enterprise data feeds (B-PIPE, Data License). Spend is dominated by named-user Terminal seats and per-feed enterprise data licenses.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Bloomberg L.P.
  ProviderName: Bloomberg
  PublisherName: Bloomberg L.P.
  ServiceCategory: Market Data
  ServiceName: Bloomberg
layout: finops
meters:
- aggregation: sum
  dimensions:
  - named_user
  - office
  - cost_center
  name: terminal_seats
  unit: seat-year
- aggregation: sum
  dimensions:
  - service
  - terminal_user
  - application
  name: blpapi_requests
  unit: request
- aggregation: sum
  dimensions:
  - exchange
  - feed
  - application
  name: bpipe_updates
  unit: update
- aggregation: sum
  dimensions:
  - product
  - field
  - exchange
  name: data_license_records
  unit: record
- aggregation: sum
  dimensions:
  - product
  - department
  name: enterprise_module_subscriptions
  unit: month
name: Bloomberg Finops
provider_name: Bloomberg
provider_slug: bloomberg
publisher_name: Bloomberg L.P.
service_category: Market Data / Financial Services
slug: bloomberg-finops
source_filename: bloomberg-finops.yml
source_heading: FinOps Profile
source_url: https://www.bloomberg.com/professional/products/bloomberg-terminal/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Bloomberg\nproviderId: bloomberg\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Market Data\n  - Enterprise\n  - Financial Services\ndescription: 'FOCUS-aligned FinOps for Bloomberg: per-user Terminal seat subscriptions plus\n  contract-negotiated enterprise data feeds (B-PIPE, Data License). Spend is dominated by named-user\n  Terminal seats and per-feed enterprise data licenses.'\nsources:\n  - https://www.bloomberg.com/professional/products/bloomberg-terminal/\n  - https://en.wikipedia.org/wiki/Bloomberg_Terminal\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Bloomberg L.P.\nserviceCategory: Market Data / Financial Services\n\
  billingModel:\n  pricingCategory: Subscription (Seat) + Enterprise Data License\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\n    - Tax\n    - Adjustment\nfocusColumns:\n  ServiceName: Bloomberg\n  ServiceCategory: Market Data\n  ProviderName: Bloomberg\n  PublisherName: Bloomberg L.P.\n  InvoiceIssuerName: Bloomberg L.P.\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: terminal_seats\n    unit: seat-year\n    aggregation: sum\n    dimensions:\n      - named_user\n      - office\n      - cost_center\n  - name: blpapi_requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - service\n      - terminal_user\n      - application\n  - name: bpipe_updates\n    unit: update\n    aggregation: sum\n    dimensions:\n      - exchange\n      - feed\n      - application\n  - name: data_license_records\n    unit: record\n    aggregation: sum\n    dimensions:\n      - product\n      - field\n      - exchange\n\
  \  - name: enterprise_module_subscriptions\n    unit: month\n    aggregation: sum\n    dimensions:\n      - product\n      - department\nprinciples:\n  - name: Visibility\n    description: Use BPS<GO> (Bloomberg Profile Statistics) and the Customer Service portal for\n      seat-level usage; pull WAPI<GO> usage tables to track BDH/BDP daily quota burn against\n      contractual ceilings.\n  - name: Allocation\n    description: Map each Terminal login (BUID) to a cost center / desk; reconcile annual\n      seat-license invoices against the named-user roster.\n  - name: Optimization\n    description: Reclaim inactive seats during the annual renewal window; consolidate B-PIPE\n      symbol subscriptions; favor Bloomberg Anywhere for hoteling instead of dedicated seats; route\n      bulk historical pulls through Data License (EDF) instead of BLPAPI to avoid per-Terminal caps.\n  - name: Accountability\n    description: Designate a Terminal Administrator per legal entity; review the SR<GO>\
  \ Service\n      Reports monthly; run quarterly seat-utilization reviews with the Bloomberg account team.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/bloomberg/refs/heads/main/finops/bloomberg-finops.yml
sources:
- https://www.bloomberg.com/professional/products/bloomberg-terminal/
- https://en.wikipedia.org/wiki/Bloomberg_Terminal
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Market Data
- Enterprise
- Financial Services
---
