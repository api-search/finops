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
  - Usage
  - Purchase
  pricingCategory: Custom Enterprise Services
description: Sykes Enterprises (now Foundever) is a CX/BPO services provider with no public API or published billing surface; FinOps shape is negotiated per enterprise contract.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Foundever
  ProviderName: Foundever
  PublisherName: Foundever (formerly Sykes Enterprises, Incorporated)
  ServiceCategory: Customer Experience / BPO Services
  ServiceName: Sykes Enterprises (Foundever)
layout: finops
meters:
- aggregation: sum
  description: Contracted CX/BPO service consumption, terms defined per-engagement.
  name: contracted_services
  unit: varies
name: Sykes Enterprises Finops
provider_name: Sykes Enterprises
provider_slug: sykes-enterprises
publisher_name: Foundever (formerly Sykes Enterprises, Incorporated)
service_category: Customer Experience / BPO Services
slug: sykes-enterprises-finops
source_filename: sykes-enterprises-finops.yml
source_heading: FinOps Profile
source_url: https://www.sykes.com
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Sykes Enterprises\nproviderId: sykes-enterprises\npublisherName: Foundever (formerly Sykes Enterprises, Incorporated)\nserviceCategory: Customer Experience / BPO Services\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - BPO\n  - Customer Experience\n  - FinOps\n  - FOCUS\ndescription: Sykes Enterprises (now Foundever) is a CX/BPO services provider with no public API or published billing surface; FinOps shape is negotiated per enterprise contract.\nsources:\n  - https://www.sykes.com\n  - https://foundever.com\nnotes: No public usage telemetry, FOCUS-aligned export, or self-service billing surface. Cost data must be reconciled\
  \ from negotiated enterprise CX invoices.\nbillingModel:\n  pricingCategory: Custom Enterprise Services\n  billingFrequency: Per-Contract\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\nfocusColumns:\n  ServiceName: Sykes Enterprises (Foundever)\n  ServiceCategory: Customer Experience / BPO Services\n  ProviderName: Foundever\n  PublisherName: Foundever (formerly Sykes Enterprises, Incorporated)\n  InvoiceIssuerName: Foundever\n  BillingCurrency: USD\nmeters:\n  - name: contracted_services\n    description: Contracted CX/BPO service consumption, terms defined per-engagement.\n    unit: varies\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Cost visibility is provided through contracted reporting agreed in the master services agreement; there is no self-service usage API.\n  - name: Allocation\n    description: Allocation follows the cost centers and program codes specified in the customer's CX engagement.\n  - name: Optimization\n \
  \   description: Optimization levers are negotiated (volume commitments, FTE staffing models, channel mix) rather than self-service tier changes.\n  - name: Accountability\n    description: A named Foundever account team and the customer's program owner share accountability for spend versus contracted scope.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/sykes-enterprises/refs/heads/main/finops/sykes-enterprises-finops.yml
sources:
- https://www.sykes.com
- https://foundever.com
specification: FinOps Framework
tags:
- BPO
- Customer Experience
- FinOps
- FOCUS
---
