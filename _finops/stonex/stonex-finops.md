---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: stonex-payments-openapi.yml
  format: yaml
  label: StoneX Payments API
  slug: stonex-payments
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/stonex/refs/heads/main/openapi/stonex-payments-openapi.yml
- filename: stonex-clearing-openapi.yml
  format: yaml
  label: StoneX Clearing API
  slug: stonex-clearing
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/stonex/refs/heads/main/openapi/stonex-clearing-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Per-Trade or Monthly Statement
  chargeCategories:
  - Purchase
  - Tax
  - Adjustment
  pricingCategory: Contract-Negotiated Services
description: StoneX bills under institutional agreements (commissions, spreads, FX margins, payments fees, connectivity). This artifact captures publisher and category surface only; meters are placeholders pending a published rate card.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: StoneX Group Inc.
  ProviderName: StoneX
  PublisherName: StoneX Group Inc.
  ServiceCategory: Financial Services
  ServiceName: StoneX
layout: finops
meters:
- aggregation: sum
  description: Negotiated commissions, spreads, FX margins, payments fees, and connectivity charges on the institutional agreement
  name: contract_services
  unit: varies
name: Stonex Finops
provider_name: StoneX
provider_slug: stonex
publisher_name: StoneX Group Inc.
service_category: Financial Services
slug: stonex-finops
source_filename: stonex-finops.yml
source_heading: FinOps Profile
source_url: https://www.stonex.com
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: StoneX\nproviderId: stonex\npublisherName: StoneX Group Inc.\nserviceCategory: Financial Services\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Finance\n  - Trading\n  - Payments\n  - Clearing\ndescription: StoneX bills under institutional agreements (commissions, spreads, FX margins, payments\n  fees, connectivity). This artifact captures publisher and category surface only; meters are placeholders\n  pending a published rate card.\nsources:\n  - https://www.stonex.com\nnotes: 'Reconciliation marked false: StoneX does not publish a public billing/pricing schedule for programmatic\n  access.\
  \ All commercial terms are private to the institutional agreement.'\nbillingModel:\n  pricingCategory: Contract-Negotiated Services\n  billingFrequency: Per-Trade or Monthly Statement\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Tax\n    - Adjustment\nfocusColumns:\n  ServiceName: StoneX\n  ServiceCategory: Financial Services\n  ProviderName: StoneX\n  PublisherName: StoneX Group Inc.\n  InvoiceIssuerName: StoneX Group Inc.\n  BillingCurrency: USD\nmeters:\n  - name: contract_services\n    description: Negotiated commissions, spreads, FX margins, payments fees, and connectivity charges\n      on the institutional agreement\n    unit: varies\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Visibility into StoneX-related spend is via post-trade and statement files plus the\n      assigned relationship manager, not a usage API.\n  - name: Allocation\n    description: Allocation is by trading desk, account, or payments program per the institutional\
  \ agreement.\n  - name: Optimization\n    description: Optimization levers are commercial (renegotiating commission tiers, consolidating venues,\n      managing FX exposure) and operational (batching payment instructions).\n  - name: Accountability\n    description: Account ownership rests with the institution's treasury, trading, or operations team.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/stonex/refs/heads/main/finops/stonex-finops.yml
sources:
- https://www.stonex.com
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Finance
- Trading
- Payments
- Clearing
---
