---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: sigma-aldrich-product-openapi.yml
  format: yaml
  label: Sigma-Aldrich Product Search API
  slug: sigma-aldrich-product-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/sigma-aldrich/refs/heads/main/openapi/sigma-aldrich-product-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Per-Order
  chargeCategories:
  - Purchase
  pricingCategory: B2B Procurement / Catalog
description: FOCUS-aligned FinOps placeholder for Sigma-Aldrich (MilliporeSigma). API integrations are not billed as a discrete line; cost flows through product purchases (reagents, consumables, equipment) and contracted procurement terms. No public usage telemetry or per-call billing surface exists.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: MilliporeSigma
  ProviderName: Sigma-Aldrich
  PublisherName: MilliporeSigma
  ServiceCategory: Life Science Procurement
  ServiceName: Sigma-Aldrich
layout: finops
meters:
- aggregation: sum
  description: Orders placed via the procurement integration; cost flows through product price and negotiated contract pricing rather than per-API-call charges.
  dimensions:
  - account
  - product_category
  - region
  name: catalog_orders
  unit: order
name: Sigma Aldrich Finops
provider_name: Sigma-Aldrich
provider_slug: sigma-aldrich
publisher_name: MilliporeSigma (Merck KGaA, Darmstadt, Germany)
service_category: Life Science Procurement
slug: sigma-aldrich-finops
source_filename: sigma-aldrich-finops.yml
source_heading: FinOps Profile
source_url: https://www.sigmaaldrich.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Sigma-Aldrich\nproviderId: sigma-aldrich\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Life Science\n  - Chemistry\n  - Laboratory\n  - FinOps\n  - FOCUS\ndescription: FOCUS-aligned FinOps placeholder for Sigma-Aldrich (MilliporeSigma). API integrations\n  are not billed as a discrete line; cost flows through product purchases (reagents, consumables,\n  equipment) and contracted procurement terms. No public usage telemetry or per-call billing surface\n  exists.\nsources:\n  - https://www.sigmaaldrich.com/\nnotes: No public API billing model. FinOps treatment is procurement-driven; reconciliation pending\n  direct vendor confirmation.\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\n\
  publisherName: MilliporeSigma (Merck KGaA, Darmstadt, Germany)\nserviceCategory: Life Science Procurement\nbillingModel:\n  pricingCategory: B2B Procurement / Catalog\n  billingFrequency: Per-Order\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: Sigma-Aldrich\n  ServiceCategory: Life Science Procurement\n  ProviderName: Sigma-Aldrich\n  PublisherName: MilliporeSigma\n  InvoiceIssuerName: MilliporeSigma\n  BillingCurrency: USD\nmeters:\n  - name: catalog_orders\n    description: Orders placed via the procurement integration; cost flows through product price and\n      negotiated contract pricing rather than per-API-call charges.\n    unit: order\n    aggregation: sum\n    dimensions:\n      - account\n      - product_category\n      - region\nprinciples:\n  - name: Visibility\n    description: Spend visibility comes from the lab/procurement system that issues purchase orders\n      and the supplier invoice; API call volume does not appear on an\
  \ invoice.\n  - name: Allocation\n    description: Allocate by purchase order, requesting lab/cost center, project/grant, and product\n      category captured in the procurement system.\n  - name: Optimization\n    description: Optimization is procurement-led — negotiate volume discounts, consolidate orders to\n      reduce shipping, and use punchout to enforce contract pricing rather than tuning API patterns.\n  - name: Accountability\n    description: Lab procurement and finance own Sigma-Aldrich spend; integration owners ensure punchout\n      and order traffic stays within contract terms.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/sigma-aldrich/refs/heads/main/finops/sigma-aldrich-finops.yml
sources:
- https://www.sigmaaldrich.com/
specification: FinOps Framework
tags:
- Life Science
- Chemistry
- Laboratory
- FinOps
- FOCUS
---
