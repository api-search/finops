---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: acuity-brands.json
  format: json
  label: Acuity Brands API
  slug: acuity-brands-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/acuity-brands/refs/heads/main/openapi/acuity-brands.json
billing_model:
  billingCurrency: USD
  billingFrequency: Per-Order
  chargeCategories:
  - Purchase
  pricingCategory: Bundled With Distributor Agreement
description: FOCUS-aligned FinOps scaffold for the Acuity Brands distributor API. Acuity Brands invoices distributors for product (hardware) — not for API access. The API is bundled into the partner relationship, so FinOps relevance is to the consuming distributor's integration economics, not a separately-billed Acuity surface.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Acuity Brands Lighting, Inc.
  ProviderName: Acuity Brands
  PublisherName: Acuity Brands Lighting, Inc.
  ServiceCategory: Lighting / Building Controls
  ServiceName: Acuity Brands API
layout: finops
meters:
- aggregation: sum
  description: API request consumed against the distributor's allocation; not directly billed.
  dimensions:
  - endpoint
  - distributor
  name: api_request
  unit: request
- aggregation: sum
  description: B2B order placed through Acuity's order-entry surface (the underlying business transaction that the API supports).
  dimensions:
  - distributor
  - product_family
  name: product_order
  unit: order
name: Acuity Brands Finops
provider_name: acuity-brands
provider_slug: acuity-brands
publisher_name: Acuity Brands Lighting, Inc.
service_category: Lighting / Building Controls
slug: acuity-brands-finops
source_filename: acuity-brands-finops.yml
source_heading: FinOps Profile
source_url: https://api-docs.acuitybrands.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Acuity Brands\nproviderId: acuity-brands\npublisherName: Acuity Brands Lighting, Inc.\nserviceCategory: Lighting / Building Controls\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Lighting\n  - B2B\n  - Inventory\n  - Order Management\n  - Building Controls\n  - FinOps\n  - FOCUS\ndescription: FOCUS-aligned FinOps scaffold for the Acuity Brands distributor API. Acuity Brands invoices\n  distributors for product (hardware) — not for API access. The API is bundled into the partner relationship,\n  so FinOps relevance is to the consuming distributor's integration economics, not a separately-billed\n  Acuity surface.\n\
  sources:\n  - https://api-docs.acuitybrands.com/\nnotes: No commercial API line item. Reconciled flag is false because there is no provider invoice that\n  separates API from product spend.\nbillingModel:\n  pricingCategory: Bundled With Distributor Agreement\n  billingFrequency: Per-Order\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: Acuity Brands API\n  ServiceCategory: Lighting / Building Controls\n  ProviderName: Acuity Brands\n  PublisherName: Acuity Brands Lighting, Inc.\n  InvoiceIssuerName: Acuity Brands Lighting, Inc.\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: api_request\n    description: API request consumed against the distributor's allocation; not directly billed.\n    unit: request\n    aggregation: sum\n    dimensions:\n      - endpoint\n      - distributor\n  - name: product_order\n    description: B2B order placed through Acuity's order-entry surface (the underlying business transaction\n      that\
  \ the API supports).\n    unit: order\n    aggregation: sum\n    dimensions:\n      - distributor\n      - product_family\nprinciples:\n  - name: Visibility\n    description: There is no Acuity API invoice. Visibility is internal to the distributor — track which\n      ERP / e-commerce systems hit the API and at what frequency.\n  - name: Allocation\n    description: Allocate integration cost (distributor-side compute and engineering) to the function\n      it supports — order entry, catalog refresh, inventory checks.\n  - name: Optimization\n    description: Cache catalog and inventory responses where appropriate, batch order-status polls, and\n      avoid duplicate calls across multiple internal systems.\n  - name: Accountability\n    description: The distributor's IT integration owner is accountable; Acuity Brands acts as a partner\n      contact for limit increases.\nmaintainers:\n  - FN: Kin Lane\n    email: info@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/acuity-brands/refs/heads/main/finops/acuity-brands-finops.yml
sources:
- https://api-docs.acuitybrands.com/
specification: FinOps Framework
tags:
- Lighting
- B2B
- Inventory
- Order Management
- Building Controls
- FinOps
- FOCUS
---
