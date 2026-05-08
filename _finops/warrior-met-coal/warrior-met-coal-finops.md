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
  pricingCategory: Commodity Supply Contract
description: FinOps view of Warrior Met Coal at the corporate level. There is no API consumption surface; commodity-supply costs flow through bilateral metallurgical-coal supply contracts and are out-of-scope of software FinOps.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Warrior Met Coal, Inc.
  ProviderName: Warrior Met Coal
  PublisherName: Warrior Met Coal, Inc.
  ServiceCategory: Mining / Metallurgical Coal
  ServiceName: Warrior Met Coal Supply
layout: finops
meters:
- aggregation: sum
  description: Metallurgical coal delivered under the bilateral supply contract (out-of-scope for software FinOps; included to give the FOCUS row a unit of measure).
  dimensions:
  - grade
  - port
  name: coal_tonnage
  unit: ton
name: Warrior Met Coal Finops
provider_name: Warrior Met Coal
provider_slug: warrior-met-coal
publisher_name: Warrior Met Coal, Inc.
service_category: Mining / Metallurgical Coal
slug: warrior-met-coal-finops
source_filename: warrior-met-coal-finops.yml
source_heading: FinOps Profile
source_url: https://www.warriormetcoal.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Warrior Met Coal\nproviderId: warrior-met-coal\npublisherName: Warrior Met Coal, Inc.\nserviceCategory: Mining / Metallurgical Coal\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Mining\n  - Coal\n  - FinOps\n  - FOCUS\ndescription: FinOps view of Warrior Met Coal at the corporate level. There\n  is no API consumption surface; commodity-supply costs flow through\n  bilateral metallurgical-coal supply contracts and are out-of-scope of\n  software FinOps.\nsources:\n  - https://www.warriormetcoal.com/\nnotes: No API invoice surface. FOCUS attribution is not applicable to a\n  commodity supplier.\nbillingModel:\n  pricingCategory: Commodity Supply Contract\n  billingFrequency:\
  \ Per-Invoice\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: Warrior Met Coal Supply\n  ServiceCategory: Mining / Metallurgical Coal\n  ProviderName: Warrior Met Coal\n  PublisherName: Warrior Met Coal, Inc.\n  InvoiceIssuerName: Warrior Met Coal, Inc.\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: coal_tonnage\n    description: Metallurgical coal delivered under the bilateral supply\n      contract (out-of-scope for software FinOps; included to give the\n      FOCUS row a unit of measure).\n    unit: ton\n    aggregation: sum\n    dimensions:\n      - grade\n      - port\nprinciples:\n  - name: Visibility\n    description: Not applicable - commodity-supply settlement is observed\n      via the supply contract, not a software billing API.\n  - name: Allocation\n    description: Not applicable to software FinOps; coal-supply cost is\n      allocated by the buyer's metallurgical operations.\n  - name: Optimization\n  \
  \  description: Not applicable to software FinOps.\n  - name: Accountability\n    description: Not applicable to software FinOps; supply contract is\n      owned by the buyer's procurement team.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n    url: https://apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/warrior-met-coal/refs/heads/main/finops/warrior-met-coal-finops.yml
sources:
- https://www.warriormetcoal.com/
specification: FinOps Framework
tags:
- Mining
- Coal
- FinOps
- FOCUS
---
