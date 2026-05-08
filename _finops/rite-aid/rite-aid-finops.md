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
description: Rite Aid integrations are partner-contract driven; no public billing surface or usage API exists. FinOps shape is placeholder until a partner contract is in place.
focus_columns:
  BillingCurrency: USD
  ProviderName: Rite Aid
  PublisherName: Rite Aid Corporation
  ServiceCategory: Retail / Pharmacy
  ServiceName: Rite Aid Integrations
layout: finops
meters:
- aggregation: sum
  description: Negotiated trading-partner charges
  dimensions:
  - contract
  name: contract_charges
  unit: varies
name: Rite Aid Finops
provider_name: Rite Aid
provider_slug: rite-aid
publisher_name: Rite Aid Corporation
service_category: Retail / Pharmacy
slug: rite-aid-finops
source_filename: rite-aid-finops.yml
source_heading: FinOps Profile
source_url: https://www.riteaid.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Rite Aid\nproviderId: rite-aid\npublisherName: Rite Aid Corporation\nserviceCategory: Retail / Pharmacy\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Pharmacy\n  - Retail\n  - EDI\n  - FinOps\n  - FOCUS\ndescription: >-\n  Rite Aid integrations are partner-contract driven; no public billing surface or usage API\n  exists. FinOps shape is placeholder until a partner contract is in place.\nnotes: >-\n  No published billing model. Integration costs are typically buried in vendor contract terms\n  rather than itemized on a usage invoice.\nsources:\n  - https://www.riteaid.com/\nbillingModel:\n  pricingCategory: Contract-Based\n\
  \  billingFrequency: Per Contract\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: Rite Aid Integrations\n  ServiceCategory: Retail / Pharmacy\n  ProviderName: Rite Aid\n  PublisherName: Rite Aid Corporation\n  BillingCurrency: USD\nmeters:\n  - name: contract_charges\n    description: Negotiated trading-partner charges\n    unit: varies\n    aggregation: sum\n    dimensions:\n      - contract\nprinciples:\n  - name: Visibility\n    description: >-\n      Track Rite Aid integration spend through the vendor master file and AP system; there is\n      no provider-side usage API to consume.\n  - name: Allocation\n    description: >-\n      Allocate Rite Aid vendor charges to the merchandising or pharmacy program that owns the\n      trading-partner relationship.\n  - name: Optimization\n    description: >-\n      Re-negotiate contract terms at renewal; consolidate EDI VAN spend across retail\n      counterparties where feasible.\n  - name: Accountability\n\
  \    description: >-\n      Vendor relations and supply-chain leads own the Rite Aid partner relationship and review\n      contracted terms annually.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/rite-aid/refs/heads/main/finops/rite-aid-finops.yml
sources:
- https://www.riteaid.com/
specification: FinOps Framework
tags:
- Pharmacy
- Retail
- EDI
- FinOps
- FOCUS
---
