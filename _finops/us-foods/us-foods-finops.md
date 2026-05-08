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
  pricingCategory: Bundled with Distribution Contract
description: 'FinOps shape for US Foods: API access is bundled into the customer/distribution agreement rather than billed as a developer plan. Cost flows through purchase orders for foodservice goods, not through API metering.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: US Foods, Inc.
  ProviderName: US Foods
  PublisherName: US Foods, Inc.
  ServiceCategory: Food Service Distribution
  ServiceName: US Foods
layout: finops
meters:
- aggregation: count
  description: API access provisioned under a customer or integration partner agreement; not metered as a developer billing line
  name: contracted_access
  unit: varies
name: Us Foods Finops
provider_name: US Foods
provider_slug: us-foods
publisher_name: US Foods, Inc.
service_category: Food Service Distribution
slug: us-foods-finops
source_filename: us-foods-finops.yml
source_heading: FinOps Profile
source_url: https://www.usfoods.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: US Foods\nproviderId: us-foods\npublisherName: US Foods, Inc.\nserviceCategory: Food Service Distribution\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Food Service\n  - Distribution\n  - FinOps\n  - FOCUS\ndescription: 'FinOps shape for US Foods: API access is bundled into the customer/distribution agreement rather than billed as a developer plan. Cost flows through purchase orders for foodservice goods, not through API metering.'\nsources:\n  - https://www.usfoods.com/\nnotes: No public usage-based billing surface for US Foods APIs. Costs sit inside the foodservice distribution contract; FinOps observability is not\
  \ exposed to consumers as a separate billing line.\nbillingModel:\n  pricingCategory: Bundled with Distribution Contract\n  billingFrequency: Per-Invoice\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: US Foods\n  ServiceCategory: Food Service Distribution\n  ProviderName: US Foods\n  PublisherName: US Foods, Inc.\n  InvoiceIssuerName: US Foods, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: contracted_access\n    description: API access provisioned under a customer or integration partner agreement; not metered as a developer billing line\n    unit: varies\n    aggregation: count\nprinciples:\n  - name: Visibility\n    description: API usage is not exposed via a public usage API; integration partners must coordinate with their US Foods account team for any required reporting.\n  - name: Allocation\n    description: Costs are allocated through the underlying distribution invoice (goods + services), not via API meters.\n  - name: Optimization\n\
  \    description: Optimization happens at the procurement and integration design level (batching orders, EDI cadence) rather than via per-call cost levers.\n  - name: Accountability\n    description: Owned by the customer's procurement/operations function and the integration partner managing the EDI / API connection.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/us-foods/refs/heads/main/finops/us-foods-finops.yml
sources:
- https://www.usfoods.com/
specification: FinOps Framework
tags:
- Food Service
- Distribution
- FinOps
- FOCUS
---
