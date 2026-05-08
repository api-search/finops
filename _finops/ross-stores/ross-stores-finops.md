---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: Per Contract
  chargeCategories:
  - Purchase
  pricingCategory: Contract-Based
description: Ross Stores integrations are supplier-contract driven; no public billing surface or usage API exists. FinOps shape is placeholder until a supplier contract is in place.
focus_columns:
  BillingCurrency: USD
  ProviderName: Ross Stores
  PublisherName: Ross Stores, Inc.
  ServiceCategory: Off-Price Retail
  ServiceName: Ross Stores Supplier Integration
layout: finops
meters:
- aggregation: sum
  description: Negotiated supplier or chargeback line items
  dimensions:
  - contract
  - chargeback_type
  name: contract_charges
  unit: varies
name: Ross Stores Finops
provider_name: Ross Stores
provider_slug: ross-stores
publisher_name: Ross Stores, Inc.
service_category: Off-Price Retail / Supplier Integration
slug: ross-stores-finops
source_filename: ross-stores-finops.yml
source_heading: FinOps Profile
source_url: https://www.rossstores.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Ross Stores\nproviderId: ross-stores\npublisherName: Ross Stores, Inc.\nserviceCategory: Off-Price Retail / Supplier Integration\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Retail\n  - Off-Price\n  - Supply Chain\n  - FinOps\n  - FOCUS\ndescription: >-\n  Ross Stores integrations are supplier-contract driven; no public billing surface or usage\n  API exists. FinOps shape is placeholder until a supplier contract is in place.\nnotes: >-\n  No published billing model. Integration costs are absorbed in supplier terms (chargebacks,\n  EDI VAN fees) rather than itemized on a usage invoice.\nsources:\n  - https://www.rossstores.com/\n\
  billingModel:\n  pricingCategory: Contract-Based\n  billingFrequency: Per Contract\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: Ross Stores Supplier Integration\n  ServiceCategory: Off-Price Retail\n  ProviderName: Ross Stores\n  PublisherName: Ross Stores, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: contract_charges\n    description: Negotiated supplier or chargeback line items\n    unit: varies\n    aggregation: sum\n    dimensions:\n      - contract\n      - chargeback_type\nprinciples:\n  - name: Visibility\n    description: >-\n      Track Ross-related spend and chargebacks through the supplier portal and AP system; no\n      provider-side usage telemetry is exposed.\n  - name: Allocation\n    description: >-\n      Allocate Ross supplier costs and chargeback exposure to the merchandising department\n      that owns the buy.\n  - name: Optimization\n    description: >-\n      Reduce chargeback exposure with cleaner ASN/EDI compliance;\
  \ consolidate VAN spend across\n      retail counterparties.\n  - name: Accountability\n    description: >-\n      Wholesale or merchandising leads own the Ross supplier relationship and review\n      chargeback trend monthly.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/ross-stores/refs/heads/main/finops/ross-stores-finops.yml
sources:
- https://www.rossstores.com/
specification: FinOps Framework
tags:
- Retail
- Off-Price
- Supply Chain
- FinOps
- FOCUS
---
