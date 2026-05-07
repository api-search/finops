---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: inttra-ocean-execution-openapi.yml
  format: yaml
  label: INTTRA Ocean Execution API
  slug: inttra-ocean-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/e2open/refs/heads/main/openapi/inttra-ocean-execution-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Purchase
  - Usage
  - Tax
  - Adjustment
  pricingCategory: Subscription + Usage
description: 'FOCUS-aligned FinOps for e2open: per-module SaaS subscription plus per-transaction meters (bookings, shipments, customs filings) governed by the contract. Public per-call pricing is not published.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: E2open, LLC
  ProviderName: e2open
  PublisherName: E2open, LLC
  ServiceCategory: Supply Chain
  ServiceName: e2open Connected Network
layout: finops
meters:
- aggregation: sum
  dimensions:
  - module
  - tenant
  name: api_requests
  unit: request
- aggregation: sum
  dimensions:
  - carrier
  - lane
  name: ocean_bookings
  unit: transaction
- aggregation: sum
  dimensions:
  - mode
  - region
  name: shipments_tracked
  unit: shipment
- aggregation: sum
  dimensions:
  - country
  name: customs_filings
  unit: filing
- aggregation: sum
  dimensions:
  - module
  name: module_seats
  unit: seat
name: E2Open Finops
provider_name: e2open
provider_slug: e2open
publisher_name: E2open, LLC
service_category: Supply Chain
slug: e2open-finops
source_filename: e2open-finops.yml
source_heading: FinOps Profile
source_url: https://www.e2open.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: e2open\nproviderId: e2open\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Supply Chain\n  - Logistics\ndescription: 'FOCUS-aligned FinOps for e2open: per-module SaaS subscription plus per-transaction meters\n  (bookings, shipments, customs filings) governed by the contract. Public per-call pricing is not published.'\nnotes: e2open does not publish public API pricing. Reconcile FOCUS columns and per-meter rates against\n  the master subscription agreement.\nsources:\n  - https://www.e2open.com/\n  - https://apidocs.inttra.com/\n  - https://marketplace.e2open.com/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: E2open, LLC\nserviceCategory:\
  \ Supply Chain\nbillingModel:\n  pricingCategory: Subscription + Usage\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\n    - Tax\n    - Adjustment\nfocusColumns:\n  ServiceName: e2open Connected Network\n  ServiceCategory: Supply Chain\n  ProviderName: e2open\n  PublisherName: E2open, LLC\n  InvoiceIssuerName: E2open, LLC\n  BillingCurrency: USD\nmeters:\n  - name: api_requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - module\n      - tenant\n  - name: ocean_bookings\n    unit: transaction\n    aggregation: sum\n    dimensions:\n      - carrier\n      - lane\n  - name: shipments_tracked\n    unit: shipment\n    aggregation: sum\n    dimensions:\n      - mode\n      - region\n  - name: customs_filings\n    unit: filing\n    aggregation: sum\n    dimensions:\n      - country\n  - name: module_seats\n    unit: seat\n    aggregation: sum\n    dimensions:\n      - module\nprinciples:\n  - name: Visibility\n   \
  \ description: Use the e2open Marketplace usage reports and per-module dashboards to see consumption;\n      pull invoice line items into FOCUS-formatted tables.\n  - name: Allocation\n    description: Tag bookings/shipments/filings with originating business unit; charge back module subscriptions\n      to owning logistics team.\n  - name: Optimization\n    description: Consolidate ocean carriers through INTTRA to leverage volume; reduce module count at\n      renewal where capabilities overlap.\n  - name: Accountability\n    description: Supply-chain operations owns the e2open subscription and reviews monthly usage against\n      forecast.\nmaintainers:\n  - name: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/e2open/refs/heads/main/finops/e2open-finops.yml
sources:
- https://www.e2open.com/
- https://apidocs.inttra.com/
- https://marketplace.e2open.com/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Supply Chain
- Logistics
---
