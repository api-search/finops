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
  - Adjustment
  pricingCategory: Custom (Partner Contract)
description: FOCUS-aligned FinOps scaffold for Cavco Industries. No public API pricing exists; meters capture integration telemetry against retailer / lender contracts that are the actual cost surface.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Cavco Industries, Inc.
  ProviderName: Cavco Industries
  PublisherName: Cavco Industries, Inc.
  ServiceCategory: Manufactured Housing
  ServiceName: Cavco Industries API
layout: finops
meters:
- aggregation: sum
  dimensions:
  - endpoint
  - partner
  name: api_requests
  unit: request
- aggregation: count
  dimensions:
  - retailer
  name: orders_synchronized
  unit: order
name: Cavco Industries Finops
provider_name: Cavco Industries
provider_slug: cavco-industries
publisher_name: Cavco Industries, Inc.
service_category: Manufactured Housing
slug: cavco-industries-finops
source_filename: cavco-industries-finops.yml
source_heading: FinOps Profile
source_url: https://www.cavco.com
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Cavco Industries\nproviderId: cavco-industries\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Manufactured Homes\n  - Housing\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps scaffold for Cavco Industries. No public API pricing exists; meters\n  capture integration telemetry against retailer / lender contracts that are the actual cost surface.'\nnotes: Cost surface is contract-driven; no per-call invoicing.\nsources:\n  - https://www.cavco.com\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Cavco Industries, Inc.\nserviceCategory: Manufactured Housing\nbillingModel:\n  pricingCategory: Custom (Partner Contract)\n  billingFrequency: Per-Contract\n\
  \  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Adjustment\nfocusColumns:\n  ServiceName: Cavco Industries API\n  ServiceCategory: Manufactured Housing\n  ProviderName: Cavco Industries\n  PublisherName: Cavco Industries, Inc.\n  InvoiceIssuerName: Cavco Industries, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: api_requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - endpoint\n      - partner\n  - name: orders_synchronized\n    unit: order\n    aggregation: count\n    dimensions:\n      - retailer\nprinciples:\n  - name: Visibility\n    description: Track partner integration via the negotiated reporting surface delivered with the retailer\n      / lender contract; no public usage API.\n  - name: Allocation\n    description: Tag integration costs to the retailer or lender relationship that drives them.\n  - name: Optimization\n    description: Batch order / inventory updates aligned to Cavco's published refresh windows.\n  - name: Accountability\n\
  \    description: A retail-channel owner reconciles partner fees against contracts; IT owns integration\n      uptime.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/cavco-industries/refs/heads/main/finops/cavco-industries-finops.yml
sources:
- https://www.cavco.com
specification: FinOps Framework
tags:
- Manufactured Homes
- Housing
- FinOps
- FOCUS
---
