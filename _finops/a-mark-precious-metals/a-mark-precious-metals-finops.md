---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: Per-Invoice
  chargeCategories:
  - Purchase
  pricingCategory: Contract
description: A-Mark integrations are settled inside a wholesale-trading agreement; there is no metered API invoice. FinOps mapping is structural only.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: A-Mark Precious Metals, Inc.
  ProviderName: A-Mark Precious Metals
  PublisherName: A-Mark Precious Metals, Inc.
  ServiceCategory: Financial Services / Commodities
  ServiceName: A-Mark Precious Metals
layout: finops
meters:
- aggregation: count
  description: Wholesale dealer relationship — not a metered unit.
  dimensions:
  - dealer
  name: dealer_contract
  unit: contract
name: A Mark Precious Metals Finops
provider_name: A-Mark Precious Metals
provider_slug: a-mark-precious-metals
publisher_name: A-Mark Precious Metals, Inc.
service_category: Financial Services / Commodities
slug: a-mark-precious-metals-finops
source_filename: a-mark-precious-metals-finops.yml
source_heading: FinOps Profile
source_url: https://www.amark.com/services
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: A-Mark Precious Metals\nproviderId: a-mark-precious-metals\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Precious Metals\n  - Trading\n  - Finance\n  - FinOps\n  - FOCUS\ndescription: A-Mark integrations are settled inside a wholesale-trading agreement; there is no metered\n  API invoice. FinOps mapping is structural only.\nnotes: No public developer pricing — placeholder only. Costs flow through metals trading P&L, not a metered\n  API line item.\nsources:\n  - https://www.amark.com/services\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: A-Mark Precious Metals, Inc.\nserviceCategory: Financial Services / Commodities\nbillingModel:\n  pricingCategory:\
  \ Contract\n  billingFrequency: Per-Invoice\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: A-Mark Precious Metals\n  ServiceCategory: Financial Services / Commodities\n  ProviderName: A-Mark Precious Metals\n  PublisherName: A-Mark Precious Metals, Inc.\n  InvoiceIssuerName: A-Mark Precious Metals, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: dealer_contract\n    description: Wholesale dealer relationship — not a metered unit.\n    unit: contract\n    aggregation: count\n    dimensions:\n      - dealer\nprinciples:\n  - name: Visibility\n    description: Track integration cost as part of trading-desk operations and metals procurement spend;\n      A-Mark does not provide a metered usage feed.\n  - name: Allocation\n    description: Allocate integration cost to the trading or treasury function that owns the wholesale\n      relationship.\n  - name: Optimization\n    description: Optimize quote/order flows by batching where the contract allows\
  \ and aligning trading\n      activity with desk hours.\n  - name: Accountability\n    description: Trading operations leadership owns the relationship; IT owns integration runtime. Review\n      transaction volume during quarterly business reviews with A-Mark.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/a-mark-precious-metals/refs/heads/main/finops/a-mark-precious-metals-finops.yml
sources:
- https://www.amark.com/services
specification: FinOps Framework
tags:
- Precious Metals
- Trading
- Finance
- FinOps
- FOCUS
---
