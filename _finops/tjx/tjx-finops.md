---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: N/A
  chargeCategories: []
  pricingCategory: Not Applicable
description: 'FOCUS-aligned FinOps placeholder for TJX Companies: an off-price retail holding company with no public developer program or vendor-published rate card.'
focus_columns:
  BillingCurrency: USD
  ProviderName: TJX Companies
  PublisherName: The TJX Companies, Inc.
  ServiceCategory: Retail
  ServiceName: TJX Companies
layout: finops
meters:
- aggregation: sum
  dimensions:
  - vendor
  - banner
  name: vendor_portal_transactions
  unit: varies
name: Tjx Finops
provider_name: TJX Companies
provider_slug: tjx
publisher_name: The TJX Companies, Inc.
service_category: Retail
slug: tjx-finops
source_filename: tjx-finops.yml
source_heading: FinOps Profile
source_url: https://www.tjx.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: TJX Companies\nproviderId: tjx\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Retail\n  - Off-Price\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps placeholder for TJX Companies: an off-price retail holding company\n  with no public developer program or vendor-published rate card.'\nsources:\n  - https://www.tjx.com/\n  - https://focus.finops.org/focus-specification/v1-3/\nnotes: TJX is the consumer of vendor APIs, not a publisher of them. There is no TJX developer invoice\n  to model; FinOps shape is a placeholder until any internal vendor-portal surface is documented externally.\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: The TJX\
  \ Companies, Inc.\nserviceCategory: Retail\nbillingModel:\n  pricingCategory: Not Applicable\n  billingFrequency: N/A\n  billingCurrency: USD\n  chargeCategories: []\nfocusColumns:\n  ServiceName: TJX Companies\n  ServiceCategory: Retail\n  ProviderName: TJX Companies\n  PublisherName: The TJX Companies, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: vendor_portal_transactions\n    unit: varies\n    aggregation: sum\n    dimensions:\n      - vendor\n      - banner\nprinciples:\n  - name: Visibility\n    description: TJX publishes no developer telemetry; visibility is internal vendor-portal reporting,\n      not a vendor-issued usage API.\n  - name: Allocation\n    description: Vendor and EDI integration costs land on the supply-chain or merchandising P&L for the\n      relevant banner (T.J. Maxx, Marshalls, HomeGoods, etc.).\n  - name: Optimization\n    description: Optimization is at the supplier-integration design level (EDI batch sizing, catalog\n      sync cadence) rather than against\
  \ any public API rate card.\n  - name: Accountability\n    description: TJX IT and merchandising leadership owns vendor integration spend; there is no external\n      developer billing relationship.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/tjx/refs/heads/main/finops/tjx-finops.yml
sources:
- https://www.tjx.com/
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Retail
- Off-Price
- FinOps
- FOCUS
---
