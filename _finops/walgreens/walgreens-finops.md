---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: walgreens-store-locator-openapi.yml
  format: yaml
  label: Walgreens Store Locator API
  slug: walgreens-store-locator
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/walgreens/refs/heads/main/openapi/walgreens-store-locator-openapi.yml
- filename: walgreens-prescription-refill-openapi.yml
  format: yaml
  label: Walgreens Prescription Refill API
  slug: walgreens-prescription-refill
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/walgreens/refs/heads/main/openapi/walgreens-prescription-refill-openapi.yml
- filename: walgreens-vaccine-scheduling-openapi.yml
  format: yaml
  label: Walgreens Vaccine Scheduling API
  slug: walgreens-vaccine-scheduling
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/walgreens/refs/heads/main/openapi/walgreens-vaccine-scheduling-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Per-Invoice
  chargeCategories:
  - Adjustment
  - Credit
  pricingCategory: Revenue Share
description: FinOps view of the Walgreens Developer Program. There is no publicly metered API price; the commercial model is approval-based partner access with a revenue-share commission for the Photo Prints API. FOCUS mapping is partial because no per-call cost surface is exposed - what flows to FinOps is the partner-share settlement.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Adjustment
  InvoiceIssuerName: Walgreen Co.
  ProviderName: Walgreens
  PublisherName: Walgreen Co.
  ServiceCategory: Retail / Pharmacy Partner API
  ServiceName: Walgreens Developer Program
layout: finops
meters:
- aggregation: sum
  description: Successful Photo Prints orders eligible for partner revenue-share commission.
  dimensions:
  - partner
  - product
  name: photo_print_orders
  unit: order
- aggregation: sum
  description: Successful Walgreens partner-API requests, attributed by API key (used for capacity and audit, not direct billing).
  dimensions:
  - api
  - api_key
  name: api_calls
  unit: request
name: Walgreens Finops
provider_name: Walgreens
provider_slug: walgreens
publisher_name: Walgreen Co.
service_category: Retail / Pharmacy Partner API
slug: walgreens-finops
source_filename: walgreens-finops.yml
source_heading: FinOps Profile
source_url: https://developer.walgreens.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Walgreens\nproviderId: walgreens\npublisherName: Walgreen Co.\nserviceCategory: Retail / Pharmacy Partner API\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Pharmacy\n  - Retail\n  - Healthcare\n  - FinOps\n  - FOCUS\ndescription: FinOps view of the Walgreens Developer Program. There is no\n  publicly metered API price; the commercial model is approval-based partner\n  access with a revenue-share commission for the Photo Prints API. FOCUS\n  mapping is partial because no per-call cost surface is exposed - what flows\n  to FinOps is the partner-share settlement.\nsources:\n  - https://developer.walgreens.com/\n  - https://developer.walgreens.com/apis\nnotes:\
  \ No published per-call price; no Walgreens-issued usage / billing API for\n  partners. FOCUS records depend on the partner-share statements issued under\n  the integration agreement.\nbillingModel:\n  pricingCategory: Revenue Share\n  billingFrequency: Per-Invoice\n  billingCurrency: USD\n  chargeCategories:\n    - Adjustment\n    - Credit\nfocusColumns:\n  ServiceName: Walgreens Developer Program\n  ServiceCategory: Retail / Pharmacy Partner API\n  ProviderName: Walgreens\n  PublisherName: Walgreen Co.\n  InvoiceIssuerName: Walgreen Co.\n  BillingCurrency: USD\n  ChargeCategory: Adjustment\nmeters:\n  - name: photo_print_orders\n    description: Successful Photo Prints orders eligible for partner\n      revenue-share commission.\n    unit: order\n    aggregation: sum\n    dimensions:\n      - partner\n      - product\n  - name: api_calls\n    description: Successful Walgreens partner-API requests, attributed by API\n      key (used for capacity and audit, not direct billing).\n    unit:\
  \ request\n    aggregation: sum\n    dimensions:\n      - api\n      - api_key\nprinciples:\n  - name: Visibility\n    description: Track Photo Prints order volume and revenue-share statements\n      issued by Walgreens; reconcile partner-side order events against the\n      monthly Walgreens settlement.\n  - name: Allocation\n    description: Attribute partner-share revenue (and any Walgreens-side fees)\n      to the consuming product or storefront via the API key dimension.\n  - name: Optimization\n    description: Optimize conversion on partner integrations (Photo Prints,\n      Add to Cart) to grow share-based earnings; reduce latency on\n      Store Locator / Store Inventory to keep dependent apps inside any\n      negotiated SLA.\n  - name: Accountability\n    description: Partnership / business-development owns the Walgreens\n      revenue-share contract; engineering owns API-key hygiene and\n      throttling-respecting clients.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n\
  \    url: https://apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/walgreens/refs/heads/main/finops/walgreens-finops.yml
sources:
- https://developer.walgreens.com/
- https://developer.walgreens.com/apis
specification: FinOps Framework
tags:
- Pharmacy
- Retail
- Healthcare
- FinOps
- FOCUS
---
