---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: ruckus-one-api-openapi.yml
  format: yaml
  label: RUCKUS One API
  slug: ruckus-one-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/commscope-holding/refs/heads/main/openapi/ruckus-one-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Per-Invoice
  chargeCategories:
  - Purchase
  - Tax
  - Adjustment
  - Refund
  pricingCategory: Hardware + Subscription
description: 'FOCUS-aligned FinOps for CommScope Holding: hardware (CapEx) plus product-line subscriptions (RUCKUS Cloud) sold through channel partners. No public consumption-metered API surface at the holding level.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: CommScope, Inc.
  ProviderName: CommScope
  PublisherName: CommScope, Inc.
  ServiceCategory: Networking
  ServiceName: CommScope
layout: finops
meters:
- aggregation: sum
  dimensions:
  - product_family
  - sku
  name: hardware_units
  unit: unit
- aggregation: sum
  dimensions:
  - tier
  name: ruckus_cloud_subscription
  unit: ap-month
- aggregation: sum
  dimensions:
  - device
  - tier
  name: support_subscription
  unit: month
name: Commscope Holding Finops
provider_name: CommScope Holding
provider_slug: commscope-holding
publisher_name: CommScope, Inc.
service_category: Networking
slug: commscope-holding-finops
source_filename: commscope-holding-finops.yml
source_heading: FinOps Profile
source_url: https://www.commscope.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: CommScope Holding\nproviderId: commscope-holding\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Networking\n  - Hardware\ndescription: 'FOCUS-aligned FinOps for CommScope Holding: hardware (CapEx) plus product-line subscriptions\n  (RUCKUS Cloud) sold through channel partners. No public consumption-metered API surface at the holding\n  level.'\nsources:\n  - https://www.commscope.com/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: CommScope, Inc.\nserviceCategory: Networking\nbillingModel:\n  pricingCategory: Hardware + Subscription\n  billingFrequency: Per-Invoice\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n\
  \    - Tax\n    - Adjustment\n    - Refund\nfocusColumns:\n  ServiceName: CommScope\n  ServiceCategory: Networking\n  ProviderName: CommScope\n  PublisherName: CommScope, Inc.\n  InvoiceIssuerName: CommScope, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: hardware_units\n    unit: unit\n    aggregation: sum\n    dimensions:\n      - product_family\n      - sku\n  - name: ruckus_cloud_subscription\n    unit: ap-month\n    aggregation: sum\n    dimensions:\n      - tier\n  - name: support_subscription\n    unit: month\n    aggregation: sum\n    dimensions:\n      - device\n      - tier\nprinciples:\n  - name: Visibility\n    description: Reconcile partner invoices to product SKUs and AP/device serial numbers; pull subscription\n      data from RUCKUS Cloud / RUCKUS One dashboards.\n  - name: Allocation\n    description: Tag hardware to site and product-line subscriptions to tenant/site.\n  - name: Optimization\n    description: Consolidate AP licenses where deployments shrink; align hardware\
  \ refresh cycles with\n      depreciation schedule.\n  - name: Accountability\n    description: Network engineering owns AP fleet; finance owns CapEx vs subscription mix.\nnotes: No public corporate API consumption pricing.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/commscope-holding/refs/heads/main/finops/commscope-holding-finops.yml
sources:
- https://www.commscope.com/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Networking
- Hardware
---
