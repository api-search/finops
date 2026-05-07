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
description: A. Schulman / LyondellBasell APS integrations settle through commercial customer/distributor agreements, not a metered API invoice. FinOps mapping is structural only.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: LyondellBasell Industries N.V.
  ProviderName: A. Schulman
  PublisherName: LyondellBasell Industries N.V.
  ServiceCategory: Industrial / Chemicals
  ServiceName: A. Schulman (LyondellBasell APS)
layout: finops
meters:
- aggregation: count
  description: Customer / distributor relationship — not a metered unit.
  dimensions:
  - customer
  name: customer_contract
  unit: contract
name: A Schulman Finops
provider_name: A. Schulman
provider_slug: a-schulman
publisher_name: LyondellBasell Industries N.V.
service_category: Industrial / Chemicals
slug: a-schulman-finops
source_filename: a-schulman-finops.yml
source_heading: FinOps Profile
source_url: https://www.lyondellbasell.com
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: A. Schulman\nproviderId: a-schulman\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Plastics\n  - Polymers\n  - Manufacturing\n  - FinOps\n  - FOCUS\ndescription: A. Schulman / LyondellBasell APS integrations settle through commercial customer/distributor\n  agreements, not a metered API invoice. FinOps mapping is structural only.\nnotes: No public developer pricing — placeholder only. Costs flow through goods/services pricing, not\n  a metered API line item.\nsources:\n  - https://www.lyondellbasell.com\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: LyondellBasell Industries N.V.\nserviceCategory: Industrial / Chemicals\nbillingModel:\n  pricingCategory:\
  \ Contract\n  billingFrequency: Per-Invoice\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: A. Schulman (LyondellBasell APS)\n  ServiceCategory: Industrial / Chemicals\n  ProviderName: A. Schulman\n  PublisherName: LyondellBasell Industries N.V.\n  InvoiceIssuerName: LyondellBasell Industries N.V.\n  BillingCurrency: USD\nmeters:\n  - name: customer_contract\n    description: Customer / distributor relationship — not a metered unit.\n    unit: contract\n    aggregation: count\n    dimensions:\n      - customer\nprinciples:\n  - name: Visibility\n    description: Track integration cost as part of procurement / supply-chain spend; LyondellBasell does\n      not provide a metered usage feed for catalog or order APIs.\n  - name: Allocation\n    description: Allocate integration cost to the procurement function or product line that consumes the\n      polymer catalog.\n  - name: Optimization\n    description: Optimize order/catalog calls by batching\
  \ and caching catalog data per the customer agreement.\n  - name: Accountability\n    description: Procurement leadership owns the relationship; IT owns integration runtime. Review activity\n      against contract terms during quarterly business reviews.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/a-schulman/refs/heads/main/finops/a-schulman-finops.yml
sources:
- https://www.lyondellbasell.com
specification: FinOps Framework
tags:
- Plastics
- Polymers
- Manufacturing
- FinOps
- FOCUS
---
