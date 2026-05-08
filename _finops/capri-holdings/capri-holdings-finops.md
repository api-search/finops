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
  - Adjustment
  pricingCategory: Custom Partner Agreement
description: 'FOCUS-aligned FinOps for Capri Holdings: bilateral retail/luxury partner integrations rather than a metered public API; all billing is contract-based.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Capri Holdings Limited
  ProviderName: Capri Holdings
  PublisherName: Capri Holdings Limited
  ServiceCategory: Retail / Luxury Brand Integration
  ServiceName: Capri Holdings Partner Integration
layout: finops
meters:
- aggregation: sum
  dimensions:
  - partner
  - brand
  name: contract_fee
  unit: month
- aggregation: sum
  name: integration_volume
  unit: varies
name: Capri Holdings Finops
provider_name: Capri Holdings
provider_slug: capri-holdings
publisher_name: Capri Holdings Limited
service_category: Retail / Luxury Brand Integration
slug: capri-holdings-finops
source_filename: capri-holdings-finops.yml
source_heading: FinOps Profile
source_url: https://www.capriholdings.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Capri Holdings\nproviderId: capri-holdings\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Retail\n  - Luxury\n  - Fashion\ndescription: 'FOCUS-aligned FinOps for Capri Holdings: bilateral retail/luxury partner integrations rather\n  than a metered public API; all billing is contract-based.'\nnotes: Capri Holdings does not publish a public API billing surface. FinOps mapping is provisional pending\n  partner-contract reconciliation.\nsources:\n  - https://www.capriholdings.com/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Capri Holdings Limited\nserviceCategory: Retail / Luxury Brand Integration\nbillingModel:\n  pricingCategory:\
  \ Custom Partner Agreement\n  billingFrequency: Per-Invoice\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Adjustment\nfocusColumns:\n  ServiceName: Capri Holdings Partner Integration\n  ServiceCategory: Retail / Luxury Brand Integration\n  ProviderName: Capri Holdings\n  PublisherName: Capri Holdings Limited\n  InvoiceIssuerName: Capri Holdings Limited\n  BillingCurrency: USD\nmeters:\n  - name: contract_fee\n    unit: month\n    aggregation: sum\n    dimensions:\n      - partner\n      - brand\n  - name: integration_volume\n    unit: varies\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Visibility into billing depends on partner contract reporting; no public usage telemetry\n      is exposed.\n  - name: Allocation\n    description: Allocate by partnership and by brand (Versace, Jimmy Choo, Michael Kors) where contracts\n      are brand-scoped.\n  - name: Optimization\n    description: Renegotiate volume tiers at renewal; align integration\
  \ scope to brand omnichannel priorities.\n  - name: Accountability\n    description: Partnership owner holds budget; quarterly business reviews with Capri Holdings counterparts\n      are typical.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/capri-holdings/refs/heads/main/finops/capri-holdings-finops.yml
sources:
- https://www.capriholdings.com/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Retail
- Luxury
- Fashion
---
