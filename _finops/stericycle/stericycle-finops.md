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
  - Tax
  - Adjustment
  pricingCategory: Contract-Negotiated Services
description: Stericycle bills under negotiated B2B service contracts; the line items consumers see are pickup/service charges, not API meters. This artifact captures the publisher and category surface only; meters are placeholders.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Stericycle, Inc.
  ProviderName: Stericycle
  PublisherName: Stericycle, Inc.
  ServiceCategory: Regulated Waste & Compliance Services
  ServiceName: Stericycle
layout: finops
meters:
- aggregation: sum
  description: Negotiated service line items on the underlying customer contract; not exposed as a public API meter
  name: contract_services
  unit: varies
name: Stericycle Finops
provider_name: Stericycle
provider_slug: stericycle
publisher_name: Stericycle, Inc.
service_category: Regulated Waste & Compliance Services
slug: stericycle-finops
source_filename: stericycle-finops.yml
source_heading: FinOps Profile
source_url: https://www.stericycle.com
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Stericycle\nproviderId: stericycle\npublisherName: Stericycle, Inc.\nserviceCategory: Regulated Waste & Compliance Services\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Healthcare\n  - Medical Waste\n  - Waste Management\ndescription: Stericycle bills under negotiated B2B service contracts; the line items consumers see are\n  pickup/service charges, not API meters. This artifact captures the publisher and category surface only;\n  meters are placeholders.\nsources:\n  - https://www.stericycle.com\nnotes: 'Reconciliation marked false: Stericycle does not publish a public pricing/billing document\
  \ for\n  programmatic access. API consumption is bundled into a negotiated service contract.'\nbillingModel:\n  pricingCategory: Contract-Negotiated Services\n  billingFrequency: Per-Invoice\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Tax\n    - Adjustment\nfocusColumns:\n  ServiceName: Stericycle\n  ServiceCategory: Regulated Waste & Compliance Services\n  ProviderName: Stericycle\n  PublisherName: Stericycle, Inc.\n  InvoiceIssuerName: Stericycle, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: contract_services\n    description: Negotiated service line items on the underlying customer contract; not exposed as\n      a public API meter\n    unit: varies\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Visibility into Stericycle spend is via the customer-portal account view and contract\n      invoices, not a usage API.\n  - name: Allocation\n    description: Allocate cost by service location and waste stream as defined on the customer\
  \ contract.\n  - name: Optimization\n    description: Optimization levers are operational (pickup frequency, container right-sizing, route\n      consolidation) and contractual (renegotiation), not technical.\n  - name: Accountability\n    description: Account ownership rests with the contracting facilities/compliance team; review against\n      the contract schedule annually.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/stericycle/refs/heads/main/finops/stericycle-finops.yml
sources:
- https://www.stericycle.com
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Healthcare
- Medical Waste
- Waste Management
---
