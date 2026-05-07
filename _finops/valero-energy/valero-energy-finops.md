---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: Per-Contract
  chargeCategories:
  - Purchase
  pricingCategory: Bundled with Commercial Contract
description: 'FinOps shape for Valero Energy: there is no developer-billed API surface. Trading-partner and commercial customer integrations live inside private B2B contracts; cost flows through the underlying commodity transactions, not API metering.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Valero Energy Corporation
  ProviderName: Valero Energy
  PublisherName: Valero Energy Corporation
  ServiceCategory: Energy
  ServiceName: Valero Energy
layout: finops
meters:
- aggregation: count
  description: API/EDI access provisioned under a trading-partner or customer agreement; not metered as a developer billing line
  name: contracted_access
  unit: varies
name: Valero Energy Finops
provider_name: Valero Energy
provider_slug: valero-energy
publisher_name: Valero Energy Corporation
service_category: Energy
slug: valero-energy-finops
source_filename: valero-energy-finops.yml
source_heading: FinOps Profile
source_url: https://www.valero.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Valero Energy\nproviderId: valero-energy\npublisherName: Valero Energy Corporation\nserviceCategory: Energy\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Energy\n  - Petroleum\n  - FinOps\n  - FOCUS\ndescription: 'FinOps shape for Valero Energy: there is no developer-billed API surface. Trading-partner and commercial customer integrations live inside private B2B contracts; cost flows through the underlying commodity transactions, not API metering.'\nsources:\n  - https://www.valero.com/\nnotes: No public usage-based billing surface for Valero APIs. Costs are settled inside the commodity/distribution contract.\nbillingModel:\n\
  \  pricingCategory: Bundled with Commercial Contract\n  billingFrequency: Per-Contract\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: Valero Energy\n  ServiceCategory: Energy\n  ProviderName: Valero Energy\n  PublisherName: Valero Energy Corporation\n  InvoiceIssuerName: Valero Energy Corporation\n  BillingCurrency: USD\nmeters:\n  - name: contracted_access\n    description: API/EDI access provisioned under a trading-partner or customer agreement; not metered as a developer billing line\n    unit: varies\n    aggregation: count\nprinciples:\n  - name: Visibility\n    description: Valero does not expose public API usage telemetry; partners reconcile via their own EDI/middleware logs.\n  - name: Allocation\n    description: Costs are not allocated to API line items; they sit in the underlying purchase or sales invoice for petroleum/renewable products.\n  - name: Optimization\n    description: Optimization happens at the commercial-contract and\
  \ integration-cadence level (batching, scheduling, EDI map design) rather than per-call cost.\n  - name: Accountability\n    description: Owned by the trading-partner counterparty's commercial and IT operations teams under the master agreement.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/valero-energy/refs/heads/main/finops/valero-energy-finops.yml
sources:
- https://www.valero.com/
specification: FinOps Framework
tags:
- Energy
- Petroleum
- FinOps
- FOCUS
---
