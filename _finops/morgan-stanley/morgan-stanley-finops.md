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
  - Adjustment
  - Tax
  pricingCategory: Bundled with Client Agreement
description: 'FOCUS-aligned FinOps profile for Morgan Stanley APIs: an institutional, invitation-only platform whose costs are bundled into the underlying client services agreement (advisory, brokerage, custody, equity comp). There is no public per-call price; consumption is governed by entitlement and scheme fees rather than developer-platform metering.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Morgan Stanley & Co. LLC
  ProviderName: Morgan Stanley
  PublisherName: Morgan Stanley & Co. LLC
  ServiceCategory: Financial Services
  ServiceName: Morgan Stanley API
layout: finops
meters:
- aggregation: sum
  dimensions:
  - account
  - product
  name: advisory_fees
  unit: month
- aggregation: count
  dimensions:
  - account
  - asset_class
  - venue
  name: trade_execution
  unit: trade
- aggregation: sum
  dimensions:
  - exchange
  - feed
  name: market_data_entitlements
  unit: month
- aggregation: max
  dimensions:
  - employer
  name: equity_comp_seats
  unit: seat
name: Morgan Stanley Finops
provider_name: Morgan Stanley
provider_slug: morgan-stanley
publisher_name: Morgan Stanley & Co. LLC
service_category: Financial Services
slug: morgan-stanley-finops
source_filename: morgan-stanley-finops.yml
source_heading: FinOps Profile
source_url: https://developer.morganstanley.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Morgan Stanley\nproviderId: morgan-stanley\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Financial\n  - Investment Banking\n  - Wealth Management\ndescription: 'FOCUS-aligned FinOps profile for Morgan Stanley APIs: an institutional, invitation-only\n  platform whose costs are bundled into the underlying client services agreement (advisory, brokerage,\n  custody, equity comp). There is no public per-call price; consumption is governed by entitlement and\n  scheme fees rather than developer-platform metering.'\nsources:\n  - https://developer.morganstanley.com/\n  - https://developer.morganstanley.com/terms\nnotes: No public usage / billing API. Reconciliation set to false; meters are modeled against expected\n  invoice line items.\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n\
  \  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Morgan Stanley & Co. LLC\nserviceCategory: Financial Services\nbillingModel:\n  pricingCategory: Bundled with Client Agreement\n  billingFrequency: Per-Invoice\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Adjustment\n    - Tax\nfocusColumns:\n  ServiceName: Morgan Stanley API\n  ServiceCategory: Financial Services\n  ProviderName: Morgan Stanley\n  PublisherName: Morgan Stanley & Co. LLC\n  InvoiceIssuerName: Morgan Stanley & Co. LLC\n  BillingCurrency: USD\nmeters:\n  - name: advisory_fees\n    unit: month\n    aggregation: sum\n    dimensions:\n      - account\n      - product\n  - name: trade_execution\n    unit: trade\n    aggregation: count\n    dimensions:\n      - account\n      - asset_class\n      - venue\n  - name: market_data_entitlements\n    unit: month\n    aggregation: sum\n    dimensions:\n      - exchange\n      - feed\n\
  \  - name: equity_comp_seats\n    unit: seat\n    aggregation: max\n    dimensions:\n      - employer\nprinciples:\n  - name: Visibility\n    description: Reconcile Morgan Stanley client statements (custody, advisory, equity comp) against expected\n      activity; the developer platform surfaces functional usage but not direct cost.\n  - name: Allocation\n    description: Allocate by client account / employer plan and underlying product (Wealth Management,\n      Institutional Securities, Morgan Stanley at Work).\n  - name: Optimization\n    description: Optimization happens at the relationship level (advisory tier, execution venue, market-data\n      entitlement scope) rather than at the API call.\n  - name: Accountability\n    description: The client relationship owner is the budget owner; the integration team monitors API\n      call patterns to ensure they stay within the contracted entitlement.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/morgan-stanley/refs/heads/main/finops/morgan-stanley-finops.yml
sources:
- https://developer.morganstanley.com/
- https://developer.morganstanley.com/terms
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Financial
- Investment Banking
- Wealth Management
---
