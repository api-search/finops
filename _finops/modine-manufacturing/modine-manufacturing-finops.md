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
  pricingCategory: Contract / Custom
description: Placeholder FinOps profile for Modine Manufacturing. No public API billing surface, pricing page, or invoiced consumption API was located; any API consumption would be invoiced through the standard Modine commercial relationship rather than a metered developer platform.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Modine Manufacturing Company
  ProviderName: Modine Manufacturing
  PublisherName: Modine Manufacturing Company
  ServiceCategory: Industrial OEM
  ServiceName: Modine Manufacturing
layout: finops
meters:
- aggregation: sum
  dimensions:
  - contract
  name: contract_fees
  unit: month
name: Modine Manufacturing Finops
provider_name: Modine Manufacturing
provider_slug: modine-manufacturing
publisher_name: Modine Manufacturing Company
service_category: Industrial / Thermal Management
slug: modine-manufacturing-finops
source_filename: modine-manufacturing-finops.yml
source_heading: FinOps Profile
source_url: https://www.modine.com
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Modine Manufacturing\nproviderId: modine-manufacturing\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Thermal Management\n  - Automotive\n  - HVAC\ndescription: Placeholder FinOps profile for Modine Manufacturing. No public API billing surface, pricing\n  page, or invoiced consumption API was located; any API consumption would be invoiced through the standard\n  Modine commercial relationship rather than a metered developer platform.\nsources:\n  - https://www.modine.com\nnotes: Reconciliation deferred — populate when a public developer/billing portal is identified.\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Modine Manufacturing\
  \ Company\nserviceCategory: Industrial / Thermal Management\nbillingModel:\n  pricingCategory: Contract / Custom\n  billingFrequency: Per-Invoice\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Adjustment\nfocusColumns:\n  ServiceName: Modine Manufacturing\n  ServiceCategory: Industrial OEM\n  ProviderName: Modine Manufacturing\n  PublisherName: Modine Manufacturing Company\n  InvoiceIssuerName: Modine Manufacturing Company\n  BillingCurrency: USD\nmeters:\n  - name: contract_fees\n    unit: month\n    aggregation: sum\n    dimensions:\n      - contract\nprinciples:\n  - name: Visibility\n    description: Track Modine commercial invoices in AP; no automated usage telemetry is published.\n  - name: Allocation\n    description: Allocate Modine spend to the engineering / facilities cost center carrying the underlying\n      product or service contract.\n  - name: Optimization\n    description: Optimization happens in commercial negotiation cycles, not platform usage controls.\n\
  \  - name: Accountability\n    description: Procurement and the contract owner reconcile Modine invoices; no developer-platform\n      chargeback applies absent a public billing API.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/modine-manufacturing/refs/heads/main/finops/modine-manufacturing-finops.yml
sources:
- https://www.modine.com
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Thermal Management
- Automotive
- HVAC
---
