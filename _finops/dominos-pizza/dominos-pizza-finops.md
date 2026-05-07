---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: Not Applicable
  chargeCategories: []
  pricingCategory: Not Applicable (No Public API)
description: FOCUS-aligned FinOps shape for Domino's. Domino's does not invoice for API consumption (the endpoints are undocumented and not commercial), so FinOps cost falls on the consumer's integration platform.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Not Applicable
  ProviderName: Domino's Pizza
  PublisherName: Domino's Pizza, LLC
  ServiceCategory: QSR / Food Ordering
  ServiceName: Domino's Pizza (Unofficial)
layout: finops
meters:
- aggregation: sum
  description: Internal observability of calls against undocumented Domino's endpoints
  dimensions:
  - endpoint
  name: api_requests
  unit: request
- aggregation: count
  description: Real-world pizza orders triggered via the integration
  dimensions:
  - store_id
  name: orders_placed
  unit: order
name: Dominos Pizza Finops
provider_name: Domino's Pizza
provider_slug: dominos-pizza
publisher_name: Domino's Pizza, LLC
service_category: QSR / Food Ordering
slug: dominos-pizza-finops
source_filename: dominos-pizza-finops.yml
source_heading: FinOps Profile
source_url: https://github.com/RIAEvangelist/node-dominos-pizza-api
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Domino's Pizza\nproviderId: dominos-pizza\npublisherName: Domino's Pizza, LLC\nserviceCategory: QSR / Food Ordering\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Food Service\n  - Restaurants\n  - QSR\n  - FinOps\n  - FOCUS\ndescription: FOCUS-aligned FinOps shape for Domino's. Domino's does not invoice for API consumption (the\n  endpoints are undocumented and not commercial), so FinOps cost falls on the consumer's integration platform.\nnotes: No commercial billing relationship; reconciled=false. The actual billable transaction is the pizza\n  order itself, settled to the customer's payment method.\nsources:\n  -\
  \ https://github.com/RIAEvangelist/node-dominos-pizza-api\nbillingModel:\n  pricingCategory: Not Applicable (No Public API)\n  billingFrequency: Not Applicable\n  billingCurrency: USD\n  chargeCategories: []\nfocusColumns:\n  ServiceName: Domino's Pizza (Unofficial)\n  ServiceCategory: QSR / Food Ordering\n  ProviderName: Domino's Pizza\n  PublisherName: Domino's Pizza, LLC\n  InvoiceIssuerName: Not Applicable\n  BillingCurrency: USD\nmeters:\n  - name: api_requests\n    description: Internal observability of calls against undocumented Domino's endpoints\n    unit: request\n    aggregation: sum\n    dimensions:\n      - endpoint\n  - name: orders_placed\n    description: Real-world pizza orders triggered via the integration\n    unit: order\n    aggregation: count\n    dimensions:\n      - store_id\nprinciples:\n  - name: Visibility\n    description: Track endpoint calls and order placements in the consumer's logs; Domino's does not produce\n      a usage invoice.\n  - name: Allocation\n\
  \    description: Allocate integration cost to the consuming product/feature (e.g. voice-ordering bot,\n      kiosk).\n  - name: Optimization\n    description: Cache store and menu lookups; minimise polling against undocumented endpoints to reduce\n      throttling risk.\n  - name: Accountability\n    description: Integration owner is accountable for monitoring breakage; there is no official Domino's\n      developer relationship.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/dominos-pizza/refs/heads/main/finops/dominos-pizza-finops.yml
sources:
- https://github.com/RIAEvangelist/node-dominos-pizza-api
specification: FinOps Framework
tags:
- Food Service
- Restaurants
- QSR
- FinOps
- FOCUS
---
