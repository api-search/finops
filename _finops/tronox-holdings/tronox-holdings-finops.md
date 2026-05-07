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
description: Tronox Holdings does not operate a metered API or self-serve cloud product, so no FOCUS-aligned FinOps surface is published. Procurement of titanium dioxide and zircon is contracted directly and invoiced on commercial terms negotiated with the customer.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Tronox Holdings plc
  ProviderName: Tronox Holdings
  PublisherName: Tronox Holdings plc
  ServiceCategory: Chemicals & Materials
  ServiceName: Tronox Holdings
layout: finops
meters:
- aggregation: sum
  description: Volume of titanium dioxide, zircon, or related products delivered under contract.
  name: contracted_supply
  unit: varies
name: Tronox Holdings Finops
provider_name: Tronox Holdings
provider_slug: tronox-holdings
publisher_name: Tronox Holdings plc
service_category: Chemicals & Materials
slug: tronox-holdings-finops
source_filename: tronox-holdings-finops.yml
source_heading: FinOps Profile
source_url: https://www.tronox.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Tronox Holdings\nproviderId: tronox-holdings\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Titanium Dioxide\n  - Chemical\n  - Mining\n  - FinOps\n  - FOCUS\ndescription: Tronox Holdings does not operate a metered API or self-serve cloud product, so no FOCUS-aligned\n  FinOps surface is published. Procurement of titanium dioxide and zircon is contracted directly and invoiced\n  on commercial terms negotiated with the customer.\nsources:\n  - https://www.tronox.com/\nnotes: No public API metering, usage telemetry, or FOCUS-style billing export. Trimmed to a Contact Sales\n  shape pending any future digital-product disclosure.\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\n\
  publisherName: Tronox Holdings plc\nserviceCategory: Chemicals & Materials\nbillingModel:\n  pricingCategory: Contract\n  billingFrequency: Per-Invoice\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: Tronox Holdings\n  ServiceCategory: Chemicals & Materials\n  ProviderName: Tronox Holdings\n  PublisherName: Tronox Holdings plc\n  InvoiceIssuerName: Tronox Holdings plc\n  BillingCurrency: USD\nmeters:\n  - name: contracted_supply\n    description: Volume of titanium dioxide, zircon, or related products delivered under contract.\n    unit: varies\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Spend visibility is established via the customer's procurement system and invoice review;\n      no provider-side usage API or cost dashboard is published.\n  - name: Allocation\n    description: Allocate Tronox spend through your purchase-order system; assign POs to product lines\n      and plants as they are issued.\n  - name:\
  \ Optimization\n    description: Optimization is a procurement function — volume commitments, contract terms, and product\n      grade selection — negotiated directly with Tronox sales.\n  - name: Accountability\n    description: Accountability sits with the procurement and operations leaders responsible for the contract;\n      there is no metered cost-owner concept.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/tronox-holdings/refs/heads/main/finops/tronox-holdings-finops.yml
sources:
- https://www.tronox.com/
specification: FinOps Framework
tags:
- Titanium Dioxide
- Chemical
- Mining
- FinOps
- FOCUS
---
