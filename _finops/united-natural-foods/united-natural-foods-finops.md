---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: unfi-supplier-openapi.yml
  format: yaml
  label: UNFI Harmony Core API
  slug: unfi-harmony-core-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/united-natural-foods/main/openapi/unfi-supplier-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Per-Invoice
  chargeCategories:
  - Purchase
  pricingCategory: Contract
description: UNFI does not expose a metered API billing model. API and EDI usage is bundled with the wholesale customer or supplier relationship; FinOps maps to wholesale spend, not per-call billing.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: United Natural Foods, Inc.
  ProviderName: United Natural Foods
  PublisherName: United Natural Foods, Inc.
  ServiceCategory: Food Distribution
  ServiceName: United Natural Foods
layout: finops
meters:
- aggregation: sum
  description: API / EDI access bundled with the UNFI wholesale customer or supplier agreement.
  name: customer_agreement
  unit: varies
name: United Natural Foods Finops
provider_name: United Natural Foods (UNFI)
provider_slug: united-natural-foods
publisher_name: United Natural Foods, Inc.
service_category: Food Distribution
slug: united-natural-foods-finops
source_filename: united-natural-foods-finops.yml
source_heading: FinOps Profile
source_url: https://www.unfi.com
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: United Natural Foods (UNFI)\nproviderId: united-natural-foods\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Food Distribution\n  - Wholesale\n  - FinOps\n  - FOCUS\n  - B2B\ndescription: UNFI does not expose a metered API billing model. API and EDI usage is bundled with\n  the wholesale customer or supplier relationship; FinOps maps to wholesale spend, not per-call billing.\nsources:\n  - https://www.unfi.com\nnotes: No public usage-based API billing exists. This artifact captures the contractual surface only.\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: United Natural Foods, Inc.\nserviceCategory: Food Distribution\nbillingModel:\n  pricingCategory:\
  \ Contract\n  billingFrequency: Per-Invoice\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: United Natural Foods\n  ServiceCategory: Food Distribution\n  ProviderName: United Natural Foods\n  PublisherName: United Natural Foods, Inc.\n  InvoiceIssuerName: United Natural Foods, Inc.\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: customer_agreement\n    description: API / EDI access bundled with the UNFI wholesale customer or supplier agreement.\n    unit: varies\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: API/EDI consumption is not separately metered. Track integration call volume against\n      the operational metric (orders placed, ASNs received) rather than dollar-per-call.\n  - name: Allocation\n    description: Allocate integration costs to the procurement / supply-chain function that owns\n      the UNFI commercial relationship.\n  - name: Optimization\n    description: Optimize via\
  \ order batching, EDI usage, and supplier collaboration rather than per-call\n      pricing.\n  - name: Accountability\n    description: Assign ownership to the team that manages the UNFI account; FinOps signals come\n      from invoice and SLA review.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/united-natural-foods/refs/heads/main/finops/united-natural-foods-finops.yml
sources:
- https://www.unfi.com
specification: FinOps Framework
tags:
- Food Distribution
- Wholesale
- FinOps
- FOCUS
- B2B
---
