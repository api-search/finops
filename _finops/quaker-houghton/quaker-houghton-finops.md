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
  pricingCategory: Enterprise Contract
description: Quaker Houghton does not publish a public API meter or invoice surface; any FinOps mapping must come from the customer's enterprise procurement contract.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Quaker Houghton
  ProviderName: Quaker Houghton
  PublisherName: Quaker Houghton
  ServiceCategory: Industrial Fluids
  ServiceName: Quaker Houghton
layout: finops
meters:
- aggregation: sum
  description: Any platform or data integration is scoped under the enterprise customer contract.
  dimensions:
  - contract
  name: contract_engagement
  unit: varies
name: Quaker Houghton Finops
provider_name: Quaker Houghton
provider_slug: quaker-houghton
publisher_name: Quaker Houghton
service_category: Industrial Fluids
slug: quaker-houghton-finops
source_filename: quaker-houghton-finops.yml
source_heading: FinOps Profile
source_url: https://home.quakerhoughton.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Quaker Houghton\nproviderId: quaker-houghton\npublisherName: Quaker Houghton\nserviceCategory: Industrial Fluids\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Industrial Fluids\n  - Chemical\n  - FinOps\n  - FOCUS\nnotes: No public API or developer pricing surface is published by Quaker Houghton; FinOps mapping is\n  scoped to the enterprise contract level.\ndescription: Quaker Houghton does not publish a public API meter or invoice surface; any FinOps mapping\n  must come from the customer's enterprise procurement contract.\nsources:\n  - https://home.quakerhoughton.com/\nbillingModel:\n  pricingCategory: Enterprise\
  \ Contract\n  billingFrequency: Per-Invoice\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: Quaker Houghton\n  ServiceCategory: Industrial Fluids\n  ProviderName: Quaker Houghton\n  PublisherName: Quaker Houghton\n  InvoiceIssuerName: Quaker Houghton\n  BillingCurrency: USD\nmeters:\n  - name: contract_engagement\n    description: Any platform or data integration is scoped under the enterprise customer contract.\n    unit: varies\n    aggregation: sum\n    dimensions:\n      - contract\nprinciples:\n  - name: Visibility\n    description: Treat any Quaker Houghton integration as opaque from a FinOps perspective; surface\n      contracted spend through procurement reporting rather than vendor telemetry.\n  - name: Allocation\n    description: Allocate the contract spend against the consuming manufacturing or operations cost\n      center named in the agreement.\n  - name: Optimization\n    description: Optimization happens at contract renewal;\
  \ review consumption reports furnished by the\n      Quaker Houghton account team and renegotiate as needed.\n  - name: Accountability\n    description: Procurement and the operations sponsor co-own the contract; engineering teams should\n      route integration changes through the account team.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/quaker-houghton/refs/heads/main/finops/quaker-houghton-finops.yml
sources:
- https://home.quakerhoughton.com/
specification: FinOps Framework
tags:
- Industrial Fluids
- Chemical
- FinOps
- FOCUS
---
