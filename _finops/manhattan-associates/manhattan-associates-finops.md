---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: manhattan-associates-omni-openapi.yml
  format: yaml
  label: Manhattan Active Omni and Enterprise Promise & Fulfill API
  slug: manhattan-active-omni-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/manhattan-associates/refs/heads/main/openapi/manhattan-associates-omni-openapi.yml
- filename: manhattan-associates-wms-openapi.yml
  format: yaml
  label: Manhattan Active Supply Chain API
  slug: manhattan-active-supply-chain-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/manhattan-associates/refs/heads/main/openapi/manhattan-associates-wms-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Usage
  - Purchase
  - Tax
  - Adjustment
  pricingCategory: Enterprise SaaS
description: 'FOCUS-aligned FinOps for Manhattan Associates: enterprise SaaS contract for the Manhattan Active platform suite. APIs are not separately metered; cost lines are SaaS subscription, transaction volumes (orders, shipments, fulfillments), and implementation services.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Manhattan Associates, Inc.
  ProviderName: Manhattan Associates
  PublisherName: Manhattan Associates, Inc.
  ServiceCategory: Supply Chain Software
  ServiceName: Manhattan Active
layout: finops
meters:
- aggregation: sum
  dimensions:
  - product
  name: subscription_fee
  unit: year
- aggregation: sum
  dimensions:
  - channel
  name: orders_processed
  unit: order
- aggregation: sum
  name: shipments
  unit: shipment
- aggregation: max
  name: warehouses
  unit: site
- aggregation: sum
  dimensions:
  - api
  - integration
  name: api_requests
  unit: request
name: Manhattan Associates Finops
provider_name: manhattan-associates
provider_slug: manhattan-associates
publisher_name: Manhattan Associates, Inc.
service_category: Supply Chain Software
slug: manhattan-associates-finops
source_filename: manhattan-associates-finops.yml
source_heading: FinOps Profile
source_url: https://www.manh.com
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Manhattan Associates\nproviderId: manhattan-associates\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Supply Chain\n  - Order Management\ndescription: 'FOCUS-aligned FinOps for Manhattan Associates: enterprise SaaS contract for the Manhattan\n  Active platform suite. APIs are not separately metered; cost lines are SaaS subscription, transaction\n  volumes (orders, shipments, fulfillments), and implementation services.'\nsources:\n  - https://www.manh.com\nnotes: No public pricing/billing surface; meters reflect typical SaaS supply-chain contract lines.\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Manhattan Associates, Inc.\n\
  serviceCategory: Supply Chain Software\nbillingModel:\n  pricingCategory: Enterprise SaaS\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Adjustment\nfocusColumns:\n  ServiceName: Manhattan Active\n  ServiceCategory: Supply Chain Software\n  ProviderName: Manhattan Associates\n  PublisherName: Manhattan Associates, Inc.\n  InvoiceIssuerName: Manhattan Associates, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: subscription_fee\n    unit: year\n    aggregation: sum\n    dimensions:\n      - product\n  - name: orders_processed\n    unit: order\n    aggregation: sum\n    dimensions:\n      - channel\n  - name: shipments\n    unit: shipment\n    aggregation: sum\n  - name: warehouses\n    unit: site\n    aggregation: max\n  - name: api_requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - integration\nprinciples:\n  - name: Visibility\n    description: Pull order / shipment / API call\
  \ metrics from the Manhattan Active console; reconcile\n      against contracted volumes.\n  - name: Allocation\n    description: Tag orders/shipments by channel / business unit; map Manhattan tenants to internal\n      product lines for chargeback.\n  - name: Optimization\n    description: Consolidate integrations onto Manhattan Active platform APIs; retire legacy TMS/WMS\n      connectors as Active modules absorb scope.\n  - name: Accountability\n    description: Owners review contracted-volume burn quarterly; renegotiate at renewal as channel mix\n      and geography change.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/manhattan-associates/refs/heads/main/finops/manhattan-associates-finops.yml
sources:
- https://www.manh.com
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Supply Chain
- Order Management
---
